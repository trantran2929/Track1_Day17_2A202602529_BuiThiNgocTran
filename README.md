# Lab 17 — Problem Interview Practice

## 1. Thông tin cá nhân và nhóm

| Thông tin | Chi tiết |
|-----------|----------|
| **MHV** | 2A202602529 |
| **Họ tên** | Bùi Thị Ngọc Trân |
| **Tên nhóm** | فتيات جميلات |
| **Case đã chọn** | **Case A — AI Tutor: Diagnostic Refresher** |

### Danh sách thành viên nhóm فتيات جميلات

| STT | Họ và tên | Mã sinh viên (MSV/MHV) | Vai trò |
|:---:|-----------|:----------------------:|---------|
| 1 | **Phạm Thành Đạt** | 2A202602721 | Đội trưởng / Product Lead |
| 2 | **Đinh Thị Minh Tâm** | 2A202602433 | Thành viên |
| 3 | **Bùi Thị Ngọc Trân** | 2A202602529 | Thành viên |

---

## 2. Problem Hypothesis Brief (Kết quả Chặng 1)

### 2.1. Solution — Tách solution khỏi hình thức biểu hiện cụ thể

**Case được chọn:** Case A — AI Tutor: Diagnostic Refresher

| Thành phần | Solution đã mô tả |
|-----------|-------------------|
| Trigger | Học viên bấm "Tôi vẫn chưa hiểu" |
| Input | Bài hiện tại, câu trả lời gần đây và lịch sử học tập |
| AI action | Chẩn đoán và lựa chọn khái niệm nền |
| Output | Một phần ôn lại ngắn trước khi quay lại bài hiện tại |
| User control | Học viên chủ động yêu cầu trợ giúp |

**Chỉ thị solution ban đầu:**

> Học viên bấm nút "Tôi vẫn chưa hiểu", hệ thống dùng AI để chẩn đoán điểm hổng kiến thức qua câu trả lời gần đây/lịch sử học tập, chọn khái niệm nền tương ứng, đưa ra một phần ôn lại ngắn trước khi đưa học viên quay lại bài hiện tại.

**Năng lực trung tính tương ứng:**

> Khả năng tự động chẩn đoán lỗ hổng kiến thức của học viên ngay tại thời điểm gặp khó khăn và cung cấp nội dung ôn tập bổ trợ ngắn, đúng trọng tâm để giúp họ tiếp tục bài học.

### 2.2. Change — Chuỗi thay đổi kỳ vọng

```
Giải pháp
  → Học viên nhận biết điểm hổng và hoàn thành phần ôn tập bổ trợ
  → Nắm vững kiến thức nền và tự tin tiếp tục bài học
  → Tác động mong muốn: Tăng tỉ lệ hoàn thành bài học và giảm tỉ lệ bỏ dở
```

Tóm tắt chuỗi thay đổi:

1. Học viên chủ động yêu cầu trợ giúp và hoàn thành phần ôn tập ngắn do hệ thống chẩn đoán.
2. Học viên lấy lại kiến thức nền kịp thời, hiểu bài học hiện tại và giảm cảm giác bế tắc.
3. Tỉ lệ học viên thoát bài học giữa chừng giảm và hiệu quả tiếp thu kiến thức tăng lên.

### 2.3. Actor — Xác định các nhóm người có liên quan

| Actor | Hành vi hiện tại | Vấn đề & Hệ quả tồn tại | Giá trị nhận được |
|-------|-----------------|-------------------------|------------------|
| Học viên | Gặp bài học/câu hỏi khó nhưng không hiểu nguyên nhân gốc rễ; thường cố gắng đoán mò, chuyển sang bài tiếp theo hoặc bỏ dở giữa chừng. | Bị mất gốc kiến thức nền dẫn đến cảm giác bế tắc, giảm động lực học tập và tăng tỉ lệ bỏ học (drop-out). | Được chẩn đoán đúng lỗ hổng kiến thức ngay lập tức, ôn tập bổ trợ đúng trọng tâm mà không cần thoát khỏi luồng bài học. |
| Coach | Phải hỗ trợ thủ công từng học viên bị kẹt kiến thức hoặc phản hồi thắc mắc thụ động qua forum/tin nhắn. | Tốn nhiều thời gian lặp đi lặp lại việc giải thích các khái niệm nền cơ bản cho từng cá nhân. | Giảm tải khối lượng công việc lặp lại, tập trung vào hỗ trợ các trường hợp phức tạp hơn. |
| Instructor / Ban chuyên môn | Thiết kế lộ trình cố định, khó điều chỉnh linh hoạt theo tốc độ tiếp thu của từng học viên. | Thiếu dữ liệu chi tiết về các lỗ hổng kiến thức phổ biến khiến học viên thường xuyên bỏ dở. | Nâng cao tỉ lệ hoàn thành khóa học và có thêm dữ liệu chẩn đoán để cải thiện giáo trình. |

