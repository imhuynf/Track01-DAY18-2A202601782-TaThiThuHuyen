# AI Support Log — Option C

Tôi phụ trách hiện thực hóa Option C dưới dạng một micro-prototype HTML đặt trong giao diện đọc slide giống VLearn. Tôi tự dựng bản HTML ban đầu, chuẩn bị dữ liệu mô phỏng và viết nội dung giải thích sao cho nối lại với các thuật ngữ đang xuất hiện trên slide. AI được dùng để rà soát và chỉnh code HTML/CSS/JavaScript cho chỉn chu, thống nhất và dễ thao tác hơn. Prototype không gọi model hoặc API và không sử dụng dữ liệu thật của học viên.

**Artifact hiện tại:** [Option C — Khái niệm nền và chẩn đoán nhanh](prototype/Option%20C.html)

## Prompt tổng hợp dùng cho phiên bản hiện tại

Prompt dưới đây là bản tổng hợp từ nhiều lần trao đổi và sửa thiết kế. Đây không phải prompt được viết đầy đủ ngay từ đầu.

```text
Hãy rà soát và chỉnh lại micro-prototype HTML Option C mà tôi đã dựng theo giao
diện VLearn. Tôi đã chuẩn bị slide Data Observability, nội dung giải thích, câu hỏi
và dữ liệu mô phỏng; hãy giữ các nội dung này, chủ yếu chỉnh code và interaction
cho gọn, thống nhất và có thể test được.

Luồng học viên:
- Highlight thuật ngữ đã được giảng viên duyệt; bấm vào sẽ mở popup giải thích
  theo ngữ cảnh slide và có nhãn “Giảng viên đã duyệt”.
- Khi bôi đen từ chưa có tag, hiển thị giải thích AI tạm thời và ghi rõ chưa được
  kiểm duyệt.
- Nút “Vẫn chưa hiểu !?” mở ba câu kiểm tra nhanh. Chấm mock thành Strong/Weak,
  sau đó giải thích phần Weak và cho mở tài liệu học thêm.
- Kết quả mới nhất được đưa vào tổng hợp ẩn danh của lớp, không cộng trùng khi
  học viên làm lại.

Luồng giảng viên:
- Hiển thị tỷ lệ Weak theo khái niệm từ dữ liệu mô phỏng tôi cung cấp.
- Chỉ đề xuất tag khi hơn 50% học viên Weak. Giảng viên vẫn phải kiểm chứng,
  chỉnh sửa nếu cần, duyệt rồi mới phát hành.
- Nút test luồng giảng viên đặt ở header; dưới slide chỉ giữ hai nút học viên
  “Khái niệm nền” và “Vẫn chưa hiểu !?” có kích thước bằng nhau.

Không gọi API. Dùng HTML/CSS/JavaScript thuần. Mọi nút phải hoạt động, có hover,
active state và có đường đóng hoặc quay lại.
```

## AI đã giúp tôi ở đâu?

Tôi đã có bản HTML và nội dung chính trước. AI giúp tôi rà soát lại cấu trúc, chỉnh CSS để các nút và panel đồng đều hơn, đồng thời sửa JavaScript để các trạng thái mở, đóng, quay lại và làm lại bài không bị đứt luồng.

AI cũng hỗ trợ hiện thực phần logic từ dữ liệu tôi chuẩn bị: chấm Strong/Weak bằng đáp án viết sẵn, cập nhật kết quả mới nhất vào bảng tổng hợp thay vì cộng trùng, khóa bước duyệt khi giảng viên chưa xác nhận kiểm chứng và chỉ highlight tag sau khi phát hành.

Ngoài ra, AI giúp tôi kiểm tra cú pháp, ID trùng, nút không có phản hồi và cách tách nút test giảng viên khỏi chức năng của học viên. Phần nội dung giải thích, câu hỏi và dữ liệu mẫu do tôi chuẩn bị.

## AI sai hoặc hời hợt ở đâu?

Ở các lần đầu, AI đề xuất một thanh gợi ý có nhiều lựa chọn gần giống nhau như “Để sau”, “Tắt gợi ý” và “Hiện lại”. Cách này làm giao diện nặng hơn và buộc học viên phải xử lý thêm quyết định trong lúc bài giảng vẫn tiếp tục.

