# Track 1 - Day 17 — Finding and Validating Pain Points

## 1. Thông tin cá nhân và nhóm

- **MHV:** 2A202601782
- **Họ tên:** Tạ Thị Thu Huyền
- **Tên nhóm:** _điền tên nhóm_
- **Thành viên nhóm:**
  1. Phạm Tiến Đại — 2A202601610
  2. Tạ Thị Thu Huyền — 2A202601782
  3. Nguyễn Trí Trung — 2A202601594
- **Case đã chọn:** Case A — AI Tutor: Diagnostic Refresher

---

## 2. Problem Hypothesis Brief (kết quả Chặng 1)

### 2.1 Solution — Gỡ solution khỏi hình thức cụ thể

**Solution directive (nguyên văn):**

> Thêm nút "Tôi vẫn chưa hiểu" vào bài học. Khi học viên bấm nút, AI Tutor sử dụng nội dung bài hiện tại, các câu trả lời gần đây và lịch sử học tập để: đặt 2–3 câu hỏi chẩn đoán ngắn, chọn một khái niệm nền để học viên ôn lại, tạo một phần giải thích ngắn, đưa học viên trở về bài đang học.

**Capability trung tính:**

> Học viên có thể nhận ra mình đang bị kẹt, xác định đúng kiến thức nền còn thiếu
> và nhận được lượng thông tin vừa đủ để tiếp tục nội dung hiện tại mà không phải
> rời luồng học để tự dò tìm.

### 2.2 Change — Chuỗi thay đổi được kỳ vọng

```text
Capability
  → Học viên nhận ra mình đang bị kẹt
  → Hệ thống xác định đúng kiến thức nền còn thiếu
  → Học viên tin và hiểu phần giải thích ngắn
  → Học viên quay lại nội dung chính mà không mất mạch
  → Outcome
```

Các thay đổi được kỳ vọng:

1. **Nhận biết (awareness/trigger):** học viên nhận ra mình đang bị kẹt và tin rằng yêu cầu hỗ trợ sẽ hữu ích hơn tự dò tìm.
2. **Chấp nhận chẩn đoán (trust the diagnosis):** học viên tin rằng khái niệm nền hệ thống chọn ra đúng là gốc rễ vấn đề của mình.
3. **Tiếp thu & quay lại bài (comprehension → re-entry):** học viên hiểu phần giải thích và tiếp tục nội dung chính mà không bị đứt mạch.

- **Output:** điểm kích hoạt hỗ trợ, câu hỏi chẩn đoán, kiến thức nền được chọn và phần giải thích ngắn.
- **Behavioral outcome:** học viên quay lại nội dung chính nhanh hơn và giảm số phần bài bị bỏ lỡ vì phải tra cứu bên ngoài.
- **Learning outcome:** học viên hiểu và áp dụng được kiến thức nền để tiếp tục bài học.
- **Mắt xích rủi ro nhất sau interview đầu tiên:** xác định đúng kiến thức nền và đưa người học trở lại bài đủ nhanh. P01 cho biết họ thường vẫn hiểu thuật ngữ sau khi dùng Chat/Google; pain nổi bật là mất 5–10 phút hoặc lâu hơn và không theo kịp phần giảng tiếp theo. Vì vậy, “có tìm được lời giải thích hay không” chưa phải rủi ro lớn nhất được quan sát ở vòng này.

### 2.3 Actor — Các nhóm người liên quan

| Actor | Họ đang làm gì? | Pain/hậu quả có thể có | Giá trị kỳ vọng |
|---|---|---|---|
| Học viên gặp thuật ngữ/khái niệm chưa hiểu | Đang nghe giảng, xem video hoặc đọc slide và phải dừng lại | Không biết mình thiếu kiến thức nền nào; mất thời gian tra cứu; lỡ mạch bài | Xác định đúng phần cần ôn và tiếp tục học nhanh hơn |
| Học viên đang kẹt nhưng không chủ động báo hiệu | Bỏ qua hoặc tiếp tục học trong trạng thái chưa hiểu | Mang lỗ hổng sang phần sau nhưng khó xuất hiện trong dữ liệu | Được hỗ trợ nếu hệ thống có tín hiệu phát hiện phù hợp |
| Instructor/người vận hành khoá học | Theo dõi tiến độ và mức độ hiểu bài | Khó biết đoạn nào khiến nhiều học viên mất mạch | Nhìn thấy điểm nghẽn phổ biến để điều chỉnh cách dạy |
| Content/curriculum team | Thiết kế bài học và cấu trúc kiến thức nền | Mapping kiến thức nền thiếu hoặc quá rộng có thể làm chẩn đoán sai | Có feedback để cải thiện nội dung và prerequisite |

