# 1 Thông tin thành viên nhóm

| STT | Họ và tên        | Mã học viên |
| --: | ---------------- | ----------- |
|   1 | Trần Hoàng Quân  | 2A202601805 |
|   2 | Trần Thị Hoa Mai | 2A202601317 |
|   3 | Nguyễn Minh Đức  | 2A202601946 |

**Case C — AI Support Radar**
Sau mỗi phiên học, hệ thống phân tích các tín hiệu như di chuyển giữa slide, dừng lâu hoặc xem lại, highlight và ghi chú, đánh dấu “Chưa hiểu”, thay đổi câu trả lời, và nội dung trao đổi với AI Chat.

AI tạo một _Support Queue_ cho giảng viên, gồm:

- Những học viên có thể cần hỗ trợ.
- Phần nội dung mà họ có thể đang gặp khó khăn.
- Các tín hiệu dẫn đến nhận định đó.
- Một hành động hỗ trợ được đề xuất.

Giảng viên xem lại và quyết định có liên hệ với học viên hay không.

# 2. Problem Hypothesis Brief

## 1. Solution - Gỡ solution khỏi hình thức cụ thể

### **Solution directive**

Sau mỗi phiên học, hệ thống phân tích các tín hiệu như:

- Di chuyển giữa slide.
- Dừng lâu hoặc xem lại.
- Highlight và ghi chú.
- Đánh dấu “Chưa hiểu”.
- Thay đổi câu trả lời.
- Nội dung trao đổi với AI Chat.

Sau đó, AI tạo một **Support Queue** cho giảng viên, gồm:

1. Những học viên có thể cần hỗ trợ.
2. Phần nội dung mà họ có thể đang gặp khó khăn.
3. Các tín hiệu dẫn đến nhận định đó.
4. Một hành động hỗ trợ được đề xuất.

Giảng viên xem lại và quyết định có liên hệ với học viên hay không.

### **Capability trung tính**

Giúp giảng viên nhận biết những học viên có khả năng cần hỗ trợ, hiểu họ có thể đang gặp khó khăn ở nội dung nào và dựa trên những dấu hiệu nào, để giảng viên quyết định cách hỗ trợ phù hợp.

## 2. Change - Làm lộ chuỗi thay đổi được kỳ vọng

Các thay đổi được kỳ vọng:

- Giảng viên có thêm thông tin để nhận biết sớm những học viên có khả năng cần hỗ trợ, thay vì chỉ dựa vào việc học viên chủ động hỏi.
- Giảng viên thay đổi hành vi: chủ động kiểm tra các trường hợp được gợi ý và quyết định có liên hệ/hỗ trợ hay không thay vì chỉ bị động chờ được học viên hỏi.
- Học viên có khả năng nhận được hỗ trợ sớm và đúng vào phần đang gặp khó khăn hơn.
- Kết quả kỳ vọng: giảm số trường hợp học viên gặp khó khăn nhưng không được phát hiện hoặc hỗ trợ kịp thời.

## 3. Actor - Xác định các nhóm người có liên quan

| Actor          | Họ đang làm gì?                                       | Pain hoặc hậu quả có thể có                                                     | Họ hưởng lợi thế nào?                                           |
| -------------- | ----------------------------------------------------- | ------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| **Learner**    | Học nội dung, trả lời câu hỏi, tự xử lý khi chưa hiểu | Có thể gặp khó khăn nhưng không chủ động hỏi hoặc không nhận ra mình cần hỗ trợ | Được hỗ trợ đúng lúc, giảm nguy cơ để lỗ hổng kiến thức kéo dài |
| **Instructor** | Theo dõi tiến độ và hỗ trợ nhiều learner              | Khó biết ai thực sự cần chú ý và cần hỗ trợ ở nội dung nào                      | Giảm công sức rà soát và ưu tiên hỗ trợ tốt hơn                 |
| **Coach / TA** | Hỗ trợ learner theo yêu cầu hoặc theo phân công       | Có thể thiếu context trước khi tiếp cận learner                                 | Có context rõ hơn để hỗ trợ đúng vấn đề                         |

### **Actor nhóm chọn để điều tra trước**

Instructor / Coach chịu trách nhiệm theo dõi và hỗ trợ learner.

### **Vì sao chọn nhánh này thay vì actor khác?**

