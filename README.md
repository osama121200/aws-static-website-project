# aws-static-website-project
 Secure, scalable static website hosted with AWS services ( S3, CloudFront, WAF, and CloudWatch )
 
# 📁 1. Project Overview
This project demonstrates how to securely host a fast and reliable static website using AWS services, while applying industry-level best practices.


Many developers can upload a website to AWS S3, but often overlook three critical aspects:

- Security: Preventing attacks and unauthorized access

- Performance: Ensuring global users get fast load times

- Monitoring: Tracking access and anomalies to ensure reliability

Why This Matters?

In real-world applications, slow or unsecured sites can lead to:

- User drop-off and bounce rates

- Vulnerabilities to hackers or bots

- No visibility into issues due to lack of monitoring

What We've Done

This project hosts a static Website using:

- S3 for scalable and durable storage

- CloudFront to deliver content globally with low latency

- ACM for HTTPS encryption (planned for future, domain-dependent)

- AWS WAF to filter malicious traffic

- CloudWatch to monitor requests and errors

# 🔨 3. Services Used


| AWS Service       | Purpose                                                          |
| ----------------- | ---------------------------------------------------------------- |
| **Amazon S3**     | Hosting the static website files                                 |
| **CloudFront**    | Delivering content globally with caching and HTTPS support       |
| **AWS WAF**       | Blocking bots, malicious traffic, SQLi, and XSS attempts         |
| **CloudWatch**    | Monitoring CloudFront requests and WAF activity                  |
| **ACM (planned)** | Enabling HTTPS using SSL certificates (skipped due to no domain) |
