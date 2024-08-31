---
title: "Configuring Security Group and Nginx"
date: "`r Sys.Date()`"
weight: 7
chapter: false
pre: " <b> 2.1.7 </b> "
---

#### Configuring Security Group and Nginx

1. Configure Security Group.

- Click **Security**
- Click **Security groups**

![VPC](/images/17.png)

2. Add rule

- Select **Custom TCP**
- Step 2: Enter the port running in Docker Container
- Step 3: Select Anywhere
- Click **Save rule**

![VPC](/images/18.png)

3. Successfully deploy the website running on Docker with port other than 3000.

- But the problem is still not being able to move between website paths. We need to configure Nginx.

![VPC](/images/20.png) 4. Configure Nginx.

- Access the bash of the docker container running the website.
- Edit nginx.conf file:

```bash
  user nginx;
  worker_processes auto;
  error_log /var/log/nginx/error.log warn;
  pid /var/run/nginx.pid;
  events { worker_connections 1024;
  } http { include /etc/nginx/mime.types;
  default_type application/octet-stream;
  log_format main '$remote_addr - $remote_user [$time_local] "$request" ' '$status $body_bytes_sent "$http_referer" ' '"$http_user_agent" "$http_x_forwarded_for"';
  access_log /var/log/nginx/access.log main;
  sendfile on;
  #tcp_nopush on;

keepalive_timeout 65;
#gzip on;
#include /etc/nginx/conf.d/\*.conf;
server {
listen 80;
location / {
root /usr/share/nginx/html;
index index.html index.htm;
try_files $uri $uri/ /index.html;
}
}
}

```

- Once completed, restart the container.

![VPC](/images/21.png)

5. Successfully accessed the endpoints in the website.

![VPC](/images/22.png)
