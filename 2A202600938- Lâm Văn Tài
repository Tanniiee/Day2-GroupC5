> Case nhóm: **Kính hỗ trợ thanh toán độc lập cho người người khiếm thị tại Việt Nam**
>
> Actor: Người khiếm thị (bẩm sinh, mù do bệnh lý hoặc tai nạn, thị lực rất thấp) thực hiện giao dịch tài chính hằng ngày một mình tại Việt Nam.
 
---
 
# 01 — Individual Problem Scan
 
## Scan rộng
 
Tôi tập trung scan 10 problems dựa trên lăng kính: **Sự cô lập thông tin trực quan** và **thiếu cơ chế phản hồi bằng âm thanh (Audio Feedback)** trong môi trường thanh toán số và tiền mặt tại Việt Nam.
 
| # | Lăng kính | Problem quan sát được | Ai đang đau? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Lặp lại | Không thể tự kiểm tra số dư hiển thị trên màn hình điện thoại khi mở app ngân hàng | Người khiếm thị | VoiceOver/TalkBack thường đọc sai cấu trúc số tiền (Ví dụ: đọc "100000" thành các chữ số rời rạc hoặc bỏ sót số 0) |
| 2 | Pain từ người khác | Người khiếm thị dễ bị lừa đưa nhầm mệnh giá tiền lớn khi mua sắm ở chợ truyền thống | Người khiếm thị | 3/3 người được hỏi thừa nhận từng đưa nhầm tờ 500k thay vì 20k do kích thước và chất liệu polymer khá tương đồng khi cũ |
| 3 | Tốn thời gian | Mất quá nhiều thời gian để canh góc camera điện thoại trúng mã QR đặt tại quầy | Người khiếm thị | Không có tín hiệu âm thanh hướng dẫn "di chuyển camera sang trái/phải", mất trung bình hơn 2 phút chỉ để quét QR |
| 4 | AI có thể tốt hơn | OCR thông thường hoàn toàn bất lực trước các hóa đơn in nhiệt bị mờ hoặc chữ viết tay của chủ quán | Người khiếm thị | Các app như Seeing AI không thể dịch chính xác layout hóa đơn quán ăn vỉa hè Việt Nam |
| 5 | Tốn thời gian | Gặp khó khăn khi xác định vị trí vật lý của máy POS hoặc khe cắm thẻ tại các cửa hàng | Người khiếm thị | Phải sờ soạng khắp quầy thanh toán hoặc bắt buộc phải đưa thẻ cho nhân viên làm hộ |
| 6 | Lặp lại | Nguy cơ lộ mã PIN ngân hàng khi nhập bằng voice trên app ở nơi công cộng | Người khiếm thị | Khi bật VoiceOver, app đọc to số đang chọn lên loa ngoài, gây rủi ro bảo mật nghiêm trọng |
| 7 | Pain từ người khác | Không có cách nào kiểm tra số tiền ghi trên biên lai quẹt thẻ POS trước khi ký tên | Người khiếm thị | Hoàn toàn ký đại theo niềm tin vào lời nói của nhân viên thu ngân |
| 8 | Lặp lại | Quá trình nhận tiền thối từ shipper hoặc người bán vé số hoàn toàn dựa vào "độ trung thực" của đối phương | Người khiếm thị | Người khiếm thị không thể kiểm tra nhanh tập tiền lẻ gồm nhiều mệnh giá trộn lẫn |
| 9 | Tốn thời gian | Nhập thủ công số tài khoản ngân hàng từ lời đọc của người khác rất dễ sai sót | Người khiếm thị | Tỷ lệ nhập sai và phải xóa đi nhập lại lên đến 4-5 lần cho một giao dịch |
| 10 | AI có thể tốt hơn | Không thể phân biệt được các sản phẩm có bao bì giống nhau nhưng giá tiền khác nhau trên kệ hàng | Người khiếm thị | Barcode scanner chỉ đọc mã vạch, không đọc được giá tiền và chương trình khuyến mãi thực tế tại quầy |
 
## Top 3
 
| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | **Thiếu khả năng tự xác thực giao dịch (QR, Tiền mặt, POS) theo thời gian thực** | Đánh thẳng vào quyền tự chủ và an toàn tài chính. Có baseline đo lường được bằng thời gian và tỷ lệ sai sót. | Ranh giới giữa việc AI hỗ trợ đọc thông tin và việc AI can thiệp vào lệnh chuyển tiền thực tế. |
| 2 | Nhận diện và đếm tiền polymer Việt Nam trộn lẫn (tiền thối) | Pain cực lớn trong đời sống vỉa hè tại Việt Nam. | Khả năng xử lý của AI khi tờ tiền bị nhăn, cũ hoặc thiếu ánh sáng dưới camera góc rộng. |
| 3 | Định vị vật lý và đọc màn hình máy POS | Giải quyết được bài toán hands-free khi đi siêu thị, trung tâm thương mại. | Khó tiếp cận dataset đa dạng của các dòng máy POS đang lưu hành tại Việt Nam. |
 
## Problem Card #1 — Tự xác thực giao dịch tài chính độc lập
 
**Problem 1 câu:**
 
Người khiếm thị tại Việt Nam hoàn toàn bị "mù thông tin" trong bước xác thực cuối cùng trước khi xuống tiền (không biết QR có đúng tên, tiền thối có đủ mệnh giá, màn hình POS có đúng số tiền), dẫn đến việc mất quyền tự chủ tài chính và đối mặt với rủi ro bị lừa đảo cao.
 
**Actor:**
 
Người khiếm thị (bẩm sinh hoặc do tai nạn) thực hiện các giao dịch mua sắm, thanh toán hằng ngày mà không có người thân đi cùng.
 
**Thời điểm / bối cảnh:**
 
Tại quầy thanh toán của cửa hàng tiện lợi, chợ truyền thống, hoặc khi thanh toán cho shipper tại cửa nhà.
 
**Current workflow (3 hình thức phổ biến tại VN):**
 
```
Tiền mặt:
  Ước lượng tiền trong ví → Đưa tiền mặt → Nhận tiền thối → Cất vào túi mà không thể kiểm tra mệnh giá → Rủi ro bị thối thiếu tiền.
 
Thẻ tín dụng/ATM:
  Đưa thẻ cho nhân viên → Nhân viên quẹt máy POS → Nhân viên đọc số tiền → Người khiếm thị bấm PIN theo cảm giác → Ký biên lai vô điều kiện.
 
Mã VietQR:
  Mở app ngân hàng → Bật VoiceOver → Mò mẫm đưa camera quét QR → App nhận diện (hoặc không) → Không có bước đọc lại tên người nhận và số tiền bằng voice rõ ràng → Bấm chuyển tiền trong lo sợ.
```
 
**Bottleneck:**
 
Sự đứt gãy thông tin ở **bước kiểm tra cuối cùng (Verification step)**. Người dùng không có một công cụ "tai nghe mắt thấy" nào để chuyển đổi dữ liệu trực quan trên màn hình/tờ tiền thành âm thanh tiếng Việt chuẩn xác trước khi ra quyết định.
 
**Impact:**
 
Gây tâm lý sợ hãi, tự ti khi ra ngoài một mình. Phụ thuộc 100% vào sự trung thực của người lạ. Tổn thất tài chính trực tiếp từ các lỗi sai mệnh giá hoặc gian lận từ người bán.
 
**Success metric:**
 
- Thời gian để một người khiếm thị tự xác định đúng mệnh giá tiền hoặc thông tin QR giảm từ vài phút xuống dưới 10 giây.
- Tỷ lệ phát hiện sai lệch thông tin (sai tên người nhận, sai số tiền) đạt > 98%.
- Đạt mức độ độc lập 100% trong khâu kiểm tra (không cần hỏi lại người xung quanh).
**Non-AI alternative:**
 
Sử dụng khuôn đúc nhựa để đo kích thước tiền giấy (quá chậm, không phân biệt được tiền giả/tiền thật cùng kích thước). Dùng VoiceOver mặc định của điện thoại (không đọc được chữ trên ảnh QR hoặc màn hình POS bên ngoài).
 
**AI hypothesis:**
 
Hệ thống AI Multi-modal (Vision-to-Text-to-Speech) tích hợp trên thiết bị đeo (kính) có khả năng quét, trích xuất dữ liệu thực tế (OCR, QR code) và chuyển đổi thành giọng đọc tiếng Việt tự nhiên, đóng vai trò là "mắt thần" xác thực cho người dùng.
 
**Quick gut:** Workflow.
 
### Draft current workflow
 