Vì đây là actor:

1. Trực tiếp nhận giá trị từ capability.
2. Phải đưa ra quyết định **“có hỗ trợ hay không?”**.
3. Phải thay đổi hành vi thì outcome mới xảy ra.
4. Nếu actor này không có nhu cầu hoặc không tin tín hiệu, solution gần như mất giá trị.

Learner vẫn cần được interview vì learner là người:

- Trực tiếp trải nghiệm khó khăn học tập.
- Có thể không muốn bị can thiệp chỉ dựa trên tín hiệu hành vi.
- Có thể đã có cách tự xử lý khác.
- Có thể không xem việc instructor chủ động liên hệ là hữu ích.

**Vòng này chỉ có learner-side evidence; instructor-side job chưa được kiểm chứng.**

## 4. Situation & Job — User đang cố làm gì trong tình huống nào?

Tình huống bắt đầu
→ Sau một phiên học hoặc khi cần rà soát tình hình học tập của lớp.

User muốn hoàn thành việc gì
→ Xác định học viên nào đang gặp khó khăn và cần được hỗ trợ trước.

Hiện tại họ làm như thế nào
→ Dựa vào quan sát trên lớp, câu hỏi học viên chủ động đặt ra, kết quả bài tập/quiz, trao đổi trực tiếp hoặc tự kiểm tra tiến độ từng học viên.

Điểm bắt đầu gặp vướng mắc
→ Khi số lượng học viên lớn hoặc học viên không chủ động thể hiện rằng mình đang gặp khó khăn, khiến giảng viên khó biết ai thực sự cần hỗ trợ và đang vướng ở phần nào.

### **Mô tả Situation & Job**

Khi kết thúc một phiên học và cần kiểm tra tình trạng của lớp, giảng viên đang cố xác định những học viên có thể đang gặp khó khăn để ưu tiên hỗ trợ bằng cách quan sát hành vi học tập, xem kết quả bài tập và dựa vào những trao đổi hoặc câu hỏi mà học viên chủ động đưa ra.

### **JTBD Hypothesis**

Khi tôi cần rà soát tình trạng học tập của lớp sau một phiên học, tôi muốn nhanh chóng nhận biết học viên nào có khả năng đang gặp khó khăn và khó khăn ở đâu, để có thể ưu tiên sự chú ý và hỗ trợ đúng người, đúng vấn đề, đúng thời điểm.

## 5. Pain - Viết các cách giải thích cạnh tranh

### Pain Hypothesis A — Thiếu khả năng quan sát

Khi cần rà soát tình hình học tập của lớp sau một phiên học, giảng viên gặp khó khăn trong việc xác định học viên nào đang gặp khó khăn và cần được ưu tiên hỗ trợ vì nhiều dấu hiệu khó khăn không được học viên chủ động thể hiện và giảng viên không thể quan sát đầy đủ từng người, dẫn đến một số học viên cần hỗ trợ có thể bị phát hiện muộn hoặc bị bỏ sót.

**Ý của A là**

Barrier: thiếu thông tin / thiếu visibility
→ Giảng viên muốn hỗ trợ nhưng không biết ai cần hỗ trợ.

### Pain Hypothesis B — Biết nhưng không đủ khả năng xử lý

Khi cần rà soát tình hình học tập của lớp sau một phiên học, giảng viên gặp khó khăn trong việc hỗ trợ kịp thời những học viên đang gặp khó khăn vì thời gian và nguồn lực hỗ trợ có hạn, trong khi có nhiều học viên và nhiều vấn đề cần xử lý, dẫn đến giảng viên phải trì hoãn hoặc bỏ qua một số trường hợp dù đã nhận biết được học viên đang cần hỗ trợ.

Ý của B là:

Barrier: thiếu thời gian / capacity
→ Giảng viên đã biết ai cần hỗ trợ nhưng không đủ khả năng hỗ trợ hết.

### Giả thuyết nhóm chọn để điều tra trước: A

Lý do:

A nên được kiểm chứng trước vì AI Support Radar đang ngầm giả định rằng vấn đề chính là giảng viên thiếu khả năng nhận biết học viên cần hỗ trợ. Nếu thực tế giảng viên đã nhận biết khá tốt nhưng vấn đề nằm ở thiếu thời gian hoặc nguồn lực để can thiệp, việc cung cấp thêm một Support Queue có thể không giải quyết pain, thậm chí còn tạo thêm workload.

