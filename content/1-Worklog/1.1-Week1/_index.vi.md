---
title: "Worklog Tuần 1"
date: 2026-04-17
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Mục tiêu tuần 1:

* Kết nối, làm quen với các thành viên trong First Cloud Journey (FCJ) và mentor hướng dẫn.
* Nắm được lộ trình thực tập (17/04/2026 - 10/07/2026), nội quy và quy trình báo cáo worklog.
* Hiểu tổng quan về hạ tầng toàn cầu của AWS, các nhóm dịch vụ cơ bản và mô hình Shared Responsibility Model.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                             |
| --- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------------------------------- |
| 6   | - Gặp gỡ, làm quen với các thành viên FCJ và mentor <br> - Đọc và lưu ý nội quy, quy định tại đơn vị thực tập <br> - Tìm hiểu tổng quan hạ tầng toàn cầu của AWS (Region, Availability Zone, Edge Location) và mô hình Shared Responsibility Model <br> - Tìm hiểu các nhóm dịch vụ chính và mối liên hệ giữa chúng <br>&emsp; + Compute (EC2, Lambda) <br>&emsp; + Storage (S3, EBS) <br>&emsp; + Networking (VPC, Route 53) <br>&emsp; + Database (RDS, DynamoDB) | 17/04/2026   | 17/04/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| 7   | - Xem lại note buổi onboarding chi tiết hơn, tự vẽ lại sơ đồ phân chia trách nhiệm giữa AWS và khách hàng theo Shared Responsibility Model cho từng nhóm dịch vụ, chuẩn bị tạo AWS Free Tier account cho tuần sau | 18/04/2026   | 18/04/2026      |                                               |
| CN  | - Đọc thêm tài liệu tổng quan về EC2 (các loại instance, hình thức thanh toán) và VPC (CIDR block, subnet) để chuẩn bị cho các bài thực hành ở tuần 2                                                                                                                                                                                          | 19/04/2026   | 19/04/2026      |                                               |

### Kết quả đạt được tuần 1:

* Làm quen với các thành viên FCJ, mentor và nắm được lịch trình thực tập.
* Nắm được nội quy, quy định và quy trình báo cáo worklog hàng tuần.
* Xây dựng được mô hình tư duy rõ ràng về hạ tầng toàn cầu của AWS (Region/AZ đảm bảo tính sẵn sàng cao, Edge Location phục vụ CDN) và mô hình Shared Responsibility Model (AWS chịu trách nhiệm bảo mật "của" cloud, khách hàng chịu trách nhiệm bảo mật "trong" cloud).
* Có cái nhìn tổng quan về các nhóm dịch vụ chính của AWS và cách một workload thực tế thường kết hợp chúng với nhau:
  * Compute (EC2 cho máy ảo, Lambda cho serverless)
  * Storage (S3 cho object storage, EBS cho block storage)
  * Networking (VPC là ranh giới mạng cô lập, Route 53 phụ trách DNS)
  * Database (RDS cho relational, DynamoDB cho NoSQL)
