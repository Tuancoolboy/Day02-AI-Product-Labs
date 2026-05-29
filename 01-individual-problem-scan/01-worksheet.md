# Ví dụ bản nộp — Kiểm tra bài nộp lab trước và sau AI

> Bản này làm theo cấu trúc của `02-deliverable-example.md`, nhưng đổi nội dung sang case học viên AI trong khóa học. Mục tiêu là học cách đi từ problem scan → workflow → top 3 Problem Cards → chọn candidate đáng pitch.

Case ví dụ: **Học viên AI làm lab trong khóa học**

Nhân vật ví dụ: Nam, học viên đang tham gia khóa AI Product Labs. Nam có nền tảng lập trình cơ bản, mới bắt đầu học cách xác định problem, vẽ workflow, dùng AI đúng chỗ và làm các bài lab kỹ thuật. Mỗi buổi học Nam phải đọc worksheet dài, làm bài cá nhân, phối hợp nhóm, chạy code/demo, nhận feedback và nộp repo đúng deadline.

## Vì sao đây là ví dụ tốt?

- Có actor cụ thể.
- Có workflow lặp lại qua nhiều buổi lab.
- Có bottleneck rõ: đọc worksheet, setup môi trường, debug lỗi, tìm lại câu trả lời cũ, kiểm tra bài nộp.
- Có metric thời gian.
- Có thể so sánh Rule / Workflow / Agent.
- Có thể vẽ before/after workflow.

---

# 01 — Individual Problem Scan

## Scan rộng

Nam scan 12 problems, vượt mức tối thiểu 5.

| # | Lăng kính | Problem quan sát được | Ai đang đau? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | AI có thể tốt hơn | Không biết bài nộp lab còn thiếu phần nào sau khi đọc worksheet dài | Nam và học viên đang làm lab | Phải đọc lại yêu cầu nhiều lần, dễ bỏ sót file cần nộp, workflow hoặc field trong Problem Card |
| 2 | Tốn thời gian | Đọc worksheet/tài liệu AI dài mất thời gian và khó lọc ra việc cần làm ngay | Nam | Mất 30-45 phút để đọc, highlight và tự tách checklist trước khi bắt đầu làm |
| 3 | Lặp lại | Quên deadline bài cá nhân hoặc deadline nhóm | Nam / nhóm học | Gần cuối buổi mới hỏi lại deadline, có lúc nộp sát giờ hoặc thiếu cập nhật cho nhóm |
| 4 | Tốn thời gian | Setup môi trường lab AI bị lỗi và mất nhiều thời gian tự sửa | Nam khi chạy notebook/project mẫu | Gặp lỗi dependency, sai version Python/package, thiếu API key; phải search nhiều nguồn hoặc hỏi bạn |
| 5 | Pain từ người khác | Tổng hợp ý kiến nhóm sau discussion bị rối, khó chốt một candidate problem | Thành viên nhóm / nhóm trưởng | Ý kiến nằm rải rác trong chat, notes và miệng; sau thảo luận vẫn không rõ nhóm chọn gì |
| 6 | Tốn thời gian | Tìm lại câu trả lời cũ trong Discord/Zalo/nhóm chat mất thời gian | Nam và học viên khác | Câu hỏi đã được trả lời nhưng phải kéo chat hoặc search nhiều keyword mới thấy |
| 7 | Lặp lại | Điền thông tin repo, link bài nộp, form khảo sát nhiều lần dễ sai sót | Nam / người tham gia khóa học | Phải nhập lại cùng thông tin ở nhiều form, dễ sai link GitHub, mã học viên hoặc tên file |
| 8 | Pain từ người khác | Phân công task nhóm không rõ ai làm workflow, ai research, ai viết Problem Statement | Thành viên nhóm | Có việc bị trùng người làm, có việc không ai nhận, đến gần deadline mới phát hiện |
| 9 | AI có thể tốt hơn | Không biết lỗi trong bài code/lab đến từ dữ liệu, logic, prompt hay cách chạy lệnh | Nam khi làm lab kỹ thuật | Khi chương trình lỗi, phải đọc log dài và thử nhiều cách sửa nhưng không biết nguyên nhân chính |
| 10 | Pain từ người khác | Nhận feedback từ mentor/bạn học nhưng không biết nên sửa phần nào trước | Nam sau khi được review | Feedback có nhiều ý rời rạc, khó ưu tiên lỗi ảnh hưởng điểm hoặc ảnh hưởng logic bài làm |
| 11 | Lặp lại | Theo dõi tiến độ cá nhân trong khóa học khó | Nam | Không biết mình đã xong phase nào, còn thiếu bài nào, hoặc cần làm tiếp bước gì để hoàn thành repo |
| 12 | AI có thể tốt hơn | Không biết ưu tiên làm phần nào trước khi vừa có bài cá nhân, vừa có việc nhóm | Nam | Dễ làm phần ít quan trọng trước, còn phần cần nộp hoặc cần share với nhóm thì xử lý sát giờ |

