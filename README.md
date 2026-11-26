# Nhóm 14 – Điện toán đám mây

## Đề tài
**Phát hiện và đếm bông lúa mì trên ảnh đồng ruộng bằng YOLO11n (1024 px).**

## Giao diện web
Trang web tiếng Việt nằm trong thư mục `docs/`.

Để xuất bản, vào **Settings → Pages** của kho GitHub này, chọn **Deploy from a branch**, nhánh **main**, thư mục **/docs**, rồi **Save**. Sau khi GitHub Pages được bật và xây dựng thành công, địa chỉ dự kiến sẽ là:

https://mavanhung123dhtn-rgb.github.io/nhom14-dien-toan-dam-may/

**Trạng thái:** Giao diện đã được đưa lên GitHub; GitHub Pages có thể cần bật thủ công. Địa chỉ dự kiến trên chưa được xác nhận đang hoạt động.

## Kiến trúc Cloud
Trình duyệt → API Gateway → S3 → SQS → AWS Lambda (YOLO11n) → DynamoDB/S3 → trả kết quả.

GitHub Pages **chỉ lưu HTML/CSS/JavaScript**, không chạy được Python/YOLO11n. Khi chưa triển khai API và mô hình bông lúa mì đã huấn luyện, trang chỉ hiển thị giao diện và ảnh xem trước do bạn chọn, **không bịa ra khung hoặc số lượng nhận diện**.

Sau khi API AWS hoạt động, điền địa chỉ vào `docs/config.js`. Cần thiết lập CORS cho miền GitHub Pages và cấu hình truy cập an toàn phía máy chủ; tuyệt đối không commit mật khẩu, mã truy cập, `best.pt` có hạn chế sử dụng hoặc khóa AWS.

## Bộ mã nguồn đầy đủ
Gói ZIP đã bàn giao trong cuộc trò chuyện có mã nguồn localhost, hướng dẫn, tập kiểm thử, báo cáo và bộ AWS SAM. Kho GitHub hiện đã có **giao diện tĩnh**; những tệp khác trong gói ZIP chưa được đưa lên kho này.

## Thông tin nhóm
Nhóm 14 – Học phần Điện toán đám mây. Danh sách thành viên và giảng viên chưa được cung cấp chính thức, cần điền trước khi nộp.
