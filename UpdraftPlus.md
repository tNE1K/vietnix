# Hướng dẫn sử dụng Plugin UpdraftPlus để migrate website WordPress

## Để migrate website WordPress sử dụng plugin UpdraftPlus sẽ có 2 thao tác chính sau:

- Export các file backup (zip file) từ website cũ.
- Import các file backup của website cũ vào website mới.

## 1. Export các file backup từ website cũ

- Bước 1: Đăng nhập vào trang `wp-admin` của trang web.

- Bước 2: Truy cập vào phần `Plugin` -> `Cài mới`.

- Bước 3: Upload Plugin `UpdraftPlus` lên.

- Bước 4: Chọn `Kích hoạt plugin`.

- Bước 5: Truy cập vào Plugin `UpdraftPlus` -> Chọn phần `Backup / Restore` -> Chọn `Backup Now`.

- Bước 6: Chọn vào các checkbox `Include your database in the backup (...)` và `Include your files in the backup (...)` sau đó chọn `Backup Now`.

- Bước 7: Đợi đến khi quá trình backup hoàn tất, sau đó chọn `Close` để tắt pop-up thông báo đi.

- Bước 8: Sau khi hoàn tất Backup, kiểm tra phần `Existing backups` sẽ thấy bản backup với thời gian cụ thể.

- Bước 9: Tiến hành download các file backup của website về bằng cách chọn vào các phần cần Download (Database, Plugins, Themes, Uploads, Others).

## 2. Import các file backup của website cũ vào website mới.

- Bước 1: Cài đặt website WordPress mặc định lên website mới.

- Bước 2: Thực hiện lại các bước từ 1 -> 4 ở phần `Export` để cài đặt và active Plugin.

- Bước 3: Upload các file vừa download được ở trên vào đường dẫn `domain/wp-content/updraft/`

- Bước 4: Truy cập vào Plugin `UpdraftPlus` -> Chọn phần `Backup / Restore` -> Kiểm tra phần `Existing backups`.

- Bước 5: Kiểm tra nếu đã đầy đủ các thành phần của website WordPress (Database, Plugins, Themes, Uploads, Others) -> Chọn `Restore` để tiến hành restore website.

- Bước 6: Tại phần `Choose the components to restore:` chọn các phần cần restore -> Chọn `Next`.

- Bước 7: Ở phần `Retrieving (if necessary) and preparing backup files...` 