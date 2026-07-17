---
title: "Worklog Tuần 2"
date: 2026-04-20
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2:

* Tạo AWS Free Tier account, làm quen AWS Console & AWS CLI.
* Hiểu và thực hành các dịch vụ compute cơ bản: EC2 (các dòng instance, hình thức thanh toán), EBS, Elastic IP và nền tảng networking của VPC.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                 | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                             |
| --- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------------------------------- |
| 2   | - Tạo AWS Free Tier account <br> - Cài đặt & cấu hình AWS CLI (Access Key, Secret Key, Region mặc định) <br> - Bật MFA cho root account và tạo IAM user riêng để dùng hàng ngày thay vì dùng root | 20/04/2026   | 20/04/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| 3   | - Tìm hiểu sâu về EC2: <br>&emsp; + Các dòng instance (t3 burstable, m5 general purpose, c5 compute-optimized) <br>&emsp; + AMI (public, custom, Marketplace) <br>&emsp; + Các loại EBS volume (gp3 vs gp2 vs io2) và khái niệm IOPS/throughput <br>&emsp; + Elastic IP và lý do cần dùng để tránh đổi public IP mỗi lần stop/start instance | 21/04/2026   | 21/04/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| 4   | - **Thực hành:** <br>&emsp; + Tạo EC2 instance với Security Group tùy chỉnh <br>&emsp; + Kết nối SSH bằng key pair <br>&emsp; + Gắn thêm EBS volume, mount và resize volume mà không cần tắt máy | 22/04/2026   | 22/04/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| 5   | - Tìm hiểu nền tảng networking của VPC: <br>&emsp; + Quy hoạch CIDR block cho subnet public/private <br>&emsp; + Route table và route "local" mặc định <br>&emsp; + Internet Gateway so với NAT Gateway <br>&emsp; + Security Group (stateful, ở cấp instance) so với Network ACL (stateless, ở cấp subnet) | 23/04/2026   | 23/04/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| 6   | - **Thực hành:** <br>&emsp; + Tự dựng VPC tùy chỉnh từ đầu với subnet public/private trải trên 2 Availability Zone <br>&emsp; + Cấu hình route table sao cho chỉ subnet public mới đi ra được Internet Gateway <br>&emsp; + Cấu hình Security Group theo nguyên tắc least-privilege (chỉ mở đúng port cần thiết) | 24/04/2026   | 24/04/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| 7   | - Ôn lại các dòng instance của EC2 và logic routing của VPC, làm lại toàn bộ bài lab trong tuần mà không xem hướng dẫn để kiểm tra xem đã thực sự nắm vững kiến thức chưa | 25/04/2026   | 25/04/2026      |                                               |
| CN  | - Đọc tài liệu về Amazon S3 (storage class, độ bền dữ liệu, bucket policy) để chuẩn bị cho nội dung tuần 3                                                                                  | 26/04/2026   | 26/04/2026      |                                               |

### Kết quả đạt được tuần 2:

* Tạo và cấu hình thành công AWS Free Tier account, bật MFA cho root và tạo IAM user với quyền tối thiểu để dùng hàng ngày thay vì dùng root.
* Hiểu các dòng instance của EC2 và khi nào nên chọn loại nào (t3 cho tải nhẹ/không ổn định, m5 cho tải cân bằng, c5 cho tải nặng về tính toán), cùng với AMI, các loại EBS volume và lý do cần Elastic IP để có địa chỉ public ổn định.
* Thực hành tạo EC2 instance, kết nối SSH bằng key pair, gắn thêm và resize EBS volume mà không gây downtime.
* Xây dựng được VPC tùy chỉnh với subnet public/private trải trên 2 AZ, cấu hình route table đúng phạm vi, và hiểu rõ sự khác biệt thực tế giữa Security Group (stateful) và Network ACL (stateless).
* ...