### 2.4. Situation & Job

- Khi đang học các chủ đề nâng cao hoặc làm bài tập tổng hợp và gặp phải khái niệm không hiểu, học viên muốn nhanh chóng xác định đúng lỗ hổng kiến thức nền đang gặp phải để có thể bổ sung ngay lập tức mà không bị ngắt quãng tiến trình học.
- Khi cảm thấy bế tắc với bài học hiện tại, học viên muốn nhận được sự trợ giúp cá nhân hóa đúng lúc để khôi phục sự tự tin và tiếp tục hoàn thành bài học.

### 2.5. Pain

- Không biết bản thân đang hổng kiến thức ở đâu để tự tìm tài liệu ôn tập lại.
- Việc phải quay lại tìm kiếm các bài học cũ tốn nhiều thời gian và làm gián đoạn luồng học tập.
- Cảm giác nản lòng khi cố gắng đọc lại toàn bộ chương cũ chỉ để tìm một khái niệm nhỏ.

### 2.6. Evidence

- Tỉ lệ dừng học hoặc thoát ứng dụng tăng cao tại các bài học có tính tổng hợp hoặc yêu cầu kiến thức nền phức tạp.
- Dữ liệu hệ thống cho thấy học viên thường xuyên làm sai lặp đi lặp lại các câu hỏi liên quan đến cùng một nhóm khái niệm nền.
- Phản hồi từ khảo sát người dùng: *"Tôi không biết mình sai từ đâu"*, *"Tài liệu ôn lại quá dài và không đúng trọng tâm phần tôi quên"*.

### 2.7. Problem Hypothesis

> Học viên thường xuyên bị vướng mắc và bỏ dở bài học khi gặp các khái niệm nâng cao vì họ thiếu khả năng tự chẩn đoán chính xác lỗ hổng kiến thức nền của mình và không có giải pháp ôn tập bổ trợ ngắn gọn, tức thì ngay tại luồng học.

### 2.8. Solution Parking Lot

| # | Hướng giải quyết có thể có | Ghi chú |
|---|---------------------------|---------|
| 1 | Thêm nút "Tôi vẫn chưa hiểu" để AI Tutor đặt 2–3 câu hỏi chẩn đoán, chọn khái niệm nền, tạo giải thích ngắn và đưa học viên trở về bài cũ | Solution chính được chọn |
| 2 | Tự động đề xuất bài kiểm tra chẩn đoán ngắn (Diagnostic quiz) bắt buộc trước khi bước vào mỗi chương mới | |
| 3 | Kết nối tự động tới trợ giảng hoặc nhóm thảo luận học tập khi học viên bấm yêu cầu trợ giúp | Không sử dụng AI |
| 4 | Gợi ý một nhánh lộ trình ôn tập dài hạn riêng biệt ngoài luồng bài học chính nếu phát hiện học viên bị hổng kiến thức quá sâu | |

### CHECKPOINT 1 — Problem Hypothesis ✅

```
Solution: Chẩn đoán lỗ hổng kiến thức và cung cấp ôn tập bổ trợ tức thì
  ↓
Change: Học viên nhận biết điểm hổng → hoàn thành ôn tập → nắm vững kiến thức nền
  ↓
Actor: Học viên (chính), Coach, Instructor/Ban chuyên môn (gián tiếp)
  ↓
Situation & Job: Gặp khái niệm nâng cao không hiểu, muốn xác định lỗ hổng và bổ sung ngay
  ↓
Pain: Không biết hổng ở đâu, mất thời gian tìm bài cũ, nản lòng khi đọc lại toàn bộ
  ↓
Evidence: Drop-out rate tại bài tổng hợp, sai lặp lại cùng nhóm concept, user nói "không biết sai từ đâu"
```

---

## 3. Conversation Guide (Phiên bản cuối — đã sửa sau khi luyện)

### 3.1. Chốt Big 3 (Điều quan trọng nhất cần học & Evidence)

