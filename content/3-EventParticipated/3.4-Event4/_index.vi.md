---
title: "Event 4"
date: 2024-01-01
weight: 4
chapter: false
pre: " <b> 4.4. </b> "
---

# Bài thu hoạch "Cloud Native & Infrastructure - Kubernetes, Elixir & IaC"

### Mục Đích Của Sự Kiện

- Giới thiệu các công nghệ nền tảng trong hệ thống cloud-native hiện đại
- Cung cấp kiến thức về Kubernetes, DevOps và Infrastructure as Code
- Chia sẻ tư duy thiết kế hệ thống resilient và scalable
- Giúp người tham dự hiểu rõ hơn về cách vận hành hệ thống production

### Danh Sách Diễn Giả

- **Bao Huynh** - Junior Cloud Native Developer, Endava Vietnam; Founder / Head Lab, ITea Lab
- **Nguyen Ta Minh Triet** - R&D Member at ITea Lab, Swinburne Vietnam; SAP Developer Intern, Bosch GSV
- **Thinh Nguyen** - FCAJ Cloud Engineer Trainee

### Nội Dung Nổi Bật

#### 1. Kubernetes và Amazon EKS

**Kubernetes là gì**

- Kubernetes là hệ thống quản lý container
- Hỗ trợ deploy application
- Hỗ trợ scaling
- Hỗ trợ self-healing
- Hỗ trợ load balancing

Có thể xem Kubernetes như một "hệ điều hành cho hệ thống phân tán".

**Amazon EKS**

- EKS là dịch vụ Kubernetes được AWS quản lý
- AWS chịu trách nhiệm control plane như API server, etcd và high availability
- Người dùng quản lý worker nodes, application và workload runtime

**Vì sao sử dụng EKS**

- Giảm công sức cài đặt và vận hành Kubernetes
- Tích hợp tốt với hệ sinh thái AWS
- Giúp triển khai production nhanh hơn

**Vì sao vẫn dùng Kubernetes thuần**

- Tránh vendor lock-in
- Hỗ trợ multi-cloud
- Có khả năng tùy chỉnh sâu hơn về network, scheduler và cluster behavior

**Kiến trúc EKS tổng quan**

- Control plane do AWS quản lý
- Worker nodes chạy trên EC2 hoặc Fargate
- Networking sử dụng VPC
- Load balancing tích hợp với ALB hoặc NLB

**Insight chính**

- EKS giúp đơn giản hóa việc vận hành và triển khai nhanh
- Kubernetes thuần cho mức độ linh hoạt và kiểm soát cao hơn
- Điều quan trọng không phải chọn công nghệ nào "tốt nhất", mà là chọn trade-off phù hợp với hệ thống

#### 2. Elixir, BEAM và Fault-Tolerance

**Elixir và BEAM**

- Elixir là ngôn ngữ lập trình functional
- Chạy trên BEAM, tức Erlang Virtual Machine

**Process model**

- Sử dụng lightweight process
- Không share memory
- Giao tiếp với nhau bằng message passing

Lợi ích:

- Không cần lock
- Giảm race condition
- Scale tốt trong hệ thống concurrent

**Fault-tolerance**

- Triết lý chính là "Let it crash"
- Thay vì cố xử lý mọi lỗi, hệ thống cho phép process crash và tự phục hồi

**OTP**

- Cung cấp Supervisor tree
- Cung cấp GenServer
- Cung cấp restart strategy

Điều này giúp hệ thống tự phục hồi khi có lỗi xảy ra.

**Process supervision**

- Worker đảm nhận xử lý công việc
- Supervisor giám sát worker
- Khi worker gặp lỗi, supervisor có thể tự động restart

**Hot code upgrade**

- Elixir hỗ trợ update code mà không cần downtime
- Tuy nhiên trong thực tế hiện đại thường kết hợp với rolling update hoặc blue-green deployment trên Kubernetes

**DevOps và Elixir**

Các công cụ được nhắc đến:

- Mix để build
- Hex để quản lý package
- ExUnit để test
- Observer để monitor

**Insight chính**

