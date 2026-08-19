# Three-option Design Sheet

## Chặng 1 — Nối lại evidence từ Day 17

### Evidence ban đầu

Trong Practice Note P01, người tham gia kể rằng khi học về AWS, họ gặp hai khái niệm “Data Warehouse” và “Data Lake” nhưng không biết mình đang thiếu phần kiến thức nền nào. Họ đã sao chép nội dung slide sang Chat hoặc tìm trên Google. Việc tra cứu thường mất khoảng 5–10 phút hoặc lâu hơn; trong lúc đó, bài giảng vẫn tiếp tục nên họ bỏ lỡ phần giảng tiếp theo và khó bắt nhịp lại.

Đây mới là evidence từ một Practice Note cá nhân. Nhóm dùng chi tiết này làm điểm xuất phát cho Day 18, không xem đây là bằng chứng rằng mọi học viên đều gặp vấn đề giống nhau.

### Điều vẫn chưa được chứng minh

- Hai Practice Notes còn lại có cùng situation, workaround và hậu quả hay không.
- Học viên thường im lặng vì không muốn ngắt lời, hay vì họ nghĩ tự tra cứu sẽ nhanh hơn.
- Học viên cần AI chẩn đoán kiến thức nền, hay một lời giải thích ngắn theo đúng ngữ cảnh đã đủ.
- Hỗ trợ chủ động có giúp học viên theo kịp hơn hay lại gây thêm phân tâm.

### Tự kiểm GATE 1 — Evidence continuity

- [x] Hypothesis Problem có situation, user, job, barrier và consequence.
- [x] Có observation cụ thể từ Practice Note P01.
- [x] Đã ghi rõ những điều vẫn chưa được chứng minh.
- [ ] Nhóm đã đặt đủ ba Practice Notes cạnh nhau và kiểm tra điểm giống, khác hoặc mâu thuẫn.

## Chặng 2 — Chọn ba Solution Options

### 1. Hypothesis Problem chung

> Khi giảng viên đang dẫn dắt một khái niệm mới trên slide, học viên gặp khó khăn trong việc theo kịp bài giảng vì hai rào cản xảy ra cùng lúc: (1) họ không hiểu một từ khóa hoặc bức tranh tổng thể đằng sau khái niệm đó, nhưng không biết chính xác đó là lỗ hổng kiến thức nền nào để tự tra cứu ngay; và (2) ngay cả khi nhận ra mình đang bị hụt, họ không có thời gian để dừng lại tìm hiểu — vì bài giảng vẫn tiếp tục trôi và họ không muốn ngắt lời hoặc làm chậm cả lớp — dẫn đến việc họ im lặng bỏ qua, tiếp tục nghe trong tình trạng mất gốc, và khoảng hụt kiến thức đó dồn lại qua các phần sau của bài giảng.

### 2. Mở lại Solution Parking Lot

Các hướng được đưa ra từ Day 17:

1. Gắn phần giải thích khái niệm nền ngay bên cạnh slide.
2. Cho phép học viên chọn một thuật ngữ để xem giải thích theo ngữ cảnh.
3. Dùng một vài câu hỏi ngắn để tìm phần kiến thức nền có thể đang thiếu.
4. Cho phép đánh dấu phần chưa hiểu để xem lại sau buổi học.
5. Chủ động gợi ý kiến thức nền khi bài giảng bắt đầu một khái niệm mới.

Nhóm chọn hướng 2, 3 và 5 vì chúng cùng giải quyết một vấn đề nhưng chia công việc giữa học viên và AI theo ba cách khác nhau.

### 3. Comparison Contract

Những yếu tố dưới đây được giữ nguyên khi tester dùng A/B/C:

| Thành phần | Quyết định chung cho A/B/C |
|---|---|
| Target user | Học viên đang theo dõi một bài giảng trực tiếp và gặp khái niệm chưa hiểu trên slide |
| Situation | Giảng viên đang giải thích kiến trúc phân tích dữ liệu trên AWS và bài giảng vẫn tiếp tục |
| Task | Hiểu vì sao kiến trúc sử dụng cả Data Lake và Data Warehouse, sau đó tiếp tục theo dõi bài giảng |
| Desired outcome | Học viên nói được khác biệt chính giữa hai khái niệm, không phải mở công cụ bên ngoài và biết lớp đang học đến đâu |
| Content/data fixture | Cùng một slide “AWS Analytics Architecture” và cùng một đoạn nội dung giảng đã được chuẩn bị sẵn |
| Điểm bắt đầu | Học viên nhìn thấy sơ đồ nhưng chưa hiểu Data Lake khác Data Warehouse ở đâu và vì sao cần cả hai |
| Điểm kết thúc | Học viên xem xong phần hỗ trợ, quay lại slide hiện tại và có thể tiếp tục nghe giảng |

