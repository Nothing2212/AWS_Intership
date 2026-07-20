---
title: "Worklog Tuần 6"
date: 2026-05-18
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:

* Hiểu sâu các routing policy của DNS (Route 53) và cơ chế caching của CDN (CloudFront).
* Tìm hiểu các khái niệm networking nâng cao: VPC Peering (và tính chất không bắc cầu của nó) và NAT Gateway.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                     | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                             |
| --- | -------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------------------------------- |
| 2   | - Tìm hiểu sâu Route 53: hosted zone, các loại record (A, CNAME, Alias) và các routing policy (simple, weighted, latency-based, failover)                               | 18/05/2026   | 18/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| 3   | - **Thực hành:** trỏ domain về EC2/ALB thông qua Route 53 bằng Alias record, so sánh với việc dùng CNAME thông thường                                            | 19/05/2026   | 19/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| 4   | - Tìm hiểu sâu Amazon CloudFront: cơ chế edge caching của CDN, các loại origin (S3, ALB), cache behavior, cấu hình TTL, và Origin Access Control (OAC) cho origin S3 private                                            | 20/05/2026   | 20/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| 5   | - **Thực hành:** tạo CloudFront distribution cho website tĩnh trên S3 sử dụng OAC (thay vì để bucket public); lần đầu quên cập nhật bucket policy cho đúng principal của OAC nên bucket vẫn truy cập public trực tiếp được, phải kiểm tra lại và sửa policy mới chặn đúng                                | 21/05/2026   | 21/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| 6   | - Tìm hiểu VPC Peering (kết nối điểm-điểm, không bắc cầu giữa các VPC) và NAT Gateway (dịch vụ quản lý sẵn, độ sẵn sàng cao, so với việc tự dựng NAT instance)                                                                | 22/05/2026   | 22/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| 7   | - Ôn lại cấu hình Route 53/CloudFront và lý do OAC an toàn hơn so với để bucket policy public, dọn dẹp resource test để tránh phát sinh chi phí | 23/05/2026   | 23/05/2026      |                                               |
| CN  | - Đọc tài liệu tổng quan về dự án LunaGenZ để chuẩn bị tham gia dự án từ tuần sau      | 24/05/2026   | 24/05/2026      |                                               |

### Kết quả đạt được tuần 6:

* Cấu hình thành công domain trỏ về hạ tầng AWS thông qua Route 53 bằng Alias record, hiểu được cách các routing policy (weighted, latency-based, failover) áp dụng vào các kịch bản phân phối traffic thực tế.
* Triển khai CloudFront distribution phía trước static website trên S3 sử dụng Origin Access Control; sau khi tự phát hiện lỗi bucket policy chưa khóa đúng quyền truy cập public trực tiếp, đã sửa lại để đảm bảo chỉ CloudFront mới đọc được object, trong khi vẫn phục vụ nội dung nhanh qua HTTPS nhờ edge caching.
* Hiểu cách kết nối giữa các VPC (Peering) và lý do các kết nối peering không bắc cầu (non-transitive), cũng như cách NAT Gateway cho phép subnet private truy cập internet theo hướng đi ra (outbound-only) mà không lộ ra traffic đi vào.
* ...
