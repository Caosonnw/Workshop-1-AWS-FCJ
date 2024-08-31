---
title: "Session Management"
date: "`r Sys.Date()`"
weight: 1
chapter: false
---

# Hướng Dẫn Triển Khai Trang Web Trên AWS EC2 Bằng Docker và Cấu Hình NGINX

### Tổng quan

Bài hướng dẫn này cung cấp một cái nhìn tổng quan về quá trình triển khai một trang web lên AWS EC2, sử dụng Docker và NGINX. Bạn sẽ học cách tạo một instance EC2, cài đặt Docker, và xây dựng một container để chạy ứng dụng web của mình. Sau đó, chúng ta sẽ cấu hình NGINX để làm reverse proxy, điều phối các yêu cầu HTTP đến container của bạn một cách hiệu quả. Hướng dẫn này không chỉ giúp bạn hiểu rõ từng bước của quy trình triển khai mà còn giúp tối ưu hóa và bảo mật ứng dụng của bạn trên cloud.

### Nội dung

1.  [Giới thiệu](1-introduce/)
2.  [Các bước chuẩn bị](2-Prerequiste/)
3.  [Tạo kết nối đến máy chủ EC2](3-Accessibilitytoinstance/)
4.  [Quản lý session logs](4-s3log/)
5.  [Port Forwarding](5-Portfwd/)
6.  [Dọn dẹp tài nguyên](6-cleanup/)