| # | Điều cần học (Big 3) | Evidence cần tìm | Điều khiến nhóm xem lại giả thuyết? |
|---|----------------------|------------------|-------------------------------------|
| 1 | Khó khăn thực tế khi tiếp cận/chuyển ngành sang AI & Kỹ thuật đối với nhân sự non-tech (Marketing/mới ra trường). | Mức độ thiếu hụt kiến thức nền (syntax, thuật toán, DB schema), cảm xúc áp lực, rào cản tư duy giữa góc nhìn người dùng và bản chất kỹ thuật đằng sau. | Người non-tech tự tiếp cận dễ dàng mà không gặp rào cản thuật toán hay tư duy kỹ thuật nào. |
| 2 | Phương pháp tự xử lý & hành vi thực tế khi gặp tài liệu khó hiểu hoặc task gấp từ cấp trên. | Lần gần nhất đọc tài liệu không hiểu / nhận task gấp; hành động cụ thể đã làm (search Google, đọc lại tài liệu, dùng AI Agent tạo checklist, nhắn tin/email chốt yêu cầu, đề xuất giải pháp A/B). | Nhân sự không gặp khó khăn khi đọc tài liệu chuyên ngành, hoặc giải quyết hoàn toàn mà không cần công cụ/hỗ trợ. |
| 3 | Khoảng cách & mức độ ứng dụng kiến thức đào tạo (trường học/khóa học) vào thực tế công việc BA/AI. | Các môn học/kiến thức phát huy tác dụng thực tế (Database, Phân tích yêu cầu, UI/UX); khả năng hiểu code để giao tiếp với Dev; sự khác biệt giữa môi trường tư nhân và nhà nước. | Kiến thức trường lớp hoàn toàn không áp dụng được gì vào thực tế. |

---

### 3.2. Bộ câu hỏi & Quy trình phỏng vấn

#### Tiêu chí tuyển người (Recruitment criteria)
Chúng tôi cần nói chuyện với người đã **tham gia học AI thực chiến hoặc làm vị trí BA (Business Analyst) trong môi trường tư nhân/nhà nước** trong vòng **30–90 ngày** gần đây.

#### Recruitment check (Câu xác nhận)
> *"Gần đây bạn có từng trải qua việc tiếp cận kiến thức AI/công nghệ mới hoặc thực hiện các task phân tích yêu cầu (BA) trong công việc/khóa học không?"*

#### Lời mở đầu
> *"Chào bạn, cảm ơn bạn đã dành thời gian. Hôm nay mình muốn trao đổi nhẹ nhàng để tìm hiểu về trải nghiệm học tập, cách bạn xử lý khó khăn khi gặp kiến thức mới hoặc khi làm task thực tế. Buổi trao đổi hoàn toàn mang tính chất lắng nghe góc nhìn và câu chuyện thực tế từ bạn, không có câu trả lời đúng hay sai."*

#### Story opener (Câu hỏi mở đầu câu chuyện)
> *"Kể mình nghe về lần gần nhất bạn phải học một kiến thức công nghệ/AI hoàn toàn mới hoặc nhận một task công việc mà bạn chưa hiểu rõ đằng sau nó vận hành thế nào?"*

#### Big 3 Questions (Bộ câu hỏi chính)
1. **Câu hỏi 1 (Khó khăn người non-tech):**  
   *"Khi mới bắt đầu tiếp cận các kiến thức kỹ thuật/AI (như LLM, syntax, thuật toán đằng sau), rào cản lớn nhất bạn gặp phải là gì?"*
2. **Câu hỏi 2 (Xử lý bế tắc & tài liệu khó hiểu/task gấp):**  
   *"Lần gần nhất bạn đọc tài liệu chuyên ngành hoặc nhận task gấp từ sếp/lead mà hoàn toàn không hiểu, bạn đã thực hiện từng bước cụ thể nào để giải quyết?"*
3. **Câu hỏi 3 (Độ hiệu quả & ứng dụng thực tế):**  
   *"Trong quá trình đi làm hoặc đi học gần đây, những kiến thức/kỹ năng nào bạn thấy thực sự phát huy tác dụng giúp bạn hoàn thành công việc?"*

