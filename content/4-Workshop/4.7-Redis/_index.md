---
title: "Redis"
date: 2024-01-01
weight: 7
chapter: false
pre: " <b> 4.7. </b> "
---

#### Overview

Redis is used in the project as the caching layer. This workshop records the provisioning flow for the ElastiCache for Redis environment and the key settings required for integration.

#### Implementation steps

1. Open the **ElastiCache** console and choose to create a Redis deployment.

![Redis step 1](r.1.jpg)

![Redis step 2](r.2.jpg)

![Redis step 3](r.3.jpg)

2. Enter the basic deployment settings such as cluster name and engine details.

![Redis step 4](r.4.jpg)

![Redis step 5](r.5.jpg)

![Redis step 6](r.6.jpg)

3. Configure the node layout, capacity, and availability options.

![Redis step 7](r.7.jpg)

![Redis step 8](r.8.jpg)

![Redis step 9](r.9.jpg)

4. Configure VPC, subnet group, and security settings for the cluster.

![Redis step 10](r.10.jpg)

![Redis step 11](r.11.jpg)

![Redis step 12](r.12.jpg)

5. Review additional parameters and maintenance-related options.

![Redis step 13](r.13.jpg)

![Redis step 14](r.14.jpg)

6. Review the final configuration and submit the Redis deployment.

![Redis step 15](r.15.jpg)

![Redis step 16](r.16.jpg)

7. Wait for the cluster to become available and review its details.

![Redis step 17](r.17.jpg)

![Redis step 18](r.18.jpg)

8. Verify the endpoint and final Redis status for application integration.

![Redis step 19](r.19.jpg)
