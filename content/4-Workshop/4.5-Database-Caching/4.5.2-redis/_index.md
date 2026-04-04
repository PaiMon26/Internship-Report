---
title: "Provision Redis"
date: 2026-04-04
weight: 2
chapter: false
pre: " <b> 4.5.2. </b> "
---

#### Overview

This section presents the steps to provision **Redis** on **ElastiCache** and configure its application integration.

#### Implementation steps

1. Before creating the cache, open **ElastiCache > Subnet groups** to create the subnet group for Redis.

![Redis step 1](r.1.jpg)

2. Create `lunchsync-redis-subnets`, choose `lunchsync-vpc`, and add the two private subnets from different AZs.

![Redis step 2](r.2.jpg)

3. Review the subnet group list and confirm that `lunchsync-redis-subnets` has been created.

![Redis step 3](r.3.jpg)

4. Open **Redis OSS caches** and start creating a new cluster.

![Redis step 4](r.4.jpg)

5. Choose **Redis OSS**, use a **Node-based cluster**, and keep **Cluster mode = Disabled**.

![Redis step 5](r.5.jpg)

6. Name the cluster `lunchsync-redis`, deploy it in **AWS Cloud**, enable **Multi-AZ** and **Auto-failover**, and keep port `6379`.

![Redis step 6](r.6.jpg)

7. Choose node type `cache.t3.micro` and attach the cluster to the subnet group `lunchsync-redis-subnets`.

![Redis step 7](r.7.jpg)

8. Place the primary and replica in different Availability Zones so failover can work correctly.

![Redis step 8](r.8.jpg)

9. In **Security**, enable **Encryption at rest**, enable **Encryption in transit = Required**, and attach security group `redis-sg`.

![Redis step 9](r.9.jpg)

10. Configure backup and maintenance by enabling automatic backups, setting retention, defining a maintenance window, and enabling minor version upgrades.

![Redis step 10](r.10.jpg)

11. Enable **Slow logs** and send them to CloudWatch Logs.

![Redis step 11](r.11.jpg)

12. Enable **Engine logs** as well and configure the corresponding CloudWatch log group.

![Redis step 12](r.12.jpg)

13. Review backup, maintenance, and logging settings before creating the cluster.

![Redis step 13](r.13.jpg)

14. After the cluster becomes available, review the primary endpoint, reader endpoint, node type, and overall `Available` status.

![Redis step 14](r.14.jpg)

15. If you want to harden security further, open **Modify > Security** and recheck TLS, AUTH token, and the attached security group.

![Redis step 15](r.15.jpg)

16. Move to **AWS Secrets Manager**, choose **Other type of secret**, and store values such as `auth_token`, `host`, and `port` for Redis.

![Redis step 16](r.16.jpg)

17. Name the secret `lunchsync/redis`.

![Redis step 17](r.17.jpg)

18. Skip rotation if it is not needed yet, keep the secret static, and finish creating it.

![Redis step 18](r.18.jpg)

19. Return to ElastiCache and verify the node list, primary endpoint, and reader endpoint so the backend can integrate with Redis.

![Redis step 19](r.19.jpg)
