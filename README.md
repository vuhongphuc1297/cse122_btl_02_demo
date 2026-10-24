# 🌿 CampusMind — Nền Tảng Điều Phối Hỗ Trợ Sức Khỏe Tinh Thần Sinh Viên

> **Học phần:** Phát triển ứng dụng Web cơ bản — CSE122 · BTL-02  
> **Khoa Công nghệ Thông tin — Trường Đại học Thủy Lợi (TLU)**  
> **Bộ mã nguồn demo mới:** `cse122-campusmind-team02_demo`  
> **Được chuẩn hóa theo:** [Bản thiết kế 24 Mockups SVG (design/new_mockups)](file:///d:/E/NAM%202/HK%201/WEB/cse122-campusmind-team02/design/new_mockups/README.md) & [Báo cáo Phân tích Bài toán CampusMind (BTL CSE122)](file:///d:/E/NAM%202/HK%201/WEB/cse122-campusmind-team02/t%C3%A0i%20li%E1%BB%87u%20BTL/Bao%20cao%20Phan%20tich%20Bai%20toan%20CampusMind%20-%20BTL%20CSE122.docx).

---

## 📌 1. Phân Tích 4 Vai Trò, Nhiệm Vụ & Quyền Hạn (RBAC Matrix)

Căn cứ theo mục 2, 3 và 4 của Báo cáo Phân tích bài toán CampusMind:

| Vai Trò | Người Dùng Mẫu | Trách Nhiệm & Mục Tiêu | Quyền Hạn Nghiệp Vụ (Permissions) | Giao Diện Trọng Tâm |
| :--- | :--- | :--- | :--- | :--- |
| **1. Khách** *(Visitor)* | *Chưa đăng nhập* | Tìm hiểu thông tin, khám phá danh bạ dịch vụ và tài nguyên tự học để xây dựng niềm tin ban đầu. | **Read-only**: Xem danh bạ dịch vụ, cẩm nang thư viện, hồ sơ chuyên gia; làm trắc nghiệm AI-1; nút CTA chuyển sang đăng nhập khi cần đặt lịch. | `index.html`<br>`pages/visitor-service-directory.html`<br>`pages/visitor-resource-library.html`<br>`pages/visitor-counselor-detail.html` |
| **2. Sinh viên** *(Student)* | **Lê Ngọc An**<br>*(MSV: 2251061234 · K64 CNTT)* | Tự đánh giá mức độ căng thẳng, đặt/đổi/hủy lịch hẹn tư vấn bảo mật, theo dõi lộ trình và bài tập cá nhân. | **CRUD Lịch cá nhân**: Đặt lịch mới (Wizard 4 bước), hủy ca hẹn, xem chi tiết ca (Drawer), lưu bài tập AI-2 đề xuất, đánh giá cảm xúc (Mood Tracker). | `pages/student-dashboard.html`<br>`pages/student-booking.html`<br>`pages/student-appointments.html`<br>`pages/profile.html` |
| **3. Chuyên viên** *(Counselor)* | **TS. Nguyễn Minh Hà**<br>*(MS: CSL-004 · Phòng P.204 A1)* | Thiết lập quỹ thời gian trực tuần, tiếp nhận hàng chờ duyệt ca, ghi biên bản tham vấn và sử dụng trợ lý AI-3. | **Quản trị ca trực & Hồ sơ**: Cài đặt slot trống theo tuần/tháng, phê duyệt hoặc từ chối ca hẹn, soạn biên bản lâm sàng, phê duyệt tóm tắt từ AI-3. | `pages/counselor-appointment-queue.html`<br>`pages/counselor-schedule.html`<br>`pages/counselor-session-note.html` |
| **4. Quản trị viên** *(Admin)* | **Nguyễn Minh Đức**<br>*(MS: ADM-001 · Ban CTSV TLU)* | Giám sát vận hành toàn trường, quản trị danh mục dịch vụ và kiểm soát tài khoản người dùng an toàn. | **Toàn quyền hệ thống**: Giám sát KPIs & Audit Logs, CRUD danh mục dịch vụ (Thêm, Sửa, Ẩn/Hiện, Xóa), Khóa/Mở tài khoản, Đổi quyền RBAC. | `pages/admin-dashboard.html`<br>`pages/admin-service-management.html`<br>`pages/admin-user-management.html` |

---

## 📱 2. Bảng Đối Chiếu 24 Bản Thiết Kế Mockups & Mã Nguồn HTML

| Mockup SVG (`design/new_mockups/`) | Tên Màn Hình & Nghiệp Vụ BTL | Tệp HTML Mã Nguồn | Vai Trò Chính | Trạng Thái & Tính Năng Nổi Bật |
| :--- | :--- | :--- | :---: | :--- |
| `01_trang_chu_gioi_thieu.svg` | Trang chủ giới thiệu nền tảng & Hero TLU | [index.html](file:///d:/E/NAM%202/HK%201/WEB/cse122-campusmind-team02/cse122-campusmind-team02_demo/index.html) | Chung / Khách | Hero Banner, 4 lối vào dịch vụ, 3 cam kết an toàn, Crisis Hotline. |
| `02_danh_ba_dich_vu_ai1.svg` | Danh bạ 12 dịch vụ & AI-1 Sàng lọc nhu cầu | [`pages/visitor-service-directory.html`](file:///d:/E/NAM%202/HK%201/WEB/cse122-campusmind-team02/cse122-campusmind-team02_demo/pages/visitor-service-directory.html) | Khách / SV | Lọc thời gian thực theo danh mục, thanh tìm kiếm từ khóa, kích hoạt AI-1. |
| `04_ai1_buoc1_nhap_lieu.svg` | AI-1 Bước 1: Khung nhập liệu trắc nghiệm | *Tích hợp trong Modal AI-1* | AI-1 | Bộ 4 câu hỏi định hướng, tiến trình 25% → 100%, kiểm tra hợp lệ. |
| `05_ai1_buoc2_dang_xu_ly.svg` | AI-1 Bước 2: Hiệu ứng phân tích từ khóa | *Tích hợp trong Modal AI-1* | AI-1 | Trạng thái xử lý 1 giây, trích xuất từ khóa tâm lý và khớp slot chuyên gia. |
| `06_ai1_buoc3_ket_qua_giai_thich.svg` | AI-1 Bước 3: Đề xuất dịch vụ & Giải thích minh bạch | *Tích hợp trong Modal AI-1* | AI-1 | Thẻ kết quả, 3 luận điểm minh bạch (Explainability), nút Chấp nhận/Làm lại. |
| `07_ai1_buoc4_that_bai_chuyen_huong.svg` | AI-1 Bước 4: Xử lý ngoại lệ & Hotline khẩn cấp | *Tích hợp trong Modal AI-1* | AI-1 | Xử lý khi AI thất bại hoặc phát hiện khủng hoảng, 2 lối thoát an toàn. |
| `08_thu_vien_tai_nguyen_ai2.svg` | Thư viện tài nguyên & AI-2 Recommender | [`pages/visitor-resource-library.html`](file:///d:/E/NAM%202/HK%201/WEB/cse122-campusmind-team02/cse122-campusmind-team02_demo/pages/visitor-resource-library.html) | Khách / SV | Widget tương tác bài tập thở 4-7-8 có nhịp co giãn, gợi ý AI-2 cá nhân. |
| `09_ho_so_chuyen_vien_tu_van.svg` | Hồ sơ chi tiết chuyên gia TS. Nguyễn Minh Hà | [`pages/visitor-counselor-detail.html`](file:///d:/E/NAM%202/HK%201/WEB/cse122-campusmind-team02/cse122-campusmind-team02_demo/pages/visitor-counselor-detail.html) | Khách / SV | Thông tin bằng cấp, đánh giá sao, bảng lịch trực tuần có chấm trạng thái. |
| `10_bang_dieu_khien_sinh_vien.svg` | Bảng điều khiển sinh viên (Desktop & Mobile) | [`pages/student-dashboard.html`](file:///d:/E/NAM%202/HK%201/WEB/cse122-campusmind-team02/cse122-campusmind-team02_demo/pages/student-dashboard.html) | Sinh viên | 4 KPIs cá nhân, ca hẹn sắp tới chiều nay, bộ theo dõi tâm trạng (Mood Tracker). |
| `12_dat_lich_tu_van_wizard.svg` | Quy trình đặt lịch tư vấn 4 bước (Wizard) | [`pages/student-booking.html`](file:///d:/E/NAM%202/HK%201/WEB/cse122-campusmind-team02/cse122-campusmind-team02_demo/pages/student-booking.html) | Sinh viên | Wizard 4 bước: Chọn dịch vụ → Chọn slot → Nhập lý do & AI-2 → Xác nhận. |
| `14_lich_hen_cua_toi_drawer.svg` | Quản lý lịch hẹn sinh viên & Ngăn kéo chi tiết | [`pages/student-appointments.html`](file:///d:/E/NAM%202/HK%201/WEB/cse122-campusmind-team02/cse122-campusmind-team02_demo/pages/student-appointments.html) | Sinh viên | Bộ lọc 5 trạng thái, Side Drawer chi tiết #APT-1042, đổi ngày và hủy hẹn. |
| `15_trang_thai_chua_co_lich_hen_empty.svg` | Giao diện trạng thái rỗng (Empty State) | *Tích hợp tự động* | Trạng thái | Minh họa rỗng khi không có dữ liệu phù hợp kèm nút hành động. |
| `16_trang_thai_dang_tai_skeleton.svg` | Giao diện khung xương chờ tải (Skeleton Loading) | *Tích hợp tự động* | Trạng thái | Hiệu ứng shimmer chờ dữ liệu từ LocalStorage. |
| `17_trang_thai_loi_ket_noi_error.svg` | Giao diện thông báo lỗi kết nối mạng (Error State) | *Tích hợp tự động* | Trạng thái | Hộp cảnh báo lỗi và nút "Thử kết nối lại ngay". |
| `18_quan_ly_lich_lam_viec_chuyen_vien.svg` | Quản lý ca trực & Khung giờ làm việc chuyên gia | [`pages/counselor-schedule.html`](file:///d:/E/NAM%202/HK%201/WEB/cse122-campusmind-team02/cse122-campusmind-team02_demo/pages/counselor-schedule.html) | Chuyên viên | Ma trận lịch tuần Thứ 2 - Thứ 7, Bật/Tắt ca trực, Thêm slot mới, Khóa slot bận. |
| `19_hang_cho_duyet_ca_tu_van.svg` | Hàng chờ tiếp nhận và duyệt ca tư vấn | [`pages/counselor-appointment-queue.html`](file:///d:/E/NAM%202/HK%201/WEB/cse122-campusmind-team02/cse122-campusmind-team02_demo/pages/counselor-appointment-queue.html) | Chuyên viên | Danh sách sinh viên chờ duyệt, Tiếp nhận ca, Từ chối kèm lý do xây dựng. |
| `20_ghi_chu_ca_tu_van_ai3.svg` | Ghi chép biên bản ca tư vấn & Trợ lý AI-3 | [`pages/counselor-session-note.html`](file:///d:/E/NAM%202/HK%201/WEB/cse122-campusmind-team02/cse122-campusmind-team02_demo/pages/counselor-session-note.html) | Chuyên viên | Textarea đếm từ tự động, Trợ lý AI-3 tóm tắt 3 câu & 3 hành động, switch lỗi BTL. |
| `21_bang_dieu_khien_van_hanh_admin.svg` | Bảng điều phối vận hành toàn trường | [`pages/admin-dashboard.html`](file:///d:/E/NAM%202/HK%201/WEB/cse122-campusmind-team02/cse122-campusmind-team02_demo/pages/admin-dashboard.html) | Quản trị | 4 KPIs hệ thống, biểu đồ thanh ngang công suất theo ngày, Audit Log thời gian thực. |
| `22_quan_ly_danh_muc_dich_vu_crud.svg` | Quản lý danh mục dịch vụ CRUD đầy đủ | [`pages/admin-service-management.html`](file:///d:/E/NAM%202/HK%201/WEB/cse122-campusmind-team02/cse122-campusmind-team02_demo/pages/admin-service-management.html) | Quản trị | Bảng 12 dịch vụ, Modal Thêm/Sửa, Toggle Ẩn/Hiện (Active/Archive), Xóa an toàn. |
| `23_quan_ly_nguoi_dung_phan_quyen.svg` | Quản lý người dùng & Phân quyền RBAC | [`pages/admin-user-management.html`](file:///d:/E/NAM%202/HK%201/WEB/cse122-campusmind-team02/cse122-campusmind-team02_demo/pages/admin-user-management.html) | Quản trị | Bảng người dùng toàn trường, Khóa/Mở tài khoản, Đổi quyền, Cam kết bảo mật y tế. |
| `24_dang_nhap_chuyen_vai_tro.svg` | Đăng nhập hệ thống & 1-Click Role Switch | [`pages/login.html`](file:///d:/E/NAM%202/HK%201/WEB/cse122-campusmind-team02/cse122-campusmind-team02_demo/pages/login.html) | Xác thực | Form đăng nhập chuẩn, 4 nút 1-click chuyển nhanh vai trò phục vụ chấm điểm. |
| — | Đăng ký tài khoản sinh viên mới | [`pages/register.html`](file:///d:/E/NAM%202/HK%201/WEB/cse122-campusmind-team02/cse122-campusmind-team02_demo/pages/register.html) | Xác thực | Biểu mẫu thông tin sinh viên kèm kiểm tra hợp lệ validation chặt chẽ. |
| — | Hồ sơ cá nhân & Cài đặt thông báo | [`pages/profile.html`](file:///d:/E/NAM%202/HK%201/WEB/cse122-campusmind-team02/cse122-campusmind-team02_demo/pages/profile.html) | Cá nhân | Cập nhật số điện thoại, email, tùy chọn nhắc nhở và nút đăng xuất. |
| — | Trang từ chối truy cập RBAC (Forbidden) | [`pages/403.html`](file:///d:/E/NAM%202/HK%201/WEB/cse122-campusmind-team02/cse122-campusmind-team02_demo/pages/403.html) | Lỗi RBAC | Giải thích phân quyền, nút chuyển vai trò nhanh để tiếp tục kiểm thử. |
| — | Trang thông báo không tìm thấy (Not Found) | [`pages/404.html`](file:///d:/E/NAM%202/HK%201/WEB/cse122-campusmind-team02/cse122-campusmind-team02_demo/pages/404.html) | Lỗi 404 | Giao diện điều hướng thân thiện và các nút quay về trang dịch vụ an toàn. |
| — | **Showcase Hub & 3 Kích Thước Viewport** | [showcase.html](file:///d:/E/NAM%202/HK%201/WEB/cse122-campusmind-team02/cse122-campusmind-team02_demo/showcase.html) | Điều khiển | Trình duyệt đa thiết bị: Desktop (1440px), Tablet (768px), Mobile (390px). |

---

## 🎨 3. Quy Chuẩn Design Tokens 8 Màu Cốt Lõi (WCAG AA Compliant)

| Token Name | Mã Hex | Vai trò ngữ nghĩa | Ứng dụng trên giao diện |
| :--- | :---: | :--- | :--- |
| **Sage** *(Chủ đạo)* | `#2F7A66` | Màu chính (Primary) | Nút bấm chính, viền active, tab đang chọn, icon nổi bật |
| **Sage Deep** | `#1C5344` | Nhấn đậm (Deep Accent) | Thanh Header, tiêu đề lớn, button hover, sidebar badge |
| **Amber AI** | `#D79B34` | Nhận diện AI (Intelligence) | Huy hiệu AI (`badge-ai`), tiến trình 4 bước, cảnh báo nhẹ |
| **Clay Alert** | `#C4643F` | Cảnh báo / Hủy (Danger) | Lỗi nhập liệu, hủy ca hẹn, trạng thái bị từ chối, nút xóa |
| **Ink** | `#16241D` | Màu chữ chính (Text Primary) | Tiêu đề Fraunces, văn bản nội dung Be Vietnam Pro |
| **Paper** | `#F2EEE6` | Nền canvas (Surface Background) | Màu nền ấm áp cho toàn bộ 24 màn hình, chống chói mắt |
| **Sage Tint** | `#DCEAE3` | Nền phụ mềm mại (Soft Tint) | Chip phân loại dịch vụ, badge sinh viên, nền hover |
| **Sky Info** | `#3B6E92` | Thông tin / Trực tuyến (Info) | Trạng thái tư vấn online, badge chuyên viên, link trợ giúp |

---

## 🤖 4. Đáp Ứng Chuẩn 3 Trải Nghiệm AI (Mục 11–12 BTL-02)

Toàn bộ 3 tính năng AI đều tuân thủ chu trình 5 bước:
$$\text{Nhập} \longrightarrow \text{Đang xử lý (Loading 1s)} \longrightarrow \text{Kết quả} \longrightarrow \text{Lý giải minh bạch (Explainability)} \longrightarrow \text{Người dùng kiểm soát (Human-in-the-loop)}$$

1. **AI-1: Support Navigator** *(Trang `pages/visitor-service-directory.html`)*:
   - 4 câu hỏi trắc nghiệm sàng lọc áp lực học tập, lo âu, mất ngủ.
   - Trạng thái loading 1.0 giây trích xuất từ khóa tâm lý.
   - Thẻ kết quả kèm khối lý giải: *"Vì sao có kết quả này?"* và 2 nút: *Chấp nhận & Đặt lịch* hoặc *Làm lại*.
   - **Xử lý ngoại lệ (Fallback):** Khi bật test lỗi hoặc chọn câu trả lời khủng hoảng ➔ Hệ thống tự động chuyển sang giao diện Hotline 1900 6012 và tự duyệt 12 dịch vụ thủ công.
2. **AI-2: Resource Recommender** *(Trang `pages/visitor-resource-library.html` & `pages/student-booking.html`)*:
   - Tự động gợi ý bài tập thở 4-7-8 hoặc kỹ thuật neo 5-4-3-2-1 dựa trên từ khóa tìm kiếm và lý do đăng ký của sinh viên.
3. **AI-3: Counselor Summary Assistant** *(Trang `pages/counselor-session-note.html`)*:
   - Chuyên viên nhập ghi chép thô ➔ AI cô đọng thành **3 câu tóm tắt cốt lõi** và **3 hành động tiếp theo có thời hạn**.
   - **Xử lý ngoại lệ (Fallback):** Có nút gạt test lỗi *"Ghi chú < 25 từ"* ➔ AI từ chối tóm tắt để tránh sai lệch thông tin bệnh lý. Chuyên viên có toàn quyền chỉnh sửa và phê duyệt trước khi lưu chính thức.

---

## 🚀 5. Hướng Dẫn Chạy & Kiểm Thử Demo

### Cách 1: Mở trực tiếp bằng trình duyệt (Hỗ trợ 100% giao thức `file:///`)
- Bạn chỉ cần nhấp đúp chuột mở tệp [index.html](file:///d:/E/NAM%202/HK%201/WEB/cse122-campusmind-team02/cse122-campusmind-team02_demo/index.html) hoặc [showcase.html](file:///d:/E/NAM%202/HK%201/WEB/cse122-campusmind-team02/cse122-campusmind-team02_demo/showcase.html) trong Google Chrome, Microsoft Edge hoặc Cốc Cốc.
- Không cần cài đặt server hay cấu hình môi trường phức tạp.

### Cách 2: Trải nghiệm Showcase Hub Đa Thiết Bị
- Mở [showcase.html](file:///d:/E/NAM%202/HK%201/WEB/cse122-campusmind-team02/cse122-campusmind-team02_demo/showcase.html) để kiểm thử responsive trên cả 3 khung nhìn:
  - 🖥️ **Desktop:** 1440px
  - 📱 **Tablet:** 768px (iPad)
  - 📲 **Mobile:** 390px (iPhone)

### Cách 3: Thanh công cụ Demo Dock nổi (Floating Demo Toolbar)
- Ở dưới cùng của **mọi màn hình**, bạn sẽ thấy thanh điều khiển màu xanh Sage đậm:
  - Cho phép chuyển nhanh 4 vai trò (**Khách, Sinh viên, Chuyên viên, Admin**) chỉ với 1 click.
  - Cho phép nhảy ngay tới bất kỳ trang nào trong 17 trang chức năng.
  - Nút **Khôi phục dữ liệu gốc** (Reset LocalStorage) để làm mới toàn bộ dữ liệu mẫu ban đầu.
