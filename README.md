# Website cá nhân Nguyễn Thùy Trang

- Website: https://nguyentrang2309.github.io
- Trang quản trị: https://nguyentrang2309.github.io/admin/

Website chạy trên GitHub Pages. Nội dung được quản trị bằng Sveltia CMS, không cần biết lập trình.

## 1. Đăng nhập trang quản trị

Lần đầu cần tạo một **token** (chìa khoá riêng để CMS sửa kho này). Chỉ làm một lần.

1. Vào GitHub, chọn ảnh đại diện, **Settings**, **Developer settings**, **Personal access tokens**, **Fine-grained tokens**, rồi **Generate new token**.
2. Đặt tên (ví dụ `cms-website`), chọn thời hạn.
3. Ở **Repository access**, chọn **Only select repositories** và chọn `nguyentrang2309.github.io`.
4. Ở **Permissions**, mục **Contents**, chọn **Read and write**.
5. Bấm **Generate token** và sao chép token.
6. Mở https://nguyentrang2309.github.io/admin/, chọn đăng nhập bằng token (**Sign in with token**), dán token vào.

Lưu ý bảo mật:
- Token chỉ dán vào ô đăng nhập của trang admin. Không gửi cho ai, không ghi vào file trong kho.
- Nếu lộ token, vào GitHub xoá token đó và tạo token mới.
- Token hết hạn thì tạo lại theo các bước trên.

## 2. Viết bài blog

1. Vào admin, mục **Bài viết blog**, bấm **Bài viết mới**.
2. Điền:
   - **Tiêu đề:** hiện ở đầu bài và trong danh sách.
   - **Ngày đăng:** mặc định là hôm nay.
   - **Tóm tắt:** 1 đến 2 câu, hiện ở danh sách blog.
   - **Hiển thị công khai:** tắt nếu muốn lưu nháp, chưa cho ai xem.
   - **Nội dung:** viết như trong trình soạn thảo thông thường (tiêu đề, danh sách, in đậm, ảnh).
3. Bấm **Lưu / Publish**. Khoảng 1 phút sau bài xuất hiện trên website.

Sửa hoặc xoá bài: mở bài trong admin, sửa rồi lưu, hoặc dùng nút xoá.

## 3. Sửa nội dung giao diện

Vào admin, mục **Nội dung website**, chọn **Trang chủ và thông tin chung**. Ở đây sửa được:

- Tên, dòng giới thiệu, ảnh chân dung, chữ trên nút liên hệ
- Các con số nổi bật
- Các việc đã làm
- Hành trình (nơi làm việc, thời gian)
- Kỹ năng (bật "Kỹ năng nổi bật" để tô đậm)
- Giới thiệu Blog
- Các link liên hệ (email dạng `mailto:địa-chỉ-email`)

Bấm lưu, khoảng 1 phút sau trang cập nhật.

## 4. Thêm hoặc đổi ảnh

Trong trình soạn bài hoặc ô ảnh, chọn tải ảnh lên. Ảnh được lưu vào thư mục `uploads/`. Nên dùng ảnh dưới 500 KB để trang tải nhanh.

## 5. Việc CMS không làm được

Màu sắc, font và bố cục nằm trong file `style.css` và thư mục `_layouts/`. Muốn đổi, nhờ Claude Code sửa rồi đẩy lên.

## 6. Khi có sự cố

| Triệu chứng | Cách xử lý |
| --- | --- |
| Lưu xong nhưng website chưa đổi | Đợi 1 đến 2 phút rồi tải lại trang (Ctrl+F5). |
| Admin báo lỗi quyền hoặc không lưu được | Token hết hạn hoặc thiếu quyền **Contents: Read and write**. Tạo token mới. |
| Bài không hiện trong danh sách blog | Kiểm tra ô "Hiển thị công khai" đã bật chưa, và ngày đăng không nằm ở tương lai. |
| Trang trắng hoặc lỗi sau khi lưu | Vào tab **Actions** của kho trên GitHub xem bản dựng có báo lỗi không. |

## 7. Cấu trúc kho (để tham khảo)

| Đường dẫn | Là gì |
| --- | --- |
| `index.html`, `blog.html` | Trang chủ và trang danh sách blog |
| `_data/site.yml` | Nội dung trang chủ (CMS sửa file này) |
| `_posts/` | Các bài blog (CMS tạo file ở đây) |
| `_layouts/` | Khung chung của trang và bài viết |
| `style.css`, `fonts/` | Giao diện và font |
| `admin/` | Trang quản trị Sveltia CMS |
| `uploads/` | Ảnh tải lên từ CMS |