Vì sao phần scan này mạnh:

- Có scan rộng trước khi hội tụ.
- Có nhiều lăng kính khác nhau.
- Mỗi problem có actor và dấu hiệu thật.
- Không bắt đầu bằng "làm chatbot" hoặc "xây agent".
- Các problem đều đi ra từ workflow học lab thật của Nam.

## Top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Kiểm tra bài nộp lab còn thiếu phần nào | Sát với case Nam, actor rõ, workflow dễ vẽ, có thể đo bằng thời gian kiểm tra bài nộp và số mục bị thiếu | Cần biết worksheet có đủ cấu trúc để chuyển thành checklist đáng tin hay không |
| 2 | Setup môi trường lab AI bị lỗi | Thực tế với lab kỹ thuật, workflow rõ từ đọc hướng dẫn → chạy thử → đọc log → sửa lỗi; impact lớn vì chặn Nam bắt đầu phần chính | Cần biết lỗi thường gặp có lặp lại ở nhiều học viên hay chỉ là lỗi cá nhân |
| 3 | Tìm lại câu trả lời cũ trong nhóm chat | Nhiều học viên cùng đau, có dấu hiệu lặp lại, rất hợp với bài toán truy xuất thông tin có ngữ cảnh | Cần kiểm tra quyền truy cập dữ liệu chat và cách tránh trả lời sai/thiếu nguồn |

## Problem Card #1 — Kiểm tra bài nộp lab còn thiếu phần nào

**Problem 1 câu:**  
Nam không biết bài nộp lab còn thiếu phần nào sau khi đọc worksheet dài, dẫn đến phải kiểm tra lại nhiều lần và vẫn dễ bỏ sót.

**Actor:**  
Nam, học viên đang tham gia khóa AI Product Labs.

**Thời điểm / bối cảnh:**  
Sau khi Nam đọc worksheet, làm bài cá nhân/nhóm và chuẩn bị kiểm tra repo trước khi nộp.

**Current workflow:**

```text
1. Mở file yêu cầu lab hoặc worksheet
2. Đọc nhiều phần hướng dẫn: output cuối, checklist, phase, rubric
3. Tự ghi nhớ những mục cần làm và cần nộp
4. Làm bài theo hiểu biết của mình trong repo
5. Đối chiếu lại bài làm với worksheet trước khi nộp
6. Sửa các phần phát hiện còn thiếu
```

**Bottleneck:**  
Bước 5 — đối chiếu yêu cầu với bài làm mất khoảng 20-30 phút/lần và vẫn dễ sót field hoặc file cần nộp.

**Impact:**  
Nam có thể nộp thiếu phần, mất thời gian sửa lại sau feedback, hoặc bị trừ điểm vì bài không đáp ứng đủ yêu cầu.

**Success metric:**  
Giảm thời gian kiểm tra bài nộp từ khoảng 30 phút xuống dưới 10 phút và giảm số mục bị thiếu trong bài.

**Non-AI alternative:**  
Checklist cố định theo từng lab và template repo rõ hơn.

**AI hypothesis:**  
AI đọc worksheet, tạo checklist các mục cần nộp và hỗ trợ Nam đối chiếu bài làm để chỉ ra phần còn thiếu. Nam vẫn quyết định sửa gì trước khi nộp.

**Quick gut:**  
Workflow.

### Draft current workflow

```text
CURRENT STATE — 30 phút

[1 Đọc lại worksheet: 10']
→ [2 Tự tách checklist: 7']
→ [3 Mở repo đối chiếu từng mục: 10']  <-- bottleneck
→ [4 Sửa phần thiếu: 3']
```

### Draft future workflow

```text
FUTURE STATE — 10 phút

[1 AI tạo checklist từ worksheet: 2']
→ [2 Nam dán/link phần bài làm cần kiểm: 2']
→ [3 AI gợi ý mục còn thiếu + vị trí cần sửa: 1']
→ [4 Nam tự kiểm và sửa trước khi nộp: 5']  <-- human boundary

Fallback: AI đọc sai yêu cầu → Nam quay lại checklist gốc trong worksheet.
```

## Problem Cards #2 và #3 — tóm tắt

| Card | Actor | Bottleneck | Metric | Quick gut | Vì sao chưa chọn làm #1 |
|---|---|---|---|---|---|
| Setup môi trường lab AI bị lỗi | Nam, học viên chạy notebook/project mẫu | Đọc log và xác định nguyên nhân chính của lỗi | 60 phút → dưới 20 phút | Workflow | Impact lớn nhưng phụ thuộc lỗi có lặp lại ở nhiều học viên không |
| Tìm lại câu trả lời cũ trong nhóm chat | Nam và học viên trong khóa AI | Search keyword rồi đọc nhiều thread để tìm đúng câu trả lời | 15 phút → dưới 3 phút | Workflow / RAG Workflow | Data access và kiểm chứng nguồn phức tạp hơn |

---
