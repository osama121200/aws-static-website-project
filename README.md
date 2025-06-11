# aws-static-website-project
 Secure, scalable static website hosted with AWS services ( S3, CloudFront, WAF, and CloudWatch )
 
# 📁 1. Project Overview
This project demonstrates how to securely host a fast and reliable static website using AWS services, while applying industry-level best practices.


Many developers can upload a website to AWS S3, but often overlook three critical aspects:

- Security: Preventing attacks and unauthorized access

- Performance: Ensuring global users get fast load times

- Monitoring: Tracking access and anomalies to ensure reliability

**Why This Matters?**

In real-world applications, slow or unsecured sites can lead to:

- User drop-off and bounce rates

- Vulnerabilities to hackers or bots

- No visibility into issues due to lack of monitoring

**What We've Done:**

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

# 🧱 4. Implementation Steps
Here’s a breakdown of each step with what was done:

**1. Upload Website to S3**

- Created a new S3 bucket with public access enabled.

- Uploaded index.html and assets (CSS, JS, images).

- Enabled Static Website Hosting.

- Made bucket content publicly accessible with proper bucket policy.

**2. Connect to CloudFront**

- Created a CloudFront distribution pointing to S3 static hosting endpoint.

- Set Viewer Protocol Policy to “Redirect HTTP to HTTPS”.

- Got a ".cloudfront.net" URL for global delivery.

**3. Add Security via AWS WAF**

- Created a Web ACL and attached it to CloudFront.

- Added Core Rule Set, Anonymous IP Block, and SQL Injection filters.

- Created a rate-based rule to block traffic if request count from an IP exceeded 100 in 5 mins.

**4. Monitor with CloudWatch**

- Created a custom dashboard.

- Added widgets for:

    Allowed requests

    Cache hits and misses

    WAF blocked requests

- Observed real-time and historical traffic patterns.

**5. (Optional ACM Step Skipped)**

- Skipped due to no custom domain. But in production, ACM + Route 53 + HTTPS redirect would be crucial.

# 🧠 5. Business Impact

- **Speed:** CloudFront drastically reduced load time via caching and edge locations.

- **Security:** WAF filtered bad bots, XSS, SQLi attempts, protecting the site from attacks.

- **Scalability:** S3 + CloudFront scales automatically with traffic.

- **Monitoring:** CloudWatch gave full visibility, allowing proactive response to anomalies.

# 📸 Screenshots
All setup and configuration screenshots are available inside the images/ folder for reference.


