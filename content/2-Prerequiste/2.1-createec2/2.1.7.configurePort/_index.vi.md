---
title: "Cấu hình Security Group và Nginx"
date: "`r Sys.Date()`"
weight: 7
chapter: false
pre: " <b> 2.1.7 </b> "
---

#### Cấu hình Security Group và Nginx

1. Cấu hình Security Group.

- Click **Security**
- CLick **Security groups**

![VPC](/images/17.png)

2. Add rule

- Chọn **Custom TCP**
- Bước 2: Nhập port đã chạy ở Container Docker
- Bước 3: Chọn Anywhere
- Click **Save rule**

![VPC](/images/18.png)

3. Deploy thành công trang web chạy bằng Docker với port ngoài 3000.

- Nhưng vấn đề vẫn còn là chưa thể di chuyển giữa các đường dẫn trang web. Chúng ta cần cấu hình Nginx.


![VPC](/images/20.png)

4. Cấu hình Nginx.

- Truy cập vào bash của container docker đang chạy trang web.
- Chỉnh sửa file nginx.conf:

```bash
user  nginx;
worker_processes  auto;
error_log  /var/log/nginx/error.log warn;
pid        /var/run/nginx.pid;
events {
  worker_connections  1024;
}
http {
  include       /etc/nginx/mime.types;
  default_type  application/octet-stream;
  log_format  main  '$remote_addr - $remote_user [$time_local] "$request" '
  '$status $body_bytes_sent "$http_referer" '
  '"$http_user_agent" "$http_x_forwarded_for"';
  access_log  /var/log/nginx/access.log  main;
  sendfile        on;
  #tcp_nopush     on;

  keepalive_timeout  65;
  #gzip  on;
  #include /etc/nginx/conf.d/*.conf;
server {
  listen 80;
  location / {
    root   /usr/share/nginx/html;
    index  index.html index.htm;
    try_files $uri $uri/ /index.html;
  }
}
}
```

- Sau khi hoàn thành, khởi động lại container.

![VPC](/images/21.png)

5. Thành công truy cập các endpoint trong trang web.

![VPC](/images/22.png)
