---
title: "Worklog Tuần 7"
date: 2026-05-25
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:

* Được phân công tham gia dự án **LunaGenZ**, phụ trách phần **AI**.
* Nắm được kiến trúc tổng thể hệ thống trên AWS (frontend, backend, thanh toán, AI, báo cáo).
* Tìm hiểu Amazon Bedrock và model Claude 3 Haiku.

{{% notice note %}}
Từ tuần này, worklog tập trung vào phần việc AI của dự án LunaGenZ mà bản thân trực tiếp phụ trách.
{{% /notice %}}

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                       | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | -------------- |
| 2   | - Tham gia họp kickoff dự án LunaGenZ, tìm hiểu bài toán & yêu cầu nghiệp vụ                                                                          | 25/05/2026   | 25/05/2026      |                |
| 3   | - Nghiên cứu kiến trúc tổng thể: WAF, CloudFront, Amplify (Next.js), API Gateway, Cognito, Lambda, DynamoDB                                            | 26/05/2026   | 26/05/2026      |                |
| 4   | - Tìm hiểu Amazon Bedrock, các foundation model <br> - Kích hoạt quyền truy cập model **Claude 3 Haiku**                                               | 27/05/2026   | 27/05/2026      |                |
| 5   | - **Thực hành:** gọi thử Bedrock InvokeModel API với Claude 3 Haiku qua console/SDK                                                                    | 28/05/2026   | 28/05/2026      |                |
| 6   | - Tìm hiểu luồng xử lý AI trong hệ thống: request người dùng &rarr; AWS Lambda (Core Logic) &rarr; Amazon Bedrock &rarr; trả kết quả (Gen Prompt AI)  | 29/05/2026   | 29/05/2026      |                |
| 7   | - Tham gia sự kiện **Meeting 30/5** cùng các thành viên FCJ (xem chi tiết tại mục "Các events đã tham gia" &rarr; Event 1)                              | 30/05/2026   | 30/05/2026      |                |
| CN  | - Đọc thêm tài liệu về Amazon Bedrock và cách viết prompt hiệu quả để chuẩn bị cho tuần 8                                              | 31/05/2026   | 31/05/2026      |                |

### Kết quả đạt được tuần 7:

* Nắm được sơ đồ kiến trúc tổng thể của dự án LunaGenZ và vai trò của từng service: WAF, CloudFront, Amplify, Cognito, API Gateway, Lambda, DynamoDB, Bedrock, SQS, S3, SES.
* Hiểu vị trí và vai trò của phần AI (bước "Gen Prompt AI") trong toàn bộ luồng xử lý.
* Gọi thử thành công model Claude 3 Haiku thông qua Amazon Bedrock.
* ...

