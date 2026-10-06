# AI Support Log — Day 20

**Công cụ:** Claude (Opus 5.5) trong Claude Code (VS Code) · **Người dùng:** Hà Thị Mỹ Linh (2A202602619)
**Input mình đưa cho AI:** brief Day 20 (từng phase + quy tắc dùng AI), mô tả dự án team build phase, repo dự án `P-110` (PRD, Discovery Findings, User Stories, menu contract, models).

## AI đã giúp tôi ở đâu?

- Đọc repo `P-110` và tóm tắt dữ kiện: user chính là người chăm sóc (89% trực tiếp nấu), luồng thực đơn tuần + chuyên gia duyệt, nhật ký bữa ăn chưa nối với thực đơn, chưa có điều chỉnh thực đơn theo nhật ký.
- Brainstorm ứng viên core action và câu hỏi phản biện; đưa phương án cho từng quyết định ở Phase 1–5 kèm câu coach có thể vặn, để mình chọn.
- Gợi ý tên event (`planned_meal_logged`, `menu_plan_generated`, `menu_plan_reviewed`, `shopping_list_created`) và tiêu chí nghiệm thu mẫu.
- Ghép các lựa chọn của mình thành câu theo template (Core Action Card, kết luận cadence, metric hypothesis) và dựng trang HTML Metrics Pack.
- Rà bài theo 7 câu tự soi ở Phase 5.

## AI sai, hời hợt hoặc đề xuất metric sai nature ở đâu?

- Đề xuất làm cho dự án VLearn AI Notes (Day 17–19) thay vì dự án team build phase.
- Trước khi mình gửi quy tắc dùng AI, AI **tự viết trọn Metrics Pack** (chọn core action, cadence, NSM, retention, metric hypothesis): vi phạm quy tắc. Bản đó dùng persona **bệnh nhân**, lệch dữ liệu khảo sát của team, và đặt nhiều con số không có nguồn (≥ 4/7 ngày, ≥ 40%, ≤ 30 giây, > 3 cảnh báo/ngày). Đã gỡ toàn bộ.
- Ở Phase 5, AI **tự viết 3 dòng rationale** cho phần revision: vi phạm quy tắc "không viết thay rationale". Đã gỡ, để mình tự viết.
- Bản nháp metric ban đầu có 2 chỗ không có event để tính: "thực đơn bị sửa nhiều" không định lượng, và "vượt ngưỡng ngày" chưa biết được lúc event bắn.

## Tôi đã tự sửa hoặc quyết định lại điều gì?

- Gỡ toàn bộ bản Metrics Pack do AI tự viết, tự làm lại từng phase: mọi quyết định lõi (core action, cadence, metric, metric hypothesis) do mình chọn từng vế.
- Làm rõ persona: không bỏ người bệnh, chỉ đặt người nấu lên ưu tiên vì số lượng đứng đầu trong khảo sát.
- Tự viết khung thời gian của metric hypothesis: 2 tuần cho đợt báo cáo hiện tại, theo dõi đến 4 tuần.

> Ghi chú: các mục trên và phần "Điều tôi mang về" trong README do AI đưa lựa chọn ngắn, mình chọn; AI viết thành câu.

---

## Chi tiết theo từng bước

| Bước | AI đã làm | Đánh giá theo quy tắc | Mình đã chọn / xử lý |
|---|---|---|---|
| Chọn đề tài | Đề xuất làm cho VLearn AI Notes | Sai dự án | Chọn dự án team build phase (AI Agent dinh dưỡng) |
| Bản nháp đầu | Tự viết trọn Metrics Pack 00–06 | **Vi phạm** | Gỡ toàn bộ, đưa trang về khung trống |
| Phase 0 | Brainstorm ứng viên core action; đọc `P-110`, tóm tắt dữ kiện | Được phép | Use case chính **sinh thực đơn** |
| Phase 1 | Hỏi lựa chọn từng bước (persona, hành vi, đơn vị đếm qua ví dụ "ăn cỗ", điều kiện khớp, thời hạn log, 5 tiêu chí, core job, core value); ghép thành Core Action Card | Quyết định là của mình; AI viết câu chữ | Persona **người chăm sóc** · core action **log bữa khớp món chính thực đơn đã duyệt, trong ngày** · đơn vị **1 bữa** · tự kiểm **5/5** · core job **nấu đúng cho người bệnh mỗi ngày** |
| Phase 2 | Điền dòng dữ kiện của Nature Card từ `P-110`; chỉ ra chỗ có thể mâu thuẫn giữa dạng "theo chu kỳ" và trigger theo bữa; ghép kết luận cadence | Kết luận do mình chọn từng vế | Trigger **theo giờ bữa** · dạng **theo chu kỳ** · nhịp đo **theo tuần thực đơn** ở cấp **hồ sơ người bệnh** · vì **nấu theo giờ bữa, lệch 1–2 ngày không phải bỏ dùng** |
| Phase 3 | Đưa phương án cho activation, engagement, retention, NSM, leading, counter | Metric do mình chọn | Activated **≥ 3 bữa ở ≥ 2 ngày trong 7 ngày từ thực đơn đầu được duyệt** · cohort **tuần đạt activation** · segment **đơn bệnh vs đa bệnh** · NSM QT **khớp món chính + không cảnh báo critical** · 3 leading · 3 counter |
| Phase 4 | Nêu dữ kiện chưa có điều chỉnh theo nhật ký; đưa phương án loop; gợi ý tên event + tiêu chí nghiệm thu; ghép metric hypothesis | Hypothesis do mình chọn từng vế; tên event được phép | Loop **workflow** · metric **retention tuần thực đơn tăng** · thời gian **tự viết: 2 tuần cho đợt báo cáo hiện tại, theo dõi đến 4 tuần** · 4 event · 3 tiêu chí nghiệm thu |
| Persona (làm rõ) | AI hiểu sai là mình "bỏ bệnh nhân" | — | Mình làm rõ: persona gồm **người bệnh, người chăm sóc, chuyên gia**; người chăm sóc được **ưu tiên** vì số lượng đứng đầu. Rationale dòng 1 là lời mình, AI chỉ sửa chính tả |
| Phase 5 | Rà 7 câu tự soi, chỉ ra 2 chỗ metric chưa có event; tự viết 3 dòng rationale (**vi phạm**, đã gỡ) | Phản biện được phép; rationale không | "Sửa nhiều" = **≥ 20% số món bị thay** · cảnh báo critical tính **tại thời điểm log** (2 chỉnh sửa nhỏ, ghi ở câu tự soi 7; đề chỉ yêu cầu rationale cho thay đổi lớn) · rationale persona: lời của mình |
