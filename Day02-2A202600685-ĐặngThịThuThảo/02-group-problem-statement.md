# 02 — Group Problem Statement

> Nhóm: [C5] | Thành viên: [Hà Đức, Nguyễn Đăng Huy, Đặng Thị Thu Thảo, Lâm Văn Tài,]

---

## Nhật ký hội tụ (Phase 3)

### Bước 3.1 — Tổng hợp candidates từ các thành viên

| # | Người đưa ra | Candidate problem | Người gặp vấn đề | Điểm nghẽn | Cảm nhận nhanh |
|---|---|---|---|---|---|
| 1 | [Hà Đức] | AI assistant toàn diện cho người khiếm thị trong sinh hoạt tài chính & di chuyển hàng ngày | Người khiếm thị tại VN (~1.8M người) | Không đọc được màn hình, QR, tiền mặt, bảng giá, biển hiệu — phụ thuộc hoàn toàn vào người khác | Thị trường bị bỏ ngỏ, pain rõ ràng, impact lớn |
| 2 | [Lâm Tài] | Thanh toán độc lập: nhận diện QR, POS, xác nhận số tiền | Người khiếm thị | Không verify được số tiền phải trả, dễ bị lừa/nhầm | Sub-problem của #1, agent, khả thi với camera |
| 3 | [Đăng Huy] | Nhận dạng tiền mặt (mệnh giá, tờ thật/giả) | Người khiếm thị | Không phân biệt tờ 50k vs 500k khi cầm tiền thối | Sub-problem của #1, model nhận dạng ảnh, dễ đo |
| 4 | [Thu Thảo] | Điều hướng trong siêu thị / cửa hàng (tìm sản phẩm, đọc giá, hạn dùng) | Người khiếm thị | Phải nhờ nhân viên, mất tự chủ, xấu hổ khi mua sắm | Sub-problem của #1, cần multimodal, AR tiềm năng |
| 5 | [Đăng Huy] | Đọc và hiểu hóa đơn, hợp đồng, giấy tờ in tay | Người khiếm thị | Ký nhầm, bị lợi dụng khi không đọc được nội dung | Sub-problem của #1, OCR + summarize, privacy nhạy cảm |
| 6 | [Thu Thảo] | Hỗ trợ di chuyển: đọc biển xe buýt, số tuyến, giờ khởi hành | Người khiếm thị đi xe công cộng | Không đọc được bảng điện tử, bảng giấy ở bến xe | Sub-problem của #1, real-time, location-aware |
| 7 | [Hà Đức] | Mô tả môi trường xung quanh theo ngữ cảnh (đang ở đâu, có gì trước mặt) | Người khiếm thị mới ra ngoài một mình | Mất định hướng, lo sợ, không dám đi một mình | Sub-problem của #1, agent phức tạp, high value |
| 8 | [Thu Thảo] | Nhận diện người đối diện, đọc cảm xúc khuôn mặt trong giao tiếp | Người khiếm thị trong công việc / xã hội | Bỏ lỡ tín hiệu phi ngôn ngữ, giao tiếp kém tự tin | Sub-problem của #1, ethical risk (privacy), cần cân nhắc |
| 9 | [Thu Thảo] | Trợ lý điền form online / app cho người khiếm thị (BIDV, MoMo, v.v.) | Người khiếm thị dùng smartphone | App không accessible, screen reader không đọc được nút bấm | Sub-problem, workflow rõ, tích hợp accessibility API |
| 10 | [Hà Đức] | Đọc menu nhà hàng, gọi món độc lập không cần nhờ người | Người khiếm thị đi ăn ngoài | Menu in giấy, không có braille, phải hỏi nhân viên | Sub-problem của #1, camera + voice, quick win |
| 11 | [Lâm Tài] | Cảnh báo nguy hiểm thụ động: bậc thang, vật cản, xe đang đến | Người khiếm thị đi bộ | Cần phản xạ nhanh, tai nghe liên tục | Sub-problem của #1, safety-critical, latency thấp là must |
| 12 | [Thu Thảo] | Hỗ trợ tìm việc: đọc JD, soạn CV, luyện phỏng vấn cho người khiếm thị | Người khiếm thị đang tìm việc | JD không accessible, CV khó soạn không nhìn thấy layout | Adjacent problem, workflow rõ, measurable impact |
| 13 | [Đăng Huy] | Giảm thời gian dùng điện thoại: AI phân tích habit, gợi ý giới hạn & thay thế | Người trẻ / gen Z bị phone addiction | Dùng quá nhiều mà không nhận ra, app hiện tại chỉ báo số liệu thô không có hành động | Behavior change, metric rõ (screen time), cạnh tranh với OS built-in |
| 14 | [Thu Thảo] | Auto-generate commit description từ diff code cho newbie | Dev intern / junior dev | Viết commit message chung chung ("fix bug", "update"), mất 5-10'/lần nếu làm đúng | Workflow lặp lại cao, quick win, dễ đo quality |
| 15 | [Thu Thảo] | Trợ lý cá nhân quản lý task + tự động tạo plan ngày dựa trên todo list | Người đi làm, freelancer, sinh viên | Có task nhưng không biết sắp xếp thứ tự ưu tiên, plan ngày mất 15-30' mỗi sáng | Agent, tích hợp calendar tiềm năng, thị trường rộng |
| 16 | [Hà Đức] | Nhận diện đèn giao thông và cảnh báo khi băng qua đường | Người khiếm thị đi bộ qua đường | Không biết tín hiệu đã bật xanh/chuyển đỏ, dễ gặp nguy hiểm khi băng qua đường | Cần real-time, camera + object detection, an toàn cao | 
| 17 | [Lâm Tài] | Trợ lý kiểm soát tủ đồ: chọn trang phục, nhận diện quần áo, thông báo đồ bỏ quên | Người khiếm thị tự phục trang hàng ngày | Khó chọn đồ, không biết trong tủ có gì, dễ mặc sai hoặc quên mất món đồ cần dùng | Hỗ trợ tự chủ cá nhân, có thể học thói quen, tích hợp voice và barcode/QR nội bộ |

