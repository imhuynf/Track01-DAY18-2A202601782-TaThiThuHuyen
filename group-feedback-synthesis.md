# Group Feedback Synthesis — sau khi có ba bản

## Nguồn feedback được tổng hợp

| Feedback | Facilitator | Tester/context | Phạm vi so sánh |
|---|---|---|---|
| **Feedback 1** | Đỗ Thu Liễu, Nguyễn Trí Trung | Phạm Tiến Đại — cần hiểu **Data Pipeline** khi bài giảng vẫn tiếp tục | A/B/C với cùng task; chú trọng luồng hỏi giảng viên |
| **Feedback 2** | Phạm Tiến Đại | Tạ Thị Thu Huyền — cần tìm đúng vùng kiến thức liên quan tới **Data Pipeline** | A/B/C với cùng task; chú trọng sơ đồ kiến thức |
| **Feedback 3** | Tạ Thị Thu Huyền | Phạm Hải Yến — cần giải thích thuật ngữ và xác định phần nền còn yếu ngay trên slide | A/B/C với cùng task; chú trọng giải thích và quiz nhanh |


## Bảng tổng hợp hành vi và feedback

| Nội dung | Feedback 1 | Feedback 2 | Feedback 3 | Pattern hoặc khác biệt |
|---|---|---|---|---|
| **First action** | Tester mở **Hỏi**, tìm câu tương tự rồi tự nhập câu hỏi về sự khác nhau giữa Data Pipeline và ETL. | Tester mở **Sơ đồ kiến thức**, chọn node Data Observability rồi lần theo nhánh tới Data Pipeline. | Tester bấm trực tiếp từ **Data Pipeline** được highlight; chỉ mở **“Vẫn chưa hiểu!?”** sau khi phần giải thích nhanh chưa đủ. | A bắt đầu bằng việc tạo câu hỏi, B bắt đầu bằng điều hướng, còn C bắt đầu ngay từ đối tượng đang gây vướng trên slide. |
| **Breakdown chính** | Tester không biết phải chờ phản hồi bao lâu; trạng thái **“Chưa trả lời”** chưa đủ nổi bật để tạo cảm giác tiến triển. | Tester mở nhiều node, phải quay lại hai lần và mất dấu nhánh chính khi sơ đồ trở nên dày. | Tester hiểu nhầm **“Khái niệm nền”** là phần cài đặt; quiz và giải thích cho khái niệm Weak còn dài, che một phần slide. | Cả ba đều có nguy cơ làm người học lỡ bài, nhưng nguyên nhân khác nhau: chờ đợi ở A, tìm kiếm ở B và lượng nội dung ở C. |
| **Evidence được dùng** | Tester đọc câu hỏi tương tự và trạng thái tiếp nhận, nhưng chưa nhận được câu trả lời tại thời điểm cần. | Tester dùng mô tả node và quan hệ ETL/ELT để hiểu bức tranh tổng thể; bỏ qua tài liệu tham khảo. | Tester đọc định nghĩa, liên hệ với slide, nhãn đã duyệt và kết quả Strong/Weak; bỏ qua danh sách kiến thức sâu hơn. | Tester đều ưu tiên evidence ngắn, trực tiếp; tài liệu sâu hoặc metadata bị bỏ qua khi bài giảng vẫn chạy. |
| **Cách lấy lại control** | Đóng bảng hỏi và trở về slide sau khi câu hỏi được ghi nhận, dù vấn đề chưa được giải quyết ngay. | Thu gọn hai nhánh không liên quan, quay lại node Data Pipeline rồi đóng sơ đồ. | Đóng popup, xem kết quả quiz và bấm **“Tiếp tục học”**; tester nhận ra đường quay lại ngay. | C có đường recovery rõ và hoàn tất vòng hỗ trợ ngay trong phiên; A cho phép quay lại nhưng phải chờ, B cần thêm thao tác thu gọn. |
| **Option được chọn** | **C**, vì có phản hồi ngay và không phụ thuộc vào thời gian của giảng viên. | **B**, vì tester ưu tiên bức tranh tổng thể và muốn tự khám phá quan hệ giữa các khái niệm. | **C**, vì bắt đầu ngay từ thuật ngữ, chỉ ra Schema đang Weak và có thể quay lại bài nhanh. | C được 2/3 tester ưu tiên; B vẫn có lợi thế cho nhu cầu học tổng quan. Không tester nào chọn A cho tình huống cần hỗ trợ tức thì. |
| **Trade-off** | C nhanh hơn A nhưng tester chỉ chấp nhận nếu nguồn AI/giảng viên duyệt được ghi rõ. | B cho nhiều context hơn C nhưng mất thời gian điều hướng; C hiệu quả hơn cho một vướng mắc cụ thể. | C cá nhân hóa hơn, nhưng quiz có thể gây gián đoạn và chẩn đoán sai nếu câu hỏi không tốt. | Lợi ích nổi bật của C là tốc độ và tính cụ thể; rủi ro nổi bật là độ tin cậy của AI và tải nhận thức do quiz/popup. |
| **Điều đi ngược kỳ vọng** | Có câu hỏi tương tự không giúp tester tiếp tục bài nếu chưa có câu trả lời ngay. | Tester thích B hơn C khi muốn hiểu toàn bộ vùng kiến thức, cho thấy C không thay thế mọi kiểu hỗ trợ. | Tester bấm thuật ngữ trước thay vì mở quiz, cho thấy **“Vẫn chưa hiểu!?”** chỉ nên là bước tùy chọn. | Không option nào thắng trong mọi nhu cầu; quyết định phải bám vào context “xử lý nhanh một chỗ vướng khi bài vẫn tiếp tục”. |

