# Prototype Feedback Note — Tạ Thị Thu Huyền

## Thông tin phiên

- **Người facilitate:** Tạ Thị Thu Huyền
- **Tester/context:** Phạm Hải Yến — học viên đang xem slide **Data Observability** trên VLearn, gặp thuật ngữ **Data Pipeline** chưa hiểu trong khi bài giảng vẫn tiếp tục.
- **Thời gian:** 19/08/2026
- **Các prototype được so sánh:** [Option A — Hỏi giảng viên theo ngữ cảnh](prototypes/Option%20A.html), [Option B — Sơ đồ kiến thức](prototypes/Option%20B.html) và [Option C — Khái niệm nền và chẩn đoán nhanh](prototypes/Option%20C.html).
- **Task được giao:** Với cùng một tình huống và thuật ngữ **Data Pipeline**, thử từng option để tìm phần hỗ trợ phù hợp, xác định chỗ mình còn vướng và quay lại slide mà không mở Chat/Google.
- **Thứ tự test:** A → B → C.

## Observation theo từng option

| Nội dung | Option A — Hỏi giảng viên | Option B — Sơ đồ kiến thức | Option C — Chẩn đoán nhanh |
|---|---|---|---|
| **First action** | Tester mở bảng **Hỏi**, đọc lướt các câu hỏi đã có rồi nhập: “Data Pipeline khác ETL ở điểm nào?”. | Tester mở **Sơ đồ kiến thức**, chọn node **Data Observability** trước vì node này nổi bật nhất, sau đó mới tìm nhánh **Data Pipeline**. | Tester bấm trực tiếp vào từ **Data Pipeline** được highlight trên slide để xem giải thích ngắn. Sau khi đọc vẫn chưa chắc về Schema, tester chọn **“Vẫn chưa hiểu!?”**. |
| **Chỗ dừng, do dự hoặc hiểu sai** | Sau khi gửi câu hỏi, tester dừng lại ở trạng thái **“Chưa trả lời”** và không biết giảng viên sẽ phản hồi trong bao lâu. Tester cũng sửa câu hỏi một lần vì sợ câu hỏi ban đầu quá chung. | Tester mở liên tiếp ba nhánh **Data Observability → Data Quality → Data Pipeline**. Sơ đồ trở nên dày, khiến tester mất vài giây để xác định node nào liên quan trực tiếp tới thuật ngữ đang xem. | Tester do dự ngắn ở nút **“Khái niệm nền”** vì tưởng đây chỉ là phần cài đặt. Trong quiz, tester đọc kỹ câu đầu nhưng lướt phần mô tả dưới đáp án ở hai câu sau vì muốn quay lại bài nhanh. |
| **Evidence được đọc hay bỏ qua** | Tester đọc trạng thái câu hỏi và một câu hỏi tương tự, nhưng bỏ qua metadata về slide vì đã biết mình đang ở slide nào. | Tester đọc mô tả của node **Data Pipeline** và mối liên hệ với ETL/ELT, nhưng bỏ qua tài liệu tham khảo và hai nhánh phụ. | Tester đọc định nghĩa ngắn, phần **“Liên hệ với slide”** và kết quả Strong/Weak. Tester nhận ra nhãn **“Giảng viên đã duyệt”**, nhưng bỏ qua danh sách **Kiến thức cần có** và link **“Xem thêm”**. |
| **Breakdown chính** | Câu trả lời không xuất hiện ngay nên Option A chưa giải quyết được nhu cầu hỗ trợ trong lúc bài giảng vẫn tiếp tục. | Cấu trúc tổng quan hữu ích nhưng số node mở cùng lúc làm tăng tải nhận thức và thời gian tìm đúng nội dung. | Phần giải thích cho khái niệm Weak còn dài; panel quiz che một phần slide và ba câu hỏi vẫn có thể làm người học lỡ thêm bài. |
| **Cách sửa hoặc lấy lại control** | Tester đóng bảng hỏi sau khi thấy câu hỏi đã được ghi nhận và quay lại slide, nhưng vẫn chưa có câu trả lời để tiếp tục hiểu bài. | Tester thu gọn hai nhánh không liên quan, quay lại node **Data Pipeline**, đọc mô tả rồi đóng sơ đồ. | Tester đóng popup bằng nút ×, hoàn thành quiz, xem kết quả thuật ngữ ở trạng thái Weak, rồi bấm **“Tiếp tục học”** để trở lại slide. Đường quay lại được nhận ra ngay. |
| **Cảm nhận sau khi hoàn thành** | Có cảm giác an tâm vì câu hỏi được chuyển tới người thật, nhưng không phù hợp khi cần câu trả lời ngay. | Hiểu bức tranh tổng thể tốt hơn, nhưng phải tự xác định đường đi trong bản đồ. | Nắm được định nghĩa ngay tại chỗ và biết cụ thể mình đang yếu ở thuật ngữ đó, nên có thể quyết định xem giải thích hay quay lại bài. |

