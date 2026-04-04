---
title: "RDS"
date: 2024-01-01
weight: 6
chapter: false
pre: " <b> 4.6. </b> "
---

#### Overview

Amazon RDS is used in the project as the relational database layer. This workshop documents the main steps to provision the database instance and prepare the networking settings required by the backend.

#### Implementation steps

1. Open the **RDS console** and start the database creation workflow.

![RDS step 0.1](rds.0.1.jpg)

2. Review the initial RDS landing and creation options.

![RDS step 0.2](rds.0.2.jpg)

3. Choose the database creation method and confirm the basic engine setup.

![RDS step 0.3](rds.0.3.jpg)

4. Continue to the detailed configuration screen for the new database.

![RDS step 0.4](rds.0.4.jpg)

5. Select the database engine and template suitable for the environment.

![RDS step 1](rds.1.jpg)

6. Configure credentials, instance class, storage, and availability settings.

![RDS step 2](rds.2.jpg)

![RDS step 3](rds.3.jpg)

7. Configure connectivity settings such as VPC, subnet group, and security groups.

![RDS step 4](rds.4.jpg)

![RDS step 5](rds.5.jpg)

8. Set the database name and other additional options needed by the backend.

![RDS step 6](rds.6.jpg)

![RDS step 7](rds.7.jpg)

9. Review the final configuration and create the database instance.

![RDS step 8](rds.8.jpg)

10. Verify the database status and endpoint information after provisioning completes.

![RDS step 9](rds.9.jpg)
