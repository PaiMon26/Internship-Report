---
title: "Event 4"
date: 2024-01-01
weight: 4
chapter: false
pre: " <b> 4.4. </b> "
---

# Summary Report: "Cloud Native & Infrastructure - Kubernetes, Elixir & IaC"

### Event Objectives

- Introduce foundational technologies in modern cloud-native systems
- Provide knowledge about Kubernetes, DevOps, and Infrastructure as Code
- Share design thinking for resilient and scalable systems
- Help attendees better understand how production systems are operated

### Speakers

- **Bao Huynh** - Junior Cloud Native Developer, Endava Vietnam; Founder / Head Lab, ITea Lab
- **Nguyen Ta Minh Triet** - R&D Member at ITea Lab, Swinburne Vietnam; SAP Developer Intern, Bosch GSV
- **Thinh Nguyen** - FCAJ Cloud Engineer Trainee

### Key Highlights

#### 1. Kubernetes and Amazon EKS

**What is Kubernetes**

- Kubernetes is a container orchestration system
- Supports application deployment
- Supports scaling
- Supports self-healing
- Supports load balancing

Kubernetes can be viewed as an "operating system for distributed systems".

**Amazon EKS**

- EKS is AWS managed Kubernetes service
- AWS manages the control plane such as the API server, etcd, and high availability
- Users manage worker nodes, applications, and runtime workloads

**Why use EKS**

- Reduces Kubernetes setup and operations effort
- Integrates well with the AWS ecosystem
- Makes production deployment faster

**Why still use vanilla Kubernetes**

- Avoid vendor lock-in
- Support multi-cloud strategies
- Allow deeper customization of networking, scheduling, and cluster behavior

**High-level EKS architecture**

- Control plane is managed by AWS
- Worker nodes run on EC2 or Fargate
- Networking is built on VPC
- Load balancing integrates with ALB or NLB

**Main insight**

- EKS simplifies operations and speeds up deployment
- Vanilla Kubernetes offers more flexibility and control
- The key is not choosing the "best" tool, but choosing the right trade-off for the system

#### 2. Elixir, BEAM, and Fault Tolerance

**Elixir and BEAM**

- Elixir is a functional programming language
- It runs on BEAM, the Erlang virtual machine

**Process model**

- Uses lightweight processes
- Does not share memory
- Communicates through message passing

Benefits:

- No locking required
- Reduced race conditions
- Good scalability for concurrent systems

**Fault tolerance**

- The core philosophy is "Let it crash"
- Instead of handling every possible error, the system allows failures and recovers automatically

**OTP**

- Provides supervisor trees
- Provides GenServer
- Provides restart strategies

This helps systems recover automatically when failures occur.

**Process supervision**

- Workers perform tasks
- Supervisors monitor workers
- If a worker fails, the supervisor can restart it automatically

**Hot code upgrade**

- Elixir supports updating code without downtime
- In modern environments this is often combined with rolling updates or blue-green deployment on Kubernetes

**DevOps and Elixir**

Tools mentioned in the event:

- Mix for builds
- Hex for packages
- ExUnit for testing
- Observer for monitoring

**Main insight**

- Systems should not focus only on preventing failure, but on recovering well from failure
- Compared with traditional defensive programming, Elixir follows a resilience-first mindset

#### 3. Infrastructure as Code

**What is IaC**

- Infrastructure as Code means managing infrastructure through code instead of manual operations

Benefits:

- Automation
- Reproducibility
- Version control

**Terraform**

- Supports multi-cloud environments
- Uses a declarative model to define the desired state

Typical basic structure:

- `main.tf`
- `variables.tf`
- `outputs.tf`
- `providers.tf`

Advanced structure may include:

- `modules` for reuse
- `environment` such as dev, staging, and prod
- `bootstrap` for initial setup

**AWS CloudFormation**

- AWS native IaC tool
- Uses YAML or JSON
- Also follows a declarative model

**AWS CDK**

- Lets engineers define infrastructure using code such as TypeScript or Python
- Follows the App -> Stack -> Construct model

**CDK vs Terraform**

- CDK is developer-friendly and AWS-focused
- Terraform is strong for multi-cloud and has a broad ecosystem

**LocalStack**

- Simulates AWS services locally
- Helps test systems without large cloud cost

**Main insight**

- The tool itself is not the most important factor
- Structure, conventions, and discipline in implementation matter more

### What I Learned

#### Technology Mindset

- Better understood how modern cloud-native systems are designed
- Recognized the importance of trade-offs when choosing technologies
- Gained a clearer resilience-first mindset for system design

#### Technical Knowledge

Became familiar with:

- Kubernetes and Amazon EKS
- Fault-tolerant systems with Elixir and BEAM
- Infrastructure as Code

Gained a basic understanding of how to:

- Deploy and operate production systems
- Manage infrastructure through code

#### Applying to Work

Can apply:

- IaC thinking in system management
- Container deployment concepts on cloud platforms

In the future:

- Build more scalable systems
- Apply Kubernetes and DevOps pipelines to real projects

### Event Experience

This event helped me explore several core technologies in modern cloud-native systems such as Kubernetes, Elixir, and Infrastructure as Code. The topics were presented clearly and gave me a better understanding of how production systems are designed, deployed, and operated in practice.

The EKS and IaC sections were especially useful because they provided practical perspectives on cloud infrastructure deployment. The Elixir and BEAM discussion also expanded my understanding of fault tolerance and system self-recovery.

However, because some topics were quite advanced, I mainly absorbed them at a high level and will need more time for deeper study.

### Lessons Learned

- There is no single best technology for every case, only the right choice for the system trade-off
- Modern systems should be designed to tolerate failure and recover automatically
- Infrastructure should be managed as code for automation and reuse
- Kubernetes, DevOps, and cloud-native practices are important foundations in large systems

### Some Event Photos

![Event photo 1](/images/events/event4_1.jpg)

![Event photo 2](/images/events/event4_2.jpg)

![Event photo 3](/images/events/event4_3.jpg)
