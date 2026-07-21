
---
title : "Triển khai ứng dụng Smart Parking"
date : 2026-07-10
weight : 3
chapter : false
pre : " <b> 5.3.3 </b> "
---

Trong phần này, bạn sẽ triển khai ứng dụng **Smart Parking** lên **Amazon EC2 Instance**.

Quá trình triển khai bao gồm tải các tệp của ứng dụng lên EC2, khởi chạy ứng dụng và kiểm tra xem hệ thống Smart Parking có thể truy cập thông qua địa chỉ IP công khai của EC2 hay không.

## Tải ứng dụng lên EC2

1. Sao chép ứng dụng **Smart Parking** đã được publish lên EC2 Instance.

Bạn có thể sử dụng **SCP**, **WinSCP** hoặc bất kỳ công cụ truyền tệp nào mà bạn muốn.

![upload](/images/2-Proposal/anh13.jpg)

---

## Publish ứng dụng

Nếu ứng dụng chưa được publish, hãy thực hiện lệnh sau trong thư mục chứa dự án.

```bash
dotnet publish -c Release -o publish
```

Sau khi publish hoàn tất, tải thư mục **publish** vừa tạo lên EC2 Instance.

![publish](/images/2-Proposal/anh14.jpg)

---

## Chạy ứng dụng

Di chuyển đến thư mục **publish**.

```bash
cd publish
```

Khởi chạy ứng dụng Smart Parking.

```bash
dotnet SmartParking.dll
```

Nếu ứng dụng khởi động thành công, màn hình sẽ hiển thị thông báo tương tự như sau:

```text
Now listening on: http://localhost:5000
Application started.
```

![run](/images/2-Proposal/anh15.jpg)

---

## Kiểm tra kết quả triển khai

Mở trình duyệt web.

Nhập địa chỉ IP công khai (Public IP) của EC2 Instance.

```text
http://<EC2-Public-IP>:5000
```

Nếu quá trình triển khai thành công, trang chủ của ứng dụng **Smart Parking** sẽ được hiển thị.

![homepage](/images/2-Proposal/anh16.jpg)

---

## Tổng kết

Chúc mừng!

Bạn đã triển khai thành công ứng dụng **Smart Parking** trên **Amazon EC2**.

Ứng dụng hiện đang hoạt động và sẵn sàng cho việc cấu hình cơ sở dữ liệu cũng như tích hợp thêm các dịch vụ AWS ở các phần tiếp theo.
````
