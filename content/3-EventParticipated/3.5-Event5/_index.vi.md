---
title: "Event 5"
date: 2026-04-11
weight: 5
chapter: false
pre: " <b> 3.5. </b> "
---

# Bài thu hoạch "Cloud Mastery 2026 - Security"

### Mục Đích Của Sự Kiện

- Giới thiệu các kiến thức nền tảng về bảo mật trong hệ thống cloud
- Cung cấp kiến thức về AWS Networking, IAM và các dịch vụ bảo vệ hệ thống trên AWS
- Chia sẻ tư duy thiết kế hệ thống an toàn theo nhiều lớp
- Giúp người tham dự hiểu rõ hơn về cách bảo vệ hạ tầng và ứng dụng trong môi trường production

### Danh Sách Diễn Giả

- **Lam An Thinh** - Presenter chủ đề Networking on AWS
- **Nguyen Phan Quoc Viet** - Đồng trình bày chủ đề Networking on AWS
- **Lam Tuan Kiet** - DevOps, presenter chủ đề AWS Network & Application Protection
- **Huynh Hoang Long** - FCAJ Cloud Engineer Ambassador, presenter chủ đề Identity & Access Management
- **Dang Thi Minh Thu** - FCAJ Cloud Engineer Ambassador, đồng trình bày chủ đề Identity & Access Management

### Nội Dung Nổi Bật

#### 1. Networking on AWS

**AWS Networking là gì**

- AWS Networking là nền tảng mạng dùng để kết nối và tổ chức các tài nguyên trên cloud
- Các thành phần chính gồm VPC, CIDR, subnet, route table, internet gateway và VPC endpoint
- Giúp xây dựng hệ thống có tính phân tách, kiểm soát truy cập và tăng độ an toàn

Có thể xem đây là phần nền tảng để thiết kế hệ thống mạng trong AWS.

**VPC và CIDR**

- VPC là mạng riêng ảo trên AWS
- CIDR dùng để xác định dải IP cho toàn bộ hệ thống mạng
- Việc chọn CIDR phù hợp rất quan trọng để dễ chia subnet và mở rộng hệ thống sau này

**Subnet**

- Subnet là mạng con bên trong VPC
- Có thể tách subnet theo từng Availability Zone
- Việc chia public subnet và private subnet giúp kiểm soát tốt hơn việc truy cập từ Internet

**Internet Gateway và Route Table**

- Internet Gateway cho phép tài nguyên trong public subnet kết nối ra Internet
- Route Table quyết định đường đi của traffic trong hệ thống
- AWS Route Table hoạt động dựa trên nguyên tắc longest prefix match và định tuyến tĩnh

**NAT Gateway**

- NAT Gateway cho phép tài nguyên trong private subnet truy cập ra Internet
- Đồng thời ngăn Internet chủ động kết nối từ bên ngoài vào private resources
- Đây là cơ chế giúp tăng mức độ an toàn cho các tài nguyên nội bộ

**Security Group**

- Security Group là lớp bảo vệ ở mức instance
- Có tính stateful
- Chỉ hỗ trợ allow rule
- Giúp kiểm soát kết nối đến và đi từ từng tài nguyên cụ thể

**NACL**

- NACL là lớp bảo vệ ở mức subnet
- Có tính stateless
- Hỗ trợ cả allow và deny rule
- Dùng để lọc traffic ở phạm vi rộng hơn so với Security Group

**Insight chính**

- Thiết kế mạng trên AWS không chỉ để kết nối tài nguyên mà còn để kiểm soát rủi ro
- Security Group và NACL là hai lớp bảo vệ có vai trò khác nhau
- Điều quan trọng là phải hiểu rõ cách traffic đi qua từng lớp để cấu hình phù hợp

#### 2. AWS Network & Application Protection

**AWS WAF**

- AWS WAF là dịch vụ giúp bảo vệ ứng dụng web trước các tấn công phổ biến
- Có thể lọc và giám sát các HTTP/HTTPS request
- Hỗ trợ ngăn chặn SQL Injection và Cross-Site Scripting (XSS)
- Tích hợp với CloudFront, ALB và API Gateway

**AWS Shield**

- AWS Shield là dịch vụ bảo vệ chống DDoS
- Gồm hai mức là Standard và Advanced
- Shield Standard được bật tự động
- Shield Advanced cung cấp thêm khả năng bảo vệ nâng cao và hỗ trợ chi phí khi xảy ra tấn công lớn

**AWS Network Firewall**

- AWS Network Firewall giúp bảo vệ hệ thống ở cấp mạng
- Hỗ trợ stateful và stateless traffic filtering
- Có thể kiểm soát lưu lượng inbound và outbound trong VPC

**AWS Firewall Manager**

- AWS Firewall Manager là dịch vụ quản lý bảo mật tập trung trên nhiều AWS account
- Có thể triển khai và quản lý rule cho WAF, Shield và Network Firewall
- Phù hợp với hệ thống nhiều tài khoản cần chính sách bảo mật đồng nhất

**Insight chính**

- AWS cung cấp nhiều lớp bảo vệ ứng với từng tầng của hệ thống
- WAF bảo vệ lớp ứng dụng, Shield bảo vệ trước DDoS, còn Network Firewall bảo vệ ở tầng mạng
- Khi hệ thống mở rộng, việc quản lý tập trung bằng Firewall Manager trở nên rất cần thiết

#### 3. Identity & Access Management

**IAM là gì**

