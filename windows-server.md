# Windows Server

## 1. Thực hiện allow port, allow ip trên window fw

<div align='center'>

![Hình ảnh](./images/allow_IP_Port.png)

</div>

## 2. Thực hiện block port, block ip trên window fw

<div align='center'>

![Hình ảnh](./images/block_IP_Port.png)

</div>


## 3. Thực hiện giới hạn port, giới hạn ip trên window fw chỉ cho phép ip chỉ định truy cập

<div align='center'>

![Hình ảnh](./images/allow_specific_IP.png)

</div>

## 4. Cài đặt Webserver IIS

### Cài đặt Webserver IIS
Nhấn vào **Add roles and features**

<div align='center'>

![Hình ảnh](./images/add_roles_and_features.png)

</div>

Ở mục **Installation Type** chọn **Role-based or feature-based installation** sau đó chọn **Next**

<div align='center'>

![Hình ảnh](./images/install_type.png)

</div>

Tiếp tục **Next** đến mục **Server Roles**, chọn các **Web Server (IIS)** với các option như sau:

<div align='center'>

![Hình ảnh](./images/server_roles.png)

</div>

Những mục sau chọn mặc định cho tất cả, sau đó nhấn **Install**.

Kiểm tra trong **Tools** nếu thấy **Internet Information Services (IIS) Manager** là cài đặt thành công.

<div align='center'>

![Hình ảnh](./images/tools.png)

</div>

### Cài đặt Website WordPress

Để cài đạt WordPress, ta cần cài cài đặt PHP7.4, MySQL 5.7.44, và source code của WordPress.

#### PHP7.4:
<div align='center'>

![Hình ảnh](./images/PHP-logo.svg)

</div>

**PHP (Hypertext Preprocessor)** là một ngôn ngữ lập trình mã nguồn mở, được sử dụng phổ biến để phát triển web động. PHP chủ yếu chạy trên server-side (phía máy chủ) và có thể nhúng trực tiếp vào mã HTML.

**Link Download**: [Download](https://windows.php.net/downloads/releases/)

#### MySQL:
<div align='center'>

![Hình ảnh](./images/mysql.png)

</div>

**MySQL** là một hệ quản trị cơ sở dữ liệu quan hệ (RDBMS - Relational Database Management System) mã nguồn mở, được sử dụng rộng rãi để lưu trữ, quản lý và truy vấn dữ liệu.

**Link Download**: [Download](https://dev.mysql.com/downloads/installer/)

#### WordPress:
<div align='center'>

![Hình ảnh](./images/wordpress.png)

</div>

**WordPress** là một hệ thống mã nguồn mở dùng để xuất bản blog/website được viết bằng ngôn ngữ lập trình PHP và cơ sở dữ liệu MySQL. WordPress được biết đến như một CMS miễn phí nhưng tốt, dễ sử dụng và phổ biến nhất trên thế giới.

**Link Download**: [Download](https://vi.wordpress.org/download/)

### Cài đặt SSL
Vào **Internet Information Services(IIS) Management** chọn vào **http://localhost/** ở bên trái như sau:

<div align='center'>

![Hình ảnh](./images/IIS.png)

</div>

Sau đó chọn **Server Certificates**. Tiếp theo chọn **Create Certificate Request...** ở bên phải. Điền các thông tin cần thiết sau đó bấm **Next**.

<div align='center'>

![Hình ảnh](./images/request_csr.png)

</div>

Chọn thuật toán **RSA** và bit length là **2048** sau đó bấm **Next**.

<div align='center'>

![Hình ảnh](./images/request_csr2.png)

</div>

Chọn nơi lưu trữ cho file sau đó bấm finish. Tuy nhiên, file tạo ra là file **.txt**, ta cần chuyển lại định dạng thành **.csr**

<div align='center'>

![Hình ảnh](./images/request_csr3.png)

</div>

Sau đó tạo ssl miễn phí bằng trang web cấp SSL miễn phí như **ZeroSSL**. Sau khi quá trình tạo ssl hoàn tất, ZeroSSL sẽ trả về file **.crt** và file **key**. Dùng các file này để tạo thành file **.pfx**.

Sau khi có file **.pfx** vào **Server Certificates** trong **IIS Management** vào chọn **Import...** và điền các thông tin cần thiết vào để hoàn tất quá trình tạo SSL cho domain.

<div align='center'>

![Hình ảnh](./images/pfx.png)

</div>

## 5. Cài đặt SQL Server 2012

<div align='center'>

![Hình ảnh](./images/sql-server.webp)

</div>

**SQL Server (hay Microsoft SQL Server)** là một hệ thống quản lý cơ sở dữ liệu quan hệ (RDBMS) được phát triển bởi Microsoft.

SQL Server cung cấp cho người dùng các công cụ và tính năng để quản lý, lưu trữ, xử lý các truy vấn dữ liệu, kiểm soát truy cập, xử lý giao dịch và hỗ trợ tích hợp dữ liệu từ nhiều nguồn khác nhau.

Ngoài ra, SQL Server cũng cung cấp các công cụ để tạo báo cáo, phân tích và quản lý cơ sở dữ liệu trực quan thông qua giao diện người dùng hoặc các script lệnh SQL. 

**Link Download**: [Download](https://www.microsoft.com/en-us/download/details.aspx?id=43351)