```
CURRENT STATE — Phụ thuộc hoàn toàn & Rủi ro cao
 
[Phát sinh nhu cầu thanh toán]
  │
  ├── Tiền mặt: Đưa tiền đại → Nhận tiền thối [BẤT LỰC: Không thể đếm hoặc verify mệnh giá]
  ├── Máy POS: Đưa thẻ cho thu ngân → Nhập PIN mò [RỦI RO: Không biết máy POS đang hiển thị bao nhiêu tiền]
  └── Mã VietQR: Mò mẫm canh góc camera [TỐN THỜI GIAN] → Không có voice confirm tên/số tiền → Bấm chuyển đại
  │
  └──> Kết quả: Thường xuyên mất tiền, tốn 5-15 phút, tâm lý lo lắng.
```
 
### Draft future workflow
 
```
FUTURE STATE — Độc lập & Tự tin (Nhờ Kính AI hỗ trợ)
 
[Phát sinh nhu cầu thanh toán]
  │
  ├── Tiền mặt: Kính AI quét tập tiền thối → Loa đọc: "Tổng nhận 75 nghìn, gồm 1 tờ 50k, 1 tờ 20k, 1 tờ 5k"
  ├── Máy POS: Kính AI nhìn màn hình POS → Loa đọc: "Số tiền cần thanh toán là 120 nghìn. Bàn phím số bắt đầu từ đây..."
  └── Mã VietQR: Kính tự động bắt mã QR từ xa → Loa xác nhận: "Chuyển khoản đến Nguyễn Văn A, số tiền 50 nghìn"
  │
  └──> [HUMAN BOUNDARY]: Người dùng nghe rõ thông tin xác thực từ AI -> Tự tay bấm nút Xác nhận hoặc đưa tiền -> Hoàn tất giao dịch an toàn trong 2 phút.
```
 
## Problem Cards #2 và #3 — tóm tắt
 
| **Card** | **Actor** | **Bottleneck** | **Metric** | **Quick gut** | **Vì sao chưa chọn làm #1** |
| --- | --- | --- | --- | --- | --- |
| Nhận diện và đếm tiền Việt Nam | Người khiếm thị | Tiền Polymer cũ bị mờ, dính, khó phân biệt nếu chỉ sờ | Thời gian nhận diện < 2 giây/tờ | Workflow | Là một phần thuộc bài toán thanh toán lớn, đứng riêng lẻ thì chưa đủ bao phủ |
| Trích xuất hóa đơn giấy tiếng Việt | Người khiếm thị | Chữ in nhiệt mờ, layout lộn xộn, nhiều chữ viết tắt | Tỷ lệ trích xuất đúng item và tổng tiền > 90% | Workflow | Yêu cầu tài nguyên xử lý dữ liệu lớn, khó tối ưu cục bộ (edge) trong giai đoạn đầu |
 
---
 
# 02 — Group Problem Statement
 
## Group convergence
 
Nhóm 4 thành viên, mỗi người đưa ra 3–5 vấn đề cá nhân, tổng cộng 15+ candidates. Sau đó gom thành cluster:
 
| **Cluster** | **Ví dụ vấn đề** | **Điểm chung** |
| --- | --- | --- |
| **Thao tác tài chính** | "AI hỗ trợ thanh toán cho người khiếm thị", "Giao dịch ngân hàng bằng giọng nói", "Khiếu nại giao dịch tự động" | Yêu cầu **lấy dữ liệu tài chính → xác thực → thực thi** và luôn có *human‑in‑the‑loop* |
| **Truy xuất thông tin** | "Tìm lịch sử giao dịch nhanh", "Kiểm tra số dư qua trợ lý ảo" | Tập trung **tìm kiếm & hiển thị** dữ liệu đã có |
| **Báo cáo / giám sát** | "Tổng hợp báo cáo chi tiêu tự động", "Cảnh báo giao dịch gian lận" | Kết hợp **đánh giá rủi ro** và **tóm tắt** dữ liệu |
 
## Shortlist và score
 
| **Candidate** | **Actor rõ** | **Workflow rõ** | **Pain có evidence** | **Impact đo được** | **Làm trong lab** | **So sánh R/W/A** | **Hiểu domain** | **Tổng** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **Blind‑Payment Assistant** | 5 | 5 | 5 | 5 | 5 | 5 | 5 | **38** |
| Voice‑Banking Search | 4 | 4 | 4 | 3 | 4 | 3 | 4 | 27 |
| Automated Refund Bot | 4 | 4 | 4 | 3 | 4 | 3 | 4 | 25 |
 
**Nhóm chọn: Blind‑Payment Assistant.**
 
