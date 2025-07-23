---
title: "🚀 Day 4: AWS CloudTrail, Pre-Signed URLs & VPC Endpoints Explained with Real-World Use Cases

👋 Hello DevOps Enthusiasts!
Welcome to Day 4 of my AWS"
datePublished: Wed Jul 23 2025 13:00:43 GMT+0000 (Coordinated Universal Time)
cuid: cmdfz1suk000802jj7feo41eu
slug: day-4-aws-cloudtrail-pre-signed-urls-and-vpc-endpoints-explained-with-real-world-use-cases-hello-devops-enthusiasts-welcome-to-day-4-of-my-aws
tags: devops-articles

---

📘 1. What is AWS CloudTrail?

📌 Definition:

AWS CloudTrail is a service that records all the API calls made in your AWS account. It helps track who did what, when, and from where.

💡 Real-World Example:

Imagine you're managing a production server, and suddenly an EC2 instance is terminated. You didn’t do it — who did?

CloudTrail helps answer that!

➡ Go to CloudTrail logs

➡ See who ran the TerminateInstances API

➡ Know the time, IP address, and user

🔐 Use Case:

Security auditing, compliance, and troubleshooting suspicious activities.

\---

🔗 2. What are Pre-Signed URLs in AWS S3?

📌 Definition:

A pre-signed URL gives temporary access to private files in S3 without making them public.

💡 Real-World Example:

Let’s say you store customer invoices as PDFs in a private S3 bucket. A customer wants to download their invoice.

Instead of making the file public: ➡ You generate a pre-signed URL

➡ Send it to the customer

➡ It works for 10 minutes (or any time you set)

➡ Secure, simple, and temporary

🔐 Use Case:

Sharing files securely with clients, partners, or internal teams without exposing your S3 bucket.

\---

🌐 3. What are VPC Endpoints in AWS?

📌 Definition:

A VPC Endpoint allows your EC2 or other AWS services to communicate with AWS services like S3 or DynamoDB without going through the public internet.

💡 Real-World Example:

You have a backend app in a private subnet that needs to access S3. Without a VPC endpoint, your data goes to the internet and back (even within AWS!).

With a VPC Endpoint: ➡ Your traffic stays inside AWS's private network

➡ Faster, safer, and more cost-effective

🔐 Use Case:

Private EC2 instance uploading logs to S3, without exposing the instance to the internet.

\---

✅ Summary of Today:

Feature Purpose Real Use Case

CloudTrail Audit API calls Check who terminated an EC2 instance

Pre-Signed URL Temporary file access from S3 Share invoice PDFs securely with customers

VPC Endpoint Private communication with AWS services EC2 accessing S3 without internet exposure

\---

🧠 What I Learned:

Today I realized that security, access control, and auditing are core parts of DevOps in the cloud. Even simple actions like sharing a file or accessing logs require thoughtful design.

\---

📌 Next Steps for Day 5:

I'll explore IAM Roles vs IAM Policies, and start hands-on with creating a secure S3 bucket using the AWS CLI.

\---

🔗 Follow My Journey:

💼 LinkedIn

💻 GitHub

📝 Hashnode Blog

🙌 Thanks for reading! Let’s keep building and learning together.

#100DaysOfCloud #AWS #DevOpsWithSukaran #LearnInPublic