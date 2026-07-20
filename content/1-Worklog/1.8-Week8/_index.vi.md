---
title: "Worklog Tuần 8"
date: 2026-06-01
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8:

* Thiết kế prompt cho tính năng sinh nội dung AI của LunaGenZ.
* Tích hợp AWS Lambda (Core Logic) gọi Gemini API để sinh kết quả.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                              | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | -------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | -------------- |
| 2   | - Phân tích dữ liệu đầu vào (request từ API Gateway) <br> - Xây dựng logic validate request                                              | 01/06/2026   | 01/06/2026      |                |
| 3   | - Thiết kế prompt template cho Gemini phù hợp nghiệp vụ LunaGenZ (bản đầu tiên viết prompt còn quá chung chung nên kết quả trả về nhiều lúc lạc đề, chưa bám sát yêu cầu nghiệp vụ)                                                                          | 02/06/2026   | 02/06/2026      |                |
| 4   | - Code AWS Lambda (Core Logic): build request payload, gọi Gemini API, parse response                                                    | 03/06/2026   | 03/06/2026      |                |
| 5   | - Xử lý lỗi & retry khi gọi Gemini API (timeout, rate limit) <br> - Lưu trữ API key an toàn qua AWS Secrets Manager                        | 04/06/2026   | 04/06/2026      |                |
| 6   | - Kiểm thử prompt với nhiều input mẫu, tinh chỉnh để cải thiện chất lượng kết quả sinh ra (phải chỉnh sửa qua nhiều vòng lặp thử-sai mới thu hẹp được prompt về đúng định dạng và văn phong mong muốn)                                                  | 05/06/2026   | 05/06/2026      |                |
| 7   | - Tham gia sự kiện **Meeting 06/6** cùng các thành viên FCJ (xem chi tiết tại mục "Các events đã tham gia" &rarr; Event 2)                | 06/06/2026   | 06/06/2026      |                |
| CN  | - Ôn lại kết quả tinh chỉnh prompt trong tuần, tìm hiểu thêm về giới hạn rate limit của Gemini API                            | 07/06/2026   | 07/06/2026      |                |

### Kết quả đạt được tuần 8:

* Hoàn thành Lambda (Core Logic) gọi Gemini API để sinh nội dung theo prompt template đã thiết kế.
* Quản lý API key an toàn thông qua AWS Secrets Manager thay vì hardcode.
* Xử lý lỗi, timeout và retry khi gọi Gemini API ổn định hơn.
* Tinh chỉnh prompt qua nhiều lần thử nghiệm để cải thiện chất lượng và độ ổn định của kết quả AI, sau khi bản prompt đầu tiên còn quá chung chung khiến kết quả nhiều lúc lạc đề.
* Một số input đặc biệt/edge case vẫn khiến Gemini trả về nội dung chưa đúng định dạng mong muốn, cần tiếp tục tinh chỉnh thêm ở các tuần sau.
* ...
