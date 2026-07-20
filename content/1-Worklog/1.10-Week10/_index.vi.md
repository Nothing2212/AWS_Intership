---
title: "Worklog Tuần 10"
date: 2026-06-15
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu tuần 10:

* Xây dựng AWS Lambda (Report Processor) sinh báo cáo PDF từ kết quả AI.
* Lưu trữ báo cáo trên Amazon S3 và cấu hình lifecycle chuyển sang S3 Glacier.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | -------------- |
| 2   | - Tìm hiểu thư viện sinh PDF có thể dùng trong Lambda (theo runtime của dự án); lựa chọn đầu tiên vượt quá giới hạn kích thước gói deployment của Lambda, phải đổi sang thư viện nhẹ hơn/đóng gói qua Lambda Layer                                                | 15/06/2026   | 15/06/2026      |                |
| 3   | - Code Lambda (Report Processor): tiêu thụ message kết quả AI từ SQS, dựng nội dung báo cáo PDF                               | 16/06/2026   | 16/06/2026      |                |
| 4   | - Cấu hình lưu file PDF vào Amazon S3 (Report Bucket), đặt quy tắc đặt tên/đường dẫn object hợp lý                             | 17/06/2026   | 17/06/2026      |                |
| 5   | - Cấu hình S3 lifecycle policy: chuyển object sang **S3 Glacier** sau **30 ngày** (lần đầu đặt nhầm điều kiện transition nên rule không áp dụng đúng object, phải kiểm tra và sửa lại filter)                                              | 18/06/2026   | 18/06/2026      |                |
| 6   | - Kiểm thử toàn bộ luồng sinh & lưu trữ báo cáo, xác minh lifecycle hoạt động đúng                                            | 19/06/2026   | 19/06/2026      |                |
| 7   | - Xem lại code Lambda Report Processor, refactor một số phần theo góp ý của mentor                          | 20/06/2026   | 20/06/2026      |                |
| CN  | - Đọc tài liệu về Amazon SES để chuẩn bị cho tuần 11                                                         | 21/06/2026   | 21/06/2026      |                |

### Kết quả đạt được tuần 10:

* Hoàn thành Lambda Report Processor: nhận kết quả AI từ SQS và sinh báo cáo PDF tự động, sau khi phải đổi thư viện sinh PDF ban đầu do vượt giới hạn kích thước gói deployment của Lambda.
* Lưu trữ báo cáo PDF trên S3 (Report Bucket) với cấu trúc đặt tên rõ ràng.
* Cấu hình thành công lifecycle rule tự động chuyển object sang S3 Glacier sau 30 ngày (sau khi tự phát hiện và sửa lỗi filter áp dụng sai ở lần cấu hình đầu), giúp giảm chi phí lưu trữ dài hạn.
* ...