- Hệ thống không cần cố tránh mọi lỗi, mà cần được thiết kế để tự recover
- So với hướng defensive programming truyền thống, Elixir theo tư duy resilience-first

#### 3. Infrastructure as Code

**IaC là gì**

- Infrastructure as Code là cách quản lý hạ tầng bằng code thay vì thao tác thủ công

Lợi ích:

- Automation
- Reproducibility
- Version control

**Terraform**

- Hỗ trợ multi-cloud
- Theo mô hình declarative, mô tả trạng thái mong muốn

Cấu trúc cơ bản thường gồm:

- `main.tf`
- `variables.tf`
- `outputs.tf`
- `providers.tf`

Cấu trúc nâng cao có thể gồm:

- `modules` để tái sử dụng
- `environment` như dev, staging, prod
- `bootstrap` cho thiết lập ban đầu

**AWS CloudFormation**

- Là công cụ IaC của AWS
- Sử dụng YAML hoặc JSON
- Cũng theo hướng declarative

**AWS CDK**

- Viết infrastructure bằng code như TypeScript hoặc Python
- Theo mô hình App -> Stack -> Construct

**CDK và Terraform**

- CDK phù hợp với developer và tập trung tốt cho AWS
- Terraform mạnh ở multi-cloud và hệ sinh thái rộng

**LocalStack**

- Mô phỏng AWS ở local
- Giúp test hệ thống mà không tốn nhiều chi phí cloud

**Insight chính**

- Tool không phải yếu tố quan trọng nhất
- Điều quan trọng hơn là structure, quy ước và kỷ luật trong quá trình triển khai

### Những Gì Học Được

#### Tư Duy Công Nghệ

- Hiểu rõ hơn cách thiết kế hệ thống cloud-native hiện đại
- Nhận ra tầm quan trọng của trade-off khi chọn công nghệ
- Tiếp cận tư duy xây dựng hệ thống resilient và có khả năng tự phục hồi

#### Kiến Thức Kỹ Thuật

Làm quen với:

- Kubernetes và Amazon EKS
- Fault-tolerant system với Elixir và BEAM
- Infrastructure as Code

Hiểu sơ bộ cách:

- Deploy và vận hành hệ thống production
- Quản lý hạ tầng bằng code

#### Ứng Dụng Vào Công Việc

Có thể áp dụng:

- Tư duy IaC trong quản lý hệ thống
- Cách deploy ứng dụng container trên cloud

Trong tương lai:

- Xây dựng hệ thống scalable hơn
- Áp dụng Kubernetes và DevOps pipeline vào các project thực tế

### Trải nghiệm trong event

Sự kiện giúp em tiếp cận với nhiều công nghệ nền tảng trong hệ thống cloud-native như Kubernetes, Elixir và Infrastructure as Code. Các nội dung được trình bày rõ ràng, giúp em hiểu hơn về cách các hệ thống production được thiết kế, triển khai và vận hành trong thực tế.

Phần chia sẻ về EKS và IaC đặc biệt hữu ích vì mang lại góc nhìn thực tiễn về việc triển khai hạ tầng trên cloud. Nội dung về Elixir và BEAM cũng mở rộng thêm cách nhìn về fault-tolerance và khả năng tự phục hồi của hệ thống.

Tuy nhiên, do một số nội dung mang tính chuyên sâu, em chủ yếu tiếp cận ở mức tổng quan và cần tìm hiểu thêm để hiểu sâu hơn về các công nghệ này.

### Bài học rút ra

- Không có công nghệ tốt nhất cho mọi trường hợp, chỉ có lựa chọn phù hợp với trade-off của hệ thống
- Hệ thống hiện đại cần được thiết kế để chịu lỗi và tự phục hồi
- Infrastructure nên được quản lý bằng code để dễ tự động hóa và tái sử dụng
- Kubernetes, DevOps và cloud-native là nền tảng quan trọng trong các hệ thống lớn

### Một số hình ảnh khi tham gia sự kiện

![Hình ảnh sự kiện 1](/images/events/event4_1.jpg)

![Hình ảnh sự kiện 2](/images/events/event4_2.jpg)

![Hình ảnh sự kiện 3](/images/events/event4_3.jpg)
