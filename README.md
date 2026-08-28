# Building Check

Checklist an toàn công trường đầu ca — ứng dụng web một file (HTML + CSS + JS thuần), tối ưu cho điện thoại.

## Tính năng

- Đăng nhập (demo, lưu tên giám sát vào trình duyệt)
- Dark mode / Light mode
- Checklist 10 hạng mục an toàn, mỗi mục chọn Đạt / Không đạt / Không áp dụng
- Bắt buộc nhập ghi chú cho mục "Không đạt"
- Tự động tính điểm % và trạng thái ca trực
- Hiển thị giờ Bắt đầu ca / Kết thúc ca (giờ Việt Nam)
- Mục "Không đạt" chưa xử lý được tự động mang cảnh báo sang ca sau, tới khi được chấm "Đạt"
- Nút "Kết thúc ca": tự động xuất file JSON lưu kết quả rồi chuyển sang ca/ngày mới
- Xuất kết quả ra JSON bất cứ lúc nào (tải file hoặc sao chép)

## Chạy thử cục bộ

Mở trực tiếp `index.html` bằng trình duyệt — không cần cài đặt hay build gì thêm.

## Deploy lên Vercel

Đây là site tĩnh 100% (không có bước build, không phụ thuộc). Trên Vercel:

1. Import repo này vào Vercel.
2. Framework Preset: chọn **Other** (hoặc để Vercel tự nhận diện static site).
3. Build Command: để trống. Output Directory: để trống (mặc định root).
4. Deploy — Vercel sẽ phục vụ `index.html` tại `/`.

## Lưu ý

- Toàn bộ dữ liệu (đăng nhập, checklist, theme) được lưu trong `localStorage` của trình duyệt — không có server/database, không đồng bộ giữa các thiết bị.
- Đăng nhập chỉ mang tính minh hoạ (demo), không phải cơ chế bảo mật thật.
