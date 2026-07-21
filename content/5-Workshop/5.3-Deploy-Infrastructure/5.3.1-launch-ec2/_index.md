---
title : "Launch an Amazon EC2 Instance"
date : 2026-07-10
weight : 1
chapter : false
pre : " <b> 5.3.1 </b> "
---

In this section, you will launch an **Amazon EC2** instance to host the Smart Parking application.

The EC2 instance will serve as the application server, where the Smart Parking backend and related services will be deployed.

### Create an EC2 Instance

1. Sign in to the **AWS Management Console**.

2. In the search bar, type **EC2**, then select **EC2** to open the Amazon EC2 Console.

![ec2-console](/images/2-Proposal/anh3.jpg)

3. In the navigation pane, choose **Instances**, then click **Launch instances**.

![launch-instance](/images/2-Proposal/anh5.jpg)

4. Configure the instance with the following settings.

+ **Name:** `SmartParking`

+ **Amazon Machine Image (AMI):**
    + Ubuntu Server 24.04 LTS (64-bit)

+ **Instance type:**
    + t3.micro (Free Tier eligible)

![instance-config](/images/2-Proposal/anh6.jpg)

5. Create or select an existing **Key Pair** for SSH access.

![keypair](/images/2-Proposal/anh7.jpg)

6. Configure the network settings.

+ Select your Smart Parking **VPC**.
+ Choose the appropriate **Public Subnet**.
+ Enable **Auto-assign Public IP**.
+ Create or select a **Security Group**.

Allow the following inbound rules:

| Type | Port |
|------|------|
| SSH | 22 |
| HTTP | 80 |
| HTTPS | 443 |

![security-group](/images/2-Proposal/anh8.jpg)

7. Keep the remaining settings as default, then click **Launch Instance**.

![launch](/images/2-Proposal/anh9.jpg)

8. Wait until the instance status changes to **Running** and both status checks are passed.

![running](/images/2-Proposal/anh10.jpg)

The Amazon EC2 instance is now ready for configuring the Smart Parking application.