Đây cũng chính là giá trị của yêu cầu “cách giải thích cạnh tranh”: không cố chứng minh solution đúng, mà tìm xem nguyên nhân thật sự của hành vi/problem là gì.

## 6. Evidence - Xác định điều cần tìm trước khi viết câu hỏi

| Cần kiểm tra            | Evidence làm nhóm tin hơn                                                                                                           | Evidence làm nhóm nghi ngờ hoặc bác bỏ                                                                                 |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| **Situation có thật**   | Giảng viên kể được một tình huống gần đây sau buổi học mà họ phải rà soát xem học viên nào đang gặp khó khăn                        | Giảng viên hiếm khi hoặc không có nhu cầu rà soát tình trạng từng học viên sau buổi học                                |
| **Pain có ý nghĩa**     | Giảng viên nói họ thường không chắc ai thực sự cần hỗ trợ, phải mất nhiều thời gian kiểm tra hoặc từng bỏ sót học viên              | Giảng viên cho rằng hiện tại họ đã dễ dàng biết ai cần hỗ trợ và việc này không gây nhiều khó khăn                     |
| **Workaround tồn tại**  | Giảng viên đang tự xem quiz, hỏi từng học viên, xem trao đổi, ghi chú riêng hoặc nhờ coach theo dõi để phát hiện người gặp khó khăn | Giảng viên không làm gì thêm vì họ không thấy việc phát hiện học viên gặp khó khăn đủ quan trọng                       |
| **Consequence tồn tại** | Có trường hợp học viên chỉ được phát hiện khi đã tụt tiến độ, làm sai nhiều lần, chủ động cầu cứu hoặc đến kỳ đánh giá              | Không có hậu quả đáng kể khi giảng viên không phát hiện sớm; học viên vẫn tự giải quyết hoặc được hỗ trợ qua kênh khác |
| **Pattern có lặp**      | Giảng viên kể được nhiều trường hợp tương tự ở nhiều buổi học hoặc với nhiều học viên khác nhau                                     | Đây chỉ là sự cố hiếm gặp, xảy ra với một vài trường hợp đặc biệt và không tạo thành pattern                           |

### Problem Hypothesis nhóm mang sang Chặng 2:

Khi cần rà soát tình hình học tập của lớp sau một phiên học, giảng viên gặp khó khăn trong việc xác định học viên nào đang gặp khó khăn và cần được ưu tiên hỗ trợ vì không thể quan sát đầy đủ các dấu hiệu của từng học viên, đặc biệt khi học viên không chủ động thể hiện rằng mình đang gặp vấn đề, dẫn đến một số học viên có thể được phát hiện muộn hoặc bị bỏ sót.

### Điều gì phải đúng để giả thuyết đứng vững

Tình huống này phải thực sự xảy ra và lặp lại; giảng viên phải có nhu cầu nhận biết học viên cần hỗ trợ nhưng hiện tại thiếu đủ tín hiệu hoặc mất đáng kể công sức để làm việc đó; đồng thời việc phát hiện muộn hoặc bỏ sót phải tạo ra hậu quả có ý nghĩa cho giảng viên hoặc học viên.

### Điều gì có thể khiến nhóm sửa hoặc bác bỏ giả thuyết

Nhóm nên sửa hoặc bác bỏ giả thuyết nếu phát hiện rằng giảng viên hiện đã nhận biết khá chính xác học viên nào cần hỗ trợ, hoặc việc bỏ sót hiếm và không tạo hậu quả đáng kể; đặc biệt, nếu barrier thực tế không phải thiếu thông tin mà là thiếu thời gian hoặc nguồn lực để hỗ trợ những học viên mà giảng viên đã biết, thì problem hypothesis cần chuyển sang hướng khác.

# 3. Conversation Guide phiên bản cuối

## 3.1. Tiêu chí tuyển người

### Instructor / Coach

> Chúng tôi cần nói chuyện với instructor hoặc coach đã trực tiếp theo dõi, nhận biết hoặc hỗ trợ learner trong hoặc ngay sau ít nhất một phiên học trong vòng 30 ngày gần đây.

**Recruitment check:**