### Bước 3.2 — Cluster

| Cluster | Candidates | Pattern chung | Ghi chú |
|---|---|---|---|
| A — Developer & personal productivity | #13, #14, #15 | Tự động hóa hoặc hỗ trợ các bước lặp lại trong workflow cá nhân / dev — viết code message, sắp xếp task, giảm screen time | Scope nhỏ, dễ validate, ít impact xã hội; cạnh tranh cao với tool đã có |
| B — Accessibility: thanh toán & tài chính | #2, #3 | Hỗ trợ người khiếm thị thực hiện giao dịch tài chính độc lập — nhận diện QR, tiền mặt, xác nhận số tiền | Impact lớn, thị trường VN bị bỏ ngỏ, AI thật sự cần thiết ở nhiều bước |
| C — Accessibility: di chuyển & môi trường | #4, #6, #7, #11, #16 | Hỗ trợ người khiếm thị nhận diện và điều hướng trong không gian thực — siêu thị, xe buýt, đường đi bộ, môi trường xung quanh | Safety-critical, latency thấp là yêu cầu cứng, phức tạp phần cứng cao |
| D — Accessibility: thông tin & xã hội | #1, #5, #8, #9, #10, #12, #17 | Hỗ trợ người khiếm thị đọc, hiểu và tương tác với thông tin dạng văn bản, form, menu, JD, hợp đồng, cảm xúc người khác | Đa dạng sub-problem, một số có ethical risk (nhận diện khuôn mặt), một số scope quá rộng cho lab |

### Bước 3.3 — Shortlist

| Candidate | Vì sao vào shortlist | Rủi ro / điều chưa rõ |
|---|---|---|
| #2+#3 — Thanh toán & nhận dạng tiền mặt (gộp thành bài kính hỗ trợ thanh toán) | Pain không có giải pháp tại VN, AI cần thiết ở 3 bước rõ ràng, impact xã hội cao, workflow có thể vẽ được | Actor còn rộng, risk OCR tiếng Việt, cần hardware |
| #6 — Hỗ trợ di chuyển: đọc biển xe buýt, số tuyến, giờ khởi hành | Pain rõ với người khiếm thị đi công cộng, workflow gần thực tế, dữ liệu bảng điện tử và biển báo có thể thu thập | Safety-critical, cần độ trễ thấp, phần cứng camera/edge phức tạp |
| #16 — Nhận diện đèn giao thông để băng qua đường an toàn | Giảm nguy cơ khi đi bộ qua đường, cải thiện an toàn di chuyển | Cần real-time và độ chính xác cao; khó xử lý điều kiện ánh sáng, nhiều loại đèn |

