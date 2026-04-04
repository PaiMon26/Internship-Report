---
title: "Configure Route53 hosted zone"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 4.2.1. </b> "
---

1. Open the **Route53 console** and navigate to **Hosted zones**.

![Route53 step 1](route53.1.jpg)

2. Start creating a hosted zone for the domain or subdomain used by the application.

![Route53 step 2](route53.2.jpg)

3. Review the generated DNS records, especially the default NS and SOA records.

![Route53 step 3](route53.3.jpg)

4. Save the hosted zone configuration so it can be reused during certificate validation and later DNS mapping.

![Route53 step 4](route53.4.jpg)