> “Trong 30 ngày gần đây, có lần nào trong hoặc ngay sau một buổi học bạn phải xác định một learner có đang gặp khó khăn và có cần hỗ trợ thêm hay không?”

Câu này chỉ dùng để xác nhận interviewee thực sự từng trải qua situation, **không được tính là evidence chính**.

### Learner

> Chúng tôi cần nói chuyện với learner đã tham gia một phiên học trong vòng 30 ngày gần đây và từng có ít nhất một thời điểm phải lựa chọn giữa tiếp tục nghe, dừng lại tự tra cứu, hỏi người khác hoặc để vấn đề lại sau..

**Recruitment check:**

> “Trong 30 ngày gần đây, có buổi học nào bạn gặp một phần chưa hiểu và phải quyết định tiếp tục nghe, tự tra cứu, hỏi ai đó hoặc để lại học sau không?”

Nếu có, yêu cầu learner chọn **một lần cụ thể gần nhất** để kể.

### Thành phần phỏng vấn ưu tiên

- 2 learners.
- 1 instructor / coach.

Nếu không có instructor/coach:

> **“Vòng này chỉ có learner-side evidence; instructor-side job chưa được kiểm chứng.”**

---

## 3.2. Lời mở đầu

> “Bọn mình đang tìm hiểu cách mọi người xử lý những tình huống khó hoặc chưa chắc chắn trong quá trình học, cũng như cách việc hỗ trợ diễn ra trong và sau một phiên học. Bọn mình không đánh giá bạn hay cách bạn làm đúng hay sai. Mình chủ yếu muốn nghe về những tình huống thực tế đã xảy ra gần đây, nên nếu được bạn cứ kể càng cụ thể càng tốt.”

### Không nhắc đến

- AI Support Radar.
- Support Queue.
- Dashboard.
- AI phân tích hành vi.
- Tính năng nhóm đang nghĩ tới.

Mục tiêu là giữ interviewee ở **problem space**, không kéo họ sang solution space.

---

## 3.3. Story opener

### Với Instructor / Coach

> **“Kể mình nghe về lần gần nhất trong hoặc ngay sau một buổi học bạn nhận ra một learner có thể đang gặp khó khăn và phải quyết định có nên hỗ trợ thêm hay không?”**

Nếu interviewee trả lời quá chung:

> “Bạn có thể chọn một lần cụ thể gần nhất và kể từ lúc phiên học kết thúc không?”

### Với Learner

> **“Kể mình nghe về lần gần nhất trong một buổi học bạn gặp một phần chưa hiểu hoặc không theo kịp. Ngay lúc đó bạn đã quyết định làm gì?”**

Nếu câu trả lời quá chung:

> “Bạn chọn một lần cụ thể gần nhất nhé. Lúc đó bạn đang học phần nào và chuyện gì xảy ra?”

---

## 3.4. Big 3 Questions

### A. Dành cho Instructor / Coach

| Điều cần học                                                           | Câu hỏi đề xuất                                                                                                                                                       |
| ---------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1. Instructor nhận ra difficulty bằng cách nào và ở thời điểm nào?** | **“Trong lần đó, bạn nhận ra learner đang gặp khó khăn ở thời điểm nào? Bạn đã thấy hoặc nghe được điều gì khiến bạn nghĩ như vậy?”**                                 |
| **2. Phát hiện hoặc hỗ trợ muộn có consequence gì?**                   | **“Từ lúc learner bắt đầu gặp khó khăn đến lúc bạn nhận ra hoặc hỗ trợ, chuyện gì đã xảy ra với việc học của learner?”**                                              |
| **3. Visibility, capacity hay judgment mới là bottleneck?**            | **“Khi đã biết learner có thể đang gặp khó khăn, bạn đã quyết định hỗ trợ ngay, để learner tự xử lý hay đợi thêm như thế nào? Điều gì ảnh hưởng đến quyết định đó?”** |

### B. Dành cho Learner

