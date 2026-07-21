---
title : "Introduction"
date : 2026-07-10
weight : 1
chapter : false
pre : " <b> 5.1. </b> "
---

#### Hệ thống Smart Parking

+ **Smart Parking System** là giải pháp quản lý bãi đỗ xe thông minh được triển khai trên nền tảng AWS. Hệ thống cho phép người dùng tìm kiếm chỗ đỗ còn trống, đặt chỗ trước, thanh toán trực tuyến và nhận thông báo theo thời gian thực.
+ Hệ thống được xây dựng dựa trên các dịch vụ AWS theo kiến trúc microservices nhằm đảm bảo khả năng mở rộng, tính sẵn sàng cao, bảo mật và quản lý tài nguyên hiệu quả.

#### Tổng quan Workshop

Trong workshop này, bạn sẽ triển khai hệ thống Smart Parking trên AWS với kiến trúc bảo mật, linh hoạt và có khả năng mở rộng.

Kiến trúc của hệ thống bao gồm các thành phần chính sau:

+ **Amazon VPC** cung cấp môi trường mạng riêng và an toàn cho toàn bộ hệ thống.
+ **Application Load Balancer (ALB)** phân phối lưu lượng truy cập đến các dịch vụ backend.
+ **Amazon ECS (Fargate)** triển khai các microservices của Smart Parking, bao gồm Authentication, User, Parking, Booking, Payment và Notification.
+ **Amazon RDS MySQL** lưu trữ dữ liệu của hệ thống như người dùng, bãi đỗ xe, đặt chỗ và lịch sử thanh toán.
+ **Amazon S3** lưu trữ hình ảnh bãi đỗ xe, mã QR và các tệp được tải lên.
+ **AWS Lambda**, **Amazon SNS** và **Amazon SES** xử lý các tác vụ tự động và gửi thông báo đến người dùng.
+ **Amazon CloudWatch** giám sát hiệu năng hệ thống, thu thập nhật ký (logs) và hỗ trợ theo dõi hoạt động của ứng dụng.
+ **AWS IAM** và **AWS Secrets Manager** quản lý quyền truy cập và bảo vệ các thông tin nhạy cảm của hệ thống.

Trong workshop này, bạn sẽ lần lượt triển khai hạ tầng AWS, cài đặt và cấu hình các dịch vụ cần thiết, triển khai ứng dụng Smart Parking và kiểm tra để đảm bảo toàn bộ hệ thống hoạt động ổn định.

![overview](/images/2-Proposal/smart_parking_architecture.jpg)