**Actor chọn điều tra trước:** Học viên gặp thuật ngữ hoặc khái niệm chưa hiểu trong lúc học nhưng vẫn chủ động tìm cách tiếp tục.

**Lý do:** Đây là người trực tiếp trải qua pain và có thể kể lại hành vi gần đây như tự nhớ, tra cứu, quay lại bài giảng và xử lý phần bị bỏ lỡ. Kết luận từ actor này không đại diện cho nhóm âm thầm bỏ qua khó khăn, instructor hoặc content team; các actor đó vẫn là vùng chưa điều tra.

### 2.4 Situation & Job

**Mô tả Situation & Job:**

> Khi đang nghe giảng, xem video hoặc đọc slide và gặp một thuật ngữ chuyên ngành chưa hiểu, học viên cố xác định kiến thức nền mình đang thiếu và tìm một lời giải thích đủ nhanh để tiếp tục bài học. Hiện tại, họ thường tự nhớ lại, sao chép nội dung sang công cụ chat, tìm trên Google hoặc xem lại tài liệu cũ; trong lúc đó, bài giảng vẫn tiếp diễn và họ có thể bỏ lỡ phần tiếp theo.

**JTBD Hypothesis:**

> Khi tôi gặp một thuật ngữ hoặc khái niệm chưa hiểu trong lúc bài giảng đang tiếp diễn, tôi muốn nhanh chóng xác định kiến thức nền mình đang thiếu và được giải thích đúng phần đó trong ngữ cảnh hiện tại, để có thể tiếp tục theo dõi bài mà không phải rời luồng học để tìm kiếm mò mẫm.

### 2.5 Pain — Các cách giải thích cạnh tranh

**Hypothesis A — thiếu thông tin/định hướng (information gap):**

> Khi gặp một thuật ngữ hoặc khái niệm chưa hiểu trong lúc học, học viên không xác định được chính xác kiến thức nền mình đang thiếu. Vì vậy, họ phải tự dò tìm qua nhiều nguồn; kết quả tra cứu có thể phát sinh thêm thuật ngữ mới, làm tăng thời gian xử lý và khiến họ khó quay lại mạch bài.

**Hypothesis B — né tránh/động lực (motivation/ego):**

> Khi gặp một thuật ngữ hoặc khái niệm chưa hiểu, học viên cảm thấy thất bại, xấu hổ hoặc nản nên né tránh việc đối mặt với lỗ hổng ngay lúc đó, dẫn đến họ bỏ qua nội dung hoặc trì hoãn việc học.

**Hypothesis C — áp lực thời gian:**

> Học viên biết mình cần tìm nội dung gì và biết cách tra cứu, nhưng bài giảng đang tiếp diễn nên họ không có đủ thời gian để dừng lại tìm hiểu sâu — pain chủ yếu là áp lực thời gian, không phải thiếu định hướng hay động lực.

**Giả thuyết chọn điều tra trước:** A

**Lý do:** A có thể được kiểm tra trực tiếp qua một câu chuyện gần nhất: học viên có biết mình thiếu nền tảng nào, đã tra cứu ra sao và có phải tiếp tục dò qua nhiều khái niệm hay không. Nếu họ luôn biết chính xác cần tìm gì thì A suy yếu và C trở thành cách giải thích cạnh tranh mạnh hơn. B và C được giữ lại để tránh mặc định mọi khó khăn đều do thiếu thông tin.

### 2.6 Evidence — Điều cần tìm trước khi phỏng vấn

| Cần kiểm tra | Evidence làm nhóm tin hơn (A) | Evidence làm nhóm nghi ngờ/bác bỏ A |
|---|---|---|
| Situation có thật | Kể được buổi học, nội dung và thuật ngữ cụ thể | Chỉ trả lời chung chung, không nhớ lần cụ thể |
| Pain có ý nghĩa | Tự mô tả sự mơ hồ hoặc mất phương hướng | Biết ngay kiến thức cần xem và tìm được tức thì |
| Workaround tồn tại | Kể từng bước tra cứu, nguồn dùng và thời gian | Không tra cứu hoặc bỏ qua ngay (có thể ủng hộ B) |
| Consequence tồn tại | Mất mạch bài, bỏ lỡ nội dung hoặc phải học bù | Tra cứu không ảnh hưởng đáng kể đến việc học |
| Pattern có lặp | Tình huống xảy ra nhiều lần trong các buổi học | Chỉ xảy ra một lần và hiếm khi lặp lại |

