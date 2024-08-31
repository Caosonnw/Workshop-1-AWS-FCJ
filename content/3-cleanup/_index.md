+++
title = "Cleaning up resources"
date = 2021
weight = 3
chapter = false
pre = "<b>3. </b>"
+++

We will perform the following steps to delete the resources we created in this lab.

#### Delete EC2 instance

1. Delete the key pair

- Go to [EC2 service management interface](https://console.aws.amazon.com/ec2/v2/home)
- Click **Key Pairs**.
- Click to select the original key pair we created.
- Click **Actions** and then select Delete

![VPC](/images/33.png)

![VPC](/images/34.png)

2. Remove and delete Security Groups.

- Click **Security Groups**
- Click to select the Security Groups that are currently matched to the original EC2.
- Click **Actions** ![VPC](/images/35.png) - Click **Delete Security Groups** ![VPC](/images/36.png) - Click **Delete** ![VPC](/images/37.png) 3. Stop and delete EC2.

- Click **Instance** - Click the initially created Instance.
- Click **Instance state** ![VPC](/images/38.png) - Click to select **Terminate (delete) instance** ![VPC](/images/39.png) - Click **Terminate (delete)** ![VPC](/images/40.png)