#### Content fixture dùng trong cả ba prototype

**Slide 12 — AWS Analytics Architecture**

```text
Nguồn dữ liệu
CSV · log ứng dụng · ảnh · sự kiện
        ↓
Amazon S3 — Data Lake
        ↓
ETL / xử lý dữ liệu
        ↓
Amazon Redshift — Data Warehouse
        ↓
BI Dashboard
```

Slide chỉ thể hiện luồng dữ liệu và tên các thành phần, chưa giải thích sự khác nhau giữa Data Lake và Data Warehouse.

Điểm học viên đang vướng:

> “Nếu Data Lake và Data Warehouse đều dùng để lưu dữ liệu, tại sao kiến trúc lại cần cả hai?”

Trong lúc học viên mở phần hỗ trợ, lớp chuyển sang **Slide 13 — ETL kết nối Data Lake với Data Warehouse**. Khi học viên quay lại, cả ba option đều hiển thị cùng một thông báo ngắn về phần bài giảng đã chuyển qua. Phần này được giữ giống nhau để không tạo lợi thế riêng cho option nào.

### 4. Ba Solution Options

| Thành phần | Option A — Tra nhanh theo từ khóa | Option B — Hỏi nhanh để tìm chỗ hổng | Option C — Gợi ý kiến thức nền |
|---|---|---|---|
| Solution mechanism | Giải thích trực tiếp thuật ngữ do học viên chọn | Hỏi hai câu ngắn, sau đó đề xuất phần kiến thức nền có thể còn thiếu | Chủ động đưa ra một thẻ kiến thức nền khi slide có khái niệm mới |
| User làm gì? | Chọn “Data Lake” hoặc “Data Warehouse” trên slide | Bấm nút “Mình chưa hiểu”, trả lời hai câu hỏi và xác nhận hoặc sửa đề xuất của AI | Xem lý do thẻ được gợi ý rồi chọn mở, để sau hoặc tắt gợi ý |
| AI làm gì? | Giải thích thuật ngữ trong ngữ cảnh của Slide 12 và nêu quan hệ với thuật ngữ còn lại | Dựa trên câu trả lời để đề xuất một lỗ hổng có khả năng liên quan; chỉ giải thích sau khi học viên xác nhận | Đọc nội dung và prerequisite tag của slide để chuẩn bị một cầu nối kiến thức ngắn |
| Trigger | Học viên chủ động chọn từ khóa | Học viên chủ động báo mình đang bị hụt | AI nhận ra slide có hai khái niệm mới đã được giảng viên gắn prerequisite tag |
| Quyền quyết định | Học viên quyết định hỏi thuật ngữ nào và dừng lúc nào | AI đề xuất, học viên có quyền xác nhận, chọn phần khác hoặc bỏ qua | AI chỉ đề xuất; học viên quyết định mở, đóng hoặc tắt gợi ý chủ động |
| Trade-off chính | Nhanh và ít thao tác, nhưng có thể chỉ xử lý phần bề mặt | Có cơ hội tìm đúng chỗ hổng hơn, nhưng hai câu hỏi có thể làm học viên mất thêm thời gian | Học viên không cần tự xác định từ khóa, nhưng gợi ý sai lúc có thể gây phân tâm |

### 5. Chức năng và flow của từng option

Mỗi option chỉ có ba trạng thái: common context, critical interaction và kết quả để học viên quyết định. Ba prototype không cần gọi model thật; nội dung AI bên dưới là canned output dùng cho buổi test.

#### Option A — Tra nhanh theo từ khóa

**Trạng thái 1 — Common context**

Học viên đang xem Slide 12. Hai cụm “Data Lake” và “Data Warehouse” có dấu hiệu cho biết có thể chọn để xem giải thích. Giao diện không tự mở nội dung hỗ trợ.

**Trạng thái 2 — Critical interaction**

Khi học viên chọn một thuật ngữ, một bảng giải thích ngắn xuất hiện bên cạnh slide:

> **Data Lake là gì?**
>
> Data Lake lưu dữ liệu thô ở nhiều định dạng, ví dụ bảng CSV, log hoặc ảnh. Trong sơ đồ này, Amazon S3 giữ vai trò Data Lake. Dữ liệu chưa cần được sắp xếp hoàn chỉnh trước khi lưu.

