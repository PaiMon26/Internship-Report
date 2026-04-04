---
title: "Event 3"
date: 2026-03-21
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

# Bài thu hoạch "FCAJ Community Day"

### Mục Đích Của Sự Kiện

- Giới thiệu về GoTymeX và cơ hội nghề nghiệp trong lĩnh vực công nghệ
- Chia sẻ về DevOps trong thời đại Generative AI (GenAIOps)
- Cung cấp kiến thức về cách xây dựng và vận hành hệ thống AI hiện đại
- Giúp người tham dự hiểu rõ hơn về pipeline DevOps và AI system

### Danh Sách Diễn Giả

- **Hai Bui** - Engineering Manager, GoTymeX
- **Phuc Dang** - Cloud Architect, GoTymeX
- **Phap Nguyen** - Cloud Engineer, VPBank
- **Phat Pham** - Software Engineer, Katalon
- **Nghi Danh** - AI Engineer, Renova Cloud
- **Phong Nguyen** - Senior Software Engineer, Sympli
- **Thinh Nguyen** - DevOps Engineer, FCAJ

### 1. Giới thiệu về GoTymeX

GoTymeX là một tổ chức hoặc tập đoàn hoạt động trong lĩnh vực công nghệ và tài chính số. Doanh nghiệp này nằm trong Top 100 tập đoàn có ảnh hưởng toàn cầu, với định hướng phát triển các hệ thống công nghệ hiện đại phục vụ lĩnh vực fintech.

Các lĩnh vực chính:

- Digital banking
- Công nghệ tài chính (fintech)
- Hệ thống công nghệ quy mô lớn

Ngoài ra, trong sự kiện cũng đề cập rằng GoTymeX đang tuyển dụng, đặc biệt ở các vị trí liên quan đến kỹ sư phần mềm, DevOps và AI.

### 2. GenAIOps Essential – DevOps for Generative AI Applications

#### Vì sao DevOps trở nên essential?

Hệ thống ngày càng:

- Phức tạp
- Phân tán

Cần:

- Automation
- Continuous delivery
- Khả năng scale nhanh

#### DevOps truyền thống trên AWS

Flow:

- Code
- Build
- Test
- Release
- Deploy
- Operate
- Monitor

Toolchain:

- Planning: Git, Jira
- CI: Jenkins
- Build: Maven, Gradle
- Test: JUnit
- Deploy: Docker
- Monitor: logging tools

#### CI/CD trên AWS

Pipeline:

- Developer
- GitHub
- AWS CodePipeline
- AWS CodeBuild
- Amazon ECR
- Amazon ECS

Đặc điểm:

- Multi-stage giữa dev và prod
- Có bước manual approval
- Infrastructure được quản lý bằng CloudFormation theo mô hình IaC

#### Key DevOps Capabilities

- Continuous Integration (CI)
- Continuous Delivery / Deployment (CD)
- Infrastructure as Code (IaC)
- Monitoring & Logging
- Collaboration

#### GenAIOps Pipeline

Flow:

- Define use-case
- Model selection
- Model adaptation
- Prompt engineering
- RAG
- Fine-tuning
- App integration
- Deployment
- Monitoring

#### Monitoring cho AI

Theo dõi:

- Input user
- Output model
- Latency

Feedback loop giúp:

- Improve model
- Debug hallucination

#### AgentCore (AI runtime)

Agent gồm:

- Instruction
- Tools
- Context
- Memory

Chạy trên:

- Amazon Bedrock

#### Insight chính

- DevOps đang chuyển thành GenAIOps
- AI system cần pipeline tương tự như software system

### 3. Shipping Code in the Agentic Era

#### Agent viết code theo workflow mới

Flow:

- Assign task cho agent như Claude, Codex, Kiro
- Agent tạo branch
- Code, commit, push
- Tạo PR, sau đó merge

#### Multi-agent system

- Mỗi agent xử lý một task

Có thể:

- Spawn nhiều agent con
- Chạy song song

#### Pi-messenger architecture

Input:

- User goal
- Task list

Core:

- Spawn sub-agents
- Quản lý lifecycle

Output:

- Completed tasks
- Validated code

Capability:

- Parallel execution
- Event-driven
- Xử lý theo dependency

#### Limitation hiện tại

- Chỉ xử lý một repo tại một thời điểm
- Không có memory dài hạn
- Cần người giám sát

Kết luận:

- Coding agent chưa fully production-ready

Hướng cải tiến:

- Multi-repo orchestration
- Custom toolchains
- Remote management

#### Insight chính

- AI không thay thế developer
- AI sẽ trở thành AI teammate hỗ trợ dev

### 4. Production-Grade Multimodal GenAI on AWS

#### AI là một hệ thống, không chỉ là model

AI Application Stack gồm các layer:

- Agent & Orchestration
- RAG system
- Vector store
- Embeddings
- Infrastructure
- Hardware

#### Foundation Model vs Traditional ML

Traditional ML:

- Train riêng cho từng task
- Khó scale

Foundation Model:

- Được pretrain ở quy mô lớn
- Hỗ trợ multi-task
- Q&A
- Translation
- Code generation

#### Multimodal AI

Input:

- Text
- Image
- Video
- Audio

Tất cả được embedding vào vector space.

#### Nova Embeddings

- Dimension từ 256 đến 3072

Trade-off:

- Dimension cao cho độ chính xác tốt hơn
- Dimension thấp cho tốc độ nhanh hơn

#### GraphRAG (advanced RAG)

Flow:

- Data như PDF, CSV đưa vào Amazon S3
- Chunk và embedding
- Graph construction
- Index gồm vector và graph
- Query

Stack:

- Amazon Bedrock
- Amazon Neptune
- Amazon OpenSearch

Lợi ích:

- Context chính xác hơn
- Giảm hallucination
- Scale tốt

#### Multi-agent workflow

Flow:

- User query
- Retrieve documents
- Evaluate relevance
- Nếu thiếu thì search thêm
- Generate answer

#### Agent architecture

- Prompt template
- Planning và reasoning
- Tool calling
- Memory

Framework:

- LangGraph với node, edge và state

#### Safety & Guardrails

Rủi ro:

- Nội dung độc hại
- Prompt injection
- Data leakage

Giải pháp:

- Amazon Bedrock Guardrails

### Trải nghiệm trong event

Sự kiện mang lại góc nhìn rõ ràng hơn về cách kết hợp DevOps với AI trong quá trình xây dựng và vận hành các hệ thống hiện đại. Đặc biệt, nội dung về GenAIOps và agent-based system cho thấy rõ cách AI được triển khai trong thực tế.

Do một số nội dung có tính chuyên sâu cao, phần lớn kiến thức được tiếp cận ở mức tổng quan và cần thêm thời gian để tìm hiểu sâu hơn.

### Bài học rút ra

- DevOps đang phát triển thành GenAIOps trong kỷ nguyên AI
- AI system cần pipeline hoàn chỉnh như software system
- Agent-based architecture là xu hướng quan trọng
- AI sẽ hỗ trợ developer thay vì thay thế hoàn toàn

### Một số hình ảnh khi tham gia sự kiện

![Hình ảnh sự kiện 1](/images/events/event3.jpg)

![Hình ảnh sự kiện 2](/images/events/event3_2.jpg)
