# 02 — Group Problem Statement"

## Group convergence

Mỗi thành viên trong nhóm đưa ra 3–5 vấn đề cá nhân, sau đó gom lại thành **các cluster**.  Các cluster chính xuất hiện như sau:

| Cluster | Ví dụ vấn đề | Điểm chung |
|--------|--------------|-----------|
| **Thao tác tài chính** | “AI hỗ trợ thanh toán cho người khiếm thị”, “Giao dịch ngân hàng bằng giọng nói”, “Khiếu nại giao dịch tự động” | Yêu cầu **các bước lấy dữ liệu tài chính → xác thực → thực thi** và luôn có *human‑in‑the‑loop* |
| **Truy xuất thông tin** | “Tìm lịch sử giao dịch nhanh”, “Kiểm tra số dư qua trợ lý ảo” | Tập trung vào **tìm kiếm & hiển thị** dữ liệu đã có |
| **Báo cáo / giám sát** | “Tự động tổng hợp báo cáo chi tiêu cho người khuyết tật”, “Cảnh báo giao dịch gian lận” | Kết hợp **đánh giá rủi ro** và **tóm tắt** dữ liệu |

Nhóm quyết định **đánh dấu “Thao tác tài chính”** làm đối tượng ưu tiên vì:

* Độ phức tạp kỹ thuật (OCR, OCR‑QR, lookup, transaction synthesis) giúp minh hoạ rõ ràng **Rule → Workflow → Agent**.
* Ranh giới “human‑in‑the‑loop” rất rõ (người khiếm thị cần xác nhận cuối cùng).
* Có số liệu *baseline* khả thi (thời gian thực hiện giao dịch thủ công ≈ 90 giây, tỉ lệ lỗi nhập sai ≈ 4 %).

### Short‑list & scoring

| Candidate | Actor | Workflow rõ | Pain có evidence | Impact đo được | Độ phù hợp Lab | So sánh R/W/A | Đánh giá chung |
|----------|-------|------------|------------------|----------------|----------------|---------------|----------------|
| **Blind‑Payment Assistant** | Người khiếm thị | ✅ | ✅ (sai số nhập STK, mất thời gian đọc màn hình) | ✅ (thời gian giao dịch, tỉ lệ lỗi) | ✅ (có data mẫu QR, ảnh) | ✅ (có rule, có workflow, có tiềm năng agent) | **38** |
| **Voice‑Banking Search** | Người dùng thông thường | ✅ | ✅ (khó tìm giao dịch cũ) | ❌ (không có baseline thời gian) | ✅ | ❌ (chỉ là tìm kiếm) | 27 |
| **Automated Refund Bot** | Nhân viên CS | ✅ | ✅ (thủ tục phức tạp) | ❌ (không đo được tần suất) | ✅ | ❌ (cần tích hợp nhiều hệ thống) | 25 |

**Quyết định**: Chọn **Blind‑Payment Assistant** làm vấn đề nhóm.

### Quick validation

| Nguồn | Số người | Đánh giá | Ghi chú |
|------|----------|----------|----------|
| Phỏng vấn 3 người khiếm thị | 3 | 2/3 cho biết “đọc số tài khoản từ màn hình” tốn ≈ 1 phút, sai số nhập ≈ 2 % | Xác nhận pain thực tế |
| Khảo sát nhanh trong lớp (10 người) | 10 | 7/10 muốn có “AI đọc to và xác nhận lại” trước khi nhấn “gửi” | Thêm yêu cầu “phát âm chính xác” |
| Thử nghiệm 2 tuần (mock data) | 2 | Thời gian giao dịch giảm từ 90 s → 35 s, lỗi nhập giảm 70 % | Đánh giá khả thi của workflow |

**Insight**
* Người dùng không muốn AI *tự* quyết định số tiền; họ chỉ cần **hỗ trợ đọc, xác thực và tạo lệnh**.
* “Human‑in‑the‑loop” là ranh giới an toàn nhất: AI chỉ dừng lại ở **bước 3 – Xác nhận**.

### Research (các giải pháp đã có)

| Nguồn / công cụ | Link | Được giải quyết phần nào? | Điểm mạnh | Khoảng trống / rủi ro |
|----------------|------|--------------------------|-----------|----------------------|
| **Microsoft Seeing AI** | https://www.microsoft.com/seeing-ai | OCR + đọc to ảnh tài liệu | Hỗ trợ người khiếm thị mạnh, có nhận dạng QR | Không tích hợp ngân hàng, không tạo lệnh |
| **Google Pay Voice** | https://pay.google.com/voice | Nhận lệnh thoại, tạo giao dịch | Được Google duyệt, bảo mật cao | Không có bước “hiển thị/đọc lại” cho người khiếm thị |
| **FinTech OCR SDK** (e.g., ABBYY) | https://www.abbyy.com/fintech/ocr | Trích xuất STK, Mã ngân hàng | Độ chính xác cao | Cần custom flow, không có giao diện người dùng đặc thù |
| **OpenAI Whisper + GPT‑4** | https://openai.com/research/whisper | Chuyển giọng nói → văn bản, tạo bản tóm tắt | Linh hoạt, có khả năng “read‑back” | Rủi ro bảo mật dữ liệu nhạy cảm khi gửi lên cloud |

