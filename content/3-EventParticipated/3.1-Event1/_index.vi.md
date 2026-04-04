---
title: "Event 1"
date: 2026-01-29
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# Bài thu hoạch "AWS re:Invent Recap Vietnam 2025"

### Mục Đích Của Sự Kiện

- Tổng hợp và chia sẻ các công nghệ nổi bật từ AWS re:Invent 2025
- Giới thiệu xu hướng phát triển của AI và Cloud trong thực tế
- Cung cấp góc nhìn về cách xây dựng hệ thống AI hiện đại
- Giúp người tham dự tiếp cận nhanh các dịch vụ mới của AWS

### Nội Dung Nổi Bật

#### 1. Các pattern sử dụng LLM

**Quick Research**

- Phân tích dữ liệu phức tạp
- Tạo báo cáo nhanh

Dùng khi:

- Data lớn
- Cần insight nhanh cho business

**Quick Flows**

- Xây dựng pipeline nhiều bước
- Tổng hợp email
- Gom dữ liệu
- Phân tích, đánh giá

LLM đóng vai trò như một workflow engine.

**Quick Automate**

- Xử lý bài toán phức tạp
- Kết hợp nhiều module

Hướng phát triển:

- AI automation system thay backend truyền thống

#### 2. AWS AI Stack

**Amazon Bedrock**

- Nền tảng chạy LLM theo mô hình managed
- Hỗ trợ nhiều foundation model

**Bedrock AgentCore**

- Xây dựng hệ thống AI agent
- Điều phối logic orchestration

#### 3. Thành phần trong AI System

**Policy**

- Kiểm soát output
- Đảm bảo safety và governance

**Evaluation**

- Đánh giá model
- Accuracy
- Reliability

**Enhancements**

- Cá nhân hóa
- Xử lý real-time
- Xác thực và phân biệt user

**Reinforcement Fine-tuning**

- Cải thiện model dựa trên feedback

**Strands Agent**

- Framework hỗ trợ TypeScript và Python

**Nova Model**

- Có nhiều phiên bản như Lite và các bản nâng cấp

#### 4. Data Layer

**Embedding**

- Áp dụng cho text
- Áp dụng cho image
- Áp dụng cho video

Dùng cho:

- Semantic search
- RAG (Retrieval-Augmented Generation)

**Search Web**

- Lấy dữ liệu từ internet

**Force Mode**

- Model tự học từ hành vi user
- Model tự học từ data thực tế

**Action Layer (Act)**

- Thực thi hành động
- Gọi API
- Tương tác với hệ thống

**SageMaker AI**

- Training model
- Deploy và scale
- Quản lý pipeline

#### 5. Networking trong hệ thống AWS

- Multi-cloud interconnect
- Transit Gateway để kết nối nhiều VPC
- Site-to-site VPN
- Direct Connect ổn định hơn internet

So sánh:

- VPN phụ thuộc internet
- Direct Connect ổn định hơn

Lưu ý:

- Chi phí tăng theo region và gateway

#### 6. Infrastructure

**Container-based**

- ECS

**Serverless**

- AWS Lambda

#### 7. MCP (Model Context Protocol)

- Chuẩn kết nối giữa model và tool
- Chuẩn kết nối giữa model và external system

Use case:

- Agent gọi tool qua MCP
- Kết nối client, AWS và hệ thống

#### 8. Agent Architecture

- Multi-agent system

Các loại agent:

- Planner
- Tool
- Executor

**Agent + Memory**

- Lưu conversation
- Giữ context

**Serverless memory**

- Không cần tự build hạ tầng

#### 9. Storage & Logging

Lưu:

- Conversation history
- Context

Phục vụ:

- Debug
- Improve model

#### 10. Key Takeaways

AI system hiện đại gồm:

- Model (Bedrock)
- Agent (AgentCore)
- Data (Embedding, Search)
- Tool (MCP)
- Infrastructure (ECS, Lambda)
- Networking

Xu hướng chính:

- Agent-based architecture
- Multi-agent orchestration
- LLM là core engine của hệ thống

### Những Gì Học Được

#### Tư Duy Công Nghệ

- AI không chỉ là chatbot mà là một hệ thống hoàn chỉnh
- LLM có thể đóng vai trò trung tâm trong hệ thống
- Hiểu rõ hơn về kiến trúc AI hiện đại trên cloud

#### Kiến Thức Kỹ Thuật

Làm quen với:

- AI agent
- Embedding
- RAG
- Multi-agent system

Hiểu sơ bộ cách các thành phần AI kết nối với nhau.

#### Ứng Dụng Vào Công Việc

Có thể áp dụng:

- Sử dụng AI để automation task
- Hiểu cách tích hợp AI vào hệ thống

Trong tương lai:

- Xây dựng AI-based system
- Áp dụng agent-based architecture

### Trải nghiệm trong event

Sự kiện "AWS re:Invent Recap Vietnam 2025" mang lại góc nhìn tổng quan về các công nghệ mới trong lĩnh vực AI và Cloud, đặc biệt là cách xây dựng hệ thống AI hiện đại trên nền tảng AWS.

Các nội dung về AI agents, embedding và hệ thống multi-agent giúp mở rộng cách nhìn về việc tổ chức AI thành một hệ thống hoàn chỉnh thay vì chỉ dừng ở mô hình chatbot đơn lẻ. Một số khái niệm còn khá mới nên phần lớn nội dung được tiếp cận ở mức khái quát.

Nhìn chung, chương trình giúp làm rõ hơn xu hướng công nghệ hiện nay cũng như các hướng ứng dụng AI và Cloud trong thực tế.

### Bài học rút ra

- AI system cần nhiều thành phần, không chỉ là model
- Agent-based architecture là xu hướng quan trọng
- Cloud đóng vai trò nền tảng cho AI system
- Cần học từ cơ bản đến nâng cao để hiểu sâu hơn

### Một số hình ảnh khi tham gia sự kiện

![Hình ảnh sự kiện 1](/images/events/event1_1.jpg)

![Hình ảnh sự kiện 2](/images/events/event1_2.jpg)

![Hình ảnh sự kiện 3](/images/events/event1_3.jpg)
