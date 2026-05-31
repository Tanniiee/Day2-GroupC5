# Individual Problem Scan

Case: **Kính AI hỗ trợ thanh toán độc lập cho người khiếm thị tại Việt Nam **

Nhân vật ví dụ: Tùng, 1 sinh viên đại học, hiện không thể tự chủ trong việc thanh toán trong những trang trải sinh hoạt hàng ngày, luôn cần người hỗ trợ cả trong những giao dịch đơn giản nhất.


| #  | Lăng kính               | Problem quan sát được                                                                                                                                                                         | Ai đang đau?                                                 | Dấu hiệu thật                                                                                                                                    |
| ---- | --------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1  | Lặp lại                 | Tùng đóng tiền trọ mỗi tháng — phải nhờ bạn cùng phòng chuyển khoản hộ vì không tự xác nhận được tên chủ nhà và số tiền trên MoMo                                  | Sinh viên khiếm thị, bạn cùng phòng                      | Lặp lại 12 lần/năm. Bạn cùng phòng của Tùng nói "tháng nào cũng phải nhắc mình làm hộ"                                            |
| 2  | Lặp lại định kỳ      | Mỗi sáng Tùng mua đồ ăn sáng tại quán quen bằng tiền mặt — phải đưa tờ 200k và nhờ người bán thối đúng, không kiểm tra được                                         | Người khiếm thị, người bán hàng                        | ~25 lần/tháng. Tùng chỉ dám mua ở quán quen vì "biết họ không gian lận"Lặp lại mỗi tuần                                             |
| 3  | Rủi ro tài chính       | Tùng nhập số điện thoại để chuyển khoản MoMo cho bạn — bấm nhầm 1 số, chuyển tiền đến người lạ; hoặc bị người bán thối sai tiền mặt mà không phát hiện được tại chỗ | Người khiếm thị chuyển tiền, mua sắm                   | MoMo không đọc to tên người nhận trước khi xác nhận; người mù tránh chợ truyền thống vì rủi ro tiền thối — ghi nhận qua diễn đàn hội người mù |
| 4  | Phụ thuộc người khác | Tùng không thể một mình vào siêu thị — cần người đọc màn hình POS, xác nhận số tiền, nhận biên lai. Mọi chuyến đi mua sắm đều cần "đồng hành"                     | Sinh viên khiếm thị, bạn bè / người thân bị kéo vào | Bạn cùng nhóm của Tùng: "Mỗi tuần mình đi siêu thị cùng Tùng 1-2 lần dù không có nhu cầu"                                         |
| 5  | Phụ thuộc người khác | Tùng muốn tự rút tiền ATM nhưng tất cả ATM ở gần ký túc xá không có Talking ATM — phải nhờ người đi cùng mỗi lần cần tiền mặt                                          | Sinh viên khiếm thị, bạn bè                               | Talking ATM chưa phổ biến tại VN; Napas chưa có chuẩn bắt buộc accessibility cho ATM nội địa                                            |
| 6  | Tốn thời gian           | Tùng mất 10–15 phút mỗi lần thanh toán tại quầy vé xe buýt vì phải giao tiếp qua lại để xác nhận số tiền, chờ nhân viên hỗ trợ                                          | Người khiếm thị, nhân viên bán vé                      | Người dùng thông thường mất <2 phút. Chênh lệch 5–8x tại cùng điểm giao dịch                                                        |
| 7  | Tốn thời gian           | Sau mỗi giao dịch thẻ, Tùng phải gọi điện hotline ngân hàng để nghe số dư xác nhận — vì biên lai in không đọc được và app không có audio balance                      | Người khiếm thị dùng thẻ ngân hàng                     | 5–8 phút/lần gọi. Tùng nói "mình gọi hotline nhiều hơn mọi người khác vì đó là cách duy nhất"                                   |
| 8  | Khẩn cấp                | Tùng bị ngã xe, cần thanh toán tiền xe ôm đưa đến bệnh viện — không nhìn thấy mã QR của tài xế, không tự chuyển khoản được một mình trong tình huống hoảng loạn | Người khiếm thị trong tình huống khẩn cấp              | Tình huống giả định nhưng có cơ sở — người mù phụ thuộc người lạ trong khẩn cấp cao hơn đáng kể                             |
| 9  | Môi trường mới        | Tùng đến quán cà phê lần đầu — không biết máy POS đặt ở đâu, khe thẻ chiều nào, QR dán ở vị trí nào. Mỗi địa điểm mới là một lần mò mẫm từ đầu            | Người khiếm thị, nhân viên thu ngân                     | Tùng chỉ đến những quán "đã quen địa hình" — tự loại bỏ trải nghiệm mới vì chi phí friction quá cao                            |
| 10 | AI có thể tốt hơn    | Tùng không thể tự xác nhận mệnh giá tờ tiền đang cầm trước khi đưa cho người bán — kính AI nhận diện tờ tiền và đọc to "200.000 đồng" ngay khi Tùng cầm lên, loại bỏ rủi ro đưa nhầm mệnh giá | Người khiếm thị thanh toán tiền mặt | Nhận diện mệnh giá tiền là tác vụ computer vision đơn giản — AI có thể làm real-time, không cần kết nối mạng |

## Top 3