Vì sao chọn:
 
- Workflow rõ nhất (3 hình thức thanh toán, mỗi hình thức có bottleneck cụ thể).
- Có baseline thời gian đo được.
- Pain thật — xác nhận qua 3 người phỏng vấn khiếm thị.
- Khoảng trống thị trường rõ: không có giải pháp nào tại VN giải đủ 3 bước.
- Có thể so sánh Rule / Workflow / Agent rõ ràng.
Vì sao không chọn các bài khác:
 
- Voice‑Banking Search: chỉ là tìm kiếm, thiếu chiều sâu kỹ thuật.
- Automated Refund Bot: cần tích hợp nhiều hệ thống, không đo được tần suất.
## Quick validation
 
| **Nguồn** | **Số người** | **Tín hiệu xác nhận** | **Tín hiệu phản bác** | **Nhóm sửa problem thế nào** |
| --- | --- | --- | --- | --- |
| Phỏng vấn người khiếm thị | 3 | 2/3 xác nhận "đọc số tài khoản từ màn hình" tốn ≈ 1 phút, sai số nhập ≈ 2% | 1 người nói đã quen nhờ con cái | Giữ nguyên problem, thêm context VN (QR payment dominant) |
| Khảo sát nhanh trong lớp | 10 | 7/10 muốn có "AI đọc to và xác nhận lại" trước khi nhấn "gửi" | Một số lo ngại bảo mật | Thêm boundary: xử lý cục bộ, không gửi ảnh lên cloud |
| Thử nghiệm 2 tuần (mock data) | 2 | Thời gian giao dịch giảm 90 s → 35 s, lỗi nhập giảm 70% | — | Xác nhận tính khả thi của workflow |
 
**Insight sau validation:**
 
```
Pain thật không nằm ở bước "nhập số" đơn thuần.
Pain nằm ở việc không thể TỰ XÁC NHẬN thông tin trước khi bấm gửi.
Human-in-the-loop là ranh giới an toàn: AI chỉ đọc và cấu trúc thông tin, người dùng quyết định cuối.
```
 
## Research giải pháp hiện có
 
| **Nguồn / công cụ** | **Link** | **Họ giải quyết phần nào?** | **Điểm mạnh** | **Khoảng trống / rủi ro** | **Bài học cho nhóm** |
| --- | --- | --- | --- | --- | --- |
| Microsoft Seeing AI | https://www.microsoft.com/seeing-ai | OCR + đọc to ảnh tài liệu, nhận dạng QR | Hỗ trợ người khiếm thị mạnh | Không tích hợp ngân hàng, không tạo lệnh, không train trên data VN | Tốt cho một bước nhận dạng, chưa đủ cho cả workflow |
| Google Pay Voice | https://pay.google.com/voice | Nhận lệnh thoại, tạo giao dịch | Bảo mật cao, được duyệt | Không có bước "đọc lại" cho người khiếm thị | Pattern: AI tạo lệnh nhưng thiếu confirmation step |
| Envision Glasses | https://www.letsenvision.com | OCR hands-free, nhận dạng tiền, đọc màn hình | Hands-free hoàn toàn, $2,499 | Giá cao, không tích hợp thanh toán VN, không có QR voice-confirm | Proof of concept phần cứng, chưa giải bài toán VN |
| OrCam MyEye 3 Pro | https://www.orcam.com | Đọc văn bản mọi bề mặt, nhận dạng sản phẩm | Clip-on, dùng giọng/cử chỉ | Đang đóng mảng phát triển kính đọc; chưa có VN payment flow | Không nên phụ thuộc platform này |
| Be My Eyes + Ray-Ban Meta | https://www.bemyeyes.com | Mô tả visual thời gian thực hands-free | Tích hợp 2024 | Không có QR payment confirm, cần kết nối internet tốt | Pattern hay: real-time visual description |
| FinTech OCR SDK (ABBYY) | https://www.abbyy.com/fintech/ocr | Trích xuất STK, mã ngân hàng | Độ chính xác cao | Cần custom flow, không có UI người dùng | Có thể dùng làm Vision component trong workflow |
 
**Research takeaway:**
 
```
Không có giải pháp nào đáp ứng đủ 3 bước (nhận dạng → xác nhận tên/số tiền → human confirmation)
VÀ phù hợp VN context (VietQR, hóa đơn tiếng Việt có dấu, tiền polymer VN).
 
Khoảng trống thật sự: QR payment voice-confirmation + đọc hóa đơn tiếng Việt.
Đây là 2 điểm có differentiation rõ ràng so với Envision Glasses hay Seeing AI.
```
 