#### Probe bank (Ngân hàng câu hỏi đào sâu — chỉ dùng khi cần đào sâu câu chuyện)
- *"Lúc đó chuyện gì xảy ra tiếp theo?"*
- *"Bạn đã làm gì cụ thể? Cho mình xem ví dụ cách bạn nhắn tin/email xác nhận yêu cầu hoặc đặt lệnh cho AI agent?"*
- *"Vì sao bạn chọn cách đó (ví dụ: nhờ AI tạo checklist từng bước, hay chủ động đề xuất giải pháp A/B cho sếp)?"*
- *"Phần nào là khó nhất khi bạn cố gắng hiểu logic đằng sau (code, DB, hay tài liệu nghiệp vụ)?"*
- *"Bạn đã thử cách nào khác chưa (như search Google, tra tài liệu, hỏi đồng nghiệp/BA khác)?"*
- *"Nếu không hiểu mà vẫn phải chốt task gấp thì hậu quả kéo theo là gì?"*

#### Ba phản xạ khi data bắt đầu lệch
| Dữ liệu người dùng đưa ra | Phản xạ | Cách quay lại evidence |
|---------------------------|---------|------------------------|
| **Lời khen** (vd: *"Khóa học này rất hay, tư duy tuyệt vời"*) | **Deflect** | Cảm ơn ngắn gọn và kéo về thực tế: *"Cảm ơn bạn. Cho mình hỏi tuần vừa qua khi thực hành làm task, bước nào cụ thể khiến bạn tốn nhiều thời gian nhất?"* |
| **Câu chung chung / Lời hứa tương lai** (vd: *"Sau này mình sẽ chăm đọc code hơn"*) | **Anchor** | *"Lần gần nhất bạn thực sự ngồi đọc hiểu từng đoạn code/tài liệu kỹ thuật là khi nào? Lúc đó bạn làm như thế nào?"* |
| **Ý tưởng / Feature Request** (vd: *"Nên có tài liệu tóm tắt ngắn hơn"*) | **Dig** | *"Điều đó giúp bạn giải quyết vấn đề gì? Hiện tại khi chưa có tài liệu đó, bạn đang xử lý ra sao?"* |

---

### 3.3. Tự rà soát & Phân công (Checklist)
- [x] **Không lộ solution:** Tất cả các câu hỏi tập trung vào trải nghiệm và hành vi quá khứ, hoàn toàn không nhắc tới tên giải pháp hay tính năng AI cụ thể.
- [x] **Không hỏi dự đoán tương lai:** Neo chặt vào *"lần gần nhất"*, *"tuần qua"*, *"dự án vừa rồi"*, không hỏi *"bạn có muốn/sẽ dùng không"*.
- [x] **Story opener phù hợp:** Đã neo vào lần gần nhất tiếp cận kiến thức mới hoặc nhận task thực tế.
- [x] **Nối khớp Big 3:** 3 câu hỏi chính liên kết trực tiếp với 3 điều cần học rút ra từ các case study.
- [x] **Có câu hỏi thách thức giả thuyết:** Kiểm tra sự thật về rào cản non-tech và tính thực tế của kiến thức học đường.

---

### 3.4. Điểm điều chỉnh của Conversation Guide sau vòng luyện tập
1. **Siết chặt Story Opener:** Bắt buộc neo chặt vào mốc *"lần gần nhất"* để tránh việc người trả lời kể chung chung theo thói quen hoặc lý thuyết.
2. **Bỏ triệt để câu hỏi cảm xúc / ý kiến:** Loại bỏ các câu hỏi dạng *"bạn cảm thấy thế nào về áp lực"* vì người phỏng vấn sẽ trả lời bằng triết lý/quan điểm cá nhân thay vì bằng chứng hành vi (behavioral evidence).
3. **Bổ sung Probe về hậu quả cụ thể (Consequence probe):** Thêm câu hỏi *"Nếu không hiểu mà vẫn phải chốt task gấp thì hậu quả kéo theo là gì?"* nhằm làm rõ chi phí/hậu quả thực tế khi gặp rào cản kiến thức.

---

## 4. Practice Reflection (Chặng 4)

### 4.1. Câu hỏi nào đã giúp user kể một tình huống cụ thể?

Câu Story opener "Kể mình nghe về lần gần nhất bạn phải học một kiến thức công nghệ/AI hoàn toàn mới" đã giúp Linh kể ngay câu chuyện thực tế: bạn ấy có background Marketing, vào khóa AI thực chiến tại VinUni và gặp khó khăn cụ thể với các khái niệm về LLM, syntax và thuật toán. Câu hỏi follow-up "Bạn có thể nêu một khó khăn cụ thể?" cũng hiệu quả — Linh chuyển từ nói chung "khó khăn nhiều lắm" sang mô tả rào cản cụ thể về công nghệ và sự khác biệt tư duy giữa góc nhìn người dùng và kỹ thuật.

