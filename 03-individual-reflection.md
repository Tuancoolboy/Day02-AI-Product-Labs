# 03 — Individual Reflection

## Bối cảnh cá nhân

Ở phần cá nhân, tôi chọn case **AI Lab Submission**: Nam, một học viên AI Product Labs, phải đọc worksheet dài, làm bài lab, phối hợp nhóm, chạy demo/code và nộp repo đúng deadline. Từ case này tôi scan các pain trong workflow học lab và chọn top 3 problem:

1. Kiểm tra bài nộp lab còn thiếu phần nào.
2. Setup môi trường lab AI bị lỗi.
3. Tìm lại câu trả lời cũ trong nhóm chat.

Ở phần nhóm, các candidate được gom từ 3 hướng: AI Application/Lab workflow, AI Daily for Life và RAG/AI Reliability. Sau khi score, nhóm chọn **Automated RAG Evaluation** vì workflow rõ, có metric tốt và sát với mục tiêu học sâu GenAI/RAG.

## Tôi đã tham gia vào phần nào?

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng |
|---|---|---|
| Scan cá nhân | Scan 12 problem từ workflow học lab của Nam | Có đủ candidate cụ thể, không bắt đầu bằng "làm chatbot" |
| Pitch Problem Card | Pitch bài "Kiểm tra bài nộp lab còn thiếu phần nào" | Nhóm hiểu được pain về đọc worksheet dài và nộp thiếu yêu cầu |
| Challenge bài của bạn khác | Hỏi lại các bài có metric đo được không và có đang nhảy sang Agent quá sớm không | Nhóm giữ được hướng problem-first, không chọn solution quá rộng |
| Gom trùng / cluster | Góp phần gom 9 candidates vào 3 cụm: AI Application, AI Daily for Life, RAG/AI Reliability | Nhóm nhìn rõ pattern chung thay vì so từng idea rời rạc |
| Chọn candidate problem | Đồng ý chọn Automated RAG Evaluation | Nhóm chọn bài có workflow, metric và domain fit tốt nhất |
| Validation / research | Góp ý cần validate bằng người đã từng test RAG thủ công và research tool như Ragas/LangSmith/Phoenix | Problem được thu hẹp thành "evaluation lặp lại cho RAG prototype nhỏ" |
| Workflow nhóm | Thảo luận current/future workflow cho Automated RAG Evaluation | Workflow thể hiện rõ bottleneck ở bước đọc answer/citation/chunks thủ công |
| Problem Statement | Góp ý actor, bottleneck, success metric và boundary | Problem Statement rõ hơn: AI không tự quyết kiến trúc RAG, developer vẫn review |
| Rule / Workflow / Agent | Lập luận chọn Workflow thay vì Agent | Giảm rủi ro vòng lặp, chi phí và tự động hóa quá mức |
| Decision | Đồng ý Go với scope nhỏ | Pilot có thể làm bằng 10-20 golden questions và 2 config RAG |

## Bảng dùng AI trong reflection

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai/hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| Scan | Gợi ý thêm problem theo 4 lăng kính | Giúp mở rộng từ một pain sang nhiều workflow khác nhau | Một số ý quá chung kiểu trợ lý AI toàn năng | Giữ lại các problem có actor, workflow và dấu hiệu thật |
| Problem Card | Nhờ AI phản biện actor, bottleneck, metric | Giúp phát hiện chỗ metric còn mơ hồ | AI dễ đề xuất solution quá sớm | Viết lại problem theo hướng kiểm bài nộp, setup lỗi và tìm câu trả lời cũ |
| Workflow | Dùng AI để diễn đạt before/after workflow gọn hơn | Giúp tách bước hiện tại và bước tương lai rõ ràng | AI đôi khi gộp nhiều bước làm một | Tách lại bottleneck và human boundary |
| Research | Dùng AI/search để gợi ý tool evaluation RAG | Tìm được các hướng như Ragas, LangSmith, Phoenix | Có claim cần kiểm nguồn | Chỉ giữ link/tool có nguồn rõ và ghi rủi ro LLM-as-judge |
| Problem Statement | Nhờ AI kiểm 6 field có đủ chưa | Giúp nhắc boundary và success metric | AI hay viết rộng thành "đánh giá AI nói chung" | Thu hẹp thành Automated RAG Evaluation cho prototype nhỏ |
| Rule / Workflow / Agent | Hỏi AI để so sánh Rule, Workflow, Agent | Giúp nhìn thấy Agent chưa cần thiết | AI có xu hướng đề xuất agent tự tối ưu | Chọn Workflow vì bước rõ và cần developer review |
| Decision | Dùng AI để kiểm pilot nhỏ nhất có hợp lý không | Giúp nghĩ thêm rollback/exit criteria | Một số pilot quá tham | Giữ scope nhỏ: 10-20 câu hỏi, 2 config, bảng eval |