## Workflow before / after
 
### Current state — không có hỗ trợ
 
```
CURRENT STATE — 5–15 phút / giao dịch
 
[Muốn thanh toán]
  ↓
[Chọn hình thức]
  ├── Tiền mặt
  │     [Lấy tiền ra ví]             ← Không biết mệnh giá / RỦI RO
  │     [Đưa tiền cho người bán]
  │     [Nhận tiền thối]             ← Phải nhờ người khác đếm / RỦI RO
  │
  ├── Thẻ credit
  │     [Tìm khe cắm thẻ POS]         ← Sờ mò thủ công
  │     [Nhập PIN]                    ← Không đọc được màn hình POS
  │     [Xác nhận số tiền]            ← Không biết máy hiện thị gì / RỦI RO
  │     [Nhận biên lai in]            ← Không đọc được nội dung
  │
  └── QR / ví điện tử
        [Mở app thanh toán]           ← Dùng VoiceOver/TalkBack
        [Quét mã QR]                  ← Không nhìn thấy mã / RỦI RO
        [Xác nhận người nhận]         ← Không verify tên/số tiền / RỦI RO
        [Gửi tiền]                    ← Hy vọng đúng người
  ↓
[Kết quả chung]
Phụ thuộc người khác, rủi ro bị lợi dụng
Thời gian trung bình: 5–15 phút / giao dịch
Bottleneck (đỏ): không verify số tiền, không đọc màn hình, không đọc mã QR
```
 
### Future state — có kính AI
 
```
FUTURE STATE — 2–3 phút / giao dịch
 
[Muốn thanh toán]
  ↓
[Chọn hình thức]
  ├── Tiền mặt
  │     [Kính nhận dạng tờ tiền]      → AI: "200.000 đồng"
  │     [Đưa tiền]                    → Đã biết mệnh giá
  │     [Nhận tiền thối]              → AI: Kính đếm và xác nhận
  │
  ├── Thẻ credit
  │     [Kính hướng dẫn cắm thẻ]      → AI: "Khe thẻ ở phía trái"
  │     [Nhập PIN]                    → AI: Kính đọc bàn phím → user tự nhập
  │     [Xác nhận số tiền]            → AI: Kính đọc màn hình → user xác nhận ← HUMAN DECISION
  │
  └── QR / ví điện tử
        [Kính quét mã QR]             → AI: Tự phát hiện mã trong tầm nhìn
        [Xác nhận người nhận]         → AI: "Nguyễn Văn A – 150.000đ" ← HUMAN DECISION
        [Người dùng xác nhận]         → User: "OK" hoặc nhấn nút ← HUMAN DECISION
        [Gửi tiền]                    → Đúng người, đúng số tiền
  ↓
[Giao dịch hoàn tất — độc lập, tự xác nhận]
Thời gian: 2–3 phút / giao dịch
Human boundary (vàng): Người dùng → tự quyết định xác nhận hay huỷ
```
 
**Before/after impact:**
 
| **Metric** | **Trước** | **Sau kỳ vọng** | **Ghi chú** |
| --- | --- | --- | --- |
| Thời gian giao dịch | 5–15 phút | < 3 phút | Gồm cả 3 hình thức |
| Tỉ lệ giao dịch đúng | Không đo được (phụ thuộc người khác) | > 95% | Không cần người hỗ trợ |
| Mức độ độc lập | Phụ thuộc | Tự chủ | Người dùng tự quyết định |
| Risk AI | Không có hallucination risk | Có (sai tên, sai số) | Giảm bằng human confirmation |
 
## Problem Statement v1
 
