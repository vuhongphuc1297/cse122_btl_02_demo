# 📹 DANH MỤC MINH CHỨNG VIDEO OBS (OBS EVIDENCE LOG)

> **Học phần:** Phát triển ứng dụng Web cơ bản — CSE122 · BTL-02  
> **Dự án:** CampusMind — Điều phối hỗ trợ sức khỏe tinh thần sinh viên  
> **Quy chuẩn:** Phần 8.8 [tài liệu BTL/CSE122_HUONG_DAN_THUC_HIEN_BTL.docx](file:///d:/E/NAM%202/HK%201/WEB/cse122-campusmind-team02/t%C3%A0i%20li%E1%BB%87u%20BTL/CSE122_HUONG_DAN_THUC_HIEN_BTL.docx)  
> **Quy tắc đặt tên file:** `SV<SốThứTự>-<SốMànHình>-<TênTrangKebabCase>.mp4`

---

## 📌 Yêu Cầu Kỹ Thuật Khi Quay OBS

1. **Khung hình:** Bắt buộc có webcam hiện rõ khuôn mặt sinh viên (góc màn hình).
2. **Âm thanh:** Giọng nói rõ ràng, thuyết minh luồng người dùng và cách code xử lý DOM/LocalStorage.
3. **Thao tác chứng minh:**
   - Mở giao diện trên trình duyệt (thử nghiệm cả Desktop 1440px và Mobile 390px).
   - Thao tác tương tác chính (Click, Form input, Validation, CRUD, Trợ lý AI).
   - Kiểm tra F12 Console & DevTools Application (LocalStorage được cập nhật).
   - Mở mã nguồn trong VS Code giải thích hàm JavaScript tương ứng.
   - Trình bày nhánh Git và Commit đã thực hiện.

---

## 📋 Danh Mục Video Minh Chứng Cho Toàn Bộ 18 Màn Hình

| Mã Video | Tên Giao Diện & Nghiệp Vụ | Đường Dẫn Tệp HTML | Sinh Viên Phụ Trách | Nhánh Git Phụ Trách | Thời Lượng | Trạng Thái |
| :--- | :--- | :--- | :--- | :--- | :---: | :---: |
| **SV1-01** | Bảng điều hành Quản trị & Audit Logs | `pages/admin-dashboard.html` | Trần Hoài Nam | `feat/admin-crud-management` | 03:30 | Sẵn sàng kịch bản |
| **SV1-02** | CRUD Danh mục Dịch vụ Wellbeing | `pages/admin-service-management.html` | Trần Hoài Nam | `feat/admin-crud-management` | 04:15 | Sẵn sàng kịch bản |
| **SV1-03** | Quản lý Người dùng & Phân quyền RBAC | `pages/admin-user-management.html` | Trần Hoài Nam | `feat/admin-users-rbac` | 04:00 | Sẵn sàng kịch bản |
| **SV1-04** | Đăng nhập & Chuyển quyền 1-Click | `pages/login.html` | Trần Hoài Nam | `feat/auth-rbac-guard` | 02:30 | Sẵn sàng kịch bản |
| **SV2-01** | Landing Page & 4 Lối vào Dịch vụ | `index.html` | Lê Ngọc An | `feat/visitor-directory-ai1` | 03:00 | Sẵn sàng kịch bản |
| **SV2-02** | Danh bạ 12 Dịch vụ & AI-1 Navigator | `pages/visitor-service-directory.html` | Lê Ngọc An | `feat/visitor-directory-ai1` | 04:30 | Sẵn sàng kịch bản |
| **SV2-03** | Thư viện Tài nguyên & Đồng hồ thở 4-7-8 | `pages/visitor-resource-library.html` | Lê Ngọc An | `feat/visitor-directory-ai1` | 03:45 | Sẵn sàng kịch bản |
| **SV2-04** | Hồ sơ Chuyên gia TS. Nguyễn Minh Hà | `pages/visitor-counselor-detail.html` | Lê Ngọc An | `feat/visitor-directory-ai1` | 02:45 | Sẵn sàng kịch bản |
| **SV2-05** | Bảng điều khiển Sinh viên & Mood Tracker | `pages/student-dashboard.html` | Lê Ngọc An | `feat/student-booking-wizard` | 03:30 | Sẵn sàng kịch bản |
| **SV2-06** | Quy trình Đặt lịch 4 Bước & AI-2 | `pages/student-booking.html` | Lê Ngọc An | `feat/student-booking-wizard` | 05:00 | Sẵn sàng kịch bản |
| **SV2-07** | Quản lý Lịch hẹn, Drawer & Hủy ca | `pages/student-appointments.html` | Lê Ngọc An | `feat/student-booking-wizard` | 04:15 | Sẵn sàng kịch bản |
| **SV3-01** | Quản lý Lịch làm việc tuần Chuyên viên | `pages/counselor-schedule.html` | Nguyễn Minh Hà | `feat/counselor-schedule` | 03:15 | Sẵn sàng kịch bản |
| **SV3-02** | Hàng chờ Tiếp nhận & Phê duyệt Ca hẹn | `pages/counselor-appointment-queue.html` | Nguyễn Minh Hà | `feat/counselor-queue-review` | 04:00 | Sẵn sàng kịch bản |
| **SV3-03** | Soạn thảo Ghi chú Ca & AI-3 Assistant | `pages/counselor-session-note.html` | Nguyễn Minh Hà | `feat/ai3-session-note` | 04:45 | Sẵn sàng kịch bản |
| **SV3-04** | Kiểm thử Ngoại lệ AI Thất bại (Failure Test)| `pages/counselor-session-note.html` | Nguyễn Minh Hà | `feat/ai3-session-note` | 02:30 | Sẵn sàng kịch bản |
| **CHUNG-01**| Trang Cấm Quyền Truy Cập (Route Guard) | `pages/403.html` | Toàn nhóm | `dev` | 01:30 | Sẵn sàng kịch bản |
| **CHUNG-02**| Trang Không Tìm Thấy (404 Therapeutic) | `pages/404.html` | Toàn nhóm | `dev` | 01:30 | Sẵn sàng kịch bản |
| **CHUNG-03**| Showcase Hub 3 Viewports (Responsive) | `showcase.html` | Toàn nhóm | `dev` | 03:00 | Sẵn sàng kịch bản |
