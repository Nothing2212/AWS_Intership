---
title: "Worklog Tuần 11"
date: 2026-06-22
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu tuần 11:

* Gửi báo cáo PDF cho người dùng qua email bằng Amazon SES.
* Kiểm thử end-to-end toàn bộ pipeline AI và thiết lập giám sát qua Amazon CloudWatch.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                  | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | -------------- |
| 2   | - Tìm hiểu & cấu hình Amazon SES: xác thực domain/email, phân biệt sandbox và production                                                                    | 22/06/2026   | 22/06/2026      |                |
| 3   | - Tích hợp Lambda (Report Processor) gửi email đính kèm/link báo cáo PDF cho người dùng qua SES                                                             | 23/06/2026   | 23/06/2026      |                |
| 4   | - Cấu hình CloudWatch Logs & Metrics cho các Lambda (Core Logic, Payment Webhook Handler, Report Processor) và API Gateway                                  | 24/06/2026   | 24/06/2026      |                |
| 5   | - Thiết lập CloudWatch Alarm cảnh báo lỗi/độ trễ khi gọi Amazon Bedrock                                                                                      | 25/06/2026   | 25/06/2026      |                |
| 6   | - Kiểm thử end-to-end toàn bộ luồng: User request &rarr; Auth &rarr; Validate &rarr; Payment &rarr; Gen AI &rarr; SQS &rarr; Report &rarr; S3 &rarr; SES &rarr; Email | 26/06/2026   | 26/06/2026      |                |
| 7   | - Ôn lại các CloudWatch alarm/dashboard đã thiết lập, kiểm tra lại ngưỡng cảnh báo                                                     | 27/06/2026   | 27/06/2026      |                |
| CN  | - Chuẩn bị tài liệu, ghi chú cho 2 tuần cuối kỳ thực tập (rà soát bảo mật, tổng kết)                                                    | 28/06/2026   | 28/06/2026      |                |

### Kết quả đạt được tuần 11:

* Hoàn thiện tính năng gửi email báo cáo tự động qua Amazon SES.
* Thiết lập logging và alarm giám sát qua CloudWatch cho toàn bộ các Lambda và API Gateway trong luồng AI.
* Kiểm thử thành công toàn bộ pipeline end-to-end của tính năng AI, từ request người dùng đến khi nhận được email báo cáo.
* ...

