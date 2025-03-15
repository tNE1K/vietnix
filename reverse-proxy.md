# Reverse Proxy

## 1. Web Server là gì?
**Web Server** là máy chủ cài đặt các chương trình phục vụ các ứng dụng web. Web Server có khả năng tiếp nhận request từ các trình duyệt web và gửi phản hồi đến client thông qua giao thức HTTP hoặc các giao thức khác. Có nhiều web server khác nhau như: Apache, Nginx, IIS, ...

<div>

![Hình ảnh](./images/webserver.png)

</div>

## 1. Nginx là gì?
<div>

![Hình ảnh](./images/nginx.jpg)

</div>

**Nginx** là 1 máy chủ reverse proxy mã nguồn mở cho các giao thức HTTP, HTTPS, SMTP, POP3 và IMAP, cũng như là 1 máy chủ cân bằng tải (Load Balancer), HTTP cache và web.

Không giống các web server truyền thống, Nginx được biết đến với tính linh hoạt và hiệu suất cao với mức sử dụng tài nguyên thấp. Nginx không dựa trên luồng (thread) để xử lý yêu cầu. Thay vào đó, nó sử dụng 1 kiến trúc bất đồng bộ hướng sự kiện linh hoạt. Kiến trúc này sử dụng ít, nhưng có thể dự đoán được lượng bộ nhớ khi hoạt động.

## 2. Apache là gì?
<div>

![Hình ảnh](./images/apache.jpg)

</div>

**Apache** là phần mềm mã nguồn mở phổ biến được sử dụng để phục vụ các trang web trên Internet. Apache HTTP Server chính là tên đầy đủ của hệ thống Apache. Công nghệ đưuọc phát triển và duy trì bởi Apache Software Foundation. Đây là một trong những máy chủ web phổ biến nhất trên thế giới và chạy trên hệ điều hành Unix, Linux, Windows...

Apache cung cấp các tính năng mạnh mẽ cho việc xử lý HTTP requests. Trong đó bao gồm việc hỗ trợ cho nhiều ngôn ngữ lập trình như PHP, Python, Perl và Ruby thông qua các module mở rộng. Công nghệ còn hỗ trợ SSL/TLS để bảo mật giao tiếp web và có khả năng mở rộng linh hoạt nhằm đáp ứng nhu cầu truyền tải lưu lượng truy cập khổng lồ.

## 3. Reverse Proxy là gì?

Reverse Proxy là một máy chủ trung gian thường nằm sau tường lửa trong một mạng riêng. Server này nhận request từ clients rồi chuyển tiếp đến server thích hợp. Các reverse proxy thường được triển khai để giúp tăng cường bảo mật, hiệu suất và độ tin cậy.

<div>

![Hình ảnh](./images/reverse_proxy_flow.png)

</div>

### Mô hình Reverse Proxy kết hợp giữa Nginx và Apache
<div>

![Hình ảnh](./images/reverse_proxy.png)

</div>

## 4. Cấu hình