### 4.2. Chỗ nào mình cần làm tốt hơn ở lần phỏng vấn thật?

- **Tránh hỏi cảm xúc/ý kiến:** Câu "sau ba tuần học AI thực chiến thì bạn cảm thấy như thế nào?" là câu hỏi ý kiến, không tìm được hành vi. Linh trả lời bằng triết lý cá nhân ("đời người thì cũng phải áp lực một tí") — đây không phải evidence về pain. Lần phỏng vấn thật cần thay bằng: "Tuần vừa rồi bạn có bị vướng ở bước nào cụ thể không? Lúc đó bạn đã làm gì?"
- **Follow-up sâu hơn vào workaround:** Khi Linh nói "bảo con agent tạo checklist để đi qua từng bước", đây là một workaround rất đáng đào sâu nhưng mình đã không hỏi tiếp: "Checklist đó trông như thế nào? Nó giúp bạn đến mức nào? Có lần nào checklist không đủ không?" Cần luyện phản xạ đào sâu khi nghe thấy workaround.
- **Giảm nói, tăng nghe:** Có chỗ mình nói nhiều hơn cần thiết khi đặt câu hỏi (ví dụ: lặp lại câu hỏi bằng nhiều cách diễn đạt cùng lúc). Nên hỏi ngắn gọn và đợi user trả lời.

### 4.3. Sau khi luyện, nhóm đã sửa Conversation Guide ở đâu và vì sao?

1. **Story opener:** Siết chặt hơn bằng "lần gần nhất" — vì trong luyện tập, câu hỏi chung ("bạn có khó khăn gì không") dẫn đến câu trả lời mơ hồ.
2. **Bỏ câu hỏi cảm xúc:** Câu "bạn cảm thấy như thế nào" dẫn đến triết lý cá nhân, không phải evidence. Thay bằng câu neo vào hành vi cụ thể.
3. **Bổ sung probe về consequence:** Sau luyện, nhận ra rằng cần hỏi rõ hơn về hậu quả thực tế (mất bao nhiêu thời gian? phải làm lại chưa? ảnh hưởng kết quả học không?) — vì đây là evidence quan trọng để đánh giá pain có đủ đáng giải hay không.

---

## 5. AI Support Log

### 5.1. Khai báo phạm vi sử dụng AI
Trong bài lab này, nhóm và cá nhân sử dụng công cụ AI (Gemini / Claude) với vai trò **trợ lý phản biện (sparring partner) và hỗ trợ diễn đạt**. Nhóm tuân thủ nghiêm ngặt quy định liêm chính học thuật của bài lab:
- **KHÔNG** sử dụng AI để tạo dữ liệu phỏng vấn giả lập, bịa đặt trích dẫn (quote), hay suy diễn chi tiết mà người được phỏng vấn chưa từng nói.
- **KHÔNG** để AI viết reflection thay cho việc tự nghe lại bản ghi âm và tự nhìn nhận điểm yếu của bản thân khi làm interviewer.

---

### 5.2. Nhật ký chi tiết: AI đã giúp gì, điểm sai/hời hợt và cách tự sửa

