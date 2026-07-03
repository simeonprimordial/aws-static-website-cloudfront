![AWS](https://img.shields.io/badge/AWS-S3%20%7C%20CloudFront-orange)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![License](https://img.shields.io/badge/License-MIT-blue)

# Production-Ready Static Website Hosting on AWS

> A production-ready static website hosting solution built on AWS using Amazon S3 as a private origin and Amazon CloudFront with Origin Access Control (OAC) for secure, scalable, and globally distributed content delivery.

---

## Project Overview

This project demonstrates how to deploy a secure, scalable, and cost-effective static website on Amazon Web Services (AWS).

Unlike traditional approaches that expose an Amazon S3 bucket directly to the internet, this implementation follows AWS security best practices by keeping the S3 bucket private and allowing access only through Amazon CloudFront using Origin Access Control (OAC).

The architecture provides:

- Secure content delivery
- Global low-latency access
- Automatic scalability
- High availability
- Data protection through versioning
- Encryption at rest
- HTTPS-ready architecture
- Low operational overhead

---

## Business Problem

A startup requires a secure and highly available solution to host its corporate website.

The solution must:

- Deliver static content globally with low latency
- Eliminate server management
- Protect website assets from public access
- Scale automatically with increasing traffic
- Minimize operational costs
- Support future enhancements such as custom domains and HTTPS certificates

---

## Solution Architecture

```
                    Internet Users
                           │
                           ▼
                CloudFront Distribution
               (HTTPS + Edge Locations)
                           │
                 Origin Access Control
                           │
                           ▼
                Amazon S3 (Private Bucket)
             ┌─────────────────────────────┐
             │ index.html                  │
             │ styles.css                  │
             │ script.js                   │
             └─────────────────────────────┘
```

A professional Draw.io diagram is available in the `architecture/` directory.

---

## AWS Services Used

| Service | Purpose |
|----------|---------|
| Amazon S3 | Stores static website files |
| Amazon CloudFront | Global Content Delivery Network (CDN) |
| Origin Access Control (OAC) | Secure access from CloudFront to S3 |
| AWS Identity and Access Management (IAM) | Access management |
| Amazon S3 Versioning | Object recovery |
| Amazon S3 Encryption | Data protection at rest |

---

## Project Structure

```
aws-static-website-cloudfront/
│
├── README.md
├── LICENSE
│
├── architecture/
│   ├── architecture.drawio
│   └── architecture.png
│
├── docs/
│   ├── implementation.md
│   ├── testing.md
│   ├── troubleshooting.md
│   ├── cost-analysis.md
│   ├── security.md
│   └── lessons-learned.md
│
├── screenshots/
│
└── website/
    ├── index.html
    ├── styles.css
    └── script.js
```

---

## Features

- Private Amazon S3 bucket
- CloudFront CDN
- Origin Access Control (OAC)
- HTTPS support
- Amazon S3 Versioning
- Server-side encryption
- Global content delivery
- Highly scalable architecture
- Cost-efficient hosting
- Production-oriented design

---

## Deployment Summary

The deployment consisted of the following high-level steps:

1. Build the static website locally.
2. Create a private Amazon S3 bucket.
3. Enable versioning.
4. Enable server-side encryption.
5. Upload website assets.
6. Create a CloudFront distribution.
7. Configure Origin Access Control (OAC).
8. Attach the generated bucket policy.
9. Configure the default root object.
10. Validate the deployment.

Detailed implementation steps are available in:

```
docs/implementation.md
```

---

## Validation

The deployment was validated using the following checks:

- Website loads successfully
- HTTPS is enforced
- CSS and JavaScript load correctly
- CloudFront distribution serves content successfully
- Browser returns HTTP 200 responses
- Static assets are accessible
- Cache behaviour verified

Detailed validation results are available in:

```
docs/testing.md
```

---

## Security Considerations

This implementation follows several AWS security best practices:

- Private S3 bucket
- Block Public Access enabled
- Origin Access Control (OAC)
- Server-side encryption enabled
- Versioning enabled
- Principle of Least Privilege
- HTTPS-ready architecture

Further security recommendations are documented in:

```
docs/security.md
```

---

## Cost Optimization

The architecture is optimized for low operational cost by:

- Using Amazon S3 instead of EC2
- Leveraging CloudFront edge caching
- Eliminating server management
- Automatically scaling with demand
- Reducing origin requests through caching

Detailed cost analysis is available in:

```
docs/cost-analysis.md
```

---

## Challenges Encountered

Some of the implementation challenges included:

- Configuring Origin Access Control correctly
- Applying the required S3 bucket policy
- Understanding CloudFront cache behaviour
- Managing cache invalidation after content updates

Solutions to these issues are documented in:

```
docs/troubleshooting.md
```

---

## Lessons Learned

During this project, the following concepts were reinforced:

- Differences between S3 website endpoints and private origins
- CloudFront edge caching
- Origin Access Control (OAC)
- Amazon S3 Versioning
- Cache invalidation
- CDN architecture
- AWS security best practices

Complete reflections are available in:

```
docs/lessons-learned.md
```

---

## Future Improvements

Possible enhancements include:

- Route 53 custom domain
- AWS Certificate Manager (ACM)
- AWS WAF
- GitHub Actions CI/CD
- Terraform deployment
- CloudFront Functions
- Lambda@Edge
- Monitoring and logging improvements

---

## Screenshots

The `screenshots/` directory contains deployment evidence, including:

- Local website preview
- CloudFront distribution
- Origin Access Control
- Bucket policy
- Successful website deployment

---

## Skills Demonstrated

- Amazon S3
- Amazon CloudFront
- CDN Architecture
- Origin Access Control
- IAM
- AWS Security Best Practices
- Static Website Hosting
- High Availability
- Scalability
- Cost Optimization
- Git & GitHub Documentation

---

## Author

**simeon siaka**

AWS | DevOps | Cloud Infrastructure Engineer

Building production-ready AWS solutions while documenting architecture, implementation, and operational best practices.