Bảng giải thích ghi rõ: “Dựa trên Slide 12 và glossary của khóa học”. Học viên có thể chọn “So sánh với Data Warehouse”, đóng bảng hoặc quay lại bài.

**Trạng thái 3 — Result / user decision**

Nếu học viên chọn xem so sánh, hệ thống hiển thị:

> Data Lake giữ dữ liệu thô và linh hoạt. Data Warehouse giữ dữ liệu đã được làm sạch, tổ chức để truy vấn và làm báo cáo nhanh. Hai phần không thay thế nhau; ETL đưa dữ liệu cần thiết từ Data Lake sang Data Warehouse.

Sau đó, học viên chọn “Quay lại bài”.

**Điều cần quan sát:** Học viên có nhận ra từ khóa có thể chọn không; phần giải thích một thuật ngữ có đủ để họ hiểu mối quan hệ giữa hai khái niệm không.

#### Option B — Hỏi nhanh để tìm chỗ hổng

**Trạng thái 1 — Common context**

Học viên xem cùng Slide 12 và có nút “Mình đang bị hụt”. Trước khi bắt đầu, hệ thống nói rõ: “AI sẽ hỏi 2 câu ngắn, khoảng 30 giây. Đây không phải bài kiểm tra; bạn có thể bỏ qua bất cứ lúc nào.”

**Trạng thái 2 — Critical interaction**

AI lần lượt hỏi:

1. “Dữ liệu đưa vào hệ thống này có thể gồm những dạng nào?”

   Lựa chọn: “Chỉ dữ liệu dạng bảng” · “Nhiều dạng như bảng, log và ảnh” · “Mình chưa chắc”.

2. “Dữ liệu dùng để làm báo cáo thường cần ở trạng thái nào?”

   Lựa chọn: “Giữ nguyên hoàn toàn” · “Đã được làm sạch và tổ chức” · “Mình chưa chắc”.

Từ câu trả lời, AI đưa ra một đề xuất có mức độ chắc chắn thay vì khẳng định:

> **Có thể bạn đang thiếu phần nền về dữ liệu thô và dữ liệu đã xử lý.**
>
> Gợi ý này dựa trên hai câu trả lời vừa rồi và nội dung của Slide 12.

Học viên chọn một trong ba hướng: “Đúng, giải thích phần này”, “Không đúng, chọn phần khác” hoặc “Bỏ qua”.

**Trạng thái 3 — Result / user decision**

Sau khi học viên xác nhận, AI giải thích ngắn vì sao Data Lake phù hợp với dữ liệu thô và Data Warehouse phù hợp với dữ liệu đã được chuẩn bị cho phân tích. Nếu đề xuất không đúng, học viên có thể chọn lại giữa ba phần: “Dạng dữ liệu”, “ETL” hoặc “Mục đích phân tích”.

Cuối cùng, học viên chọn “Quay lại bài”.

**Điều cần quan sát:** Học viên có sẵn sàng trả lời hai câu khi bài giảng đang chạy không; họ có hiểu và sử dụng quyền sửa đề xuất của AI không.

#### Option C — Gợi ý kiến thức nền

**Trạng thái 1 — Common context**

Khi Slide 12 xuất hiện, một thẻ nhỏ hiện ở cạnh slide nhưng không che nội dung:

> **Kiến thức nền có thể hữu ích · khoảng 45 giây**
>
> Slide này bắt đầu dùng Data Lake và Data Warehouse. Bạn có muốn xem nhanh vì sao kiến trúc cần cả hai không?

Thẻ ghi rõ lý do xuất hiện: “Gợi ý từ nội dung Slide 12 và prerequisite tag do giảng viên chuẩn bị”.

**Trạng thái 2 — Critical interaction**

Học viên chọn “Xem ngay”, “Để sau” hoặc “Tắt gợi ý chủ động”. Nếu chọn xem, AI trình bày cầu nối kiến thức:

> Dữ liệu thường đi vào hệ thống ở dạng thô và chưa đồng nhất, nên được giữ trong Data Lake. Khi cần phân tích hoặc làm báo cáo ổn định, một phần dữ liệu được xử lý qua ETL rồi chuyển sang Data Warehouse. Vì vậy sơ đồ dùng cả hai, mỗi phần phục vụ một giai đoạn khác nhau.

AI không tự nhận rằng học viên “không hiểu”. Nếu gợi ý chưa phù hợp, học viên có thể chọn “Không phải phần mình đang vướng” và chọn một nội dung khác.

