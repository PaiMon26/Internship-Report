---
title: "Event 5"
date: 2026-04-11
weight: 5
chapter: false
pre: " <b> 3.5. </b> "
---

# Reflection Report "Cloud Mastery 2026 - Security"

### Purpose of the Event

- Introduce foundational knowledge of security in cloud systems
- Provide knowledge about AWS Networking, IAM, and AWS services for system protection
- Share the mindset of designing secure systems with multiple layers
- Help participants better understand how to protect infrastructure and applications in production environments

### Speaker List

- **Lam An Thinh** - Presenter of the Networking on AWS session
- **Nguyen Phan Quoc Viet** - Co-presenter of the Networking on AWS session
- **Lam Tuan Kiet** - DevOps, presenter of the AWS Network & Application Protection session
- **Huynh Hoang Long** - FCAJ Cloud Engineer Ambassador, presenter of the Identity & Access Management session
- **Dang Thi Minh Thu** - FCAJ Cloud Engineer Ambassador, co-presenter of the Identity & Access Management session

### Key Highlights

#### 1. Networking on AWS

**What is AWS Networking**

- AWS Networking is the network foundation used to connect and organize resources in the cloud
- Its main components include VPC, CIDR, subnet, route table, internet gateway, and VPC endpoint
- It helps build systems with better separation, access control, and security

It can be seen as the foundation for designing network systems in AWS.

**VPC and CIDR**

- VPC is a private virtual network on AWS
- CIDR is used to define the IP range for the whole network system
- Choosing a suitable CIDR is very important because it affects subnet division and future system expansion

**Subnet**

- A subnet is a smaller network inside a VPC
- Subnets can be separated across different Availability Zones
- Dividing public and private subnets helps better control Internet access

**Internet Gateway and Route Table**

- Internet Gateway allows resources in a public subnet to connect to the Internet
- Route Table determines how traffic moves inside the system
- AWS Route Table works based on the longest prefix match principle and static routing

**NAT Gateway**

- NAT Gateway allows resources in private subnets to access the Internet
- At the same time, it prevents the Internet from initiating connections into private resources
- This is a mechanism that improves the security of internal resources

**Security Group**

- Security Group is a protection layer at the instance level
- It is stateful
- It only supports allow rules
- It helps control inbound and outbound connections for each specific resource

**NACL**

- NACL is a protection layer at the subnet level
- It is stateless
- It supports both allow and deny rules
- It is used to filter traffic at a broader level than Security Group

**Main insight**

- Designing networks on AWS is not only about connecting resources but also about controlling risk
- Security Group and NACL are two protection layers with different roles
- The important thing is to clearly understand how traffic flows through each layer in order to configure them properly

#### 2. AWS Network & Application Protection

**AWS WAF**

- AWS WAF is a service that helps protect web applications from common attacks
- It can filter and monitor HTTP/HTTPS requests
- It helps prevent SQL Injection and Cross-Site Scripting (XSS)
- It integrates with CloudFront, ALB, and API Gateway

**AWS Shield**

- AWS Shield is a service for DDoS protection
- It has two levels: Standard and Advanced
- Shield Standard is enabled automatically
- Shield Advanced provides stronger protection and cost support during large attacks

**AWS Network Firewall**

- AWS Network Firewall helps protect systems at the network level
- It supports both stateful and stateless traffic filtering
- It can control inbound and outbound traffic inside a VPC

**AWS Firewall Manager**

- AWS Firewall Manager is a centralized security management service across multiple AWS accounts
- It can deploy and manage rules for WAF, Shield, and Network Firewall
- It is suitable for multi-account systems that require consistent security policies

**Main insight**

- AWS provides multiple layers of protection for different levels of a system
- WAF protects the application layer, Shield protects against DDoS, and Network Firewall protects the network layer
- As systems grow, centralized management with Firewall Manager becomes increasingly important

#### 3. Identity & Access Management

**What is IAM**

- IAM is the service used for identity and access management on AWS
- It is used to manage users, groups, roles, and permissions
- It ensures both authentication and authorization in the system

**Best practices with IAM**

- Apply the principle of least privilege
- Delete root access keys after creation
- Use IAM users or roles instead of the root account for daily operations
- Avoid using `*` in Action or Resource
- Enable MFA for all users
- Rotate passwords and credentials regularly

**SSO**

- SSO is a mechanism that allows one login for access to multiple systems
- It supports centralized access management
- It is suitable when working with multiple AWS accounts in one organization

**SCP and Permission Boundaries**

- SCP is a policy at the organization level used to limit the maximum permissions of accounts
- SCP does not grant permissions, it only limits them
- Permission Boundary is used to limit the maximum permissions of a user or role inside a specific account
- These two mechanisms help control access more strictly in large systems

**Credential Rotation and IAM Access Analyzer**

- IAM User Access Keys are long-term credentials and do not expire automatically
- STS provides short-term credentials that are safer
- IAM Access Analyzer helps detect policies that may be public or overly permissive
- This is a useful tool for checking and improving the security level of the system

**Main insight**

- Security is not only about the network but also about controlling identity and access
- IAM is a very important part of AWS systems
- Proper permission management helps reduce many real-world security risks

### Key Learnings

#### Technology Mindset

- Gained a clearer understanding of how to build a multi-layer security system on AWS
- Recognized that security is not only about blocking access but also about controlling permissions and reducing blast radius
- Developed a broader perspective on designing secure systems across network, application, and identity layers

#### Technical Knowledge

Became familiar with:

- VPC, subnet, route table, internet gateway, NAT Gateway
- Security Group and NACL
- AWS WAF, AWS Shield, AWS Network Firewall, AWS Firewall Manager
- IAM, SSO, SCP, Permission Boundaries, IAM Access Analyzer

A basic understanding was gained of how to:

- Design secure networks on AWS
- Protect applications from common attack methods
- Manage users and permissions in a cloud environment

#### Application to Work

Possible applications:

- The mindset of layered security when building cloud systems
- The way to divide public and private subnets properly
- The principle of least privilege in access management

In the future:

- Build more secure systems when deploying on the cloud
- Apply IAM and AWS security services in real projects
- Improve control and reduce risks during system operations

### Experience During the Event

This event helped clarify security concepts in cloud environments, especially on AWS. The content was divided into several parts, including networking, application protection, and identity and access management, providing a more complete view of how cloud systems are protected in practice.

The networking session helped clarify the roles of VPC, subnet, route table, NAT Gateway, as well as the differences between Security Group and NACL. The sessions on AWS WAF, Shield, and Network Firewall were also very useful because they showed how AWS provides different layers of protection for systems. The IAM session was especially important because it is directly related to managing users, roles, and permissions within an organization.

However, since some topics were quite technical, much of the content was understood at a general level and would still require further study for deeper understanding and more effective real-world application.

### Lessons Learned

- Security in the cloud should be built in multiple layers and should not rely on only one mechanism
- Proper network design helps reduce blast radius and improve access control
- IAM is a very important foundation for protecting systems
- Least privilege, MFA, and credential rotation are principles that should be prioritized
- AWS provides many powerful security services, but their effectiveness depends on how they are configured and operated

### Some Photos from the Event

![Event photo 1](/images/events/event5_1.jpg)

![Event photo 2](/images/events/event5_2.jpg)

![Event photo 3](/images/events/event5_3.jpg)