## OBSERVED

- A tạo cảm giác có người chịu trách nhiệm trả lời, nhưng thời gian chờ không phù hợp với nhu cầu hỗ trợ tức thì.
- B giúp nhìn thấy bức tranh tổng thể, nhưng hai tester phải dò hoặc thu gọn nhánh trước khi quay lại đúng nội dung cần tìm.
- C cho phép bắt đầu trực tiếp từ thuật ngữ trên slide, trả kết quả ngay và chỉ ra một khái niệm Weak cụ thể.
- Hai trên ba tester chọn C; tester còn lại chọn B vì ưu tiên hiểu tổng quan.
- C vẫn có breakdown: nhãn nút chưa hoàn toàn rõ, popup có thể che slide và quiz ba câu vẫn tạo gián đoạn.

## INTERPRETED

Với tình huống bài giảng đang tiếp tục và học viên chỉ vướng một thuật ngữ cụ thể, **tốc độ nhận hỗ trợ, mức liên quan tới slide và đường quay lại rõ ràng** quan trọng hơn lượng thông tin. Option C phù hợp nhất với ba tiêu chí đó. Tuy nhiên, tester không muốn bị ép làm quiz; họ muốn thử định nghĩa ngắn trước và chỉ chẩn đoán sâu hơn khi vẫn chưa hiểu.

Option B vẫn là reference tốt cho nhu cầu khám phá bức tranh tổng thể. Option A phù hợp với câu hỏi cần phán đoán của giảng viên, nhưng không nên là luồng chính cho nhu cầu refresher tức thì.

## DECIDED — OPTION CUỐI: C

> **Nhóm chọn Option C — Khái niệm nền và chẩn đoán nhanh để phát triển ở iteration tiếp theo.**

### Evidence dẫn tới quyết định

- C được 2/3 tester ưu tiên sau khi dùng cùng context và task.
- C là option duy nhất vừa đưa ra hỗ trợ ngay, vừa giúp xác định khái niệm nền Strong/Weak mà không yêu cầu rời slide.
- Luồng C hoàn tất trong cùng phiên: mở thuật ngữ → đọc giải thích → kiểm tra tùy chọn → xem phần Weak → tiếp tục học.
- C phù hợp trực tiếp nhất với hypothesis problem: học viên không biết chính xác lỗ hổng kiến thức nào và không có thời gian rời bài để tự tìm.

### MỘT NEXT CHANGE NHÓM CHỐT

> **Thiết kế C theo progressive disclosure: mặc định chỉ hiện định nghĩa ngắn, liên hệ với slide và trạng thái kiểm duyệt; quiz “Vẫn chưa hiểu!?” là bước tùy chọn, tối đa ba câu, có nút đóng hoặc “Tiếp tục học” luôn nhìn thấy.**

### Tiêu chí giữ lại khi phát triển C

- Bấm trực tiếp thuật ngữ là hành động chính.
- Popup đầu tiên không che phần trọng tâm của slide.
- Phân biệt rõ nội dung **AI tạm thời** và nội dung **Giảng viên đã duyệt**.
- Kết quả Strong/Weak chỉ dùng để gợi ý, không khẳng định tuyệt đối năng lực học viên.
- Kiến thức sâu hơn và tài liệu tham khảo nằm sau nút **“Xem thêm”**.
- Học viên luôn có quyền bỏ qua quiz, đóng panel hoặc quay lại bài.

## STILL UNPROVEN SAU BA FEEDBACK

- Chưa biết độ dài tối ưu của định nghĩa, popup và quiz trong lớp học thực tế.
- Chưa kiểm chứng cách người học hiểu và sử dụng nhãn **AI tạm thời/Giảng viên đã duyệt**.
- Chưa đánh giá tải công việc của giảng viên khi kiểm chứng, chỉnh sửa và phát hành nội dung.
- Thứ tự test có thể ảnh hưởng lựa chọn cuối cùng; cần xáo trộn thứ tự A/B/C ở vòng test tiếp theo.