### Bước 3.4 — Score để đồng thuận

| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A được | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| #6 — Hỗ trợ di chuyển | 5 | 5 | 4 | 5 | 5 | 5 | 5 | **34** |
| #2+#3 — Kính thanh toán | 3 | 4 | 5 | 4 | 3 | 5 | 4 | **28** |

**Best choices:** #6, #2 và #3 là những ứng viên hàng đầu theo score và độ cần thiết.

**Candidate nhóm chọn:** #2+#3 — Kính AI hỗ trợ thanh toán cho người khiếm thị tại Việt Nam

**Vì sao chọn:**
Dù #6 có điểm kỹ thuật và tính khả thi cao hơn, nhóm chọn bài kính hỗ trợ thanh toán vì khoảng trống giải pháp tại VN quá rõ — 2 triệu người khiếm thị, QR là chuẩn thanh toán chủ đạo nhưng 100% dựa vào thị giác, không có app hay thiết bị nào được thiết kế cho context VN. AI thật sự cần ở đây (OCR layout tự do, voice confirm, xử lý tiếng Việt) chứ không chỉ là tiện ích thêm.

**Vì sao không chọn các candidate còn lại:**
- #6 (di chuyển): kỹ thuật mạnh nhưng cần latency thấp, phần cứng cao và tính an toàn thời gian thực khiến scope khó thu gọn cho lab.
- #14 (commit message): GitHub template đã giải được phần lớn vấn đề format; AI hypothesis chưa chắc đủ differentiation so với GitHub Copilot và các công cụ đã có.
- #16 (đèn giao thông): an toàn cao nhưng cần real-time và độ chính xác rất lớn; chưa phải pilot core của bài toán thanh toán.
---

## Kiểm chứng nhanh (Phase 4)

### Bước 4.1 — Quick validation

| Nguồn | Số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác | Nhóm sửa problem thế nào |
|---|---:|---|---|---|
| Interview bạn cùng phòng học| 1 người | Xác nhận không dùng được QR trực tiếp, phải nhờ người thân hoặc dùng VoiceOver thủ công — mất 7-10 phút/giao dịch | Một số người đã quen nhờ người thân, chưa thấy cấp thiết vì chưa biết có giải pháp nào khả thi | Thu hẹp actor về người khiếm thị sống độc lập, thành thị |

### Bước 4.2 — Research giải pháp đã có

| Nguồn / tool | Link | Giải quyết phần nào? | Điểm mạnh | Khoảng trống | Bài học cho nhóm |
|---|---|---|---|---|---|
| Envision Glasses | https://www.letsenvision.com | Đọc văn bản, nhận dạng tiền mặt (USD/EUR), mô tả cảnh vật, hands-free | Tích hợp đầy đủ, UX tốt | Không hỗ trợ VND, không tích hợp VietQR, giá $2,499 — quá cao cho VN | Tập trung vào VN context: VietQR + VND + tiếng Việt |
| Seeing AI (Microsoft) | https://www.microsoft.com/en-us/ai/seeing-ai | Nhận dạng tiền mặt, đọc văn bản, barcode | Miễn phí, nhiều tính năng | Cần cầm điện thoại — không hands-free; OCR tiếng Việt yếu | Cần hands-free (kính); cần train data tiếng Việt |
| Be My Eyes + Ray-Ban Meta | https://www.bemyeyes.com | Hỗ trợ realtime qua video, tích hợp kính | Hands-free, community | Phụ thuộc tình nguyện viên/internet; chưa vào VN | Offline mode quan trọng; không nên phụ thuộc người thật |
| VietQR standard | https://vietqr.io | Chuẩn QR liên ngân hàng VN, thống nhất toàn quốc | Phổ biến, tất cả ngân hàng hỗ trợ | Có API nhưng chưa có accessibility layer | Có thể đọc QR → parse tên người nhận + số tiền → voice output |
| MoMo / ZaloPay accessibility | — | Chưa có chế độ accessibility riêng | Ecosystem lớn (30M+ users) | Phụ thuộc VoiceOver hệ điều hành, không tối ưu QR flow | Giải pháp phải layer trên top của app hiện tại, không replace |

---

## Workflow (Phase 5)

