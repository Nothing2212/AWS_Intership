---
title: "Worklog Tuần 7"
date: 2026-05-25
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:

* Được phân công tham gia dự án **LunaGenZ**, phụ trách phần **AI**.
* Nắm được kiến trúc tổng thể hệ thống trên AWS (frontend, backend, AI, báo cáo).
* Tìm hiểu Gemini API và các model Gemini.

{{% notice note %}}
Từ tuần này, worklog tập trung vào phần việc AI của dự án LunaGenZ mà bản thân trực tiếp phụ trách.
{{% /notice %}}

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                       | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | -------------- |
| 2   | - Tham gia họp kickoff dự án LunaGenZ, tìm hiểu bài toán & yêu cầu nghiệp vụ                                                                          | 25/05/2026   | 25/05/2026      |                |
| 3   | - Nghiên cứu kiến trúc tổng thể: CloudFront, Amplify (Next.js), API Gateway, Lambda, DynamoDB, SQS, S3, SES (do mới tham gia dự án nên ban đầu khá bối rối về cách các service này liên kết với nhau, phải nhờ mentor giải thích lại luồng dữ liệu)                                            | 26/05/2026   | 26/05/2026      |                |
| 4   | - Tìm hiểu Gemini API: các dòng model (Gemini Flash, Gemini Pro), giới hạn free tier <br> - Đăng ký API key trên Google AI Studio                       | 27/05/2026   | 27/05/2026      |                |
| 5   | - **Thực hành:** gọi thử Gemini API (generateContent) qua REST/SDK (bị lỗi vượt giới hạn rate limit của free tier khi gọi liên tục nhiều lần để test, phải tìm hiểu thêm về cơ chế quota/exponential backoff)                                                                                    | 28/05/2026   | 28/05/2026      |                |
| 6   | - Tìm hiểu luồng xử lý AI trong hệ thống: request người dùng &rarr; AWS Lambda (Core Logic) &rarr; Gemini API &rarr; trả kết quả (sinh nội dung)      | 29/05/2026   | 29/05/2026      |                |
| 7   | - Tham gia sự kiện **Meeting 30/5** cùng các thành viên FCJ (xem chi tiết tại mục "Các events đã tham gia" &rarr; Event 1)                              | 30/05/2026   | 30/05/2026      |                |
| CN  | - Đọc thêm tài liệu về Gemini API và cách viết prompt hiệu quả để chuẩn bị cho tuần 8                                                                   | 31/05/2026   | 31/05/2026      |                |

### Kết quả đạt được tuần 7:

* Nắm được sơ đồ kiến trúc tổng thể của dự án LunaGenZ và vai trò của từng service: CloudFront, Amplify, API Gateway, Lambda, DynamoDB, Gemini API, SQS, S3, SES, dù tuần đầu còn khá bối rối và cần mentor hỗ trợ giải thích thêm luồng dữ liệu giữa các service.
* Hiểu vị trí và vai trò của phần AI (bước sinh nội dung) trong toàn bộ luồng xử lý.
* Gọi thử thành công Gemini API để sinh nội dung mẫu, đồng thời rút kinh nghiệm về giới hạn rate limit của free tier sau khi gặp lỗi khi test liên tục.
* ...
