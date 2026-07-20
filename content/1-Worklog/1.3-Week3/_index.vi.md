---
title: "Worklog Tuần 3"
date: 2026-04-27
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3:

* Hiểu và thực hành sâu dịch vụ lưu trữ Amazon S3.
* Nắm được sự đánh đổi giữa độ bền/chi phí/tốc độ truy xuất của các storage class, lifecycle policy, versioning, các lớp kiểm soát truy cập và cách host static website trên S3.

{{% notice note %}}
Ngày 30/04 và 01/05/2026 là ngày nghỉ lễ (30/4 - 1/5) nên tuần này chỉ có 3 ngày làm việc.
{{% /notice %}}

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                       | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                             |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------------------------------- |
| 2   | - Tìm hiểu sâu Amazon S3: bucket, object, các storage class (Standard, Standard-IA, One Zone-IA, Glacier, Glacier Deep Archive) và sự đánh đổi giữa độ bền (11 số 9), độ sẵn sàng và tốc độ truy xuất | 27/04/2026   | 27/04/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| 3   | - **Thực hành:** tạo bucket, upload/download object qua console và CLI <br> - Cấu hình versioning (lần đầu quên bật versioning trước khi thử ghi đè object để test, phải tạo lại bucket và làm lại mới thấy rõ được lợi ích) & permissions (bucket policy, IAM policy, ACL và thứ tự ưu tiên giữa chúng)                                      | 28/04/2026   | 28/04/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| 4   | - Tìm hiểu S3 lifecycle policy: quy tắc chuyển đổi giữa các storage class và quy tắc hết hạn (expiration), cách chúng giúp giảm chi phí lưu trữ dài hạn <br> - **Thực hành:** host static website trên S3, hiểu rõ giới hạn chỉ hỗ trợ HTTP và lý do vì sao cần CloudFront + OAC để có HTTPS                                                                       | 29/04/2026   | 29/04/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| 5   | - Nghỉ lễ 30/4 (Giải phóng miền Nam)                                                                                                                   | 30/04/2026   | 30/04/2026      |                                               |
| 6   | - Nghỉ lễ 1/5 (Quốc tế Lao động)                                                                                                                       | 01/05/2026   | 01/05/2026      |                                               |
| 7   | - Thực hành bù thêm về S3 lifecycle policy và static website hosting do nghỉ lễ giữa tuần, đồng thời kiểm tra thực tế hành vi của object sau khi chuyển sang Glacier (độ trễ truy xuất, yêu cầu restore)                                            | 02/05/2026   | 02/05/2026      |                                               |
| CN  | - Ôn tập lại toàn bộ kiến thức S3 trong tuần, đọc trước tài liệu về RDS/DynamoDB cho tuần 4                                                   | 03/05/2026   | 03/05/2026      |                                               |

### Kết quả đạt được tuần 3:

* Hiểu các storage class của S3 (Standard, Standard-IA, One Zone-IA, các tầng Glacier) và sự đánh đổi cụ thể (chi phí, độ trễ truy xuất, độ bền) quyết định khi nào nên dùng loại nào.
* Thực hành tạo bucket, upload/download object qua cả console lẫn CLI, cấu hình versioning cùng với mô hình kiểm soát truy cập nhiều lớp (bucket policy, IAM policy, ACL) và cách chúng phối hợp với nhau.
* Cấu hình lifecycle policy để tự động chuyển đổi storage class và xóa object cũ, giúp giảm chi phí lưu trữ dài hạn.
* Triển khai thành công static website hosting trên S3 và hiểu rõ vì sao nó chỉ hỗ trợ HTTP, tạo tiền đề cho việc tích hợp CloudFront sau này.
* Rút kinh nghiệm cần bật các cấu hình quan trọng (như versioning) trước khi thử nghiệm thay vì sau, tránh phải làm lại từ đầu.
* ...
