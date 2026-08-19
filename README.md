# Track 1 — Day 18: Multiple Prototypes & Human–AI Design

## 1. Thông tin cá nhân và nhóm

- **Mã học viên:** 2A202601782
- **Họ và tên:** Tạ Thị Thu Huyền
- **Tên nhóm:** 666
- **Ba thành viên còn lại:**
  1. Đỗ Thu Liễu — 2A202601898
  2. Phạm Tiến Đại — 2A202601610
  3. Nguyễn Trí Trung — 2A202601594
- **Case nhóm chọn:** AI Tutor — Diagnostic Refresher.

Nhóm tiếp tục case từ Day 17: hỗ trợ học viên xác định phần kiến thức nền đang thiếu và nhận lượng thông tin vừa đủ để tiếp tục bài học mà không phải rời VLearn để tự dò tìm.

## 2. Hypothesis Problem

> Khi giảng viên đang dẫn dắt một khái niệm mới trên slide, học viên gặp khó khăn trong việc theo kịp bài giảng vì hai rào cản xảy ra cùng lúc: (1) họ không hiểu một từ khóa hoặc bức tranh tổng thể đằng sau khái niệm đó, nhưng không biết chính xác đó là lỗ hổng kiến thức nền nào để tự tra cứu ngay; và (2) ngay cả khi nhận ra mình đang bị hụt, họ không có thời gian để dừng lại tìm hiểu — vì bài giảng vẫn tiếp tục trôi và họ không muốn ngắt lời hoặc làm chậm cả lớp — dẫn đến việc họ im lặng bỏ qua, tiếp tục nghe trong tình trạng mất gốc, và khoảng hụt kiến thức đó dồn lại qua các phần sau của bài giảng.

- **Target user chính:** Học viên đang theo dõi bài giảng trên VLearn. Giảng viên là stakeholder phụ trong Option A và C.
- **Giả định cần kiểm tra:** Nếu học viên có thể nhanh chóng xác định phần mình chưa hiểu và nhận hỗ trợ ngay trong ngữ cảnh slide, họ sẽ quay lại bài nhanh hơn và hạn chế tích tụ lỗ hổng kiến thức.
- **Chi tiết thiết kế chung:** [Three-Option Design Sheet](three-option-design-sheet.md).

## 3. Three Solution Options

| Option | Mô tả ngắn | Prototype |
|---|---|---|
| **A — Hỏi giảng viên theo ngữ cảnh** | Học viên tự viết câu hỏi ngay trong bài. Hệ thống gắn câu hỏi với slide và mốc kiến thức; giảng viên xem, mở đúng ngữ cảnh và cập nhật trạng thái đã/chưa giải đáp. | [Mở Option A](prototype/Option%20A/student-instructor-prototype.html) |
| **B — Sơ đồ kiến thức** | AI tổ chức nội dung bài thành bản đồ khái niệm. Học viên chọn nhánh, xem phạm vi slide, kiến thức liên quan và tài liệu để tự xác định vùng kiến thức đang thiếu. | [Mở Option B](prototype/Option%20B.html) |
| **C — Khái niệm nền và chẩn đoán nhanh** | AI giải thích thuật ngữ theo ngữ cảnh slide và cung cấp bài kiểm tra ngắn để xác định khái niệm Strong/Weak. Kết quả được tổng hợp ẩn danh; giảng viên kiểm chứng, chỉnh sửa và duyệt tag trước khi phát hành. | [Mở Option C](prototype/Option%20C.html) |

Ba option nằm trên một spectrum phân chia vai trò:

```text
OPTION A                         OPTION B                         OPTION C
USER CREATES / INITIATES   →    USER + AI CO-CREATE       →    AI PREPARES, USER REVIEWS
```

## 4. Đóng góp của tôi trong nhóm

- **Option phụ trách:** Option C — Khái niệm nền và chẩn đoán nhanh.
- **Prototype:** Tôi dựng bản HTML ban đầu trong giao diện đọc slide giống VLearn, chuẩn bị slide **Data Observability**, câu hỏi, đáp án, dữ liệu lớp mô phỏng và nội dung giải thích. Tôi viết phần liên hệ giữa lời giải thích với các thuật ngữ đang có trên slide như Data Quality, Data Pipeline, Schema, Monitoring, freshness, completeness và schema drift.
- **Shared context/content:** Tôi cùng nhóm giữ chung bối cảnh học viên gặp thuật ngữ chưa hiểu khi bài giảng vẫn tiếp tục; task là nhận hỗ trợ đủ nhanh để hiểu phần nền và quay lại bài mà không mở Chat/Google. Trong Option C, tôi hiện thực bối cảnh này bằng popup thuật ngữ và panel kiểm tra nhanh ngay trên slide.
- **Human–AI decisions:** Học viên chủ động mở hoặc đóng hỗ trợ. Nội dung chưa có tag phải mang nhãn “AI giải thích tạm thời/chưa được giảng viên duyệt”. AI chỉ đề xuất khái niệm từ kết quả Strong/Weak; giảng viên phải kiểm chứng ngữ cảnh, chỉnh sửa, duyệt và phát hành. Dữ liệu lớp chỉ hiển thị ở dạng tổng hợp ẩn danh và kết quả mới nhất thay thế kết quả cũ của cùng học viên.
- **Facilitation:** Tôi facilitate các lượt thử Option C với Đỗ Thu Liễu và Phạm Tiến Đại, hướng dẫn tester thử popup từ khóa, thao tác bôi đen từ chưa có tag và luồng “Vẫn chưa hiểu!?”.
- **Observation và tổng hợp feedback:** Tôi ghi nhận hai điểm nổi bật: giải thích ngay trên slide giúp người học không phải chuyển sang công cụ khác; bài kiểm tra nhanh giúp họ nhận ra phần kiến thức còn yếu. Điểm vướng là lượng thông tin AI và số bước trong quiz có thể làm người học mất tập trung hoặc lỡ thêm nội dung giảng.

