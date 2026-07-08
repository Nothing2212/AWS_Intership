---
title: "Worklog Tuần 8"
date: 2026-06-01
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8:

* Thiết kế prompt cho tính năng sinh nội dung AI của LunaGenZ.
* Tích hợp AWS Lambda (Core Logic) gọi Amazon Bedrock để sinh kết quả (bước Gen Prompt AI).

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                              | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | -------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | -------------- |
| 2   | - Phân tích dữ liệu đầu vào (request từ API Gateway sau khi qua Cognito Authorizer) <br> - Xây dựng logic validate request               | 01/06/2026   | 01/06/2026      |                |
| 3   | - Thiết kế prompt template cho Claude 3 Haiku phù hợp nghiệp vụ LunaGenZ                                                                  | 02/06/2026   | 02/06/2026      |                |
| 4   | - Code AWS Lambda (Core Logic): build request payload, gọi Bedrock InvokeModel, parse response                                            | 03/06/2026   | 03/06/2026      |                |
| 5   | - Xử lý lỗi & retry khi gọi Bedrock (timeout, throttling) <br> - Lưu trữ API keys/secret an toàn qua AWS Secrets Manager                   | 04/06/2026   | 04/06/2026      |                |
| 6   | - Kiểm thử prompt với nhiều input mẫu, tinh chỉnh để cải thiện chất lượng kết quả sinh ra                                                  | 05/06/2026   | 05/06/2026      |                |
| 7   | - Tham gia sự kiện **Meeting 06/6** cùng các thành viên FCJ (xem chi tiết tại mục "Các events đã tham gia" &rarr; Event 2)                | 06/06/2026   | 06/06/2026      |                |
| CN  | - Ôn lại kết quả tinh chỉnh prompt trong tuần, tìm hiểu thêm về giới hạn throttling của Bedrock                            | 07/06/2026   | 07/06/2026      |                |

### Kết quả đạt được tuần 8:

* Hoàn thành Lambda (Core Logic) gọi Amazon Bedrock/Claude 3 Haiku để sinh nội dung theo prompt template đã thiết kế.
* Quản lý API keys/secret an toàn thông qua AWS Secrets Manager thay vì hardcode.
* Xử lý lỗi, timeout và retry khi gọi Bedrock ổn định hơn.
* Tinh chỉnh prompt qua nhiều lần thử nghiệm để cải thiện chất lượng và độ ổn định của kết quả AI.
* ...

