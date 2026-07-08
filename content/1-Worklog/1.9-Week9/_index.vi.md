---
title: "Worklog Tuần 9"
date: 2026-06-08
weight: 1
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9:

* Xử lý bất đồng bộ kết quả AI thông qua Amazon SQS.
* Liên kết luồng xác thực thanh toán (Verify Payment) với DynamoDB trước khi trả kết quả AI cho người dùng.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                              | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | -------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | -------------- |
| 2   | - Tìm hiểu Amazon SQS: queue, message, visibility timeout                                                                                | 08/06/2026   | 08/06/2026      |                |
| 3   | - Thiết kế luồng: Lambda (Core Logic) đẩy kết quả AI sinh ra vào SQS (bước "Out result")                                                  | 09/06/2026   | 09/06/2026      |                |
| 4   | - Code consumer xử lý message từ SQS <br> - Truy vấn DynamoDB để kiểm tra trạng thái thanh toán (Verify Payment) trước khi trả kết quả     | 10/06/2026   | 10/06/2026      |                |
| 5   | - Tích hợp với Lambda (Payment Webhook Handler): nhận callback thanh toán, cập nhật trạng thái vào DynamoDB                               | 11/06/2026   | 11/06/2026      |                |
| 6   | - Kiểm thử luồng end-to-end: request &rarr; validate &rarr; verify payment &rarr; gen AI &rarr; đẩy kết quả qua SQS                       | 12/06/2026   | 12/06/2026      |                |
| 7   | - Ôn lại luồng SQS/DynamoDB trong tuần, ghi chú lại tài liệu kỹ thuật cá nhân                                             | 13/06/2026   | 13/06/2026      |                |
| CN  | - Đọc tài liệu về các thư viện sinh PDF để chuẩn bị cho tuần 10                                                           | 14/06/2026   | 14/06/2026      |                |

### Kết quả đạt được tuần 9:

* Xây dựng thành công luồng xử lý bất đồng bộ dùng Amazon SQS cho kết quả sinh AI.
* Đảm bảo hệ thống chỉ trả kết quả AI cho người dùng khi trạng thái thanh toán đã được xác nhận trong DynamoDB.
* Tích hợp thành công với Lambda Payment Webhook Handler để cập nhật trạng thái thanh toán tự động.
* ...

