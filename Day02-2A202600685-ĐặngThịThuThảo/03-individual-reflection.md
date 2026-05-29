# 03 — Individual Reflection

## Tôi đã tham gia vào phần nào?

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng |
|---|---|---|
| Scan cá nhân | Tự scan 5+ problems từ trải nghiệm thật, bao gồm các bài liên quan đến dev workflow và người khiếm thị | Có đủ candidates đa dạng để mang vào nhóm |
| Pitch Problem Card | Pitch top 3 cards, trong đó nhấn mạnh bài hỗ trợ người khiếm thị trong thanh toán | Nhóm chọn bài này làm candidate deep-dive |
| Challenge bài của bạn khác | Đặt câu hỏi về actor và metric ở một số card | Giúp một số card làm rõ bottleneck hơn |
| Gom trùng / cluster | Tham gia phân nhóm candidates theo chủ đề | Nhóm nhìn thấy pattern rõ hơn trước khi vote |
| Chọn candidate problem | Tham gia thảo luận và đồng thuận chọn bài kính hỗ trợ thanh toán cho người khiếm thị | — |
| Validation / research | Tìm Envision Glasses, Seeing AI, Be My Eyes + Ray-Ban Meta, VietQR API; đọc spec và so sánh khoảng trống so với context VN | Nhóm xác định được gap rõ ràng: không có giải pháp nào hỗ trợ VietQR + VND + tiếng Việt; bổ sung cột "Bài học cho nhóm" vào bảng research |
| Workflow nhóm | Góp ý phân nhánh current workflow thành 3 nhánh (QR / tiền mặt / thẻ); đề xuất thêm cột thời gian thực tế vào bảng before/after | Workflow rõ hơn ở điểm "7-10 phút/giao dịch" — con số cụ thể này giúp nhóm có baseline đo được |
| Problem Statement | Tham gia review PS v0 → v1; đề xuất thu hẹp actor từ "người khiếm thị VN" về "người khiếm thị đô thị, sống độc lập, 18-55 tuổi" | PS v1 cụ thể hơn, boundary rõ hơn, metric có thể đo ngay ở pilot |
| Rule / Workflow / Agent | Tham gia lập luận vì sao không dừng ở Workflow; đưa ra ví dụ edge case thực tế (QR viết tay, màn hình POS cũ) để minh hoạ giới hạn của rule cứng | Nhóm đồng thuận chọn Agent với lập luận có dẫn chứng thực tế, không chỉ lý thuyết |
| Decision | Tham gia điền bảng Yes/Not Yet/No và đề xuất pilot scope nhỏ nhất | Decision là "Go với điều kiện" thay vì Go hoàn toàn — pilot nhỏ hơn, rủi ro thấp hơn |

---

## Bảng dùng AI trong lab

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai/hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| Scan | Gợi ý thêm candidates sau khi tự scan | Mở ra một số góc nhìn mới về pain của người khiếm thị | Một số gợi ý quá rộng, thiếu actor cụ thể | Bỏ ý không có dấu hiệu thật, giữ lại ý gắn với trải nghiệm quan sát được |
| Problem Card | Phản biện card trước khi pitch | Chỉ ra metric còn mơ hồ | Đôi khi khen trước rồi mới chỉ lỗi, không đủ sharp | Tự đặt thêm câu hỏi "nếu AI sai ở bước này thì sao" |
| Workflow | Hỏi AI gợi ý các bước trong current workflow và cách vẽ future state | Gợi ý phân nhánh theo loại thanh toán (QR / tiền mặt / thẻ) — cấu trúc rõ hơn | AI vẽ future state quá lạc quan, bỏ qua edge case tiếng Việt và ánh sáng kém | Tự thêm bước fallback và ghi rõ điều kiện thất bại vào workflow |
| Research | Dùng AI tổng hợp nhanh các tool accessibility đã có trên thị trường | Liệt kê được Envision, Seeing AI, Be My Eyes nhanh | Một số link AI đưa ra không kiểm tra được; số liệu giá Envision cần verify lại từ trang chính thức | Vào từng trang verify giá, tính năng; bỏ tool nào không có link gốc |
| Problem Statement | Dùng prompt phản biện PS v0 theo hướng "chỉ ra lỗ hổng, không viết lại thay" | Phát hiện actor còn rộng và metric "tỷ lệ tự hoàn thành" chưa có baseline | AI gợi ý thêm nhiều field phụ không cần thiết, làm PS dài ra | Giữ đúng 6 field cơ bản + 3 field AI-specific; bỏ phần AI thêm vào không có trong template |
| Rule / Workflow / Agent | Hỏi AI so sánh khi nào nên dùng Agent thay Workflow | Giải thích rõ điều kiện "AI cần tự quyết định bước tiếp theo" | AI thiên về đề xuất Agent quá sớm mà không phân tích rõ rủi ro | Tự bổ sung cột "Rủi ro" và ví dụ VN cụ thể trước khi nhóm chốt |
| Decision | Hỏi AI review bảng Yes/Not Yet/No để xem có bỏ sót câu hỏi nào không | Nhắc thêm câu hỏi về owner vận hành — nhóm đã bỏ qua | AI đề xuất thêm nhiều điều kiện không thực tế cho quy mô lab | Giữ đúng 6 câu hỏi trong template, không mở rộng |

