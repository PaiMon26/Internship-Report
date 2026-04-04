---
title: "RDS"
date: 2024-01-01
weight: 6
chapter: false
pre: " <b> 4.6. </b> "
---

#### Tổng quan

Amazon RDS được sử dụng trong dự án như tầng cơ sở dữ liệu quan hệ. Workshop này mô tả các bước chính để tạo database instance và chuẩn bị cấu hình mạng cần thiết cho backend.

#### Các bước triển khai

1. Mở **RDS console** và bắt đầu quy trình tạo cơ sở dữ liệu.

![RDS bước 0.1](rds.0.1.jpg)

2. Xem lại màn hình khởi tạo và các lựa chọn tạo database.

![RDS bước 0.2](rds.0.2.jpg)

3. Chọn cách tạo database và xác nhận cấu hình engine ban đầu.

![RDS bước 0.3](rds.0.3.jpg)

4. Chuyển sang màn hình cấu hình chi tiết cho database mới.

![RDS bước 0.4](rds.0.4.jpg)

5. Chọn engine và template phù hợp với môi trường triển khai.

![RDS bước 1](rds.1.jpg)

6. Cấu hình credentials, instance class, storage và availability settings.

![RDS bước 2](rds.2.jpg)

![RDS bước 3](rds.3.jpg)

7. Cấu hình connectivity như VPC, subnet group và security groups.

![RDS bước 4](rds.4.jpg)

![RDS bước 5](rds.5.jpg)

8. Thiết lập tên database và các tuỳ chọn bổ sung cần cho backend.

![RDS bước 6](rds.6.jpg)

![RDS bước 7](rds.7.jpg)

9. Rà soát cấu hình cuối cùng và tạo database instance.

![RDS bước 8](rds.8.jpg)

10. Kiểm tra trạng thái database và endpoint sau khi provision xong.

![RDS bước 9](rds.9.jpg)
