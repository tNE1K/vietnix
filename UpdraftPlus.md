# Hướng dẫn sử dụng Plugin UpdraftPlus để migrate website WordPress

## Để migrate website WordPress sử dụng plugin UpdraftPlus sẽ có 2 thao tác chính sau:

- Export các file backup (zip file) từ website cũ.
- Import các file backup của website cũ vào website mới.

## 1. Export các file backup từ website cũ

- Bước 1: Đăng nhập vào trang `wp-admin` của trang web.

<div align='center'>

![Hình ảnh](./images/wp-admin_login.png)

</div>

- Bước 2: Truy cập vào phần `Plugins` -> `Add Plugin`.

<div align='center'>

![Hình ảnh](./images/plugin_addnew.png)

</div>

- Bước 3: Upload Plugin `UpdraftPlus` lên.

<div align='center'>

![Hình ảnh](./images/plugin_upload.png)

</div>

- Bước 4: Chọn `Activate Plugin`.

<div align='center'>

![Hình ảnh](./images/activate_plugin.png)

</div>

- Bước 5: Truy cập vào Plugin `UpdraftPlus` -> Chọn phần `Backup / Restore` -> Chọn `Backup Now`.

<div align='center'>

![Hình ảnh](./images/updraftplus_backup_now.png)

</div>

- Bước 6: Chọn vào các checkbox `Include your database in the backup (...)` và `Include your files in the backup (...)` sau đó chọn `Backup Now`.

<div align='center'>

![Hình ảnh](./images/updraftplus_backup.png)

</div>

- Bước 7: Đợi đến khi quá trình backup hoàn tất, có thể chọn `Close` để tắt pop-up thông báo đi hoặc đợi tầm 1-2s để thông báo tự tắt.

<div align='center'>

![Hình ảnh](./images/close_popup.png)

</div>

- Bước 8: Sau khi hoàn tất Backup, kiểm tra phần `Existing backups` sẽ thấy bản backup với thời gian cụ thể.

<div align='center'>

![Hình ảnh](./images/backup_list.png)

</div>

- Bước 9: Tiến hành download các file backup của website về bằng cách chọn vào các phần cần Download (Database, Plugins, Themes, Uploads, Others) trong mục `Backup data (click to download)` sau đó chọn `Download to your computer`.

<div align='center'>

![Hình ảnh](./images/download_backup.png)

</div>

## 2. Import các file backup của website cũ vào website mới.

- Bước 1: Cài đặt WordPress mặc định lên website mới.

<div align='center'>

![Hình ảnh](./images/wp_new_site.png)

</div>

- Bước 2: Thực hiện lại các bước từ 1 -> 4 ở phần `Export` để cài đặt và active Plugin. Sau đó Upload các file vừa download được ở trên vào đường dẫn `domain/wp-content/updraft/`

<div align='center'>

![Hình ảnh](./images/updraftplus_backup_upload.png)

</div>

- Bước 3: Truy cập vào Plugin `UpdraftPlus` -> Chọn phần `Backup / Restore` -> Kiểm tra phần `Existing backups`.

<div align='center'>

![Hình ảnh](./images/backup_list_upload.png)

</div>

- Bước 4: Kiểm tra nếu đã đầy đủ các thành phần của website WordPress (Database, Plugins, Themes, Uploads, Others) -> Chọn `Restore` để tiến hành restore website.

<div align='center'>

![Hình ảnh](./images/updraftplus_restore.png)

</div>

- Bước 5: Tại phần `Choose the components to restore:` chọn các phần cần restore -> Chọn `Next`.

<div align='center'>

![Hình ảnh](./images/updraftplus_choose_component.png)

</div>

- Bước 6: Ở phần `Retrieving (if necessary) and preparing backup files...` đảm bảo checkbox `Search and replace site location in the database (migrate)` đã được chọn -> Sau đó chọn `Restore`.

<div align='center'>

![Hình ảnh](./images/updraftplus_restore(2).png)

</div>

- Bước 7: Đợi quá trình Restore hoàn tất, chọn button `Return to UpdraftPlus configuration`.

<div align='center'>

![Hình ảnh](./images/updraftplus_restore_done.png)

</div>

- Bước 8: Đăng nhập lại vào trang wp-admin của website mới bằng thông tin wp-admin của website cũ để kiểm tra.

<div align='center'>

![Hình ảnh](./images/wp-admin_login.png)

</div>

- Bước 9: Kiểm tra website mới đã chạy ổn định và đúng như website cũ chưa -> done.

<div align='center'>

![Hình ảnh](./images/updraftplus_done.png)

</div>