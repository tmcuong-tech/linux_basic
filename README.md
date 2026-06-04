# Linux basic

Kho lưu trữ này là bộ ghi chú tiếng Việt về Linux, được sắp xếp theo từng chủ đề từ cơ bản đến thực hành. Mục tiêu của repo là giúp bạn tra cứu nhanh, học theo từng bước và ôn lại các lệnh thường dùng trong môi trường Linux.

## Nội dung chính

- Giới thiệu hệ điều hành Linux
- Làm quen với lệnh cơ bản
- Quản lý tệp tin và thư mục
- Quyền truy cập, user và group
- Cài đặt phần mềm
- Mạng và cấu hình IP
- Khởi động và tắt máy
- Lập trình shell

## Cách dùng

1. Chọn đúng nhóm chủ đề ở mục lục bên dưới.
2. Mở file Markdown tương ứng để đọc chi tiết.
3. Dùng repo như một sổ tay tra cứu nhanh khi học hoặc thực hành Linux.

## Cây thư mục

```text
linux_basic/
├── README.md
├── cai_dat_phan_mem/
│   ├── cai_dat_bo_go_tieng_viet.md
│   ├── cai_dat_codeblocks.md
│   ├── cai_dat_cong_cu_lap_trinh_c-cpp.md
│   ├── cai_dat_cong_cu_lap_trinh_java.md
│   ├── cai_dat_python_pycharm.md
│   ├── cai_dat_R_va_R_Studio.md
│   ├── cai_dat_va_xoa_ung_dung.md
│   └── cai_dat_visual_studio_code.md
├── gioi_thieu_he_dieu_hanh/
│   ├── cau_truc_he_dieu_hanh.md
│   └── learn_linux.md
├── khoi_dong_va_tat_may/
│   ├── khoi_dong_va_run_levels.md
│   └── tat_va_khoi_dong.md
├── lam_quen_voi_lenh_linux/
│   ├── bieu_thuc_chinh_quy.md
│   ├── cut_va_trich_xuat.md
│   ├── ngay_va_thoi_gian.md
│   ├── nhap_xuat_va_pipeline.md
│   ├── pwd_va_cd.md
│   ├── terminal_va_cau_lenh_linux.md
│   ├── tim_kiem_grep.md
│   ├── tim_kiem_tap_tin_find.md
│   ├── trinh_soan_thao_vim.md
│   ├── whereis_which.md
│   ├── wildcard.md
│   ├── xem_noi_dung_tap_tin.md
│   └── xem_thong_tin_he_thong.md
├── lap_trinh_shell/
│   ├── lap_trinh_shell_kiem_tra_so_nguyen_to.md
│   ├── lap_trinh_shell_bash.md
│   ├── lap_trinh_shell_cach_debug.md
│   ├── lap_trinh_shell_doc_ghi_du_lieu_tu_file_va_sap_xep_mang.md
│   ├── lap_trinh_shell_lenh_dieu_kien_va_phep_so_sanh.md
│   ├── lap_trinh_shell_lenh_nhap_xuat.md
│   ├── lap_trinh_shell_mang_du_lieu.md
│   ├── lap_trinh_shell_phep_tinh.md
│   ├── lap_trinh_shell_tim_gia_tri_nho_nhat.md
│   ├── lap_trinh_shell_truyen_tham_so.md
│   ├── lap_trinh_shell_vong_lap.md
│   └── lap_trinh_shell_xay_dung_ham.md
├── mang_va_cau_hinh_ip/
│   ├── cau_hinh_IP.md
│   └── cau_hinh_mang.md
├── quan_ly_tep_tin_va_thu_muc/
│   ├── cau_truc_cay_thu_muc.md
│   ├── file_system_quan_ly_thiet_bi.md
│   ├── hard_link_symbolic_link.md
│   ├── nen_va_giai_nen.md
│   └── quan_ly_file_va_thu_muc.md
└── quyen_va_nguoi_dung/
    ├── lenh_quyen_tren_file_thu_muc.md
    ├── quan_ly_group.md
    ├── quan_ly_user.md
    ├── quan_tri_group.md
    ├── quan_tri_user.md
    ├── quyen_tren_file_thu_muc.md
    └── sudo_va_password.md
```

## Mục lục

### 1. Giới thiệu hệ điều hành

- [Giới thiệu Linux](gioi_thieu_he_dieu_hanh/learn_linux.md)
- [Cấu trúc hệ điều hành](gioi_thieu_he_dieu_hanh/cau_truc_he_dieu_hanh.md)

### 2. Làm quen với lệnh Linux

