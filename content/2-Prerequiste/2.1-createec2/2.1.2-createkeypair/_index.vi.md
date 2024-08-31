---
title: "Tạo key pair"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: " <b> 2.1.2 </b> "
---

#### Tạo key pair

1. Tạo **Key pair**.

- Trong Amazon EC2 (Elastic Compute Cloud), một key pair là một cặp khóa mật mã được sử dụng để đăng nhập an toàn vào các phiên bản EC2 của bạn. Key pair bao gồm hai phần:

- Public Key (khóa công khai): Được lưu trữ trên phiên bản EC2 mà bạn tạo ra. Khi bạn tạo một phiên bản mới, bạn có thể chỉ định public key từ một key pair đã tồn tại hoặc tạo một key pair mới.

- Private Key (khóa bí mật): Được tải về và lưu trữ cục bộ trên máy tính của bạn khi bạn tạo key pair. Khóa này được sử dụng để đăng nhập vào phiên bản EC2 của bạn thông qua SSH (Secure Shell). Chỉ bạn mới có quyền truy cập vào private key này.

- Khi bạn kết nối đến phiên bản EC2 qua SSH, private key sẽ được sử dụng để xác thực rằng bạn có quyền truy cập vào phiên bản đó. Nếu không có private key tương ứng với public key trên phiên bản, bạn sẽ không thể truy cập được.

- Nói cách khác, key pair giúp đảm bảo rằng chỉ những người có private key mới có thể truy cập vào phiên bản EC2, bảo vệ phiên bản khỏi truy cập trái phép.

**Bước này sẽ rất quan trọng và sẽ cần có file .ppk để kết nối FileZilla với EC2 Ubuntu**

- **FileZilla** là một phần mềm ứng dụng mã nguồn mở được sử dụng để truyền tải tệp tin giữa máy tính cá nhân của bạn và máy chủ từ xa qua giao thức FTP (File Transfer Protocol) và các giao thức liên quan như SFTP (SSH File Transfer Protocol) và FTPS (FTP Secure).

- Click **Create new key pair**

![VPC](/images/3.png)

2. Điền thông tin tạo mới key pair

- Bước 1: Điền tên key pair
- Bước 2: Chọn định dạng file
- Bước 3: Click **Create key pair**

![VPC](/images/4.png)
