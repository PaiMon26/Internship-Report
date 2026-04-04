---
title: "Redis"
date: 2024-01-01
weight: 7
chapter: false
pre: " <b> 4.7. </b> "
---

#### Tổng quan

Redis được dùng trong dự án như tầng cache. Workshop này ghi lại quy trình tạo môi trường ElastiCache for Redis và các thiết lập chính cần cho việc tích hợp với ứng dụng.

#### Các bước triển khai

1. Mở **ElastiCache** console và chọn tạo Redis deployment.

![Redis bước 1](r.1.jpg)

![Redis bước 2](r.2.jpg)

![Redis bước 3](r.3.jpg)

2. Nhập các cấu hình cơ bản như tên cluster và thông tin engine.

![Redis bước 4](r.4.jpg)

![Redis bước 5](r.5.jpg)

![Redis bước 6](r.6.jpg)

3. Cấu hình số node, capacity và các tuỳ chọn availability.

![Redis bước 7](r.7.jpg)

![Redis bước 8](r.8.jpg)

![Redis bước 9](r.9.jpg)

4. Cấu hình VPC, subnet group và security settings cho cluster.

![Redis bước 10](r.10.jpg)

![Redis bước 11](r.11.jpg)

![Redis bước 12](r.12.jpg)

5. Rà soát các tham số bổ sung và tuỳ chọn bảo trì.

![Redis bước 13](r.13.jpg)

![Redis bước 14](r.14.jpg)

6. Kiểm tra cấu hình cuối cùng và gửi tạo Redis deployment.

![Redis bước 15](r.15.jpg)

![Redis bước 16](r.16.jpg)

7. Chờ cluster chuyển sang trạng thái available và xem lại thông tin chi tiết.

![Redis bước 17](r.17.jpg)

![Redis bước 18](r.18.jpg)

8. Kiểm tra endpoint và trạng thái cuối cùng của Redis để tích hợp vào ứng dụng.

![Redis bước 19](r.19.jpg)
