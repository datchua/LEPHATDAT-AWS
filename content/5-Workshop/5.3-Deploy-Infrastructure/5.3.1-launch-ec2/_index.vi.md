
---
title : "Khởi tạo một Amazon EC2 Instance"
date : 2026-07-10
weight : 1
chapter : false
pre : " <b> 5.3.1 </b> "
---

Trong phần này, bạn sẽ khởi tạo một **Amazon EC2** để triển khai ứng dụng **Smart Parking**.

EC2 sẽ đóng vai trò là **máy chủ ứng dụng (Application Server)**, nơi triển khai backend của Smart Parking cùng các dịch vụ liên quan.

### Tạo một EC2 Instance

1. Đăng nhập vào **AWS Management Console**.

2. Trong thanh tìm kiếm, nhập **EC2**, sau đó chọn **EC2** để mở giao diện **Amazon EC2 Console**.

![ec2-console](/images/2-Proposal/anh3.jpg)

3. Trong thanh điều hướng bên trái, chọn **Instances**, sau đó nhấn **Launch instances**.

![launch-instance](/images/2-Proposal/anh5.jpg)

4. Cấu hình EC2 với các thông số sau:

- **Tên (Name):**
  - `SmartParking`

- **Amazon Machine Image (AMI):**
  - Ubuntu Server 24.04 LTS (64-bit)

- **Loại Instance (Instance type):**
  - `t3.micro` (Đủ điều kiện sử dụng Free Tier)

![instance-config](/images/2-Proposal/anh6.jpg)

5. Tạo mới hoặc chọn **Key Pair** đã có để sử dụng khi kết nối SSH đến EC2.

![keypair](/images/2-Proposal/anh7.jpg)

6. Cấu hình **Network Settings**.

- Chọn **VPC** dành cho hệ thống Smart Parking.
- Chọn **Public Subnet** phù hợp.
- Bật tùy chọn **Auto-assign Public IP**.
- Tạo mới hoặc chọn **Security Group**.

Thiết lập các **Inbound Rules** như sau:

| Loại | Cổng |
|------|------|
| SSH | 22 |
| HTTP | 80 |
| HTTPS | 443 |

![security-group](/images/2-Proposal/anh8.jpg)

7. Giữ nguyên các thiết lập còn lại mặc định, sau đó nhấn **Launch Instance** để khởi tạo EC2.

![launch](/images/2-Proposal/anh9.jpg)

8. Chờ đến khi trạng thái của EC2 chuyển sang **Running** và cả hai **Status Checks** đều hiển thị **Passed**.

![running](/images/2-Proposal/anh10.jpg)

Amazon EC2 Instance đã được tạo thành công và sẵn sàng để triển khai ứng dụng **Smart Parking**.
```