| # | Lăng kính               | Problem quan sát được                                                                                                                                                                         | Ai đang đau?                                                 | Dấu hiệu thật                                                                                                        |
| --- | --------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| 1 | Rủi ro tài chính       | Tùng nhập số điện thoại để chuyển khoản MoMo cho bạn — bấm nhầm 1 số, chuyển tiền đến người lạ, mất 10 phút gọi hỗ trợ để hoàn                                      | Người khiếm thị chuyển tiền nhóm                        | MoMo không đọc to tên người nhận trước khi xác nhận — không có audio confirm step                         |
| 2 | Phụ thuộc người khác | Tùng không thể một mình vào siêu thị — cần người đọc màn hình POS, xác nhận số tiền, nhận biên lai. Mọi chuyến đi mua sắm đều cần "đồng hành"                     | Sinh viên khiếm thị, bạn bè / người thân bị kéo vào | Bạn cùng nhóm của Tùng: "Mỗi tuần mình đi siêu thị cùng Tùng 1-2 lần dù không có nhu cầu"             |
| 3 | Khẩn cấp                | Tùng bị ngã xe, cần thanh toán tiền xe ôm đưa đến bệnh viện — không nhìn thấy mã QR của tài xế, không tự chuyển khoản được một mình trong tình huống hoảng loạn | Người khiếm thị trong tình huống khẩn cấp              | Tình huống giả định nhưng có cơ sở — người mù phụ thuộc người lạ trong khẩn cấp cao hơn đáng kể |

# Problem Card #1 — Rủi ro tài chính

**Actor:**
Tùng — sinh viên đại học khiếm thị, thực hiện giao dịch chuyển khoản định kỳ qua MoMo/app ngân hàng.

**Thời điểm / bối cảnh:**
Khi Tùng chuyển khoản qua MoMo/app ngân hàng để đóng tiền trọ, trả tiền nhóm, hoặc thanh toán dịch vụ hằng tháng.

**Problem 1 câu:**
Tùng không thể tự xác nhận tên người nhận và số tiền trước khi bấm gửi, khiến mỗi giao dịch online trở thành rủi ro mất tiền và buộc phải phụ thuộc người khác.

**Current workflow:**

1. Người khiếm thị mở app/ngân hàng điện tử và chọn chức năng chuyển tiền online.
2. Nhập số tài khoản/số điện thoại, số tiền và nội dung chuyển.
3. Hệ thống hiển thị thông tin xác nhận bằng văn bản, nhưng ngân hàng không hỗ trợ Text to Speech để đọc tên người nhận, số tiền, hoặc đơn vị.
4. Người dùng phải tự kiểm tra bằng công cụ hỗ trợ không đầy đủ hoặc nhờ người khác xác nhận.
5. Người dùng xác nhận và gửi lệnh; nếu có nhầm lẫn, tiền bị chuyển sang tài khoản sai.

**Bottleneck:** Bước 3 - Ngân hàng không cung cấp Text to Speech khi xác nhận giao dịch.
Bước xác nhận thông tin cuối cùng chỉ hiển thị văn bản, nên người khiếm thị không thể tự kiểm tra tên người nhận và số tiền; họ phải dừng lại, tìm công cụ hỗ trợ chưa đủ tin cậy hoặc nhờ người khác, làm giao dịch định kỳ trở nên chậm và dễ nhầm.

**Impact:**

* giao dịch online định kỳ trở nên chậm hơn, mất thêm thời gian kiểm tra hoặc chờ người khác giúp
* tăng nguy cơ chuyển nhầm tiền, gây tổn thất tài chính trực tiếp
* khiến người khiếm thị phụ thuộc người khác, mất quyền tự chủ trong quản lý tiền
* giảm sự tự tin khi dùng app ngân hàng và làm họ tránh dùng dịch vụ online hơn

**Success metric:**

- **Thời gian mỗi giao dịch**: giảm thời gian trung bình để người khiếm thị hoàn thành một lần chuyển khoản online.
- **Tỷ lệ lỗi**: giảm tỷ lệ chuyển nhầm tiền hoặc hủy giao dịch do xác nhận sai thông tin.
- **Mức độ hài lòng (CSAT)**: tăng điểm hài lòng của người dùng với luồng chuyển tiền và sự tự tin khi dùng app ngân hàng.
- **Tỷ lệ độc lập**: phần trăm giao dịch hoàn thành mà không cần nhờ người khác hỗ trợ.
- **Tỷ lệ tái sử dụng**: nhiều người khiếm thị chủ động chọn chuyển khoản online thay vì né tránh.

**Non-AI alternative:

- Improve the banking app workflow with built-in accessibility support:
  - add Text-to-Speech for confirmation screens
  - expose recipient name, account/phone, amount, and fee in a clear spoken prompt
- Use a rule-based confirmation step:
  - require the user to confirm the details twice
  - show a simplified “read-back” summary before final submit
- Provide offline support tools:
  - add a dedicated “verify transfer” mode for screen readers
  - allow user to save and reuse trusted beneficiaries with audio labels
- Train staff/processes:
  - educate customer support and product teams to prioritize accessible transfer flow
  - enforce accessibility requirements in bank app updates rather than relying on AI automatio

**Quick gut:**
Workflow.