AI cũng từng mở rộng Option C thành bản đồ cả vùng kiến thức sau khi học viên bấm nhiều thuật ngữ. Ý tưởng này có thể hữu ích nhưng làm micro-prototype đi quá xa khỏi critical interaction cần test. Nó còn tạo thêm thời gian đọc và có nguy cơ khiến học viên lỡ phần bài giảng tiếp theo.

Một đề xuất khác là theo dõi giảng viên đang nói tới slide nào để giúp học viên “bắt lại mạch”. Giả định này không phù hợp vì giảng viên có thể không trình chiếu bằng VLearn, nên hệ thống không có tín hiệu đáng tin để biết lớp đang ở đâu.

AI ban đầu cũng coi số lần mở giải thích như “lượt thắc mắc”. Cách gọi này kết luận quá mạnh: học viên có thể mở vì tò mò hoặc muốn kiểm tra lại, không nhất thiết là không hiểu. Việc đặt nút “Tôi vẫn chưa rõ” trong cả popup đã được giảng viên duyệt cũng bị thừa và làm mỗi popup có thêm một hành động không cần thiết.

Cuối cùng, nút mở luồng giảng viên ban đầu nằm cùng hàng với hai chức năng của học viên. Cách đặt đó khiến người dùng có thể hiểu đây là một chức năng học tập, trong khi nó chỉ là lối vào để tester xem góc nhìn giảng viên.

## Tôi đã tự sửa hoặc quyết định lại điều gì?

Tôi tự dựng bản HTML ban đầu, chọn nội dung slide, chuẩn bị câu hỏi, đáp án và dữ liệu lớp mô phỏng. Tôi cũng viết các đoạn giải thích ngắn và chủ động nối chúng với những từ đang có trên slide như Data Quality, Schema, Monitoring, freshness, completeness và schema drift để phần hỗ trợ không trở thành một định nghĩa chung chung.

Tôi bỏ bản đồ vùng kiến thức và giữ hai mức hỗ trợ ngắn: bấm vào một thuật ngữ để xem giải thích, hoặc bấm “Vẫn chưa hiểu !?” để kiểm tra nhanh ba khái niệm nền. Panel kiểm tra mở ngay trên slide và luôn có đường đóng hoặc quay lại nên học viên không phải rời khỏi bài học.

Tôi tách rõ nội dung đã duyệt và nội dung AI tạm giải thích. Thuật ngữ đã duyệt có highlight và nhãn “Giảng viên đã duyệt”; popup này không còn nút “Tôi vẫn chưa rõ”. Thuật ngữ chưa có tag chỉ xuất hiện khi học viên chủ động bôi đen, đồng thời phải ghi rõ chưa kiểm duyệt.

Tôi đổi tín hiệu chính từ số lượt mở popup sang kết quả Strong/Weak của bài kiểm tra. Dữ liệu giảng viên nhìn thấy chỉ là số lượng và tỷ lệ tổng hợp. Trong logic mẫu, một kết quả mới thay thế kết quả cũ của cùng học viên và ngưỡng đề xuất là hơn 50% Weak. Tuy nhiên, ngưỡng chỉ giúp AI sắp xếp ưu tiên; giảng viên vẫn phải kiểm chứng, chỉnh sửa nếu cần, duyệt và phát hành.

Tôi cũng tách nút test luồng giảng viên khỏi khu vực chức năng của học viên. Bên dưới slide chỉ còn hai nút bằng nhau là “Khái niệm nền” và “Vẫn chưa hiểu !?”. Nút giảng viên được chuyển lên header và có nhãn “TEST” để thể hiện đúng vai trò trong micro-prototype.

## Điều vẫn chưa được chứng minh

Prototype mới chỉ dùng canned output và dữ liệu lớp mô phỏng. Tôi chưa thể kết luận ba câu hỏi có xác định đúng lỗ hổng kiến thức hay không, ngưỡng hơn 50% có phù hợp cho mọi lớp hay không, hoặc giảng viên có chấp nhận thêm bước kiểm chứng và phát hành hay không. Tôi cũng chưa biết panel kiểm tra có khiến học viên bỏ lỡ thêm nội dung giảng hay phần giải thích Weak có đủ ngắn để họ quay lại bài kịp thời.

Những điểm trên cần được quan sát khi tester trải nghiệm cả ba Option A/B/C trong cùng context và task. Log này không chứa quote, observation hoặc feedback tester vì nhóm chưa cung cấp evidence test thật cho các nội dung đó.
