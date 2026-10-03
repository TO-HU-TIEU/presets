# TO-HU-TIEU Presets

Nguồn phong cách mặc định cho Assistant.

- `default-presets.json`: phong cách trả lời trên X; giữ ID ổn định, tăng version khi phát hành.
- `content-styles.json`: phong cách soạn Content, tách riêng với trả lời; Góc nhìn sắc và Cơ chế & hệ quả.

Không lưu API key, prompt cá nhân hoặc dữ liệu trình duyệt. Chỉ chứa JSON, không mã chạy từ xa.

## Phát hành

Hai repo nên được clone cạnh nhau (`presets` và `configs`). Sau khi chỉnh preset, tăng version và updatedAt, commit/push presets. Trong configs chạy `node scripts/update-manifest.mjs NEW_VERSION`: script tự đồng bộ preset sang bản phân phối và tính hash toàn bộ tài nguyên. Kiểm tra rồi commit/push configs.

Extension đang dùng configs làm bản phân phối theo manifest và hash để cập nhật đồng bộ, không đọc nửa bản mới/nửa bản cũ. Thư mục presets trong configs là bản sao được tạo khi phát hành, không phải nguồn biên tập thứ hai. Giữ bản sao này để các extension đã chia sẻ vẫn cập nhật được mà không đổi URL.