| Giai đoạn / Tác vụ | AI đã giúp được gì? | Điểm sai, hời hợt hoặc thiên lệch của AI | Bạn đã tự kiểm tra & sửa lại như thế nào? |
|-------------------|---------------------|------------------------------------------|-------------------------------------------|
| **Chặng 1: Reverse Solution Directive** | • Gợi ý cách diễn đạt directive thành một **năng lực trung tính (neutral capability)** không chứa tên nút hay công nghệ.<br>• Hỗ trợ brainstorm các chuỗi thay đổi kỳ vọng (Change chain). | • **Mắc bẫy solution:** AI ban đầu vẫn giữ tư duy "cần tính năng chẩn đoán thông minh bằng AI" thay vì tập trung vào năng lực giải quyết vấn đề cốt lõi.<br>• Giải thích Pain còn chung chung dạng "học viên thiếu công cụ hỗ trợ". | • Tự loại bỏ hoàn toàn các từ khóa kỹ thuật (AI, nút bấm, chatbot) ra khỏi capability.<br>• Viết lại Pain dưới dạng rào cản nội tại của người học: *không biết mình hổng ở đâu, tốn thời gian tìm bài cũ, nản lòng khi đọc lại toàn bộ*. |
| **Chặng 2: Thiết kế Conversation Guide theo The Mom Test** | • Hỗ trợ gợi ý các tình huống thực tế cho Story Opener.<br>• Đóng góp một số câu hỏi gợi mở trong Probe Bank để đào sâu hành động tiếp theo của user. | • **Vi phạm quy tắc The Mom Test:** AI liên tục đề xuất các câu hỏi khảo sát ý kiến hoặc dự đoán tương lai như: *"Bạn có muốn một công cụ tóm tắt tự động không?"*, *"Bạn thấy khó khăn này có cần giải pháp ngay không?"*<br>• Câu hỏi chưa neo chặt vào mốc thời gian cụ thể trong quá khứ. | • **Loại bỏ toàn bộ** các câu hỏi hỏi ý kiến tương lai và câu hỏi pitch giải pháp.<br>• Bắt buộc thêm cụm từ **"Lần gần nhất..."** vào Story Opener và Big 3.<br>• Xây dựng bảng 3 phản xạ (*Deflect / Anchor / Dig*) để chủ động kéo user về sự việc có thật nếu họ nói lan man. |
| **Chặng 3: Xử lý dữ liệu phỏng vấn & Ghi chép** | • Hỗ trợ rà soát chính tả và định dạng bảng biểu Interview Record chuẩn Markdown. | • **Làm sạch dữ liệu quá mức (Data over-smoothing):** Khi yêu cầu tóm tắt câu trả lời của bạn Linh, AI có xu hướng "chuyên nghiệp hóa" bằng thuật ngữ hàn lâm, làm mất đi văn phong tự nhiên của một cử nhân Marketing.<br>• AI tự ý gộp lẫn giữa lời nói thật của user với kết luận suy diễn của nhóm. | • Tự nghe lại toàn bộ bản ghi âm để bóc tách **nguyên văn exact quote** của Linh (*"bảo con agent tạo checklist để xem kỹ từng bước..."*).<br>• Tách biệt hoàn toàn thành 2 cột: **Facts quan sát được** vs **Diễn giải của nhóm**, kiên quyết không coi lời lạc quan cá nhân của Linh là bằng chứng về pain. |
| **Chặng 4: Đánh giá & Viết Reflection** | • Gợi ý các tiêu chí tự rà soát theo 4 Gate đánh giá của bài Lab. | • **Ngộ nhận "Validated":** AI tự động kết luận rằng *"Giả thuyết của nhóm đã được chứng minh hoàn toàn đúng qua các cuộc phỏng vấn"*, vi phạm nguyên tắc cơ bản của bài lab.<br>• Viết reflection hời hợt, chung chung theo kiểu "interviewer đã làm rất tốt". | • **Bác bỏ kết luận của AI:** Khẳng định rõ đây chỉ là vòng luyện tập kỹ năng trong giờ lab, mẫu nhỏ (1 user/người), **chưa thể tuyên bố validated**.<br>• Tự chỉ ra 3 lỗi sai cụ thể của bản thân: hỏi câu cảm xúc gây triết lý suông, bỏ lỡ cơ hội đào sâu vào workaround checklist, và nói nhiều hơn nghe. |

---

### 5.3. Bài học rút ra về việc sử dụng AI trong Product Research
1. **AI luôn có xu hướng "chiều chuộng" và pitch giải pháp:** Nếu không có tư duy phản biện vững vàng theo *The Mom Test*, người làm sản phẩm rất dễ bị AI dẫn dắt vào các câu hỏi gợi ý sai lầm (hỏi khách hàng xem họ có thích ý tưởng của mình không).
2. **Dữ liệu định tính (Qualitative Data) phải giữ nguyên "chất thô":** Giá trị lớn nhất của phỏng vấn nằm ở ngôn từ đời thường, cảm xúc thật và các workaround kỳ quặc của user (như việc một bạn Marketing dùng AI Agent làm checklist đọc code). Việc để AI "tóm tắt sạch sẽ" sẽ vô tình xóa sạch những insight đắt giá nhất.
3. **AI là trợ lý định dạng, con người là người chịu trách nhiệm về Fact & Insight:** AI giúp tăng tốc độ biên soạn tài liệu, nhưng việc xác định đâu là Fact, đâu là Diễn giải và nhận diện lỗi dẫn dắt bắt buộc phải do chính interviewer tự thực hiện qua việc nghe lại bản ghi âm thực tế.

