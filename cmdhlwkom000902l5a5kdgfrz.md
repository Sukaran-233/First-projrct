---
title: "🚀 Day 5 of My #100DaysOfCloud Journey — Exploring IAM (Identity and Access Management) in AWS

Hello Cloud Enthusiasts! 👋

Today was all about secur"
datePublished: Thu Jul 24 2025 16:28:17 GMT+0000 (Coordinated Universal Time)
cuid: cmdhlwkom000902l5a5kdgfrz
slug: day-5-of-my-100daysofcloud-journey-exploring-iam-identity-and-access-management-in-aws-hello-cloud-enthusiasts-today-was-all-about-secur
tags: devops-journey

---

Hello Cloud Enthusiasts! 👋

Today was all about security and access control in AWS. I explored one of the most critical services — IAM (Identity and Access Management). Here's what I learned and practiced:

\---

🔐 What is IAM?

IAM stands for Identity and Access Management. It lets you:

Securely manage users, groups, and roles

Control who can access which AWS services and resources

Apply least privilege principle — giving only the permissions required

\---

🧠 Key Concepts I Covered

✅ IAM Users

Individual identities with long-term credentials.

I created a user named dev-admin and attached specific permissions.

✅ IAM Groups

Used to group users with similar permissions (e.g., Developers, Auditors).

Easier permission management.

✅ IAM Roles

Used for temporary access, especially for EC2 or Lambda to access other services securely.

✅ IAM Policies

JSON documents that define permissions.

Example: A policy to allow only S3 Read access.

{

"Version": "2012-10-17",

"Statement": \[

{

"Effect": "Allow",

"Action": \["s3:GetObject"\],

"Resource": \["arn:aws:s3:::my-bucket-name/\*"\]

}

\]

}

\---

🛠 Hands-on Practice

Created a custom IAM policy using the policy generator.

Attached policies to a user and group.

Assigned a role to an EC2 instance to allow S3 access without storing AWS credentials.

\---

🧩 Real-World Example

Imagine you're a system admin in a company where developers only need access to deploy on EC2 and read logs from CloudWatch. You:

Create a Developer group

Attach a custom policy that only allows ec2:\* and cloudwatch:Get\*

Add developers to the group — Simple and Secure ✅

\---

🔍 Lessons Learned

IAM is foundational for cloud security.

Always follow least privilege access.

IAM roles are better than hardcoding access keys in code.

\---

📌 What’s Next?

Tomorrow, I’ll be diving into AWS CLI to manage resources from the terminal. Stay tuned! 💻