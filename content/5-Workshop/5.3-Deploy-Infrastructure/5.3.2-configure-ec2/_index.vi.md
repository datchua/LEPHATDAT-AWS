````md
---
title : "Cấu hình EC2 Instance"
date : 2026-07-10
weight : 2
chapter : false
pre : " <b> 5.3.2 </b> "
---

Trong phần này, bạn sẽ cấu hình **Amazon EC2 Instance** để chuẩn bị cho việc triển khai ứng dụng **Smart Parking**.

Quá trình cấu hình bao gồm cập nhật hệ điều hành, cài đặt các phần mềm cần thiết và kiểm tra môi trường trước khi triển khai ứng dụng.

## Kết nối đến EC2 Instance

1. Mở **Amazon EC2 Console**.

2. Chọn EC2 Instance **SmartParking**.

3. Nhấn **Connect**.

![connect](/images/2-Proposal/anh11.jpg)

4. Chọn **EC2 Instance Connect** (hoặc kết nối bằng SSH nếu muốn), sau đó nhấn **Connect**.

![instance-connect](/images/2-Proposal/anh12.jpg)

Đến đây, bạn đã kết nối thành công với EC2 Instance.

---

## Cập nhật hệ điều hành

Chạy các lệnh sau để cập nhật các gói phần mềm của hệ thống.

```bash
sudo apt update
sudo apt upgrade -y
```

![update]

---

## Cài đặt các phần mềm cần thiết

Cài đặt Git và Nginx.

```bash
sudo apt install git -y
sudo apt install nginx -y
```

Cài đặt .NET SDK.

```bash
sudo apt install dotnet-sdk-8.0 -y
```

Kiểm tra phiên bản sau khi cài đặt.

```bash
dotnet --version
git --version
nginx -v
```

![install]

---

## Cấu hình tường lửa (Firewall)

Cho phép lưu lượng truy cập HTTP và HTTPS.

```bash
sudo ufw allow 80
sudo ufw allow 443
sudo ufw enable
```

Kiểm tra trạng thái của Firewall.

```bash
sudo ufw status
```

![firewall]

---

## Kiểm tra môi trường

Xác nhận rằng tất cả các phần mềm cần thiết đã được cài đặt thành công.

```bash
dotnet --version
git --version
systemctl status nginx
```

![verify]

---

## Tổng kết

Chúc mừng! Bạn đã cấu hình thành công **Amazon EC2 Instance** cho hệ thống **Smart Parking**.

Máy chủ hiện đã sẵn sàng để triển khai ứng dụng **Smart Parking** ở phần tiếp theo.
````