## 5. Prototype Feedback

### Observation từ phiên tôi facilitate

- Tester nhận ra được cách bấm từ khóa để xem giải thích và đánh giá phần hỗ trợ ngay trên slide là hữu ích.
- Chức năng **“Vẫn chưa hiểu!?”** và kết quả Strong/Weak giúp tester thấy rõ hơn phần kiến thức nền đang thiếu.
- Tester muốn nội dung giải thích ngắn hơn, panel không che nhiều slide và câu hỏi kiểm tra đủ ngắn để không làm đứt mạch học.

### Ba điểm feedback synthesis

1. Hỗ trợ phải xuất hiện nhanh, ngắn gọn và có đường quay lại bài rõ ràng.
2. Hệ thống cần giúp học viên xác định phần mình chưa hiểu, không chỉ đưa ra một định nghĩa chung.
3. Mỗi trạng thái chỉ nên hiển thị lượng thông tin cần thiết; sơ đồ, popup hoặc nội dung AI quá dài đều có thể tạo thêm tải nhận thức.

### Next Change

Nhóm ưu tiên tiếp tục **Option C** vì đây là phương án giải quyết trực tiếp việc xác định và bổ sung kiến thức nền mà học viên đang thiếu. Iteration tiếp theo sẽ rút gọn phần giải thích mặc định, giữ định nghĩa và liên hệ với slide ở lớp thông tin đầu tiên; phần tài liệu và nội dung sâu hơn chỉ mở khi học viên yêu cầu. Bài kiểm tra cần ít câu, kết quả trực quan và luôn có nút đóng hoặc quay lại slide.

### Still Unproven

- Chưa chứng minh được quiz xác định đúng kiến thức nền học viên đang thiếu.
- Chưa chứng minh được hỗ trợ theo thời gian thực giúp học viên theo kịp bài tốt hơn cách tra cứu hiện tại.
- Chưa biết ngưỡng hơn 50% Weak có phù hợp với các lớp khác nhau hay không.
- Chưa biết giảng viên có chấp nhận thêm bước kiểm chứng, chỉnh sửa và phát hành tag hay không.
- Chưa xác định được lượng thông tin tối ưu để vừa giúp hiểu bài vừa không làm người học mất mạch.

Chi tiết: [Prototype Feedback Note](prototype-feedback-note.md) và [Group Feedback Synthesis](group-feedback-synthesis.md).

## 6. AI Support Log
- **AI đã hỗ trợ nhóm:** Hỗ trợ so sánh cách phân chia vai trò giữa học viên, AI và giảng viên; rà soát HTML/CSS/JavaScript; hoàn thiện các trạng thái tương tác của ba prototype; đồng thời giúp nhóm phát hiện nút không hoạt động, luồng bị cụt hoặc nội dung hiển thị quá dài.
- **AI sai hoặc hời hợt:** Một số đề xuất ban đầu chỉ khác nhau về giao diện nhưng chưa khác rõ về cơ chế. AI cũng có xu hướng thêm nhiều chức năng, làm Option C quá rộng và tạo thêm thao tác trong lúc học viên đang cần quay lại bài nhanh. Một số suy luận như coi lượt mở popup là bằng chứng học viên không hiểu, hoặc giả định hệ thống luôn biết giảng viên đang trình chiếu slide nào, không có đủ căn cứ từ bối cảnh thực tế.
- **Nhóm đã tự sửa:** Nhóm chốt lại ba cơ chế khác nhau: A là học viên chủ động hỏi giảng viên, B là học viên điều hướng trong bản đồ kiến thức do AI chuẩn bị, C là AI giải thích và chẩn đoán nhanh nhưng học viên và giảng viên vẫn giữ quyền quyết định. Nhóm thống nhất lại target user, situation, task và desired outcome; rút gọn các critical interactions; tự chuẩn bị nội dung, câu hỏi và dữ liệu mô phỏng; đồng thời không dùng output AI làm feedback thật.
- **Giới hạn sử dụng AI:** Các prototype chỉ dùng canned output và logic mô phỏng, không gọi model/API và không sử dụng dữ liệu thật của học viên. Nội dung do AI đề xuất vẫn cần người phụ trách option kiểm tra trước khi đưa vào prototype.
