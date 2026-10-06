# Track1 · Day20 — Product Metrics: Core Action, Retention, Loop, Tracking

## 1. Thông tin

- **Họ tên:** Hà Thị Mỹ Linh · **MHV:** 2A202602619
- **Dự án chọn làm:** **AI Agent Trợ Lý Dinh Dưỡng & Lối Sống Theo Bệnh Lý**, dự án team build phase. Mình phụ trách NLP (RAG guideline, parser câu tiếng Việt) + BA (ràng buộc lâm sàng theo bệnh) + docs/eval/presentation.
- **Tệp Metrics Pack:** [metrics-pack.html](metrics-pack.html) · xem trực tiếp: https://htmlpreview.github.io/?https://github.com/HaRin2806/Track1_Day20_2A202602619_HaThiMyLinh/blob/main/metrics-pack.html

**Cấu trúc repo**

```
Track1_Day20_2A202602619_HaThiMyLinh/
├── README.md
├── ai-support-log.md
└── metrics-pack.html
```

---

## 2. Điều tôi mang về áp dụng cho dự án thật

**Điều làm tôi nghĩ khác đi**
- Người dùng chính của thực đơn là **người nấu**; người bệnh là người được theo dõi.
- **Sinh thực đơn chưa phải value**: AI sinh xong chỉ là output, value chỉ có khi người bệnh thật sự ăn theo.
- **App hiện chưa biết người dùng có nấu theo thực đơn không**, vì nhật ký bữa ăn chưa nối với thực đơn.

**Tôi sẽ làm trong phần mình phụ trách**
- Đưa bảng 4 event + tiêu chí nghiệm thu vào `docs/` của dự án.
- Dùng NSM "số bữa nấu đúng thực đơn và an toàn mỗi tuần thực đơn" khi thuyết trình sản phẩm.

**Tôi sẽ đề xuất với team**
- Nối bữa ăn đã log với bữa trong thực đơn, để đo được core action.
- Đổi cách tính "tỷ lệ tuân thủ" trong báo cáo tuần: thêm % bữa nấu theo thực đơn.
- Theo dõi thời gian chuyên gia duyệt thực đơn, vì duyệt chậm là mất những ngày đầu tuần.

---

## 3. AI Support Log

Chi tiết: [ai-support-log.md](ai-support-log.md)