| **Field** | **Nội dung** |
| --- | --- |
| **Actor** | Người khiếm thị tại Việt Nam — bao gồm mù bẩm sinh, mù do bệnh lý hoặc tai nạn, và người thị lực rất thấp — khi thực hiện giao dịch tài chính hằng ngày một mình. |
| **Workflow** | Người khiếm thị cần thanh toán qua 3 hình thức phổ biến tại VN: tiền mặt (sờ phân biệt mệnh giá → đưa → nhận thối nhờ người khác đếm), thẻ credit (sờ mò POS → nhập PIN → không đọc được màn hình xác nhận → nhận biên lai không đọc được), QR/ví điện tử (không nhìn thấy mã QR → không verify tên người nhận và số tiền trước khi gửi). |
| **Bottleneck** | Người khiếm thị không thể tự xác nhận thông tin giao dịch (tên người nhận, số tiền, mã QR) — phải phụ thuộc vào người xung quanh hoặc chấp nhận rủi ro giao dịch sai. |
| **Impact** | Mất quyền tự chủ tài chính. Dễ bị lợi dụng (tiền thối, số tiền tính sai). Tránh né giao dịch ngoài đời thực. Phụ thuộc người thân cho mọi khoản chi tiêu nhỏ. |
| **Success Metric** | Giảm thời gian giao dịch từ 5–15 phút xuống dưới 3 phút. Tỉ lệ giao dịch đúng số tiền > 95% (không cần người hỗ trợ). Người dùng hoàn thành giao dịch mà không cần nhờ ai. |
| **Boundary** | AI **KHÔNG** tự quyết định hình thức thanh toán, số tiền, hay xác thực giao dịch. Người dùng luôn nghe thông tin và tự xác nhận trước khi bất kỳ lệnh nào được thực thi. |
| **AI intervention point** | Nhận dạng (tiền mặt, QR, màn hình POS, biên lai in) và đọc to thông tin để người dùng xác nhận — trước bước người dùng quyết định. |
| **Mức chọn** | **Workflow**: rule cho các bước có cấu trúc (OCR SDK, VietQR API), AI cho nhận dạng ngữ cảnh và đọc to, người dùng cho xác nhận cuối. |
| **Rủi ro & người thật kiểm tra** | Nhận dạng sai (sai số tiền, sai tên) → human confirmation bắt buộc. OCR nhầm STK → người dùng nghe lại và sửa. Xử lý ảnh cục bộ để bảo mật. |
 
## Rule / Workflow / Agent
 
| **Mức** | **Phương án** | **Khi nào đủ** | **Rủi ro** | **Chọn?** |
| --- | --- | --- | --- | --- |
| **Rule** | App có accessibility tốt (VoiceOver, TalkBack được tối ưu) + NFC talking POS | Đủ cho bước điều hướng UI cơ bản | Không giải được QR reading, biên lai tiếng Việt, tiền thối | Dùng cho một số bước, không đủ toàn bộ |
| **Workflow** | OCR/Vision nhận dạng → AI đọc to thông tin → Người dùng xác nhận → Tạo lệnh | Hợp vì workflow tuyến tính, AI chỉ nhận dạng và đọc, người dùng quyết định | Hallucination tên/số, cần human check | **Chọn** |
| **Agent** | Agent tự lấy nhiều nguồn, phân tích bất thường, ra quyết định | Chỉ cần cho "phát hiện giao dịch bất thường theo ngữ cảnh cá nhân" — scope mở rộng sau | Quá rộng, many permission risk, chưa có data history | Chưa chọn — để sau |
 
**Mức chọn: Workflow.**
 
Vì sao:
 
- 3 hình thức thanh toán đều có workflow tuyến tính, ít nhánh động.
- AI nằm ở bước nhận dạng và đọc to — không cần lập kế hoạch động.
- Người dùng luôn là người quyết định cuối → kiểm soát được risk.
- Chưa cần agent vì chưa có data history cá nhân để phân tích bất thường.
## Final decision
 
**Decision: Go với scope nhỏ — pilot Workflow với 3 agent chuyên nhiệm vụ.**
 
**Pilot nhỏ nhất:**
 
- Vision Agent: OCR + QR reading cục bộ trên thiết bị Android.
- Confirmation Agent: TTS đọc STK, tên người nhận, số tiền bằng tiếng Việt.
- Transfer Agent: Điền sẵn thông tin vào form chuyển khoản, chờ người dùng xác nhận.
**Milestone:**
 
| **Milestone** | **Nội dung** | **KPI** |
| --- | --- | --- |
| **M1** (Week 1) | Vision Agent: OCR + QR chạy cục bộ | Độ chính xác ≥ 95% trên 200 mẫu ảnh |
| **M2** (Week 2) | Lookup Agent kết nối VietQR API sandbox | Khớp tên người nhận ≥ 98% |
| **M3** (Week 3) | Confirmation Agent: TTS đọc thông tin tiếng Việt | Thời gian đọc ≤ 5 s, user xác nhận > 90% lần |
| **M4** (Week 4) | End-to-end test với 5 người khiếm thị thực tế | Thời gian < 3 phút, lỗi nhập < 0.5% |
 
