---
title: "Day 3: EC2 on AWS - launch , Connect and host like a pro"
datePublished: Tue Jul 22 2025 05:00:24 GMT+0000 (Coordinated Universal Time)
cuid: cmde2g8wy000r02l23l4eg5ul
slug: day-3-ec2-on-aws-launch-connect-and-host-like-a-pro
tags: aws-devops-ec2-100daysofcloud-cloudcomputin

---

🔍 What is EC2?

Amazon EC2 (Elastic Compute Cloud) lets us rent virtual servers (called instances) in the cloud. You can run applications, host websites, test software, and much more—without needing physical hardware.

\&gt; 💡 Real-Life Example:

Just like you’d rent a hotel room, EC2 lets you rent a remote computer to run your app or site.

\---

🛠️ What I Did Today

✅ Launched My First EC2 Instance

Opened EC2 Dashboard

Clicked Launch Instance

Chose:

OS: Amazon Linux 2

Instance Type: t2.micro (Free Tier)

Key Pair: Created .pem file

Network: Default VPC

Storage: 8GB

Launched the instance

✅ Connected via SSH (from WSL or CMD)

chmod 400 my-key.pem

ssh -i my-key.pem ec2-user@&lt;your-ec2-ip&gt;

✅ Installed and Ran a Simple Python Web Server

sudo yum update -y

sudo yum install python3 -y

echo "Welcome to Day 3!" &gt; index.html

python3 -m http.server 8000

🧪 Accessed Webpage in Browser:

http://&lt;your-ec2-ip&gt;:8000

\---

🔐 EC2 Security Note

Make sure your Security Group allows inbound rule on port 22 (SSH) and 8000 (for web access).

\---

✅ Key Takeaways

EC2 gives you full control of a virtual server in the cloud

You manage storage, access, and software

Great for hosting, testing, and deploying apps

Easy to scale, stop, or terminate when needed

\---

🔜 What’s Next?

Tomorrow I’ll be exploring:

S3 Buckets

Uploading files

Hosting a static website from S3

\---

🔗 Stay Connected

📝 Blog: DevOpsWithSukaran

🔗 Tags: #AWS, #DevOps, #EC2, #100DaysOfCloud