---

## Reflection

Buổi lab hôm nay phần khó nhất với tôi là giai đoạn hội tụ — khi nhóm có khoảng 12 candidates mà mỗi người đều thấy bài của mình đáng làm. Tôi đóng vai trò pitch khá nhiều và cũng cố dẫn dắt thảo luận, nhưng nhận ra rằng dẫn dắt hội tụ khác với dẫn dắt brainstorm: không thể chỉ liệt kê thêm, phải biết cắt bỏ và giải thích rõ vì sao bỏ.

Khi nhóm đang loay hoay giữa nhiều candidates, điều giúp chúng tôi chốt được là quay về câu hỏi cụ thể: *ai đang đau, đau bằng chứng nào, workflow trước/sau có vẽ được không*. Bài kính hỗ trợ thanh toán cho người khiếm thị thắng vì nó có pain quan sát được rõ nhất và thị trường bị bỏ ngỏ theo đúng nghĩa — không phải vì nghe "ngầu" hơn.

Một điều tôi học được từ nghe top 3 của bạn khác là nhiều pain thật sự nằm ở những workflow rất nhỏ và lặp lại, không phải ở những bài toán lớn. Một số card của nhóm ban đầu quá rộng (ví dụ "trợ lý AI toàn diện cho người khiếm thị") và chính việc bóc tách thành sub-problems mới giúp nhìn rõ bước nào thật sự nghẽn.

Nếu làm lại, tôi sẽ challenge nhóm sớm hơn ở phần metric — nhiều candidate nghe hay nhưng khi hỏi "đo thành công bằng gì" thì loay hoay. Đó thường là dấu hiệu problem chưa đủ cụ thể, và nên là câu hỏi lọc ngay từ bước shortlist thay vì để đến Phase 5 mới phát hiện.

---

## Bài học của mình

- Khởi đầu bằng một câu hỏi rõ: ai đang đau, đau bằng chứng nào, và bước nghẽn hiện tại là gì.
- Đừng để bảng ý tưởng quá rộng; lọc sớm bằng actor và workflow giúp nhóm thoát khỏi những problem statement quá chung.
- Khi dùng AI, phải xác định rõ mục đích: tôi dùng AI để mở rộng ý, không để AI quyết định câu chuyện chính.
- Metric là nơi dễ lộ problem chưa đủ cụ thể; nếu chưa hỏi được metric trước Pilot thì nên reconsider problem sớm.

---

## Tự kiểm cuối bài

- [x] Cá nhân có 5+ problems và top 3 Problem Cards
- [x] Tôi đã pitch rõ và challenge nhóm đúng trọng tâm
- [x] Nhóm có nhật ký hội tụ từ candidates về 1 bài
- [x] Nhóm có workflow trước/sau
- [x] Nhóm có Problem Statement v0/v1 với metric và boundary rõ
- [x] Nhóm có so sánh No AI / Rule / Workflow / Agent
- [x] Nhóm có Go / Not Yet / No-Go và lý do rõ
- [x] Reflection cá nhân có nói rõ vai trò trong nhóm, cách dùng AI, điều học được và nếu làm lại sẽ đổi gì
- [x] Tôi tự giải thích được mạch problem → workflow → metric → boundary → độ phù hợp với AI