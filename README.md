# Ứng Dụng Dò Điểm Đứt Cáp Quang OTDR — Trung Tâm Viễn Thông Cẩm Phả

Ứng dụng web bản đồ hỗ trợ kỹ thuật viên viễn thông định vị tọa độ GPS và tính quãng đường di chuyển thực tế từ **Hộp GPON / ODF** đến vị trí đứt cáp quang theo số đo máy **OTDR**, tích hợp **hệ số trùng võng cáp** và chạy trực tiếp trên trình duyệt điện thoại Android (qua HTTPS, có thể đưa ra màn hình chính như ứng dụng độc lập).

## Thông tin tác giả & đơn vị
- **Đơn vị:** Trung Tâm Viễn Thông Cẩm Phả — Viễn Thông Quảng Ninh
- **Tác giả:** Vũ Ngọc Hải
- **Điện thoại:** 0918961781

## Tính năng chính
1. **Định vị GPS độ chính xác cao:** Lấy tọa độ Kinh độ/Vĩ độ theo thời gian thực (`enableHighAccuracy: true`), hiển thị sai số `±m`, vẽ vòng tròn sai số và chấm vị trí trực tiếp trên bản đồ.
2. **Tính quãng đường & độ trùng võng cáp:** Ghi nhận lộ trình từ điểm gốc **GPON (A)**, tính khoảng cách theo công thức Haversine có lọc nhiễu GPS, đồng thời hỗ trợ chọn **hệ số trùng võng cáp** (`0%`, `+1%`, `+1.5%`, `+2%`, `+3%`) để quy đổi sát với chiều dài cáp thực tế.
3. **Cảnh báo vùng điểm đứt:** Nhập số mét đo từ máy OTDR để theo dõi khoảng cách còn lại; thanh trạng thái đổi màu khi còn dưới `50m` và nhấp nháy đỏ kèm rung/âm thanh khi nằm trong vùng `±5m` quanh mốc mục tiêu.
4. **Hỗ trợ tác nghiệp hiện trường:**
   - Chuyển đổi lớp bản đồ **Đường phố** (OpenStreetMap) / **Vệ tinh** (Esri World Imagery) và mở nhanh sang **Google Maps**.
   - **Ghim cột** đánh dấu mốc cột/măng xông nghi ngờ kèm số mét tại thời điểm ghim.
   - **Chấm tay** mô phỏng/đo thử lộ trình trực tiếp trên bản đồ.
   - **Sao chép** nhanh tọa độ kèm thông tin kỹ thuật viên và quãng đường đo.
   - **Lưu / Mới** lưu lịch sử các ca đo trên thiết bị (`localStorage`).
   - **Chế độ tương phản cao** hỗ trợ nhìn rõ ngoài trời nắng và **Hướng dẫn kỹ thuật viên** tích hợp sẵn.

## Hướng dẫn triển khai & sử dụng trên Android
1. Tải file `index.html` lên repository GitHub và bật **GitHub Pages** (nhánh `main`, thư mục `/ (root)`, bật HTTPS) để có liên kết `https://<ten-tai-khoan>.github.io/<ten-repository>/`.
2. Bật **Vị trí (Location)** và **Độ chính xác vị trí của Google** trên điện thoại Android; cấp quyền **Vị trí chính xác** cho **Chrome**.
3. Mở liên kết `https://...` bằng **Chrome**, chọn **Cho phép** khi trình duyệt hỏi quyền truy cập vị trí.
4. *(Tùy chọn)* Nhấn biểu tượng **3 chấm (⋮)** trên Chrome → **Thêm vào Màn hình chính** để mở nhanh như một ứng dụng độc lập.