**Problem Hypothesis mang sang Chặng 2:**

> Khi học viên gặp một thuật ngữ hoặc khái niệm chưa hiểu trong lúc bài giảng đang tiếp diễn, họ có thể không biết chính xác kiến thức nền mình đang thiếu nên phải rời luồng học để tra cứu qua Chat, Google hoặc tài liệu cũ. Việc dò tìm này tốn thời gian, có thể tạo thêm khái niệm cần tìm hiểu và khiến họ bỏ lỡ nội dung tiếp theo.

**Điều gì phải đúng để giả thuyết đứng vững:**

- Học viên thực sự chủ động tra cứu thay vì luôn bỏ qua nội dung chưa hiểu.
- Việc không biết chính xác kiến thức nền cần xem là một nguyên nhân quan trọng làm quá trình tra cứu kéo dài.
- Việc rời luồng học tạo ra hậu quả đủ đáng kể và tình huống lặp lại đủ thường xuyên.

**Điều gì có thể khiến nhóm sửa hoặc bác bỏ giả thuyết:**

- Học viên biết ngay cần xem nội dung gì và luôn tìm được câu trả lời nhanh → A suy yếu.
- Học viên biết rõ cần ôn gì nhưng chỉ thiếu thời gian → C mạnh hơn A.
- Học viên né tránh hoặc bỏ qua vì xấu hổ, nản → B mạnh hơn A.
- Việc tra cứu hầu như không ảnh hưởng đến mạch học → pain chưa đủ lớn để ưu tiên.

**Solution Parking Lot:**

| Hướng giải quyết có thể có | AI / Không dùng AI |
|---|---|
| 1. Gắn sẵn link “khái niệm liên quan” bên cạnh từng phần nội dung bằng mapping tĩnh | Không dùng AI |
| 2. AI xác định kiến thức nền liên quan và giải thích trong ngữ cảnh hiện tại | Dùng AI |
| 3. Cho phép bookmark thuật ngữ hoặc đoạn chưa hiểu để ôn lại sau | Không dùng AI |
| 4. Diễn đàn/nhóm học theo bài để học viên hỏi mà không rời hệ thống | Không dùng AI |
| 5. AI tổng hợp các khái niệm học viên thường gặp khó và chèn phần ôn tập trước nội dung liên quan | Dùng AI |

### 2.7 Evidence sau interview đầu tiên

| Quan sát từ P01 | Ý nghĩa đối với hypothesis |
|---|---|
| Gặp “Data Warehouse” và “Data Lake” khi học triển khai project lên AWS | Situation có thật và đủ cụ thể |
| “Khá là mơ hồ” và “mất phương hướng” khi xác định nền tảng còn thiếu | Ủng hộ A trong phạm vi interview này |
| Sao chép cả đoạn sang Chat; đôi khi dùng Google | Workaround có thật và đang hoạt động |
| Thường hiểu được thuật ngữ sau khi tra cứu | Counter-evidence quan trọng: pain không nằm chủ yếu ở việc không thể tìm ra câu trả lời |
| Mất 5–10 phút hoặc lâu hơn, bỏ lỡ phần giảng tiếp theo và phải học thêm ở nhà | C là yếu tố khuếch đại pain; chi phí chính là thời gian và mất luồng học |
| Tình huống xảy ra hầu như hằng ngày, nhiều lần mỗi buổi nhưng không có con số chính xác | Có tín hiệu lặp lại, cần định lượng thêm |

**Mức độ tin cậy hiện tại:** thấp, vì mới có một người tham gia và một số câu hỏi
trong buổi phỏng vấn có tính dẫn dắt. A có tín hiệu ủng hộ nhưng chưa được xem là
đã xác thực cho toàn bộ học viên. B chưa có evidence trực tiếp; C xuất hiện đồng
thời với A thay vì thay thế hoàn toàn A.

### 2.8 Quyết định PM và bước xác thực tiếp theo

- **Quyết định hiện tại:** tiếp tục validate problem; chưa đủ evidence để ưu tiên
  xây dựng Diagnostic Refresher.