## Reflection câu hỏi mở

### Tôi học được gì khi nghe top 3 problems của các bạn khác?

Tôi thấy cùng một bài lab có thể nhìn từ nhiều lăng kính rất khác nhau. AI Lab Submission gần với trải nghiệm học tập, AI Daily for Life gần với quyết định cá nhân hằng ngày, còn Automated RAG Evaluation đi sâu vào engineering workflow. Khi nghe các bài khác, tôi nhận ra problem tốt không nhất thiết là problem nghe "AI" nhất, mà là problem có actor rõ, workflow vẽ được và có metric để kiểm tra.

### Nhóm có lúc nào bị solution-first không?

Có. Khi nói về RAG, rất dễ nhảy thẳng sang agent tự test, tự debug, tự tối ưu pipeline. Sau khi challenge lại, nhóm hạ xuống Workflow: batch eval, lưu kết quả, AI hỗ trợ phân loại lỗi, developer review. Cách này thực tế hơn và ít rủi ro hơn.

### Tôi có thay đổi ý kiến sau khi bị challenge không?

Có. Ban đầu tôi nghĩ AI Lab Submission là bài nên chọn vì gần với lab nhất và dễ làm. Sau khi so score, tôi thấy Automated RAG Evaluation có impact tốt hơn với mục tiêu học GenAI/RAG chuyên sâu, metric rõ hơn và thể hiện được tư duy kỹ thuật mạnh hơn.

### Tôi đóng góp gì thật sự vào artifact cuối?

Tôi đóng góp phần scan cá nhân, top 3 Problem Cards, workflow trước/sau cho AI Lab Submission và góc nhìn boundary khi dùng AI. Trong bài nhóm, tôi đóng góp vào cluster 9 candidates, so sánh Rule/Workflow/Agent và nhấn mạnh cần human review trong Automated RAG Evaluation.

### Điều khó nhất khi viết Problem Statement là gì?

Khó nhất là không viết quá rộng. Nếu nói "đánh giá RAG tốt hơn" thì quá chung. Khi tách ra actor, workflow, bottleneck, impact, metric và boundary, problem rõ hơn nhiều: Khánh mất 1-2 giờ mỗi vòng để đọc answer/citation/chunks thủ công và khó so sánh các cấu hình RAG.

### Nếu làm lại, tôi sẽ challenge nhóm mạnh hơn ở điểm nào?

Tôi sẽ challenge mạnh hơn ở phần evidence và metric. Ví dụ cần hỏi rõ baseline 120 phút/vòng đến từ đâu, golden questions lấy từ nguồn nào, và tiêu chí "answer quality" sẽ được chấm bằng rubric gì để tránh chấm cảm tính.

## Reflection tổng kết

```text
Qua bài này, tôi học được cách đi từ một case thật sang nhiều candidate problems, rồi hội tụ về một problem có workflow và metric rõ. Với AI Lab Submission, tôi thấy AI hữu ích khi hỗ trợ kiểm checklist, debug setup và truy xuất câu trả lời cũ, nhưng vẫn cần người học tự kiểm trước khi nộp.

Ở phần nhóm, Automated RAG Evaluation cho tôi thấy một điểm quan trọng: AI không chỉ dùng để tạo câu trả lời, mà còn có thể hỗ trợ chính quá trình đánh giá hệ thống AI. Tuy nhiên, nếu để AI tự chấm và tự quyết hết thì rủi ro cao. Hướng hợp lý là Workflow: tạo eval set, chạy batch, lưu kết quả, AI phân loại lỗi, rồi developer review.

Nếu làm lại, tôi sẽ chuẩn bị evidence tốt hơn trước khi pitch: đo thử thời gian kiểm bài nộp, thời gian setup lỗi, và số lần phải tìm lại câu trả lời cũ. Tôi cũng sẽ chuẩn bị một rubric nhỏ cho RAG evaluation để nhóm có metric chắc hơn khi quyết định Go.
```

## Tự kiểm cuối bài

- [x] Cá nhân có 5+ problems và top 3 Problem Cards.
- [x] Tôi đã pitch rõ và challenge nhóm đúng trọng tâm.
- [x] Nhóm có nhật ký hội tụ từ candidates về 1 bài.
- [x] Nhóm có workflow trước/sau.
- [x] Nhóm có Problem Statement v0/v1 với metric và boundary rõ.
- [x] Nhóm có so sánh No AI / Rule / Workflow / Agent.
- [x] Nhóm có Go / Not Yet / No-Go và lý do rõ.
- [x] Reflection cá nhân có nói rõ vai trò trong nhóm, cách dùng AI, điều học được và nếu làm lại sẽ đổi gì.
- [x] Tôi tự giải thích được mạch problem → workflow → metric → boundary → độ phù hợp với AI.
