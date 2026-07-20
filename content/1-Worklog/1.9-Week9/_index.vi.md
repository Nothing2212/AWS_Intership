---
title: "Worklog Tuần 9"
date: 2026-06-08
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9:

* Lưu kết quả AI sinh ra vào Amazon DynamoDB.
* Xử lý bất đồng bộ việc gửi job sang Report Processor thông qua Amazon SQS.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                              | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | -------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | -------------- |
| 2   | - Tìm hiểu Amazon SQS: queue, message, visibility timeout                                                                                | 08/06/2026   | 08/06/2026      |                |
| 3   | - Thiết kế luồng: Lambda (Core Logic) lưu kết quả AI sinh ra vào DynamoDB, sau đó đẩy job sang SQS cho Report Processor                   | 09/06/2026   | 09/06/2026      |                |
| 4   | - Code logic ghi kết quả vào bảng DynamoDB (thiết kế partition key theo user/request id)                                                  | 10/06/2026   | 10/06/2026      |                |
| 5   | - Code Lambda (Core Logic) gửi message chứa thông tin job sang SQS sau khi ghi DynamoDB thành công (lần test đầu Lambda bị retry do timeout nên vô tình gửi trùng message, phải bổ sung kiểm tra idempotency dựa trên request id trước khi ghi/gửi)                                        | 11/06/2026   | 11/06/2026      |                |
| 6   | - Kiểm thử luồng end-to-end: request &rarr; validate &rarr; gen AI (Gemini) &rarr; lưu DynamoDB &rarr; đẩy job qua SQS                    | 12/06/2026   | 12/06/2026      |                |
| 7   | - Ôn lại luồng SQS/DynamoDB trong tuần, ghi chú lại tài liệu kỹ thuật cá nhân                                             | 13/06/2026   | 13/06/2026      |                |
| CN  | - Đọc tài liệu về các thư viện sinh PDF để chuẩn bị cho tuần 10                                                           | 14/06/2026   | 14/06/2026      |                |

### Kết quả đạt được tuần 9:

* Xây dựng thành công logic lưu kết quả AI sinh ra vào Amazon DynamoDB với partition key hợp lý.
* Xây dựng luồng xử lý bất đồng bộ dùng Amazon SQS để gửi job sang Report Processor; sau khi phát hiện sự cố gửi trùng message do Lambda bị retry, đã bổ sung kiểm tra idempotency theo request id.
* Kiểm thử end-to-end luồng request &rarr; gen AI &rarr; lưu DynamoDB &rarr; gửi SQS chạy ổn định.
* ...
