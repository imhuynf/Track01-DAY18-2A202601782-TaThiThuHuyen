# Three-Option Design Sheet

## 1. Hypothesis Problem chung

> Khi giảng viên đang dẫn dắt một khái niệm mới trên slide, học viên gặp khó khăn trong việc theo kịp bài giảng vì hai rào cản xảy ra cùng lúc: (1) họ không hiểu một từ khóa hoặc bức tranh tổng thể đằng sau khái niệm đó, nhưng không biết chính xác đó là lỗ hổng kiến thức nền nào để tự tra cứu ngay; và (2) ngay cả khi nhận ra mình đang bị hụt, họ không có thời gian để dừng lại tìm hiểu — vì bài giảng vẫn tiếp tục trôi và họ không muốn ngắt lời hoặc làm chậm cả lớp — dẫn đến việc họ im lặng bỏ qua, tiếp tục nghe trong tình trạng mất gốc, và khoảng hụt kiến thức đó dồn lại qua các phần sau của bài giảng.

Ba option dưới đây cùng giải quyết Hypothesis Problem này, nhưng khác nhau ở cơ chế hỗ trợ và cách phân chia công việc giữa học viên, AI và giảng viên.

## 2. Những thứ phải giữ nguyên

| Thành phần | Quyết định chung cho A/B/C |
|---|---|
| **Target user** | Học viên đang theo dõi bài giảng trên VLearn. Giảng viên là stakeholder phụ, không thay đổi target user chính của phép so sánh. |
| **Situation** | Bài giảng vẫn đang tiếp tục. Trên slide có thuật ngữ **Data Pipeline** nhưng học viên chưa hiểu rõ và không muốn rời VLearn để tra cứu. |
| **Task** | Dùng từng option để tìm phần hỗ trợ phù hợp, hiểu được **Data Pipeline** ở mức đủ để tiếp tục theo dõi slide hiện tại. |
| **Desired outcome** | Học viên có thể nói ngắn gọn Data Pipeline là gì, xác định được phần mình còn vướng và quay lại bài mà không phải mở Chat/Google. |
| **Content/data fixture** | Cùng một đoạn slide: “Data Pipeline là chuỗi các bước thu thập, biến đổi và chuyển dữ liệu từ nguồn đến nơi sử dụng”; cùng các khái niệm liên quan: Data Ingestion, ETL/ELT, Data Quality, Monitoring và Schema. |

> **Quy ước khi test:** Ba prototype hiện có số slide và cách trình bày khác nhau. Tester vẫn phải bắt đầu từ cùng tình huống, thuật ngữ **Data Pipeline**, task và desired outcome nêu trên để việc so sánh có ý nghĩa.

## 3. Những thứ được phép khác

| Thành phần | Option A — Hỏi giảng viên theo ngữ cảnh | Option B — Sơ đồ kiến thức | Option C — Khái niệm nền và chẩn đoán nhanh |
|---|---|---|---|
| **Solution mechanism** | Kênh hỏi–đáp gắn với slide: học viên tự viết câu hỏi; giảng viên xem câu hỏi theo mốc kiến thức, mở đúng slide và đánh dấu đã/chưa giải đáp. | AI chuẩn bị một bản đồ cấu trúc bài học theo chủ đề, slide và các khái niệm liên quan; học viên chọn nhánh mình cần xem. | AI hỗ trợ theo ngữ cảnh ngay trên slide: giải thích thuật ngữ, kiểm tra nhanh kiến thức nền và chỉ ra khái niệm Strong/Weak; tín hiệu Weak được tổng hợp ẩn danh để giảng viên duyệt. |
| **User làm gì?** | Mở bảng hỏi, tự viết và gửi câu hỏi; xem câu hỏi của bạn khác, bấm đồng tình và theo dõi trạng thái trả lời. | Mở sơ đồ, chọn chủ đề/nhánh, thu gọn hoặc mở rộng bản đồ, xem nội dung liên quan rồi quay lại slide. | Nhấn thuật ngữ được highlight hoặc bôi đen thuật ngữ chưa có thẻ; nếu vẫn chưa hiểu thì làm quiz ngắn, xem giải thích và quyết định tiếp tục học. |
| **AI làm gì?** | Không soạn câu hỏi hay câu trả lời. Hệ thống chỉ gắn câu hỏi với slide/mốc kiến thức để giảng viên có ngữ cảnh xử lý. | Từ nội dung bài, AI tổ chức các khái niệm thành bản đồ, gắn phạm vi slide, mô tả, kiến thức liên quan và tài liệu tham khảo. AI không tự quyết định nhánh học viên phải xem. | AI tạo giải thích tạm thời cho từ chưa được duyệt, chấm quiz bằng logic mô phỏng, nối khái niệm Weak với slide và tổng hợp kết quả ẩn danh. AI chỉ đề xuất tag; giảng viên kiểm chứng, chỉnh sửa, duyệt và phát hành. |
| **Trigger** | Học viên nhấn **Hỏi** khi nhận ra mình đang vướng. | Học viên nhấn nút **Sơ đồ tư duy/Sơ đồ kiến thức** và chọn một node. | Học viên nhấn một từ được highlight, bôi đen từ chưa có thẻ hoặc nhấn **Vẫn chưa hiểu!?**. AI không tự mở panel che slide. |
| **Quyền quyết định** | Học viên quyết định nội dung cần hỏi; giảng viên quyết định cách trả lời và thời điểm đánh dấu đã giải đáp. | AI đề xuất cấu trúc, nhưng học viên quyết định đường đi, node cần xem và thời điểm đóng bản đồ. | Học viên quyết định có mở hỗ trợ hay không; giảng viên quyết định nội dung nào được gắn nhãn “đã duyệt” và phát hành cho lớp. |
| **Trade-off chính** | Câu trả lời có người chịu trách nhiệm và đúng ngữ cảnh, nhưng học viên phải biết cách đặt câu hỏi và có thể phải chờ giảng viên phản hồi. | Giúp nhìn thấy bức tranh tổng thể, nhưng bản đồ lớn có thể tạo thêm tải nhận thức và làm học viên mất thêm thời gian tìm đúng nhánh. | Hỗ trợ nhanh và cá nhân hóa hơn, nhưng AI có thể giải thích hoặc chẩn đoán sai; quiz cũng có thể làm học viên lỡ thêm bài nếu luồng quá dài. |