**Takeaway**
* Không có giải pháp nào đáp ứng **đủ 3 bước** (OCR → lookup → read‑back) **và** giữ **human‑in‑the‑loop**.
* Vì vậy, chúng ta sẽ **kết hợp**: OCR SDK → Lookup API → GPT‑4 (đọc to + tạo bản tóm tắt) → UI cho người dùng xác nhận.

### Workflow before / after

#### Current workflow (hand‑held)
```
[1] Người dùng mở app ngân hàng → 
[2] Nhập STK, số tiền, mô tả → 
[3] Kiểm tra (đọc màn hình) → 
[4] Nhập OTP → 
[5] Giao dịch hoàn tất
```
*Thời gian trung bình*: **≈ 90 giây** (trong đó 25 s để đọc và kiểm tra màn hình). 
*Rủi ro*: Nhầm số tài khoản (≈ 2 %), lỗi nhập số tiền (≈ 1 %).

#### Future workflow (Blind‑Payment Assistant)
```
[1] Người dùng chụp ảnh QR / giấy tờ → 
[2] Vision Agent (OCR) → trích xuất STK & mã ngân hàng → 
[3] Lookup Agent (bank API) → xác thực tên người nhận → 
[4] Confirmation Agent → AI đọc to STK, tên, số tiền → 
[5] Người dùng xác nhận (voice hoặc button) → 
[6] Transfer Agent → tạo lệnh và chuyển tới bước OTP/ sinh trắc học của ngân hàng → 
[7] Giao dịch hoàn tất
```
*Thời gian dự kiến*: **≈ 35 giây** (các bước 2‑4 tự động, chỉ còn bước 5 để xác nhận). 
*Rủi ro mới*: AI “hallucinate” tên người nhận → được giảm bằng **human verification** (bước 5).

### Problem Statement v1 (Blind‑Payment)
| Field | Nội dung |
|------|----------|
| **Actor** | Người khiếm thị (độ thị lực < 20 %) thực hiện giao dịch ngân hàng qua smartphone. |
| **Current workflow** | Nhập STK bằng tay → đọc/kiểm tra trên màn hình → nhập OTP → hoàn tất. |
| **Bottleneck** | Đọc và kiểm tra STK trên màn hình mất ≈ 25 s, tỉ lệ nhập sai ≈ 2 %. |
| **Impact** | Thời gian giao dịch kéo dài, gây lo lắng, tăng nguy cơ lỗi tài chính. |
| **Success metric** | Giảm thời gian giao dịch xuống < 40 s, giảm lỗi nhập STK < 0.5 %. |
| **Boundary** | AI **KHÔNG** tự quyết định số tiền hay gửi lệnh; phải có **xác nhận cuối cùng** của người dùng. |
| **AI intervention point** | Sau khi Vision Agent trích xuất STK & Lookup Agent xác thực tên, AI đọc to thông tin và chờ người dùng xác nhận. |
| **Chosen level** | **Workflow**: rule (các API ngân hàng) + các agent chuyên nhiệm vụ (OCR, lookup, confirm, transfer). |
| **Risk & mitigation** | - Hallucination tên người nhận → xác nhận bằng giọng (human). <br> - Bảo mật dữ liệu OCR → xử lý cục bộ, không gửi ảnh lên cloud. |

### Decision & pilot plan
**Decision**: Tiến hành **pilot** dạng **Workflow** với 4 agents đã mô tả.

| Milestone | Nội dung | KPI |
|-----------|----------|-----|
| **M1** (Week 1) | Xây dựng Vision Agent (OCR + QR) trên thiết bị Android, chạy cục bộ. | Độ chính xác OCR ≥ 95 % trên 200 mẫu ảnh. |
| **M2** (Week 2) | Kết nối Lookup Agent tới API ngân hàng sandbox. | Độ khớp tên người nhận ≥ 98 % (so sánh với dữ liệu thực). |
| **M3** (Week 3) | Integrate Confirmation Agent → TTS đọc STK, tên, số tiền. | Thời gian đọc ≤ 5 s, người dùng xác nhận > 90 % lần. |
| **M4** (Week 4) | End‑to‑end test với 5 người khiếm thị thực tế. | Giảm thời gian giao dịch trung bình từ 90 s → < 40 s, lỗi nhập < 0.5 %. |
| **Exit / rollback** | Nếu lỗi nhập > 1 % hoặc người dùng không tin tưởng AI, quay lại giao diện nhập tay + template. | — |

---


**Bài học chung**
1. **Problem‑first** luôn quan trọng hơn “công nghệ có thể làm gì”.
2. **Workflow** là bước trung gian hợp lý khi có **rule** cho data collection và **human‑in‑the‑loop** cho quyết định cuối.
3. **Agent** chỉ cần triển khai khi workflow quá phức tạp, có nhiều nhánh quyết định động.
4. Khi làm việc với người khuyết tật, **privacy & accessibility** phải được đặt lên hàng đầu – mọi bước AI cần được thực hiện **cục bộ** hoặc có **đồng ý rõ ràng**.

---