### Bước 5.1 — Current Workflow

```
CURRENT STATE — Thanh toán cho người khiếm thị tại VN

NHÁNH 1: QR CODE (phổ biến nhất — >50% giao dịch bán lẻ)
──────────────────────────────────────────────────────────
[Người bán show QR code]
→ [Người khiếm thị: không nhìn thấy mã]         ← BLOCKED
→ [Nhờ người bên cạnh scan/đọc hộ: 2-5']
→ [Nghe thông tin qua lời người khác — có thể sai]
→ [Mở app banking, nhập tay STK + số tiền: 3-5'] ← BOTTLENECK
→ [Bấm xác nhận — không verify được đã đúng chưa]
→ [Nhận hóa đơn in nhiệt — không đọc được]

NHÁNH 2: TIỀN MẶT
──────────────────────────────────────────────────────────
[Người bán thối tiền lẻ]
→ [Người khiếm thị không phân biệt mệnh giá]    ← BOTTLENECK
→ [Nhờ người kiểm tra hoặc chấp nhận rủi ro]
→ [Không có cách verify độc lập]

NHÁNH 3: THẺ CREDIT / ATM
──────────────────────────────────────────────────────────
[Đưa thẻ cho thu ngân]
→ [Thu ngân nhập số tiền vào POS]
→ [POS hiển thị số tiền — người khiếm thị không đọc được] ← BOTTLENECK
→ [Nhập PIN mà không biết số tiền có đúng không]
→ [Nguy cơ bị tính sai, không phát hiện được]

ĐIỂM CHUNG: Phụ thuộc người thứ ba, không có bước verify độc lập
```

| Bước | Actor | Input | Output | Thời gian | Ghi chú |
|---|---|---|---|---|---|
| 1. Người bán show QR | Người bán | — | QR code | — | Người khiếm thị không thấy |
| 2. Nhờ người scan/đọc | Người thứ ba | QR | Thông tin đọc miệng | 2-5' | Phụ thuộc người khác |
| 3. Mở app banking | Người khiếm thị | — | App mở | 1-2' | VoiceOver không optimize QR flow |
| 4. Nhập tay STK + số tiền | Người khiếm thị | Thông tin nghe lại | Lệnh chuyển tiền | 3-5' | Dễ nhập sai, không confirm rõ |
| 5. Xác nhận giao dịch | Người khiếm thị | — | Giao dịch hoàn tất | 30s | Không verify được đúng chưa |
| 6. Nhận hóa đơn | Người khiếm thị | Hóa đơn giấy | — | — | Không đọc được, bỏ qua |

**Bottleneck chính:** Bước 2 (phụ thuộc người thứ ba) và bước 4-5 (không có verification độc lập trước khi bấm xác nhận).

---

### Bước 5.2 — Future Workflow

```
FUTURE STATE — Kính AI hỗ trợ thanh toán (Agent)

NHÁNH 1: QR CODE
──────────────────────────────────────────────────────────
[Người bán show QR]
→ [Camera kính nhận diện QR: ~1s]
→ [Agent parse VietQR → tên người nhận + STK + ngân hàng]
→ [Voice: "Chuyển 150,000đ cho Nguyễn Văn A — Vietcombank. Xác nhận?"]
→ [Người khiếm thị: "Xác nhận" / "Huỷ"]  ← HUMAN DECISION BOUNDARY
→ [Agent gọi banking API tạo lệnh chuyển tiền]
→ [Voice: "Giao dịch thành công. Mã GD: 123456"]

NHÁNH 2: TIỀN MẶT
──────────────────────────────────────────────────────────
[Người bán đưa tiền thối]
→ [Camera kính nhận dạng từng tờ tiền: ~2s]
→ [Voice: "20,000đ × 2 tờ, 5,000đ × 1 — tổng 45,000đ"]
→ [Người khiếm thị tự kiểm]  ← HUMAN DECISION BOUNDARY

NHÁNH 3: THẺ CREDIT
──────────────────────────────────────────────────────────
[POS hiển thị số tiền]
→ [Camera đọc màn hình POS: ~1s]
→ [Voice: "POS đang hiển thị 230,000đ. Nhập PIN để xác nhận?"]
→ [Người khiếm thị quyết định]  ← HUMAN DECISION BOUNDARY

FALLBACK (AI sai):
→ "Không đọc được, nhờ người hỗ trợ hoặc thử lại"
→ Số tiền bất thường → cảnh báo, không tự xác nhận
→ Mất kết nối → mode manual với voice hướng dẫn từng bước
```

