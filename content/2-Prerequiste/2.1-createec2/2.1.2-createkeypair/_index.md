---
title: "Create key pair"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: " <b> 2.1.2 </b> "
---

#### Create key pair

1. Create **Key pair**.

- In Amazon EC2 (Elastic Compute Cloud), a key pair is a pair of cryptographic keys used to securely log in to your EC2 instances. A key pair consists of two parts:

- Public Key: Stored on the EC2 instance you create. When you create a new instance, you can specify a public key from an existing key pair or create a new key pair.

- Private Key: Downloaded and stored locally on your computer when you create a key pair. This key is used to log in to your EC2 instance via SSH (Secure Shell). Only you have access to this private key.

- When you connect to an EC2 instance via SSH, the private key is used to authenticate that you have access to the instance. Without the private key that matches the public key on the instance, you will not be able to access it.

- In other words, the key pair helps ensure that only those with the private key can access the EC2 instance, protecting the instance from unauthorized access.

**This step is very important and will require a .ppk file to connect FileZilla to EC2 Ubuntu**

- **FileZilla** is an open source software application used to transfer files between your personal computer and a remote server using the FTP (File Transfer Protocol) protocol and related protocols such as SFTP (SSH File Transfer Protocol) and FTPS (FTP Secure).

- Click **Create new key pair**

![VPC](/images/3.png)

2. Fill in the information to create a new key pair

- Step 1: Fill in the key pair name
- Step 2: Select the file format
- Step 3: Click **Create key pair**

![VPC](/images/4.png)