- **Rủi ro cần kiểm tra:** pain có tồn tại trong đúng bối cảnh sản phẩm hay chủ yếu
  chỉ nghiêm trọng khi giảng viên tiếp tục giảng theo thời gian thực.
- **Mẫu tiếp theo:** phỏng vấn thêm 4–6 học viên đúng tiêu chí, ưu tiên cả bài học
  tự học và lớp học trực tiếp để so sánh mức độ mất luồng.
- **Tín hiệu để tiếp tục:** nhiều người độc lập kể được tình huống gần nhất, không
  xác định được kiến thức nền, phải rời luồng học và chịu hậu quả có ý nghĩa.
- **Tín hiệu để sửa hypothesis:** đa số biết chính xác cần tra gì nhưng chỉ thiếu
  thời gian; khi đó C cần được nâng thành pain chính.
- **Tín hiệu để dừng/deprioritize:** tình huống hiếm, workaround hiện tại đủ nhanh
  hoặc không tạo ra hậu quả đáng kể.
- **Chỉ số nên thu thập ở vòng sau:** thời gian tra cứu, số lần rời luồng học,
  khả năng quay lại đúng vị trí, nội dung bị bỏ lỡ và thời gian học bù.

---

## 3. Conversation Guide (phiên bản cuối)

**Tiêu chí tuyển người:**

> Người đã gặp ít nhất một thuật ngữ hoặc khái niệm không hiểu trong lúc nghe
> giảng, xem video hoặc đọc slide trong 15 ngày gần đây; đã chủ động tìm cách xử
> lý và tiếp tục học sau đó.

**Recruitment check:**

1. “Trong 15 ngày vừa qua, có lần nào bạn đang nghe giảng, xem video hoặc đọc
   slide thì gặp một thuật ngữ chuyên ngành khiến bạn không hiểu và phải dừng lại
   không?”
2. “Sau đó bạn có tìm cách xử lý và tiếp tục bài học không?”

Chỉ tiếp tục phỏng vấn khi người tham gia trả lời “có” cho cả hai câu. Nếu không,
cảm ơn và kết thúc sớm vì không đúng tiêu chí tuyển.

**Lời mở đầu:**

> “Cảm ơn bạn đã dành thời gian. Mình đang tìm hiểu trải nghiệm của người học khi
> gặp thuật ngữ hoặc khái niệm chưa hiểu trong lúc học. Buổi trao đổi không có câu
> trả lời đúng hoặc sai; mình chỉ muốn nghe lại những gì thực sự đã xảy ra. Mình
> xin phép ghi âm để ghi chép chính xác hơn, và bản ghi chỉ được sử dụng cho mục
> đích học tập. Bạn có đồng ý không?”

**Story opener:**

> “Hãy kể lại lần gần nhất tình huống đó xảy ra, bắt đầu từ lúc bạn đang học nội
> dung gì và chuyện gì khiến bạn phải dừng lại.”

**Big 3 Questions:**

| Điều cần học | Câu hỏi sẽ dùng |
|---|---|
| 1. Cách người học hiểu nguyên nhân bị kẹt | “Ngay khi nhận ra mình không hiểu, suy nghĩ đầu tiên của bạn là gì?” → “Lúc đó bạn hiểu nguyên nhân mình bị vướng như thế nào?” |
| 2. Workaround và công sức thực tế | “Sau đó bạn đã làm gì? Hãy kể từng bước theo đúng thứ tự lúc đó.” → “Quá trình ấy mất khoảng bao lâu?” |
| 3. Kết quả và hậu quả | “Sau khi xử lý, chuyện gì xảy ra với phần bài học đang diễn ra?” → “Cuối cùng bạn hiểu được nội dung đến mức nào?” |

**Probe bank:**

- “Lúc đó chuyện gì xảy ra tiếp theo?”
- “Vì sao bạn chọn cách đó?”
- “Bạn đã sử dụng nguồn hoặc công cụ nào?”
- “Kết quả đầu tiên có đúng điều bạn cần không?”
- “Bước nào mất nhiều thời gian nhất?”
- “Khi quay lại nội dung chính, chuyện gì xảy ra?”
- “Bạn đã phải dành thêm thời gian cho việc này sau buổi học không?”
- “Lần gần nhất trước đó là khi nào?”
- “Trong 15 ngày qua, tình huống tương tự xảy ra khoảng bao nhiêu lần?”

