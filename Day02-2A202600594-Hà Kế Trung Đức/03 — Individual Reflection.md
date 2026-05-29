# 03 — Individual Reflection 

| Hoạt động | Mô tả thực tế | Kết quả / Insight |
|-----------|---------------|-------------------|
| **Problem Scan** | Thu thập 12 vấn đề liên quan tới thanh toán cho người khiếm thị (OCR, UI, bảo mật). | Đã có đủ data để nhóm chọn **Blind‑Payment Assistant**. |
| **Pitch** | Trình bày vấn đề “AI hỗ trợ thanh toán cho người khiếm thị” tại buổi brainstorming. | Nhóm đồng ý đây là *high‑impact, low‑scope* vì đã có data mẫu QR. |
| **Workflow design** | Vẽ sơ đồ current / future bằng Mermaid → đưa cho nhóm. | Giúp mọi người nhận ra ranh giới “human‑in‑the‑loop”. |
| **Research** | Tìm kiếm các SDK OCR (ABBYY, Google ML Kit) + API ngân hàng sandbox. | Xác định công nghệ khả thi, tránh “tự build OCR từ đầu”. |
| **Rule / Workflow / Agent decision** | Đánh giá 3 mức: Rule (template), Workflow (script + AI), Agent (full autonomous). | Chọn **Workflow** vì bước “read‑back” là duy nhất cần AI. |
| **Risk analysis** | Liệt kê rủi ro: hallucination, dữ liệu nhạy cảm, lỗi OCR. | Đưa ra biện pháp: xử lý cục bộ, confirm bằng giọng. |
| **Pilot planning** | Viết roadmap 4 tuần, định nghĩa KPI chi tiết. | Khi trình bày, nhận được phản hồi: cần thêm “fallback manual entry”. |
| **Reflection on AI usage** | - **Tốt**: AI gợi ý cấu trúc workflow, đưa ra danh sách agents. <br> - **Hạn chế**: AI không luôn nhận ra ràng buộc bảo mật, đề xuất “đưa ảnh lên cloud”. <br> - **Cải thiện**: Khi AI đề xuất giải pháp, luôn kiểm tra “data‑privacy” riêng. | Học được cách cân bằng giữa *gen‑AI đề xuất* và *kiểm chứng con người*. |
| **What I’d do differently** | - Thu thập thêm ít nhất 5 mẫu ảnh QR từ người dùng thật trước khi xác định OCR SDK. <br> - Đặt tiêu chuẩn “privacy‑by‑design” trong giai đoạn research để tránh đề xuất giải pháp không phù hợp. | Tăng độ tin cậy của giải pháp, giảm thời gian sửa đổi sau này. |