**Before/After impact:**

| Metric | Trước | Sau kỳ vọng | Ghi chú |
|---|---:|---:|---|
| Số bước phụ thuộc người khác | 3/5 bước | 0/5 bước | Người khiếm thị độc lập hoàn toàn |
| Thời gian giao dịch QR | 7-10 phút | < 1 phút | Bao gồm voice confirm |
| Tỷ lệ tự verify trước khi xác nhận | 0% | ~95% | ~5% fallback do OCR lỗi |
| Số bước nhập tay STK | 1 bước dễ sai | 0 | Auto-fill từ QR parse |
| Risk mới phát sinh | — | OCR sai → sai STK | Bắt buộc human voice confirm trước mọi GD |

---

### Bước 5.3 — Problem Statement v0

| Field | Nội dung |
|---|---|
| **Actor** | Người khiếm thị (mù hoàn toàn hoặc thị lực rất thấp) tại Việt Nam, đặc biệt nhóm sống độc lập ở đô thị |
| **Workflow** | Thanh toán hằng ngày: QR code (VietQR), tiền mặt VND, thẻ credit/debit tại POS |
| **Bottleneck** | Không thể verify thông tin giao dịch (số tiền, người nhận, mệnh giá) một cách độc lập trước khi xác nhận |
| **Impact** | ~2 triệu người khiếm thị tại VN bị loại khỏi hệ sinh thái QR payment chiếm >50% giao dịch bán lẻ |
| **Success Metric** | ≥ 90% giao dịch tự hoàn thành; thời gian QR < 1 phút; sai STK/số tiền < 1% |
| **Boundary** | AI không tự xác nhận giao dịch — chỉ đọc thông tin, người dùng quyết định bằng giọng nói |

---

## Rule / Workflow / Agent (Phase 6)

### Bước 6.0 — Ma trận độ phù hợp

**Bài toán nằm ở ô: Độ mơ hồ CAO × Độ phức tạp CAO**

| | Độ mơ hồ thấp | Độ mơ hồ cao |
|---|---|---|
| **Độ phức tạp thấp** | Rule / Workflow đơn giản đủ | Workflow có AI hỗ trợ 1 bước |
| **Độ phức tạp cao** | Workflow điều phối nhiều bước | **→ Agent (bài toán của nhóm)** |

**Lý do:**
- Độ mơ hồ cao: QR, tiền mặt, màn hình POS mỗi nơi layout khác nhau — không có đáp án duy nhất, cần AI hiểu ngữ cảnh.
- Độ phức tạp cao: Camera → nhận dạng loại input → OCR → parse data → gọi API → voice output → nhận voice input → xác nhận. Mỗi bước dùng kết quả bước trước.

### Bước 6.1 — So sánh Rule / Workflow / Agent

| Mức | Phương án cụ thể | Khi nào đủ | Rủi ro | Chọn? |
|---|---|---|---|---|
| **Rule** | Hướng dẫn voice cố định: "Nhờ người scan → mở app → nhập STK" | Đủ nếu luôn có người bên cạnh | Không giải được bottleneck phụ thuộc người khác | ❌ |
| **Workflow** | Camera → OCR cố định → voice theo kịch bản → người confirm | Đủ nếu QR/POS luôn có layout chuẩn | VN thực tế quá đa dạng — rule cứng fail liên tục ở edge case | ❌ |
| **Agent** | Camera nhận diện ngữ cảnh → gọi đúng tool → voice confirm → chờ quyết định người dùng | Khi input đa dạng + nhiều API + cần hiểu ngữ cảnh thời gian thực | OCR sai → giao dịch sai; cần fallback rõ | ✅ |

**Mức chọn: Agent**

**Vì sao chọn Agent:**
Ba lý do không thể giải bằng Rule/Workflow đơn giản:
1. Input không đồng nhất (QR / tiền / POS) — Agent cần nhận diện loại input trước rồi mới gọi đúng tool.
2. Ngữ cảnh thay đổi theo từng giao dịch — không thể hardcode rule cho người nhận và số tiền khác nhau.
3. Cần phối hợp 5+ bước phụ thuộc nhau — camera, OCR, banking API, voice output, voice input.

