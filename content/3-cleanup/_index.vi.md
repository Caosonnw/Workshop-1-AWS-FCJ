+++
title = "Dọn dẹp tài nguyên  "
date = 2021
weight = 3
chapter = false
pre = "<b>3. </b>"
+++

Chúng ta sẽ tiến hành các bước sau để xóa các tài nguyên chúng ta đã tạo trong bài thực hành này.

#### Xóa EC2 instance

1. Xoá key pair

- Truy cập [giao diện quản trị dịch vụ EC2](https://console.aws.amazon.com/ec2/v2/home)
- Click **Key Pairs**.
- Click chọn key pair ban đầu chúng ta đã tạo.
- Click **Actions** và sau đó chọn Delete

![VPC](/images/33.png)

![VPC](/images/34.png)

2. Gỡ và xoá Security Groups.

- Click **Security Groups**
- Click chọn Security Groups đang được match với EC2 ban đầu.
- Click **Actions**

![VPC](/images/35.png)

- Click chọn **Delete Security Groups**

![VPC](/images/36.png)

- Click **Delete**

![VPC](/images/37.png)

3. Dừng và xoá EC2.

- Click **Instance**
- Click Instance ban đầu đã tạo.
- Click **Instance state**

![VPC](/images/38.png)

- Click chọn **Terminate (delete) instance**

![VPC](/images/39.png)

- Click **Terminate (delete)**

![VPC](/images/40.png)
