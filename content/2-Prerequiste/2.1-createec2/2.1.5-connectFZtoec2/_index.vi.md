---
title: "Kết nối FileZilla với EC2"
date: "`r Sys.Date()`"
weight: 5
chapter: false
pre: " <b> 2.1.5 </b> "
---

#### Kết nối FileZilla với EC2

1. Kết nối FileZilla với EC2

- Click **Icon đã đánh dấu**

![VPC](/images/10.png)

- Click **New site**

![VPC](/images/11.png)

- Bước 1: Các bạn có thể đổi tên tuỳ thích.
- Bước 2: Chọn SFTP - SSH File Transfer Protocol.
- Bước 3: Nhập Public IPv4 DNS.
  **Copy ở EC2 Instance**

![VPC](/images/31.png)

- Bước 4: Chọn key file.

![VPC](/images/32.png)

- Bước 5: Nhập tên user:"ubuntu".
- Bước 6: Chọn đường dẫn file key pair ở bước 2.1.2 đã tạo.
- Bước 7: Click **Connect**.

- Tích vào **Always trust this host, add this key to the cache**
- Và CLick **OK**

![VPC](/images/13.png)

- **Sau đó bạn kéo file deploy của bạn lên server.**