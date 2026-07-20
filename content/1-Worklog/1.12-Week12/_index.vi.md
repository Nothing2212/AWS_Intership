---
title: "Worklog Tuần 12"
date: 2026-06-29
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Mục tiêu tuần 12:

* Tối ưu prompt và chi phí/độ trễ khi gọi Gemini API, tìm hiểu CI/CD tự động triển khai Amplify từ GitHub.
* Rà soát bảo mật hệ thống (Secrets Manager, IAM permissions), kiểm thử hồi quy và hoàn thiện tài liệu, báo cáo tổng kết thực tập.

{{% notice note %}}
Đây là chặng cuối của kỳ thực tập (29/06/2026 - 30/07/2026), gộp chung thành tuần worklog cuối cùng.
{{% /notice %}}

### Các công việc cần triển khai trong tuần này:
| Ngày                | Công việc                                                                                                              | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------ | ------------ | --------------- | -------------- |
| 29/6 - 5/7           | - Tối ưu prompt cho Gemini API: giảm số token, đo và so sánh độ trễ/chi phí giữa các model Gemini (Flash so với Pro)      | 29/06/2026   | 05/07/2026      |                |
| 6/7 - 12/7           | - Tìm hiểu & thực hành cấu hình AWS Amplify CI/CD: kết nối GitHub repo, auto-deploy khi có commit mới (lần deploy đầu tiên bị lỗi do cấu hình sai build command, phải xem log build và sửa lại), kiểm thử rollback khi build lỗi | 06/07/2026   | 12/07/2026      |                |
| 13/7 - 19/7          | - Rà soát bảo mật: AWS Secrets Manager, phân quyền IAM cho các Lambda (phát hiện một Lambda đang được gán quyền rộng hơn mức cần thiết, phải thu hẹp lại theo least-privilege) <br> - Kiểm thử hồi quy (regression test) toàn bộ hệ thống, sửa các lỗi phát sinh | 13/07/2026   | 19/07/2026      |                |
| Thứ 2 - Thứ 5 (20-23/7) | - Chuẩn bị và demo phần AI của dự án LunaGenZ cho mentor, ghi nhận góp ý và chỉnh sửa <br> - Hoàn thiện tài liệu kỹ thuật mô tả kiến trúc & luồng xử lý AI | 20/07/2026   | 23/07/2026      |                |
| Thứ 6 - Thứ 5 (24-30/7) | - Hoàn thiện báo cáo thực tập tổng kết, bàn giao công việc, nộp báo cáo đúng hạn                                        | 24/07/2026   | 30/07/2026      |                |

### Kết quả đạt được tuần 12:

* Tối ưu prompt giúp giảm số token và chi phí gọi Gemini API, cải thiện độ trễ phản hồi; so sánh được sự đánh đổi giữa các model Gemini để chọn model phù hợp cho từng use case.
* Cấu hình thành công CI/CD trên AWS Amplify để tự động triển khai frontend mỗi khi có commit mới trên GitHub, sau khi tự sửa được lỗi build command sai ở lần deploy đầu tiên.
* Rà soát và củng cố bảo mật cho toàn hệ thống: quản lý secret qua Secrets Manager, phát hiện và thu hẹp lại một Lambda có quyền IAM rộng hơn mức cần thiết về đúng nguyên tắc least-privilege.
* Hoàn thành kiểm thử hồi quy, đảm bảo pipeline AI hoạt động ổn định.
* Hoàn thiện tài liệu kỹ thuật, demo phần AI của dự án LunaGenZ và nộp báo cáo thực tập tổng kết đúng hạn (30/07/2026).
* Nhìn lại toàn bộ quá trình thực tập, tự đánh giá bản thân nắm được kiến trúc và luồng xử lý AI của dự án LunaGenZ ở mức khá; một số mảng như tối ưu chi phí/hiệu năng Gemini API, CI/CD và bảo mật hệ thống vẫn còn có thể tìm hiểu sâu hơn nếu có thêm thời gian.