| Điều cần học                                                    | Câu hỏi đề xuất                                                                                                                                       |
| --------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1. Learner đã ra quyết định như thế nào khi gặp difficulty?** | **“Ngay khi nhận ra mình chưa hiểu, bạn đã làm gì tiếp theo? Bạn đã cân nhắc tiếp tục nghe, tự tra cứu, hỏi người khác hay để lại sau như thế nào?”** |
| **2. Difficulty và workaround gây consequence gì?**             | **“Từ lúc bạn bắt đầu bị vướng đến lúc vấn đề được giải quyết, chuyện gì xảy ra với phần bài giảng và việc học tiếp theo của bạn?”**                  |
| **3. Difficulty nào cần support và difficulty nào không cần?**  | **“Kể mình nghe một lần bạn tự giải quyết được rất nhanh. Lần đó khác gì với lần bạn vừa kể?”**                                                       |

---

## 3.5. Probe bank — chỉ dùng khi cần đào sâu câu chuyện

- “Lúc đó chuyện gì xảy ra tiếp theo?”
- “Bạn đã làm gì?”
- “Vì sao bạn chọn cách đó?”
- “Phần nào khó nhất?”
- “Bạn đã thử cách nào khác chưa?”
- “Việc đó kéo theo hậu quả gì?”
- “Lần gần nhất trước đó là khi nào?”
- “Ngay lúc đó bạn có những lựa chọn nào?”
- “Vì sao bạn không hỏi ngay?”
- “Bạn quyết định tiếp tục nghe hay dừng lại tra cứu?”
- “Đến thời điểm nào bạn nhận ra mình không thể tự giải quyết nhanh được?”

### Probe bổ sung nếu cần

- “Bạn đã xem thông tin ở đâu?”
- “Bạn mất khoảng bao lâu?”
- “Có ai khác tham gia không?”
- “Bạn có phải ghi chú hoặc dùng workaround nào để nhớ không?”
- “Có trường hợp nào bạn nghĩ là ổn nhưng sau đó mới biết là không ổn không?”
- “Trong tháng vừa rồi chuyện tương tự xảy ra khoảng bao nhiêu lần?”

---

## 3.6. Ba phản xạ khi data bắt đầu lệch

| User đưa ra                                | Phản xạ     | Cách quay lại evidence                                                                 |
| ------------------------------------------ | ----------- | -------------------------------------------------------------------------------------- |
| **Lời khen**                               | **Deflect** | Cảm ơn ngắn rồi quay lại việc họ thực sự đã làm                                        |
| **Câu chung chung hoặc lời hứa tương lai** | **Anchor**  | “Lần gần nhất chuyện đó thực sự xảy ra là khi nào?”                                    |
| **Ý tưởng hoặc feature request**           | **Dig**     | “Điều đó giúp bạn làm được gì? Lần gần nhất bạn cần làm việc đó thì bạn xử lý ra sao?” |

### Ví dụ

**User:** “Nếu có hệ thống tự báo learner nào yếu thì hay.”

**Phản xạ:**

> “Cảm ơn bạn. Quay lại lần gần nhất nhé — lúc đó bạn đã phát hiện learner cần hỗ trợ bằng cách nào?”

---

**User:** “Thường thì learner không nói khi họ không hiểu.”

**Phản xạ:**

> “Bạn nhớ lần gần nhất chuyện đó xảy ra với một learner cụ thể là khi nào không? Bạn phát hiện bằng cách nào?”

---

**User:** “Có lẽ nên có notification cho instructor.”

**Phản xạ:**

> “Notification đó sẽ giúp bạn làm được việc gì? Lần gần nhất bạn cần làm việc đó thì bạn xử lý thế nào?”

---

## 3.7. Những câu không nên hỏi

Không hỏi:

- “Bạn có thích AI Support Radar không?”
- “Bạn có thấy Support Queue hữu ích không?”
- “Nếu có hệ thống tự phát hiện learner gặp khó khăn thì bạn có dùng không?”
- “Bạn có cần AI phân tích hành vi học tập không?”
- “Có phải instructor thường bỏ sót learner không?”
- “Bạn thấy phải xem nhiều nguồn rất mất thời gian đúng không?”

Các câu này:

- Làm lộ solution.
- Dẫn dắt interviewee.
- Tạo hypothetical data.
- Khiến nhóm dễ rơi vào confirmation bias.

---

# 4. Practice Reflection

## 1. Câu hỏi nào đã giúp user kể một tình huống cụ thể?

