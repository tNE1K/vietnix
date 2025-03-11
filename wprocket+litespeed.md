# WP Rocket và Litespeed Cache

## 1. WP Rocket
WP Rocket là một plugin tăng tốc WordPress mạnh mẽ, giúp tối ưu hóa hiệu suất website bằng cách lưu cache, giảm tải máy chủ, và tối ưu mã nguồn. Đây là một trong những plugin cache phổ biến nhất do dễ sử dụng và không cần cấu hình phức tạp.

<div align="center">

![Hình ảnh](./images/wp-rocket.jpg)

</div>


### Tính năng chính của WP Rocket

#### 1. Tạo bộ nhớ đệm (Page Caching)
- Tạo cache tĩnh, giúp tải trang nhanh hơn bằng cách giảm số lần truy vấn đến máy chủ.
- Hỗ trợ preload cache để đảm bảo người dùng luôn nhận được phiên bản tối ưu nhất.

#### 2. Tối ưu mã nguồn (Minification & Concatenation)
- Nén HTML, CSS và JavaScript giúp giảm kích thước file.
- Gộp file CSS & JS để giảm số lượng request khi tải trang.

#### 3. Lazy Load hình ảnh và video
- Chỉ tải hình ảnh và video khi người dùng cuộn đến, giúp giảm tải và tăng tốc trang web.

#### 4. Tối ưu cơ sở dữ liệu (Database Optimization)
- WP Rocket sẽ hỗ trợ người dùng dọn dẹp và tối ưu cơ sở dữ liệu của website.

#### 5. Tích hợp CDN và Cloudflare
- Dễ dàng kết nối với Cloudflare hoặc dịch vụ CDN khác để tăng tốc website trên toàn cầu.

## 2. LiteSpeed Cache
LiteSpeed Cache là một plugin tối ưu tốc độ website miễn phí, được thiết kế để hoạt động tối ưu với LiteSpeed Web Server. Nó giúp cải thiện tốc độ tải trang thông qua bộ nhớ đệm cấp máy chủ (server-level caching), đồng thời tích hợp nhiều tính năng tối ưu hóa khác như nén tệp, tối ưu hình ảnh và hỗ trợ CDN.

<div align="center">

![Hình ảnh](./images/litespeed_cache.png)

</div>

### Tính năng chính của LiteSpeed Cache

#### 1. Caching cấp độ máy chủ (Server-Level Caching)
- Nhanh hơn WP Rocket vì cache được xử lý ngay ở mức độ máy chủ, không phải ở mức PHP như các plugin khác.
- Tự động preload cache để đảm bảo hiệu suất tối ưu.
- Hỗ trợ ESI (Edge Side Includes), cho phép cache từng phần của trang web thay vì toàn bộ.

#### 2. Tối ưu hóa mã nguồn
- Nén (Minify) & Gộp (Combine) các file CSS/JS/HTML để giảm kích thước và số lượng request.

#### 3. Lazy Load hình ảnh
- Chỉ tải ảnh khi người dùng cuộn đến, giúp tiết kiệm băng thông và tăng tốc trang.
- Tự động chuyển đổi hình ảnh sang WebP để giảm kích thước mà không ảnh hưởng đến chất lượng.

#### 4. Tối ưu cơ sở dữ liệu (Database Optimization)
- Hỗ trợ người dùng dọn dẹp và tối ưu cơ sở dữ liệu của website.

#### 5. Hỗ trợ CDN với QUIC.cloud
- QUIC.cloud CDN miễn phí giúp tối ưu cache động.
- Tích hợp dễ dàng với các dịch vụ CDN khác như Cloudflare.

## 3. So sánh LiteSpeed Cache và WP Rocket
### So sánh
| **Tiêu chí** | **LiteSpeed Cache** | **WP Rocket** |
|--------------|---------------------|---------------|
| **Giá**             | Miễn phí (có bản PRO)     | Trả phí                |
| **Hỗ trợ Web Server** | LiteSpeed (cấp máy chủ)  | Apache, Nginx (PHP-level) |
| **Hiệu suất cache**  | Nhanh hơn (cache server-level) | Tốt nhưng chậm hơn (PHP-level) |
| **Lazy Load & WebP** | Có sẵn, tự động chuyển đổi WebP | Có sẵn, cần thiết lập |
| **Tối ưu mã nguồn (CSS, JS, HTML)** | Có (Minify, Combine, Async, Defer) | Có (Minify, Combine, Async, Defer) |
| **Tối ưu cơ sở dữ liệu** | Có | Có |
| **Hỗ trợ CDN**       | QUIC.cloud, Cloudflare, CDN khác | Cloudflare, các CDN khác |
| **Cấu hình**         | Nhiều tùy chỉnh nâng cao | Dễ dùng, tự động tối ưu |

### Khi nào nên dùng LiteSpeed Cache?
- Khi hosting chạy LiteSpeed Web Server.
- Khi cần một plugin cache miễn phí nhưng mạnh mẽ.