**Trạng thái 3 — Result / user decision**

Học viên đóng phần giải thích hoặc chọn “Quay lại bài”. Nếu đã tắt gợi ý chủ động, hệ thống xác nhận thay đổi và không hiện thêm thẻ trong phiên prototype.

**Điều cần quan sát:** Học viên có hiểu vì sao thẻ xuất hiện không; thẻ có hỗ trợ đúng lúc hay làm họ phân tâm; họ có tìm thấy cách bỏ qua hoặc tắt gợi ý không.

### 6. Cách quay lại bài dùng chung

Sau khi hoàn thành hoặc bỏ qua hỗ trợ, cả A/B/C đều hiển thị cùng một thông báo:

> **Bạn đã quay lại bài giảng.**
>
> Lớp đang ở Slide 13: ETL kết nối Data Lake với Data Warehouse. Ý chính vừa đi qua: dữ liệu cần được làm sạch và chuyển đổi trước khi phục vụ phân tích ổn định.

Học viên có thể chọn “Đến slide hiện tại” hoặc “Xem lại Slide 12”. Mỗi prototype có nút “Bắt đầu lại” để trở về common context ban đầu.

### 7. Giả định và rủi ro cần kiểm tra

| Option | Giả định cần kiểm tra | Rủi ro chính |
|---|---|---|
| A | Học viên nhận ra mình có thể chọn thuật ngữ và lời giải thích ngắn đã đủ để tiếp tục bài | Lỗ hổng thật nằm ở kiến thức rộng hơn chứ không phải một từ khóa |
| B | Hai câu hỏi giúp học viên nhận ra chỗ hổng phù hợp và họ vẫn chấp nhận thời gian chờ | Học viên thấy mình đang bị kiểm tra hoặc bỏ cuộc vì bài giảng vẫn tiếp tục |
| C | Học viên hiểu lý do AI gợi ý và chủ động quyết định có mở hay không | Gợi ý xuất hiện sai lúc, bị hiểu là AI đang theo dõi học viên hoặc gây phân tâm |

### 8. Distance Check

- A khác B vì A giải thích ngay phần học viên đã tự xác định, còn B cùng học viên tìm phần kiến thức nền trước khi giải thích.
- B khác C vì B chỉ bắt đầu khi học viên yêu cầu, còn C chủ động đưa ra một gợi ý dựa trên nội dung slide.
- A khác C vì A để học viên quyết định từ khóa cần hỏi, còn C chuẩn bị trước một cầu nối kiến thức để học viên xem hoặc bỏ qua.

```text
OPTION A
Học viên xác định và yêu cầu
        ↓
OPTION B
Học viên và AI cùng tìm chỗ hổng
        ↓
OPTION C
AI chủ động đề xuất, học viên quyết định
```

## Chặng 3 — Human–AI Design pass

### 9. Human–AI Decision Table

| Human–AI decision | Option A — Tra nhanh | Option B — Hỏi để tìm chỗ hổng | Option C — Gợi ý kiến thức nền |
|---|---|---|---|
| User làm gì? AI làm gì? | User chọn thuật ngữ; AI giải thích đúng thuật ngữ đó theo ngữ cảnh slide | User báo bị hụt và trả lời hai câu; AI đề xuất phần nền; user xác nhận hoặc sửa trước khi AI giải thích | AI đưa ra một thẻ gợi ý; user quyết định mở, để sau hoặc tắt; AI chỉ giải thích khi user đồng ý |
| AI Act / Ask / Don't Act? Vì sao? | **Act sau yêu cầu rõ ràng.** AI không đoán học viên đang thiếu gì | **Ask trước, Act sau.** Hậu quả khi chẩn đoán sai là mất thời gian nên AI cần user xác nhận | **Đề xuất nhưng không tự mở.** Gợi ý chủ động có thể gây phân tâm nên quyền mở nội dung vẫn thuộc về user |
| User hiểu capability và limit bằng gì? | Giao diện nói “Giải thích thuật ngữ theo slide hiện tại”; không hứa tìm được toàn bộ lỗ hổng | Giao diện nói đây không phải bài kiểm tra và kết quả chỉ là một đề xuất có thể sai | Thẻ nói rõ nó xuất hiện vì slide có prerequisite tag, không phải vì AI biết chắc học viên đang gặp khó khăn |
| Evidence và uncertainty được thể hiện thế nào? | Hiển thị nguồn “Slide 12 + glossary khóa học” | Hiển thị hai câu trả lời đã dùng và dùng cách nói “Có thể bạn đang thiếu…” | Hiển thị lý do gợi ý và nguồn “nội dung slide + prerequisite tag” |
| User kiểm soát và recovery thế nào? | Đóng giải thích, chọn thuật ngữ khác, xem so sánh hoặc quay lại bài | Sửa câu trả lời, bác đề xuất, chọn phần nền khác, bỏ qua hoặc quay lại bài | Để sau, đóng, báo gợi ý không đúng, tắt gợi ý chủ động hoặc quay lại bài |