Câu hỏi “Kể mình nghe về lần gần nhất bạn gặp một phần khó hoặc chưa chắc trong lúc học mà bạn không giải quyết được ngay?” giúp learner chọn một sự kiện thật thay vì trả lời chung chung. Các câu hỏi tiếp theo như “Lúc đó bạn đang cố làm gì?” và “Sau khi nhận ra mình bị mắc, bạn đã làm gì?” giúp làm rõ trình tự hành động, chẳng hạn learner muốn hỏi giảng viên nhưng ngại hỏi, sau đó chuyển sang tra Google và ChatGPT.

## 2. Chỗ nào mình cần làm tốt hơn ở lần phỏng vấn thật?

Mình cần hạn chế diễn giải thay hoặc dẫn dắt interviewee bằng những câu như “Đương nhiên giảng viên giải thích sẽ dễ hiểu hơn đúng không?”. Thay vào đó, nên hỏi từng câu ngắn, trung tính và đào sâu sự kiện theo trình tự: vấn đề bắt đầu khi nào, learner đã làm gì, mất bao lâu, bỏ lỡ nội dung nào và cuối cùng vấn đề có được giải quyết hay không. Ngoài ra, cần hỏi rõ hơn sự khác nhau giữa một difficulty learner tự xử lý nhanh và một difficulty thực sự cần người hỗ trợ.

## 3. Sau khi luyện, nhóm đã sửa Conversation Guide ở đâu và vì sao?

Nhóm đã mở rộng phạm vi từ “sau phiên học” thành “trong hoặc ngay sau phiên học”, vì các learner chủ yếu gặp pain ngay khi bài giảng vẫn đang tiếp tục. Nhóm cũng bổ sung câu hỏi về quyết định của learner — tiếp tục nghe, tự tra cứu, hỏi người khác hay để lại sau — và thêm các probe về mất flow, bỏ lỡ kiến thức, thời gian học lại.

# 5. AI Support Log

Trong toàn bộ quá trình, AI đã hỗ trợ nhóm chuyển AI Support Radar từ một solution cụ thể thành một capability trung tính, làm rõ chuỗi thay đổi kỳ vọng từ solution đến outcome và xác định ba actor liên quan gồm learner, instructor và coach. AI cũng hỗ trợ nhóm xây dựng các giả thuyết về Situation & Job, Pain và Evidence; phân biệt output do nhóm tạo ra với outcome mà solution chỉ có thể ảnh hưởng; đồng thời đề xuất nhiều hướng giải quyết trong Solution Parking Lot, bao gồm cả các hướng không sử dụng AI.

Ở giai đoạn chuẩn bị phỏng vấn, AI giúp nhóm xây dựng và rút gọn kịch bản phỏng vấn learner, giải thích sự khác nhau giữa câu chuyện gần nhất, hành động thực tế, khó khăn, workaround, hậu quả và evidence trái giả thuyết. Sau ba cuộc phỏng vấn, AI hỗ trợ bóc tách dữ liệu thành các phần: learner đang làm gì, họ thực sự đã hành động thế nào, khó khăn và workaround đã dùng, chi phí hoặc hậu quả, cùng các câu nói nguyên văn đáng chú ý. AI cũng giúp nhóm nhận ra một số pattern như learner thường tự tra cứu bằng Google, ChatGPT hoặc học lại ở nhà; việc này đôi khi giúp giải quyết vấn đề nhưng có thể làm mất flow, bỏ lỡ nội dung tiếp theo và tốn thêm thời gian.

AI tiếp tục bổ sung câu hỏi về cách learner quyết định tiếp tục nghe, tự tra cứu, hỏi người khác hoặc để lại sau, đồng thời đào sâu consequence thực tế của việc không được hỗ trợ kịp thời.

Tuy nhiên, một số phản hồi của AI còn dài, có lúc diễn giải thay cho interviewee hoặc đưa ra kết luận mạnh hơn evidence hiện có. AI cũng từng đề xuất thêm phần support threshold, trong khi nhóm không muốn đưa nội dung này vào phiên bản cuối. Nhóm đã tự rà soát, loại bỏ phần đó, rút gọn các câu hỏi và chỉ giữ những điều chỉnh được ba cuộc phỏng vấn hỗ trợ trực tiếp. Nhóm cũng chỉnh lại cách ghi kết quả để tách rõ dữ liệu người dùng thực sự kể với phần phân tích hoặc suy luận của nhóm.