## 4. Spectrum phân chia vai trò

```text
OPTION A                              OPTION B                              OPTION C
USER CREATES / INITIATES       →       USER + AI CO-CREATE       →       AI CREATES / PREPARES,
Học viên tự viết câu hỏi          AI lập bản đồ, user chọn đường       USER REVIEWS; giảng viên duyệt
```

- **Option A:** user-led/human escalation. Học viên tạo nội dung yêu cầu; hệ thống chỉ mang theo ngữ cảnh.
- **Option B:** co-create. AI chuẩn bị cấu trúc, còn từng lựa chọn của học viên quyết định phần nội dung được mở ra.
- **Option C:** AI-led with review. AI chuẩn bị giải thích và đề xuất, nhưng không tự phát hành nội dung chưa được giảng viên kiểm chứng.

## 5. Distance Check

- **A khác B vì** A chuyển một câu hỏi do học viên tự viết tới giảng viên, còn B để học viên tự điều hướng trong cấu trúc kiến thức do AI chuẩn bị.
- **B khác C vì** B không chẩn đoán người học mà chỉ cho họ khám phá bản đồ; C dùng câu trả lời quiz để xác định Strong/Weak và tạo giải thích theo kết quả.
- **A khác C vì** A dựa vào phản hồi trực tiếp của giảng viên sau khi học viên chủ động hỏi; C cho AI hỗ trợ ngay, sau đó mới dùng tổng hợp ẩn danh để giảng viên kiểm chứng và duyệt nội dung dùng chung.

## 6. Prototype và người phụ trách

| Option | Prototype | Người phụ trách |
|---|---|---|
| A | [Student–Instructor Prototype](https://imhuynf.github.io/Track01-DAY18-2A202601782-TaThiThuHuyen/prototypes/Option%20A.html) | Đỗ Thu Liễu, Nguyễn Trí Trung |
| B | [Knowledge Map Prototype](https://imhuynf.github.io/Track01-DAY18-2A202601782-TaThiThuHuyen/prototypes/Option%20B.html) | Phạm Tiến Đại |
| C | [Foundational Concept Prototype](https://imhuynf.github.io/Track01-DAY18-2A202601782-TaThiThuHuyen/prototypes/Option%20C.html) | Tạ Thị Thu Huyền |

## 7. Giả định cần test

| Option | Giả định chính | Tín hiệu cần quan sát |
|---|---|---|
| A | Học viên có thể viết một câu hỏi đủ rõ và chấp nhận chờ giảng viên phản hồi. | Thời gian viết câu hỏi; họ có tìm câu hỏi tương tự trước khi gửi không; việc chưa có câu trả lời ngay có làm họ bỏ cuộc không. |
| B | Bản đồ giúp học viên xác định đúng vùng kiến thức nhanh hơn tự tra cứu. | Họ có chọn đúng node không; số lần mở/đóng nhánh; thời gian trước khi quay lại slide. |
| C | Giải thích theo ngữ cảnh và quiz ngắn giúp học viên xác định lỗ hổng mà không tạo thêm gián đoạn. | Họ chọn popup thuật ngữ hay quiz; họ có hiểu nhãn AI/chưa duyệt không; quiz và phần giải thích mất bao lâu; họ có quay lại bài được không. |
