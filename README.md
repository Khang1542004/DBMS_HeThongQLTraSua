# Hệ thống Quản lý Quy trình Trà Tiên Chá XíAn

## Môn học: Quản trị Cơ sở Dữ liệu  
**Trường Đại học Kinh tế – Đại học Đà Nẵng**  
**Khoa Thống kê – Tin học**

---

## Nhóm thực hiện: 48K212.05

- Nguyễn Nhuận Tiến  
- Nguyễn Trọng Khang  
- Phạm Ngọc Trung  
- Nguyễn Thị Khánh Linh  
- Đặng Thị Hậu  
- Đinh Thị Hoài Thương

**Giảng viên hướng dẫn:** Cô Cao Thị Nhâm

---

## Giới thiệu

Dự án nhằm xây dựng hệ thống quản lý cho quán trà sữa **Trà Tiên Chá XíAn**, với các chức năng quản lý nhập hàng, bán hàng, thống kê, báo cáo tài chính, và bảo mật cơ sở dữ liệu. Hệ thống mô phỏng các hoạt động thực tế như lập hóa đơn, tính lợi nhuận, backup & restore, và bảo vệ khỏi SQL Injection.

---

## Cấu trúc hệ thống

### 1. **Thiết kế Cơ sở dữ liệu**
- Sơ đồ ERD cho hóa đơn nhập hàng và bán hàng
- Chuẩn hóa, chuyển mô hình logic → vật lý
- Tích hợp sơ đồ quan hệ tổng thể

### 2. **Chức năng chính**
- Nhập - xuất hàng, cập nhật giá
- Tính toán lợi nhuận, doanh số, doanh thu
- Thống kê hàng bán chạy, hàng nhập nhiều
- Cơ chế phân quyền (Admin, Nhân viên)
- Bảo mật dữ liệu với mã hóa MD5
- Tự động backup và restore dữ liệu
- Triển khai dữ liệu lớn với Microsoft Azure

---

## Các module nổi bật

- `PROC_LuuNhapHang`: Lưu thông tin nhập hàng  
- `FUNC_TinhTongTienNhap`: Tính tổng hóa đơn nhập  
- `TRIGGER_UpdateTongTienNhap`: Cập nhật tổng tiền khi có thay đổi  
- `PROC_DoanhThuTheoNgay`: Doanh thu theo khoảng thời gian  
- `PROC_LoiNhuan`: Tính lợi nhuận bán hàng  
- `PROC_MonBanChay`: Món bán nhiều nhất cuối tuần  

---

## Bảo mật và An toàn dữ liệu

- Xác thực người dùng qua tài khoản phân quyền
- Trigger mã hóa mật khẩu bằng **MD5**
- Chống **SQL Injection** qua **Input Validation**
- Backup tự động lúc 13:30 mỗi ngày
- Hỗ trợ restore dữ liệu toàn phần

---

## Dữ liệu lớn & Azure

- Dự phòng lưu trữ qua **Microsoft Azure Storage**
- Tạo SQL Database trực tuyến
- Hỗ trợ upload file backup và kết nối từ Azure Data Studio

---

## Tài liệu dự án nhóm: https://drive.google.com/drive/folders/1wmkUV0LfG346FFeSx3AB5941vDudmyTO?usp=sharing

---

## Liên hệ
- Leader: Nguyễn Nhuận Tiến - ngnhuantien@gmail.com
- GVHD: ThS. Cao Thị Nhâm - nhamct@due.edu.vn