**Exit / rollback:**
 
- Nếu lỗi nhận dạng > 5% trong 2 tuần liên tiếp → hạ về app VoiceOver + template nhập tay.
- Nếu người dùng không tin tưởng AI (xác nhận mà không nghe → không dùng) → redesign UX, bắt buộc nghe trước khi OK.
---
 
# 03 — Individual Reflection
 
## Đóng góp của tôi trong nhóm
 
| **Hoạt động** | **Tôi đã làm gì?** | **Kết quả** |
| --- | --- | --- |
| Scan cá nhân | Tập trung mổ xẻ rào cản đa phương thức (Vision-to-Audio) và rủi ro mất an toàn thông tin của người khiếm thị Việt Nam. | Mang đến góc nhìn thực tế về sự bất lực của các bộ đọc VoiceOver mặc định, chuyển hướng nhóm tập trung vào bước **Xác thực thông tin thực tế**. |
| Pitch | Pitch ý tưởng: "Bài toán không nằm ở khâu bấm nút chuyển tiền, mà nằm ở khâu kiểm tra xem nút đó có đúng thông tin hay không". | Thuyết phục nhóm chọn hướng tiếp cận tập trung vào "Xác thực bằng giọng nói bản địa" thay vì chỉ làm chatbot ra lệnh thông thường. |
| Challenge | Đặt câu hỏi phản biện: "Nếu AI đọc sai tên hoặc số tiền do chữ in mờ, làm sao user biết để hủy giao dịch?" | Giúp nhóm định hình rõ ranh giới **Human-in-the-loop** (AI chỉ là trợ lý cung cấp thông tin, quyền duyệt thuộc về con người). |
| Workflow | Thiết kế chi tiết quy trình chuyển đổi thông tin từ hình ảnh vật lý (mã QR, tiền mặt, POS) thành Audio feedback tiếng Việt. | Cấu trúc hóa được workflow cho cả 3 hình thức thanh toán, làm tiền đề để giữ nguyên khung kết luận của nhóm. |
| Research | Khảo sát sâu các hạn chế của Seeing AI và Envision Glasses khi xử lý ngôn ngữ tiếng Việt và ngữ cảnh chợ truyền thống tại VN. | Tìm ra "khoảng trống vàng": Chưa có thiết bị nào giải quyết đồng thời việc đếm tiền polymer và đọc lệnh xác nhận VietQR bằng tiếng Việt. |
| Rule/Workflow/Agent | Phân tích lý do tại sao phương án Agent chủ động tự ra quyết định chi tiêu là quá nguy hiểm ở thời điểm hiện tại. | Nhóm đồng thuận tuyệt đối dừng lại ở mức **Workflow**, đảm bảo an toàn tuyệt đối cho tài khoản của người dùng khiếm thị. |
 
## Bảng dùng AI trong quá trình làm
 
| **Phase** | **Tôi dùng AI để làm gì?** | **AI hữu ích ở đâu?** | **AI sai/hời hợt ở đâu?** | **Tôi sửa gì** |
| --- | --- | --- | --- | --- |
| Scan | Brainstorm các kịch bản người khiếm thị bị lừa đảo hoặc gặp sự cố khi giao dịch tiền mặt. | Gợi ý tốt case-study về việc nhầm lẫn mệnh giá tiền polymer cũ/mới dựa trên kích thước. | Đề xuất giải pháp mang tính lý thuyết như "yêu cầu chính phủ in lại tiền có mã QR" — phi thực tế. | Loại bỏ các đề xuất vĩ mô, kéo AI về việc giải quyết bài toán ngay trên camera kính đeo. |
| Research | Tra cứu nhanh thông số kỹ thuật và lý do mảng phần cứng của OrCam MyEye gặp khó khăn. | Tổng hợp dữ liệu thị trường nhanh chóng, tiết kiệm thời gian đọc tài liệu tiếng Anh. | Nhầm lẫn giữa tính năng của Envision Glasses và Ray-Ban Meta. | Tự kiểm chứng lại qua trang chủ của từng hãng để phân loại đúng tính năng. |
| Workflow | Tạo bản nháp sơ đồ chuỗi hành vi từ lúc camera bắt được hình ảnh đến lúc phát ra âm thanh. | Cấu trúc văn bản dạng cây (Text-tree) rất mạch lạc, dễ nhìn. | AI tự ý thêm bước "Tự động trích tiền từ ví điện tử" mà không qua lệnh xác nhận của user. | Đẩy bước "Người dùng nói OK / Bấm nút cơ học" lên làm chốt chặn bắt buộc trước khi chuyển tiền. |
| Problem Statement | Nhờ AI đóng vai một chuyên gia bảo mật để phản biện Problem Statement v1. | Chỉ ra lỗ hổng lớn về việc bảo mật camera (nguy cơ lộ thông tin màn hình POS hoặc mã PIN). | Đề xuất giải pháp dùng mã hóa blockchain quá phức tạp và không cần thiết. | Sửa lại boundary: Toàn bộ quá trình OCR và xử lý ảnh phải thực hiện **local offline ngay trên thiết bị đeo**, không đẩy data lên cloud. |
| Scoring | Pre-fill ma trận điểm số dựa trên các tiêu chí Lab-readiness và Impact. | Tiết kiệm 80% thời gian gõ văn bản, giải thích logic chấm điểm khá hợp lý. | Đánh giá quá cao mức độ sẵn sàng của dữ liệu hóa đơn viết tay tiếng Việt (chấm 5/5). | Hạ điểm tiêu chí này xuống 2/5 vì nhận thấy chữ viết tay tiếng Việt là một "cơn ác mộng" đối với các mô hình OCR nhỏ chạy local. |
 