Các ví dụ như Chat, Google, Wikipedia hoặc slide cũ chỉ được dùng khi người tham
gia trả lời quá chung chung, tránh đưa sẵn phương án ngay từ đầu.

**Ba phản xạ khi data bắt đầu lệch:**

| User đưa ra                         | Phản xạ | Cách quay lại evidence                                     |
| ----------------------------------- | ------- | ---------------------------------------------------------- |
| Lời khen                            | Deflect | Cảm ơn ngắn rồi quay lại việc họ đang làm hiện tại         |
| Câu chung chung / lời hứa tương lai | Anchor  | "Lần gần nhất chuyện đó xảy ra là khi nào?"                |
| Ý tưởng / feature request           | Dig     | "Điều đó giúp bạn làm được gì? Hiện tại bạn xử lý ra sao?" |

**Nguyên tắc điều hành interview:**

- Hỏi hành vi quá khứ trước, không hỏi người tham gia có thích một solution hay
  có dùng trong tương lai không.
- Không gắn nhãn cảm xúc, nguyên nhân hoặc hậu quả thay cho người tham gia.
- Tách câu hỏi kép thành từng câu và chờ trả lời xong trước khi probe.
- Ghi exact quote cho kết luận quan trọng; đánh dấu riêng phần suy luận của nhóm.

---

## 4. Practice Reflection

1. **Câu hỏi nào đã giúp user kể một tình huống cụ thể?**

   Câu hỏi “Bạn có thể kể lại lần gần nhất tình huống đó xảy ra như thế nào
   không?” đã giúp người tham gia kể được tình huống xảy ra ngay buổi sáng: đang
   học triển khai project lên AWS và gặp hai thuật ngữ “Data Warehouse” và “Data
   Lake”.

2. **Chỗ nào mình cần làm tốt hơn ở lần phỏng vấn thật?**

   Cần hạn chế câu hỏi dẫn dắt hoặc xác nhận sẵn kết luận, ví dụ “Ý là bạn tra mỗi
   Chat, hoặc mỗi Google thôi đúng không?” và “Có nghĩa là bạn quay lại và vẫn
   không theo kịp bài giảng tiếp theo đúng không?”. Phiên bản cuối đổi thành câu
   hỏi mở: “Bạn đã sử dụng những nguồn nào?” và “Khi quay lại nội dung chính,
   chuyện gì xảy ra?”.

3. **Sau khi luyện, nhóm đã sửa Conversation Guide ở đâu và vì sao?**

   Nhóm đã bổ sung câu recruitment check thứ hai để xác nhận workaround và việc
   tiếp tục học; đổi story opener để neo vào lần gần nhất; thêm probe về thời
   gian, kết quả, khả năng quay lại bài và tần suất. Ví dụ về công cụ chỉ còn là
   probe dự phòng nhằm giảm dẫn dắt.

---

## 5. AI Support Log

- **AI đã giúp gì:** Hỗ trợ triển khai 6 lớp của Evidence Map (Solution → Change →
  Actor → Situation & Job → Pain → Evidence), xây dựng Conversation Guide, chuẩn
  hoá ghi chép từ transcription và đối chiếu evidence với ba Pain Hypothesis.
- **Điểm cần tự rà soát / có thể sai hoặc hời hợt:**
  - Kết quả mới dựa trên một người tham gia nên chưa thể đại diện cho toàn bộ học viên hoặc xác nhận chắc chắn Hypothesis A.
  - Một số câu hỏi trong buổi phỏng vấn có tính dẫn dắt; cần ưu tiên chi tiết người tham gia tự kể trước khi được đưa ví dụ.
  - Tần suất được mô tả là hằng ngày và nhiều lần mỗi buổi nhưng không có con số chính xác.
  - Pain về sự khác nhau giữa Colab và README chưa có tình huống gần nhất đủ cụ thể nên chưa được dùng làm evidence chính.
- **Cách tự sửa:** Nhóm đã đối chiếu nội dung AI tạo với transcription, giữ exact
  quote cho kết luận quan trọng, tách evidence trực tiếp khỏi suy luận, cập nhật
  Conversation Guide theo hướng trung lập hơn và ghi rõ giới hạn của mẫu phỏng
  vấn. Nhóm sẽ cần thêm interview trước khi khái quát kết quả hoặc quyết định giải
  pháp.
