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

```
┌──────────────────────────────────────────────────────────┐
│ PROBLEM CARD #1 — Rủi ro tài chính                      │
│                                                          │
│ Problem 1 câu:                                           │
│ Tùng không thể tự xác nhận tên người nhận và số tiền     │
│ trước khi bấm gửi, khiến mỗi giao dịch online trở thành │
│ rủi ro mất tiền và buộc phải phụ thuộc người khác.       │
│                                                          │
│ Ai đang đau? Tùng — sinh viên khiếm thị; bạn cùng phòng │
│ bị nhờ kiểm tra hộ định kỳ mỗi lần giao dịch.           │
│                                                          │
│ Workflow hiện tại:                                       │
│ 1. Mở app → 2. Nhập SĐT + số tiền →                     │
│ 3. Màn hình xác nhận hiện ra (không có TTS) →            │
│ 4. Nhờ người đọc lại → 5. Xác nhận & gửi                │
│                                                          │
│ Bước nghẽn nhất: Bước 3 — không có audio confirm step,  │
│ người khiếm thị không tự kiểm tra được tên người nhận.   │
│                                                          │
│ Đo thành công bằng gì?                                   │
│ Giảm thời gian/giao dịch; giảm tỷ lệ chuyển nhầm tiền;  │
│ tăng % giao dịch hoàn thành không cần nhờ người khác.   │
│                                                          │
│ Quick gut: □ No AI  □ Rule  ■ Workflow  □ Agent          │
└──────────────────────────────────────────────────────────┘
```

**Non-AI alternative:**
App ngân hàng/MoMo tích hợp TTS đọc to tên người nhận, số tài khoản và số tiền tại màn hình xác nhận. Thêm bước read-back bắt buộc trước khi gửi. Cho phép lưu danh sách người nhận tin cậy kèm nhãn âm thanh. (Khả thi về kỹ thuật nhưng phụ thuộc vào quyết định của từng ngân hàng — không có chuẩn bắt buộc tại VN hiện tại.)

**AI hypothesis:**
Kính AI nghe màn hình xác nhận và đọc to tên người nhận, số tài khoản và số tiền ngay trước khi Tùng bấm gửi — loại bỏ hoàn toàn bước nhờ người khác kiểm tra, áp dụng được trên mọi app ngân hàng mà không cần ngân hàng thay đổi gì.

```
┌──────────────────────────────────────────────────────────┐
│ PROBLEM CARD #2 — Phụ thuộc người khác                  │
│                                                          │
│ Problem 1 câu:                                           │
│ Tùng không thể tự hoàn thành một lần mua sắm tại siêu   │
│ thị vì không đọc được màn hình POS — mỗi chuyến đi đều  │
│ kéo theo ít nhất một người bạn không có nhu cầu.         │
│                                                          │
│ Ai đang đau? Tùng — sinh viên khiếm thị; bạn cùng nhóm  │
│ đi siêu thị hộ 1-2 lần/tuần dù không có nhu cầu.        │
│                                                          │
│ Workflow hiện tại:                                       │
│ 1. Nhắn rủ bạn → 2. Chờ bạn rảnh (0–2 ngày) →          │
│ 3. Đi cùng → 4. Bạn đọc POS & xác nhận số tiền →        │
│ 5. Bạn nhận biên lai → 6. Tùng không tự xác minh        │
│                                                          │
│ Bước nghẽn nhất: Bước 4 — không đọc được màn hình POS,  │
│ buộc phải có người đứng cạnh mỗi lần thanh toán.         │
│                                                          │
│ Đo thành công bằng gì?                                   │
│ Tăng tỷ lệ mua sắm độc lập; giảm thời gian chờ bạn;    │
│ tăng số địa điểm Tùng có thể tự đến một mình.           │
│                                                          │
│ Quick gut: □ No AI  □ Rule  □ Workflow  ■ Agent          │
└──────────────────────────────────────────────────────────┘
```

**Non-AI alternative:**
Siêu thị trang bị màn hình POS có TTS tại quầy thanh toán. Cung cấp nhân viên hỗ trợ accessibility theo yêu cầu. Thẻ thành viên với hồ sơ accessibility tự động kích hoạt chế độ hỗ trợ khi quẹt thẻ. (Đòi hỏi đầu tư hạ tầng và cam kết từ phía siêu thị — chưa phổ biến tại VN.)

**AI hypothesis:**
Kính AI nhìn vào màn hình POS và đọc to số tiền cần thanh toán trước khi Tùng chạm thẻ — cho phép Tùng tự xác nhận độc lập tại bất kỳ siêu thị nào mà không cần người đứng cạnh hay siêu thị phải thay đổi hạ tầng.

```
┌──────────────────────────────────────────────────────────┐
│ PROBLEM CARD #3 — Khẩn cấp                              │
│                                                          │
│ Problem 1 câu:                                           │
│ Khi bị ngã xe cần xe ôm đưa đến bệnh viện, Tùng không   │
│ nhìn thấy mã QR của tài xế và không tự chuyển khoản      │
│ được trong lúc hoảng loạn — buộc phụ thuộc người lạ.    │
│                                                          │
│ Ai đang đau? Tùng — người khiếm thị trong tình huống     │
│ khẩn cấp; tài xế và người xung quanh bị kéo vào hỗ trợ. │
│                                                          │
│ Workflow hiện tại:                                       │
│ 1. Tùng bị ngã → 2. Gọi xe ôm đến bệnh viện →           │
│ 3. Tài xế đưa QR thanh toán →                           │
│ 4. Tùng không định vị được QR, không tự quét →           │
│ 5. Nhờ người lạ quét/chuyển khoản hộ →                  │
│ 6. Giao dịch phụ thuộc hoàn toàn vào người lạ            │
│                                                          │
│ Bước nghẽn nhất: Bước 4 — không thể định vị và quét QR  │
│ trong tình huống căng thẳng cao độ, không có người quen. │
│                                                          │
│ Đo thành công bằng gì?                                   │
│ Tùng tự hoàn thành giao dịch khẩn cấp không cần nhờ     │
│ người lạ; giảm thời gian thanh toán trong tình huống     │
│ stress so với hiện tại.                                  │
│                                                          │
│ Quick gut: □ No AI  □ Rule  □ Workflow  ■ Agent          │
└──────────────────────────────────────────────────────────┘
```

**Non-AI alternative:**
Ứng dụng xe ôm (Grab, Be) tích hợp luồng thanh toán hỗ trợ accessibility với hướng dẫn bằng giọng nói. Tùng cài sẵn shortcut thanh toán nhanh cho các giao dịch khẩn cấp. Liên hệ khẩn cấp có thể hỗ trợ từ xa qua chia sẻ màn hình. (Phụ thuộc vào từng ứng dụng triển khai — không khả dụng trong mọi tình huống.)

**AI hypothesis:**
Kính AI tự quét môi trường xung quanh, định vị mã QR của tài xế, đọc to thông tin người nhận và hướng dẫn Tùng từng bước hoàn thành giao dịch bằng giọng nói — hoạt động độc lập kể cả khi Tùng hoảng loạn, không cần nhờ bất kỳ người lạ nào.