## Feedback sau khi so sánh

### Option được chọn: C

Tester chọn **Option C — Khái niệm nền và chẩn đoán nhanh**.

**Lý do chọn:**

- Có thể bắt đầu ngay từ thuật ngữ đang nhìn thấy trên slide, không cần tự soạn câu hỏi hoặc tìm một nhánh trên sơ đồ.
- Nhận được câu trả lời tức thì, phù hợp với bối cảnh bài giảng vẫn tiếp tục.
- Kết quả Strong/Weak giúp tester gọi tên phần kiến thức còn thiếu thay vì chỉ nhận thêm thông tin chung.
- Nút đóng, **“Quay lại kết quả”** và **“Tiếp tục học”** cho tester cảm giác chủ động và có đường thoát rõ ràng.

**Feedback tóm tắt của tester:** Option C hỗ trợ đúng thời điểm và ít làm mất ngữ cảnh nhất. Tester muốn lớp thông tin đầu tiên chỉ có định nghĩa ngắn và liên hệ với slide; quiz nên được giữ là bước tùy chọn khi phần giải thích nhanh vẫn chưa đủ.

### Trade-off được tester chấp nhận

Tester chấp nhận việc giải thích AI có thể chưa chính xác hoàn toàn để đổi lấy phản hồi nhanh, với điều kiện nội dung phải ghi rõ **“AI giải thích tạm thời”** hoặc **“Giảng viên đã duyệt”**. Tester không muốn quiz tự động bật vì điều đó có thể gây gián đoạn; quyền mở, bỏ qua và đóng hỗ trợ phải thuộc về học viên.

### Evidence chống lại kỳ vọng ban đầu

- Tester không bắt đầu bằng **“Vẫn chưa hiểu!?”** mà ưu tiên bấm thuật ngữ trước. Điều này cho thấy quiz không nên là hành động chính ở mọi tình huống.
- Hỗ trợ ngay trên slide vẫn có thể gây mất tập trung nếu popup hoặc giải thích che quá nhiều nội dung.
- Nhãn AI tạm thời làm tester thận trọng hơn, nên tốc độ không thể thay thế hoàn toàn độ tin cậy.
- Bản đồ của Option B vẫn tốt hơn C khi mục tiêu là hiểu bức tranh tổng thể, không phải xử lý nhanh một thuật ngữ cụ thể.

## Tách bốn lớp

### OBSERVED

- Tester thử cả A, B và C với cùng thuật ngữ **Data Pipeline**.
- A yêu cầu tester tự diễn đạt câu hỏi và chờ phản hồi; B yêu cầu mở/thu gọn nhiều node; C bắt đầu trực tiếp từ thuật ngữ trên slide.
- Tester đọc định nghĩa, liên hệ với slide và kết quả Strong/Weak trong C, nhưng bỏ qua phần tài liệu sâu hơn.
- Tester tìm thấy đường quay lại bài ở cả ba option; riêng A chưa cung cấp câu trả lời tại thời điểm tester quay lại.
- Sau khi so sánh, tester chọn **Option C**.

### INTERPRETED

Trong bối cảnh bài giảng vẫn tiếp tục, tester ưu tiên hỗ trợ tức thì, gắn trực tiếp với từ đang xem và có thể đóng nhanh. Chẩn đoán Strong/Weak tạo thêm giá trị khi nó chỉ ra phần nền cụ thể còn thiếu, nhưng quiz chỉ nên xuất hiện theo yêu cầu thay vì trở thành bước bắt buộc.

### DECIDED — NEXT CHANGE

Nhóm chọn **Option C** để phát triển tiếp và sẽ:

1. Giữ thao tác bấm thuật ngữ là lối vào chính.
2. Rút lớp thông tin đầu tiên còn **định nghĩa ngắn + liên hệ với slide + trạng thái đã duyệt**.
3. Giữ **“Vẫn chưa hiểu!?”** như hành động phụ, không tự mở quiz.
4. Rút quiz còn tối đa ba câu và luôn hiển thị đường đóng hoặc **“Tiếp tục học”**.
5. Đưa kiến thức cần có, tài liệu và giải thích sâu vào lớp **“Xem thêm”**.

### STILL UNPROVEN

- Chưa đo được thời gian hoàn thành và lượng nội dung bài giảng bị bỏ lỡ ở từng option.
- Chưa kiểm chứng liệu ba câu hỏi có đủ ngắn cho bối cảnh lớp học trực tiếp.
- Thứ tự test A → B → C có thể tạo hiệu ứng học trước hoặc thiên lệch gần nhất; phiên sau cần đổi thứ tự giữa các tester.