## Bài học của tôi
 
**Bài học 1 — AI sinh ra để làm chiếc gậy dẫn đường, không phải để làm người đại diện thay thế.**
 
Khi bắt đầu, tôi luôn nghĩ AI phải tự động làm hết mọi thứ cho người khiếm thị. Nhưng sau khi đào sâu bài toán, tôi hiểu rằng đối với nhóm người dùng yếu thế, **sự an tâm và tính tự chủ** mới là vô giá. AI chỉ cần làm tốt nhiệm vụ "dịch chuyển thế giới trực quan thành thế giới âm thanh" một cách chính xác nhất để họ tự ra quyết định.
 
**Bài học 2 — Hãy giải quyết bài toán ở nơi nó xảy ra, đừng giải quyết trong phòng Lab.**
 
Một ứng dụng quét QR trên điện thoại dù có tốt đến mấy cũng sẽ thất bại nếu người khiếm thị phải mất 2 phút đứng xoay xở camera giữa một hàng dài người đang đợi thanh toán phía sau. Việc chuyển đổi giải pháp sang dạng **thiết bị đeo hands-free (kính AI)** là bước ngoặt giúp workflow thực sự khả thi trong đời sống thực tế tại Việt Nam.
 
**Bài học 3 — Sức mạnh của sự kết hợp: Rule để định hướng, Workflow để xử lý.**
 
Không cần thiết phải dùng các mô hình Agent quá cao siêu để lập kế hoạch động. Việc kết hợp chặt chẽ giữa các thuật toán Rule-based (như bắt góc mã QR, API định dạng VietQR) kết hợp với AI Vision cục bộ để nhận diện mệnh giá tiền chính là công thức tối ưu nhất: Vừa nhanh, vừa chính xác, vừa không tốn tài nguyên mạng.
 
**Bài học 4 — Bảo mật cho người khuyết tật phải nghiêm ngặt gấp đôi người thường.**
 
Một khi người khiếm thị đã trao trọn niềm tin cho chiếc kính AI để đọc hộ số tiền và thông tin tài khoản, họ hoàn toàn đặt mình vào trạng thái dễ bị tổn thương. Thiết kế một hệ sinh thái xử lý cục bộ (Edge AI), không lưu trữ hình ảnh cá nhân lên máy chủ bên thứ ba không chỉ là một tính năng — đó là đạo đức làm sản phẩm.
 
**Nếu làm lại:**
 
```
Tôi sẽ trực tiếp đến các trung tâm bảo trợ khiếm thị để quay video lại cách họ tương tác với tiền mặt 
và điện thoại khi mua sắm thực tế. Việc quan sát trực quan các hành vi nhỏ nhất (như cách họ miết ngón tay 
lên tờ tiền, cách họ ghé sát tai vào loa) sẽ giúp tôi tối ưu hóa phản hồi âm thanh của Confirmation Agent 
ngay từ tuần đầu tiên, thay vì đợi đến Milestone 4 mới nhận ra các lỗi về trải nghiệm người dùng (UX).
```
 
 

