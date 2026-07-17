---
title: "Worklog Tuần 5"
date: 2026-05-11
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:

* Hiểu và triển khai cân bằng tải (Elastic Load Balancer: ALB/NLB) và Auto Scaling, bao gồm các loại scaling policy.
* Làm quen với giám sát hệ thống qua Amazon CloudWatch: metrics, alarm và cách alarm có thể kích hoạt hành động scaling.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                       | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                             |
| --- | ------------------------------------------------------------------------------------------------------------------ | ------------ | --------------- | ------------------------------------------- |
| 2   | - Tìm hiểu Elastic Load Balancer: Application Load Balancer (Layer 7, routing theo path/host) so với Network Load Balancer (Layer 4, độ trễ cực thấp)                                                                          | 11/05/2026   | 11/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| 3   | - **Thực hành:** tạo Application Load Balancer, target group, health check; tinh chỉnh ngưỡng/khoảng thời gian health check và quan sát ảnh hưởng của nó đến tốc độ failover                                          | 12/05/2026   | 12/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| 4   | - Tìm hiểu Auto Scaling Group, launch template và các loại scaling policy: target tracking, step scaling và scheduled scaling                                                                      | 13/05/2026   | 13/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| 5   | - **Thực hành:** cấu hình Auto Scaling Group kết hợp với ALB, sử dụng target-tracking policy dựa trên CPU utilization trung bình                                                        | 14/05/2026   | 14/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| 6   | - Tìm hiểu Amazon CloudWatch: metrics (standard và custom), alarm (ngưỡng, evaluation period), dashboard, và cách một alarm có thể trực tiếp kích hoạt hành động Auto Scaling                                                            | 15/05/2026   | 15/05/2026      | <https://cloudjourney.awsstudygroup.com/vi/> |
| 7   | - Ôn lại cấu hình ALB/Auto Scaling Group, thử lại kịch bản scale-out/scale-in bằng cách mô phỏng tải CPU và quan sát tốc độ phản ứng của target-tracking policy                      | 16/05/2026   | 16/05/2026      |                                               |
| CN  | - Đọc tài liệu về Route 53 và CloudFront để chuẩn bị cho tuần 6                                    | 17/05/2026   | 17/05/2026      |                                               |

### Kết quả đạt được tuần 5:

* Hiểu rõ sự khác biệt thực tế giữa ALB (Layer 7, routing theo nội dung) và NLB (Layer 4, độ trễ cực thấp), và chọn ALB phù hợp cho use case này.
* Triển khai thành công Application Load Balancer với target group và health check, hiểu được cách khoảng thời gian/ngưỡng health check đánh đổi giữa tốc độ failover và nguy cơ báo động giả (false positive).
* Cấu hình Auto Scaling Group với target-tracking scaling policy dựa trên CPU utilization, tích hợp với ALB, và kiểm chứng hành vi scale-out/scale-in dưới tải mô phỏng.
* Thiết lập CloudWatch alarm để giám sát CPU/metrics của EC2 và hiểu được cách một alarm thay đổi trạng thái có thể trực tiếp kích hoạt hành động Auto Scaling.
* ...
