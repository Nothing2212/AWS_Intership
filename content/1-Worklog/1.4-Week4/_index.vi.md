---
title: "Worklog Tuần 4"
date: 2026-05-04
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:

* Hiểu sâu dịch vụ Amazon RDS: các database engine, Multi-AZ (đồng bộ, phục vụ high availability) so với Read Replica (bất đồng bộ, phục vụ mở rộng khả năng đọc), chiến lược backup/restore.
* Làm quen với nền tảng của Amazon DynamoDB: cách thiết kế partition key/sort key và ảnh hưởng của nó đến hiệu năng.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                             | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                             |
| --- | ---------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------------------------------- |
| 2   | - Tìm hiểu sâu Amazon RDS: các database engine (MySQL, PostgreSQL,...), Multi-AZ (bản sao đồng bộ dùng để failover) so với Read Replica (bất đồng bộ, giảm tải cho các truy vấn đọc) và khi nào nên kết hợp cả hai | 04/05/2026   | 04/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| 3   | - **Thực hành:** tạo RDS instance, kết nối từ EC2/local, kiểm tra security group chỉ cho phép truy cập từ tầng ứng dụng chứ không mở ra internet                                                                  | 05/05/2026   | 05/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| 4   | - Tìm hiểu backup, snapshot và restore RDS: automated backup có retention window so với manual snapshot, và cơ chế point-in-time recovery                                                                              | 06/05/2026   | 06/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| 5   | - Tìm hiểu sâu Amazon DynamoDB: partition key so với sort key, cách partition key quyết định việc phân phối dữ liệu, và tại sao chọn key không tốt sẽ gây ra "hot partition"                                                               | 07/05/2026   | 07/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| 6   | - **Thực hành:** tạo bảng DynamoDB với composite key, thao tác CRUD, so sánh chế độ on-demand và provisioned capacity                                                                 | 08/05/2026   | 08/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| 7   | - Ôn lại Multi-AZ/Read Replica của RDS và cách thiết kế partition key của DynamoDB, thực hành thêm vài thao tác CRUD và một truy vấn đơn giản dùng khoảng giá trị của sort key                                    | 09/05/2026   | 09/05/2026      |                                               |
| CN  | - Đọc tài liệu về Elastic Load Balancer và Auto Scaling để chuẩn bị cho tuần 5                          | 10/05/2026   | 10/05/2026      |                                               |

### Kết quả đạt được tuần 4:

* Hiểu các database engine của RDS và cụ thể hơn về sự khác biệt giữa Multi-AZ (bản sao đồng bộ dùng để failover) và Read Replica (bất đồng bộ, dùng để mở rộng khả năng đọc) — cũng như khi nào một hệ thống production cần cả hai.
* Tạo và kết nối thành công RDS instance từ EC2 với phạm vi truy cập mạng chỉ giới hạn ở tầng ứng dụng.
* Nắm được sự khác biệt giữa automated backup (có retention window) và manual snapshot, cùng cơ chế point-in-time recovery.
* Làm quen với DynamoDB, thực hành thiết kế composite key (partition key + sort key), tránh được lỗi thiết kế gây hot partition dễ gặp phải, và so sánh được chế độ on-demand với provisioned capacity.
* ...
