---
title: "Connect FileZilla to EC2"
date: "`r Sys.Date()`"
weight: 5
chapter: false
pre: " <b> 2.1.5 </b> "
---

#### Connect FileZilla to EC2

1. Connect FileZilla to EC2

- Click **Marked Icon**

![VPC](/images/10.png)

- Click **New site**

![VPC](/images/11.png)

- Step 1: You can change the name as you like.

- Step 2: Select SFTP - SSH File Transfer Protocol.

- Step 3: Enter Public IPv4 DNS.

**Copy to EC2 Instance**

![VPC](/images/31.png)

- Step 4: Select the key file.

![VPC](/images/32.png)

- Step 5: Enter username:"ubuntu".

- Step 6: Select the key pair file path created in step 2.1.2.

- Step 7: Click **Connect**.

- Check **Always trust this host, add this key to the cache**
- And click **OK**

![VPC](/images/13.png)

- **Then you drag your deploy file to the server.**