- [Terminal và câu lệnh Linux](lam_quen_voi_lenh_linux/terminal_va_cau_lenh_linux.md)
- [pwd và cd](lam_quen_voi_lenh_linux/pwd_va_cd.md)
- [Xem thông tin hệ thống](lam_quen_voi_lenh_linux/xem_thong_tin_he_thong.md)
- [Ngày và thời gian](lam_quen_voi_lenh_linux/ngay_va_thoi_gian.md)
- [Tìm kiếm với grep](lam_quen_voi_lenh_linux/tim_kiem_grep.md)
- [Tìm tệp với find](lam_quen_voi_lenh_linux/tim_kiem_tap_tin_find.md)
- [whereis và which](lam_quen_voi_lenh_linux/whereis_which.md)
- [Wildcard](lam_quen_voi_lenh_linux/wildcard.md)
- [Xem nội dung tập tin](lam_quen_voi_lenh_linux/xem_noi_dung_tap_tin.md)
- [Nhập xuất và pipeline](lam_quen_voi_lenh_linux/nhap_xuat_va_pipeline.md)
- [Cut và trích xuất](lam_quen_voi_lenh_linux/cut_va_trich_xuat.md)
- [Trình soạn thảo Vim](lam_quen_voi_lenh_linux/trinh_soan_thao_vim.md)
- [Biểu thức chính quy](lam_quen_voi_lenh_linux/bieu_thuc_chinh_quy.md)

### 3. Quản lý tệp tin và thư mục

- [Quản lý file và thư mục](quan_ly_tep_tin_va_thu_muc/quan_ly_file_va_thu_muc.md)
- [Cấu trúc cây thư mục](quan_ly_tep_tin_va_thu_muc/cau_truc_cay_thu_muc.md)
- [File system và thiết bị](quan_ly_tep_tin_va_thu_muc/file_system_quan_ly_thiet_bi.md)
- [Hard link và symbolic link](quan_ly_tep_tin_va_thu_muc/hard_link_symbolic_link.md)
- [Nén và giải nén](quan_ly_tep_tin_va_thu_muc/nen_va_giai_nen.md)

### 4. Quyền và người dùng

- [Quyền trên file và thư mục](quyen_va_nguoi_dung/quyen_tren_file_thu_muc.md)
- [Lệnh quyền trên file và thư mục](quyen_va_nguoi_dung/lenh_quyen_tren_file_thu_muc.md)
- [sudo và password](quyen_va_nguoi_dung/sudo_va_password.md)
- [Quản lý user](quyen_va_nguoi_dung/quan_ly_user.md)
- [Quản trị user](quyen_va_nguoi_dung/quan_tri_user.md)
- [Quản lý group](quyen_va_nguoi_dung/quan_ly_group.md)
- [Quản trị group](quyen_va_nguoi_dung/quan_tri_group.md)

### 5. Cài đặt phần mềm

- [Cài đặt bộ gõ tiếng Việt](cai_dat_phan_mem/cai_dat_bo_go_tieng_viet.md)
- [Cài đặt Code::Blocks](cai_dat_phan_mem/cai_dat_codeblocks.md)
- [Cài đặt công cụ lập trình C/C++](cai_dat_phan_mem/cai_dat_cong_cu_lap_trinh_c-cpp.md)
- [Cài đặt công cụ lập trình Java](cai_dat_phan_mem/cai_dat_cong_cu_lap_trinh_java.md)
- [Cài đặt Python và PyCharm](cai_dat_phan_mem/cai_dat_python_pycharm.md)
- [Cài đặt R và RStudio](cai_dat_phan_mem/cai_dat_R_va_R_Studio.md)
- [Cài đặt và xóa ứng dụng](cai_dat_phan_mem/cai_dat_va_xoa_ung_dung.md)
- [Cài đặt Visual Studio Code](cai_dat_phan_mem/cai_dat_visual_studio_code.md)

### 6. Mạng và cấu hình IP

- [Cấu hình IP](mang_va_cau_hinh_ip/cau_hinh_IP.md)
- [Cấu hình mạng](mang_va_cau_hinh_ip/cau_hinh_mang.md)

### 7. Khởi động và tắt máy

- [Khởi động và run levels](khoi_dong_va_tat_may/khoi_dong_va_run_levels.md)
- [Tắt và khởi động](khoi_dong_va_tat_may/tat_va_khoi_dong.md)

### 8. Lập trình shell

- [Shell Bash](lap_trinh_shell/lap_trinh_shell_bash.md)
- [Cách debug shell script](lap_trinh_shell/lap_trinh_shell_cach_debug.md)
- [Đọc ghi dữ liệu từ file và sắp xếp mảng](lap_trinh_shell/lap_trinh_shell_doc_ghi_du_lieu_tu_file_va_sap_xep_mang.md)
- [Lệnh điều kiện và phép so sánh](lap_trinh_shell/lap_trinh_shell_lenh_dieu_kien_va_phep_so_sanh.md)
- [Lệnh nhập xuất](lap_trinh_shell/lap_trinh_shell_lenh_nhap_xuat.md)
- [Mảng dữ liệu](lap_trinh_shell/lap_trinh_shell_mang_du_lieu.md)
- [Phép tính](lap_trinh_shell/lap_trinh_shell_phep_tinh.md)
- [Tìm giá trị nhỏ nhất](lap_trinh_shell/lap_trinh_shell_tim_gia_tri_nho_nhat.md)
- [Truyền tham số](lap_trinh_shell/lap_trinh_shell_truyen_tham_so.md)
- [Vòng lặp](lap_trinh_shell/lap_trinh_shell_vong_lap.md)
- [Xây dựng hàm](lap_trinh_shell/lap_trinh_shell_xay_dung_ham.md)
- [Kiểm tra số nguyên tố](lap_trinh_shell/lap_trinh_shell_kiem_tra_so_nguyen_to.md)