- IAM là dịch vụ quản lý định danh và phân quyền trên AWS
- Dùng để quản lý user, group, role và permission
- Đảm bảo việc xác thực và phân quyền trong hệ thống

**Best practices với IAM**

- Áp dụng nguyên tắc least privilege
- Xóa root access key sau khi tạo
- Sử dụng IAM user hoặc role thay vì root account cho các thao tác thường ngày
- Tránh dùng dấu `*` trong Action hoặc Resource
- Bật MFA cho tất cả người dùng
- Thực hiện rotate password và credential định kỳ

**SSO**

- SSO là cơ chế đăng nhập một lần để truy cập nhiều hệ thống
- Hỗ trợ quản lý truy cập tập trung
- Phù hợp khi làm việc với nhiều AWS account trong cùng một tổ chức

**SCP và Permission Boundaries**

- SCP là policy ở mức tổ chức, dùng để giới hạn quyền tối đa của các account
- SCP không cấp quyền mà chỉ dùng để giới hạn quyền
- Permission Boundary dùng để giới hạn quyền tối đa của user hoặc role trong một account cụ thể
- Hai cơ chế này giúp kiểm soát quyền truy cập chặt chẽ hơn trong hệ thống lớn

**Credential Rotation và IAM Access Analyzer**

- IAM User Access Keys là credential dài hạn và không tự hết hạn
- STS cung cấp credential ngắn hạn và an toàn hơn
- IAM Access Analyzer giúp phát hiện các policy có nguy cơ public hoặc quá rộng
- Đây là công cụ hữu ích để kiểm tra và cải thiện mức độ an toàn của hệ thống

**Insight chính**

- Security không chỉ nằm ở network mà còn nằm ở việc kiểm soát danh tính và quyền truy cập
- IAM là thành phần rất quan trọng trong hệ thống AWS
- Việc quản lý quyền hợp lý sẽ giúp giảm thiểu nhiều rủi ro bảo mật trong thực tế

### Những Gì Học Được

#### Tư Duy Công Nghệ

- Hiểu rõ hơn cách xây dựng hệ thống bảo mật nhiều lớp trên AWS
- Nhận ra rằng security không chỉ là chặn truy cập mà còn là kiểm soát quyền và giảm blast radius
- Tiếp cận tư duy thiết kế hệ thống an toàn từ network, application đến identity

#### Kiến Thức Kỹ Thuật

Làm quen với:

- VPC, subnet, route table, internet gateway, NAT Gateway
- Security Group và NACL
- AWS WAF, AWS Shield, AWS Network Firewall, AWS Firewall Manager
- IAM, SSO, SCP, Permission Boundaries, IAM Access Analyzer

Hiểu sơ bộ cách:

- Thiết kế mạng an toàn trên AWS
- Bảo vệ ứng dụng trước các hình thức tấn công phổ biến
- Quản lý người dùng và quyền truy cập trong môi trường cloud

#### Ứng Dụng Vào Công Việc

Có thể áp dụng:

- Tư duy chia lớp bảo mật khi xây dựng hệ thống cloud
- Cách phân chia public subnet và private subnet hợp lý
- Áp dụng nguyên tắc least privilege trong quản lý quyền truy cập

Trong tương lai:

- Xây dựng hệ thống an toàn hơn khi triển khai trên cloud
- Áp dụng IAM và các dịch vụ security của AWS vào các project thực tế
- Tăng khả năng kiểm soát và giảm rủi ro trong quá trình vận hành hệ thống

### Trải nghiệm trong event

Sự kiện giúp làm rõ hơn các khía cạnh bảo mật trong môi trường cloud, đặc biệt là trên nền tảng AWS. Nội dung được chia thành nhiều phần từ networking, bảo vệ ứng dụng cho đến quản lý định danh và quyền truy cập, qua đó mang lại góc nhìn tổng quan hơn về cách một hệ thống cloud được bảo vệ trong thực tế.

Phần chia sẻ về AWS Networking giúp làm rõ hơn vai trò của VPC, subnet, route table, NAT Gateway cũng như sự khác nhau giữa Security Group và NACL. Phần AWS WAF, Shield và Network Firewall cũng rất hữu ích vì cho thấy cách AWS cung cấp các lớp bảo vệ khác nhau cho hệ thống. Nội dung IAM đặc biệt quan trọng vì liên quan trực tiếp đến việc quản lý người dùng, role và quyền hạn trong tổ chức.

Tuy nhiên, do một số nội dung mang tính kỹ thuật khá cao, phần lớn kiến thức được tiếp cận ở mức tổng quan và cần tìm hiểu thêm để hiểu sâu hơn cũng như áp dụng hiệu quả vào thực tế.

### Bài học rút ra

- Security trong cloud cần được xây dựng theo nhiều lớp, không nên phụ thuộc vào một cơ chế duy nhất
- Việc thiết kế network hợp lý giúp giảm blast radius và tăng khả năng kiểm soát truy cập
- IAM là nền tảng rất quan trọng trong việc bảo vệ hệ thống
- Least privilege, MFA và credential rotation là những nguyên tắc cần ưu tiên áp dụng
- AWS cung cấp nhiều dịch vụ bảo mật mạnh, nhưng hiệu quả phụ thuộc vào cách cấu hình và vận hành

### Một số hình ảnh khi tham gia sự kiện

![Hình ảnh sự kiện 1](/images/events/event5_1.jpg)

![Hình ảnh sự kiện 2](/images/events/event5_2.jpg)

![Hình ảnh sự kiện 3](/images/events/event5_3.jpg)