**Vì sao không dừng ở Workflow:**
Workflow cố định giả định layout chuẩn. Thực tế VN (QR viết tay, hóa đơn chợ, màn hình POS cũ) sẽ fail liên tục ở edge case, mất tin tưởng người dùng — nhóm đối tượng vốn đã dễ tổn thương.

### Bước 6.2 — Problem Statement v1

| Field | Nội dung |
|---|---|
| **Actor** | Người khiếm thị sống độc lập tại đô thị VN, độ tuổi 18-55, đang dùng smartphone và quen với voice interface |
| **Workflow** | Thanh toán hằng ngày tại điểm bán lẻ: QR (VietQR), tiền mặt VND, thẻ credit/debit tại POS |
| **Bottleneck** | Không thể verify thông tin giao dịch độc lập trước khi xác nhận — phụ thuộc người thứ ba hoặc chấp nhận rủi ro giao dịch sai |
| **Impact** | 933K+ người khiếm thị tại VN bị loại khỏi hệ sinh thái QR payment chiếm >50% giao dịch bán lẻ. Không có giải pháp nào tại VN hiện tại |
| **Success Metric** | ≥ 90% giao dịch QR hoàn thành độc lập; thời gian/giao dịch QR < 1 phút; sai STK/số tiền < 1%; user rating tin tưởng kết quả ≥ 4/5 |
| **Boundary** | AI không tự xác nhận giao dịch. Chỉ đọc thông tin, người dùng ra lệnh voice "Xác nhận" / "Huỷ". Mọi lỗi nhận dạng → thông báo + hướng dẫn thủ công, không im lặng tiếp tục |
| **AI intervention point** | (1) Nhận diện loại input (QR/tiền mặt/POS), (2) OCR + parse thông tin, (3) Voice output confirm, (4) Nhận voice command xác nhận/huỷ, (5) Gọi banking API tạo lệnh |
| **Mức chọn** | **Agent** |
| **Rủi ro & người kiểm tra** | OCR sai → sai STK: bắt buộc voice confirm trước mọi GD, không auto-execute. Tin tưởng thái quá: UX yêu cầu người dùng repeat số tiền trước khi xác nhận. Owner: team dev + partner ngân hàng kiểm tra log định kỳ |

### Bước 6.3 — Final Decision

| Câu hỏi | Yes / Not Yet / No | Ghi chú |
|---|---|---|
| Actor và workflow đã rõ chưa? | Yes | Thu hẹp về người khiếm thị đô thị, sống độc lập |
| Baseline và success metric đã đo được chưa? | Yes | Thời gian/giao dịch, tỷ lệ tự hoàn thành, tỷ lệ sai |
| Có data/input đủ dùng chưa? | Not Yet | Cần dataset QR + tiền VN + POS để train/test OCR tiếng Việt |
| Nếu AI sai, hậu quả có chấp nhận được không? | Yes | Có fallback: voice confirm bắt buộc, thông báo lỗi rõ, không auto-execute |
| Có người review/owner vận hành không? | Not Yet | Cần xác định partner ngân hàng và team vận hành |
| Có cách non-AI đơn giản hơn không? | No | Rule/template không giải được độ đa dạng của VN context |

**Decision: Go — với điều kiện**

**Lý do:**
Pain thật (2M người, không có giải pháp VN), AI cần thiết ở những bước không thể giải bằng rule, khoảng trống thị trường rõ ràng. Tuy nhiên cần validate OCR tiếng Việt và xác định partner banking trước khi build full product.

**Pilot nhỏ nhất:**
Dùng điện thoại (không cần kính thật) + camera + app test. Chỉ làm một tính năng: đọc QR VietQR → voice output tên người nhận + số tiền. Test với 5-10 người khiếm thị trong 1 tuần. Đo: tỷ lệ đọc đúng, thời gian, mức độ tin tưởng.

**Cần validate thêm trước khi build full:**
- OCR tiếng Việt trên QR và hóa đơn in nhiệt đạt độ chính xác bao nhiêu trong điều kiện thực tế (ánh sáng kém, QR cũ)?
- Người khiếm thị có tin tưởng voice output đủ để xác nhận giao dịch không?
- Ngân hàng nào sẵn sàng mở API sandbox cho pilot?