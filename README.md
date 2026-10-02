# TO-HU-TIEU Presets

Nguồn preset mặc định công khai cho X Assistant.

## Cập nhật preset

Chỉnh `default-presets.json`, tăng `version`, cập nhật `updatedAt`, sau đó push lên nhánh `main`.

Mỗi preset cần có `id` ổn định, `name` và `prompt`. Có thể thêm preset mới vào mảng `styles`; extension sẽ tự tải danh sách mới và giữ preset người dùng tự tạo ở bộ nhớ local.