### 10. Dữ liệu Option C được phép sử dụng

Trong prototype, Option C chỉ dùng:

- nội dung slide đang hiển thị;
- prerequisite tag do giảng viên gắn vào slide;
- lịch sử chuyển slide để báo lớp đang ở đâu.

Option C không dùng camera, micro, cảm xúc, lịch sử học cá nhân hoặc dữ liệu thao tác ngoài prototype. Việc học viên đóng hay sửa gợi ý chỉ có tác dụng trong phiên test hiện tại và không được ghi nhớ cho lần sau.

## Chặng 4 — Phạm vi ba micro-prototype

### 11. Phần dùng chung và phần khác nhau

Khoảng 70% giao diện của A/B/C được giữ giống nhau:

- header và sidebar của VLearn;
- Slide 12 và Slide 13;
- task, content fixture và desired outcome;
- độ dài phần giải thích;
- thông báo quay lại bài;
- nút “Bắt đầu lại”.

Phần critical interaction là phần duy nhất cần khác rõ:

- A: chọn một từ khóa;
- B: bấm báo bị hụt và trả lời hai câu;
- C: nhận một thẻ gợi ý chủ động rồi quyết định có mở hay không.

### 12. Prototype annotation

**Option A**

```text
We expect the tester to: chọn một thuật ngữ, đọc giải thích và quay lại bài.
Watch for: tester có nhận ra từ khóa chọn được và có cần xem cả hai thuật ngữ không.
Do not explain: từ khóa nào tester nên chọn.
```

**Option B**

```text
We expect the tester to: báo mình đang bị hụt, trả lời hai câu và duyệt đề xuất của AI.
Watch for: thời gian do dự, cảm giác bị kiểm tra và việc tester có sửa đề xuất không.
Do not explain: câu trả lời nào được xem là đúng.
```

**Option C**

```text
We expect the tester to: chú ý đến thẻ gợi ý và tự quyết định mở, để sau hoặc tắt.
Watch for: tester hiểu lý do thẻ xuất hiện thế nào và có tìm được quyền kiểm soát không.
Do not explain: vì sao AI đưa ra gợi ý.
```

### 13. Tự kiểm trước khi build

#### GATE 2 — Meaningful Options

- [x] A/B/C cùng user, situation, task, content và desired outcome.
- [x] Ba option khác nhau về mechanism, không chỉ khác màu, layout hoặc wording.
- [x] A là user-led, B là user–AI co-create, C là AI-initiated nhưng user vẫn quyết định.
- [x] Ba option dùng cùng một cách quay lại bài.
- [x] Mỗi option có một lợi ích và một trade-off hợp lý.

#### GATE 3 — Human Control

- [x] Trước khi AI hoạt động, học viên biết AI sắp làm gì.
- [x] Mỗi option nói rõ AI dựa vào dữ liệu nào và giới hạn nằm ở đâu.
- [x] AI dùng ngôn ngữ không chắc chắn khi đưa ra chẩn đoán hoặc gợi ý.
- [x] Học viên có thể đóng, bỏ qua, sửa hoặc tắt hỗ trợ.
- [x] Sau khi AI sai, học viên vẫn có đường quay lại bài giảng.

#### GATE 4 — Chỉ đánh dấu sau khi đã build và tự test

- [ ] Tester có thể tự mở và thao tác cả A/B/C.
- [ ] Ba prototype bắt đầu từ đúng cùng một common context.
- [ ] Không option nào cần facilitator giải thích giao diện.
- [ ] Mỗi option có 2–3 trạng thái quanh critical interaction.
- [ ] Nút “Bắt đầu lại” đưa prototype về common context.

> Ba prototype dùng để so sánh cách học viên phản ứng với ba cơ chế hỗ trợ. Kết quả từ ba tester chỉ giúp nhóm chọn thay đổi tiếp theo, chưa đủ để kết luận giải pháp đã được xác thực.
