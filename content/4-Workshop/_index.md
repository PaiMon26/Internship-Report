---
title: "Workshop"
date: 2024-01-01
weight: 4
chapter: false
pre: " <b> 4. </b> "
---

# AWS Workshop Series

#### Overview

This section provides an end-to-end deployment guide for the **LunchSync** system on AWS, based on the actual architecture used in the project. It covers DNS and SSL/TLS setup, VPC networking, load balancing, authentication, static content delivery, relational database provisioning, and caching.

The flow follows the real deployment order: domain and certificate preparation first, networking and security setup next, then authentication and data layers to make the cloud environment production-ready.

- **Route53 and ACM** to prepare domain and certificate resources
- **VPC, Security Group, and ALB** to build the networking path for the application
- **Cognito** to prepare authentication resources
- **S3 and CloudFront** to publish static content securely
- **RDS** to provision the relational database layer
- **Redis** to add caching support for the application

#### Content

1. [Workshop overview](4.1-Workshop-overview/)
2. [Route53 and ACM](4.2-Route53-ACM/)
3. [VPC, Security Group, and ALB](4.3-VPC-SecurityGroup-ALB/)
4. [Cognito](4.4-Cognito/)
5. [S3 and CloudFront](4.5-S3-CloudFront/)
6. [RDS](4.6-RDS/)
7. [Redis](4.7-Redis/)
