# 👥 PHÂN CÔNG NHIỆM VỤ LÁT CẮT DỌC (VERTICAL SLICE ASSIGNMENT)

> **Học phần:** Phát triển ứng dụng Web cơ bản — CSE122 · BTL-02  
> **Dự án:** CampusMind — Điều phối hỗ trợ sức khỏe tinh thần sinh viên  
> **Nhóm thực hiện:** Nhóm 02 (3 sinh viên)  
> **Căn cứ:** Phần 3.11 & Phần 8 [tài liệu BTL/CSE122_HUONG_DAN_THUC_HIEN_BTL.docx](file:///d:/E/NAM%202/HK%201/WEB/cse122-campusmind-team02/t%C3%A0i%20li%E1%BB%87u%20BTL/CSE122_HUONG_DAN_THUC_HIEN_BTL.docx)

---

## 📌 Nguyên Tắc Phân Công Bắt Buộc (Vertical Slice)

Quy chế BTL CSE122 quy định:
> *"Mỗi sinh viên phải tự hoàn thành ít nhất một luồng nghiệp vụ end-to-end từ Phân tích → Bản mô phỏng → HTML → CSS → JavaScript → Dữ liệu → Responsive → Git Branch → PR → OBS. Tuyệt đối không chấp nhận cách phân công theo chiều ngang (một người chỉ làm tài liệu/Figma, một người chỉ HTML, một người chỉ JS)."*

---

## 1. Phân Công Chi Tiết 3 Sinh Viên

### 1.1. Sinh Viên 1 (SV1 - Nhóm trưởng): Trần Hoài Nam
* **Mã sinh viên:** `2251061999`
* **Lớp:** 64CNTT1
* **Vai trò phụ trách:** **Quản trị viên (Admin)** & Kiến trúc nền tảng
* **Luồng nghiệp vụ phụ trách (Vertical Slice):**
  - Thiết kế kiến trúc module, hệ thống Design Tokens 8 màu và bộ điều khiển xác thực RBAC (`auth.js`).
  - Toàn bộ luồng CRUD Quản trị danh mục dịch vụ Wellbeing (`admin-service-management.html`).
  - Bảng điều hành năng lực toàn trường & Audit Logs (`admin-dashboard.html`).
  - Quản lý người dùng, phân quyền RBAC và cơ chế khóa mở tài khoản (`admin-user-management.html`).
* **Tính năng kỹ thuật nâng cao phụ trách:**
  - Đồng bộ đa tab LocalStorage (`setupCrossTabSync` - Bonus +0.5đ).
  - Xuất dữ liệu CSV (`exportToCSV`).
  - Bảo vệ chống lỗ hổng XSS (`escapeHTML` - VP-02 immunity).
* **Nhánh Git phụ trách:** `feat/admin-crud-management`, `feat/auth-rbac-guard`
* **Video OBS minh chứng:** `SV1-01-admin-dashboard.mp4`, `SV1-02-admin-services-crud.mp4`, `SV1-03-admin-users-rbac.mp4`

---

### 1.2. Sinh Viên 2 (SV2): Lê Ngọc An
* **Mã sinh viên:** `2251061234`
* **Lớp:** 64CNTT2
* **Vai trò phụ trách:** **Sinh viên (Student)** & Cổng Khách vãng lai (Visitor)
* **Luồng nghiệp vụ phụ trách (Vertical Slice):**
  - Trang chủ giới thiệu & 4 lối vào dịch vụ (`index.html`).
  - Danh bạ 12 dịch vụ & Trắc nghiệm định hướng **AI-1 Support Navigator** (`visitor-service-directory.html`).
  - Thư viện tài nguyên tự học, bài tập thở 4-7-8 & gợi ý **AI-2** (`visitor-resource-library.html`).
  - Hồ sơ chuyên gia & lịch trực tuần (`visitor-counselor-detail.html`).
  - Bảng điều khiển sinh viên, 4 KPIs & Mood Tracker (`student-dashboard.html`).
  - Quy trình đặt lịch 4 bước có validation đa bước (`student-booking.html`).
  - Quản lý lịch hẹn cá nhân, Slide Drawer & Hủy ca an toàn (`student-appointments.html`).
* **Nhánh Git phụ trách:** `feat/student-booking-wizard`, `feat/visitor-directory-ai1`
* **Video OBS minh chứng:** `SV2-01-student-dashboard.mp4`, `SV2-02-student-booking-wizard.mp4`, `SV2-03-student-appointments-drawer.mp4`, `SV2-04-visitor-directory-ai1.mp4`

---

### 1.3. Sinh Viên 3 (SV3): TS. / Bạn Nguyễn Minh Hà
* **Mã sinh viên:** `2251065678`
* **Lớp:** 64CNTT3
* **Vai trò phụ trách:** **Chuyên viên Tư vấn (Counselor)** & Trợ lý AI
* **Luồng nghiệp vụ phụ trách (Vertical Slice):**
  - Quản lý lịch làm việc tuần của chuyên gia (`counselor-schedule.html`).
  - Hàng chờ tiếp nhận, duyệt hoặc từ chối ca tư vấn (`counselor-appointment-queue.html`).
  - Biên tập ghi chú lâm sàng, bộ đếm từ, lưu nháp & **AI-3 Counselor Summary Assistant** (`counselor-session-note.html`).
  - Kiểm thử kịch bản ngoại lệ AI thất bại (Failure Test switch).
* **Nhánh Git phụ trách:** `feat/counselor-schedule`, `feat/counselor-queue-review`, `feat/ai3-session-note`
* **Video OBS minh chứng:** `SV3-01-counselor-schedule.mp4`, `SV3-02-counselor-appointment-queue.mp4`, `SV3-03-counselor-session-note-ai3.mp4`

---

## 2. Ma Trận Đóng Góp & Tiến Độ Cam Kết

| Thành Viên | Thiết kế Mockup | HTML5 Ngữ nghĩa | CSS Tokens | JavaScript DOM | Xử lý Dữ liệu | Responsive | Kiểm thử & OBS | Đóng Góp |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **Trần Hoài Nam** | 100% | 100% | 100% | 100% | 100% | 100% | 100% | **33.33%** |
| **Lê Ngọc An** | 100% | 100% | 100% | 100% | 100% | 100% | 100% | **33.33%** |
| **Nguyễn Minh Hà** | 100% | 100% | 100% | 100% | 100% | 100% | 100% | **33.33%** |
| **Tổng cộng** | — | — | — | — | — | — | — | **100%** |
