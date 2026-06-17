[readme.md.md](https://github.com/user-attachments/files/29029759/readme.md.md)
# HRM
# HRM - Employee Management & Organization Management

## 1. Giới thiệu

Tài liệu này mô tả các yêu cầu nghiệp vụ (BRD) cho hệ thống Quản lý Nhân sự (HRM) và Quản lý Cơ cấu Tổ chức (ORG) trong bệnh viện/cơ sở y tế.

Phạm vi bao gồm:

- Quản lý cơ cấu tổ chức
- Quản lý hồ sơ nhân sự
- Quy trình Onboarding
- Tích hợp Active Directory (AD)
- Điều chuyển nhân sự
- Theo dõi Audit Log

---

# 2. Mục tiêu

## Quản lý tổ chức (ORG)

- Quản lý cấu trúc tổ chức tập trung.
- Chuẩn hóa dữ liệu đơn vị.
- Quản lý khoa và phòng ban.
- Hỗ trợ điều chuyển nhân sự.

## Quản lý nhân sự (HRM)

- Quản lý hồ sơ nhân sự tập trung.
- Chuẩn hóa quy trình tiếp nhận nhân sự.
- Tự động hóa cấp phát tài khoản AD.
- Theo dõi vòng đời nhân sự.

---

# 3. Phạm vi nghiệp vụ

## Trong phạm vi

### ORG

- Quản lý khoa
- Quản lý phòng ban
- Điều chuyển nhân sự

### HRM

- Quản lý hồ sơ nhân sự
- Onboarding nhân sự
- Quản lý trạng thái nhân sự
- Tích hợp AD
- Audit Log

## Ngoài phạm vi

- Tuyển dụng
- Chấm công
- Tính lương
- KPI
- Đào tạo

---

# 4. Kiến trúc nghiệp vụ

```text
ORG
│
├── Khoa
│   ├── Phòng ban
│   │   └── Nhân sự
│
└── Điều chuyển nhân sự


HRM
│
├── Tạo hồ sơ nhân sự
├── Onboarding
├── Kích hoạt nhân sự
├── Tạo tài khoản AD
├── Quản lý trạng thái
└── Audit Log
```

---

# 5. Quy trình tổng quan

```text
Tạo hồ sơ nhân sự
        ↓
Deactive
        ↓
Nhân sự đến nhận việc
        ↓
HR xác nhận Onboarding
        ↓
Active nhân sự
        ↓
Tạo tài khoản AD
        ↓
Bắt đầu làm việc
        ↓
Điều chuyển đơn vị (nếu có)
        ↓
Nghỉ việc
```

---

# 6. Danh sách User Story

## Module ORG

| ID | User Story |
|----|------------|
| US-ORG-01 | Danh sách đơn vị tổ chức |
| US-ORG-02 | Xem chi tiết đơn vị tổ chức |
| US-ORG-03 | Tạo khoa |
| US-ORG-04 | Cập nhật khoa |
| US-ORG-05 | Ngừng sử dụng khoa |
| US-ORG-06 | Tạo phòng ban |
| US-ORG-07 | Cập nhật phòng ban |
| US-ORG-08 | Ngừng sử dụng phòng ban |
| US-ORG-09 | Điều chuyển nhân sự |

## Module HRM

| ID | User Story |
|----|------------|
| US-01 | Danh sách nhân sự |
| US-02 | Xem chi tiết nhân sự |
| US-03 | Tạo hồ sơ nhân sự |
| US-04 | Sinh mã nhân sự |
| US-05 | Cập nhật nhân sự |
| US-06 | Kích hoạt nhân sự |
| US-07 | Tạo tài khoản AD |
| US-08 | Quản lý trạng thái nhân sự |

---

# 7. Cấu trúc thư mục

```text
HRM/
│
├── README.md
│
├── BRD
│   │
│   ├── ORG
│   │   ├── US-ORG-01_DanhSachDonViToChuc.md
│   │   ├── US-ORG-02_ChiTietDonViToChuc.md
│   │   ├── US-ORG-03_TaoKhoa.md
│   │   ├── US-ORG-04_CapNhatKhoa.md
│   │   ├── US-ORG-05_NgungSuDungKhoa.md
│   │   ├── US-ORG-06_TaoPhongBan.md
│   │   ├── US-ORG-07_CapNhatPhongBan.md
│   │   ├── US-ORG-08_NgungSuDungPhongBan.md
│   │   └── US-ORG-09_DieuChuyenNhanSu.md
│   │
│   └── HRM
│       ├── US-01_DanhSachNhanSu.md
│       ├── US-02_XemChiTietNhanSu.md
│       ├── US-03_TaoHoSoNhanSu.md
│       ├── US-04_SinhMaNhanSu.md
│       ├── US-05_CapNhatNhanSu.md
│       ├── US-06_KichHoatNhanSu.md
│       ├── US-07_TaoTaiKhoanAD.md
│       └── US-08_QuanLyTrangThaiNhanSu.md
│
├── BPMN
│   ├── Employee_Lifecycle.md
│   ├── Onboarding_Process.md
│   ├── Organization_Management.md
│   ├── Employee_Transfer.md
│   └── AD_Integration.md
│
└── References
    ├── Business_Rules.md
    ├── Data_Model.md
    ├── RBAC.md
    └── Master_Data.md
```

---

# 8. Vai trò hệ thống

## Admin

- Quản lý cơ cấu tổ chức.
- Quản lý danh mục.
- Xem toàn bộ dữ liệu.
- Theo dõi Audit Log.

## HR

- Quản lý nhân sự.
- Onboarding nhân sự.
- Kích hoạt nhân sự.
- Điều chuyển nhân sự.
- Theo dõi trạng thái AD.

## Hệ thống AD

- Tạo tài khoản.
- Trả kết quả tạo tài khoản.
- Đồng bộ trạng thái tài khoản.

---

# 9. Mô hình dữ liệu tổ chức

## Khoa

- Mã khoa
- Tên khoa
- Trạng thái

## Phòng ban

- Mã phòng ban
- Tên phòng ban
- Khoa trực thuộc
- Trạng thái

---

# 10. Mô hình dữ liệu nhân sự

## Thông tin định danh

- Mã nhân sự
- Họ và tên

## Thông tin tổ chức

- Khoa
- Phòng ban

## Thông tin làm việc

- Ngày làm việc đầu tiên
- Ngày nghỉ việc
- Thời gian làm việc

## Thông tin hệ thống

- Trạng thái nhân sự
- Trạng thái AD
- Email AD
- Ngày tạo
- Người tạo

---

# 11. Trạng thái nhân sự

| Trạng thái | Mô tả |
|------------|--------|
| Draft | Hồ sơ mới tạo |
| Deactive | Chưa nhận việc |
| Active | Đang làm việc |
| Suspended | Tạm ngưng |
| Terminated | Nghỉ việc |

---

# 12. Trạng thái tài khoản AD

| Trạng thái | Mô tả |
|------------|--------|
| Pending | Chờ tạo |
| Success | Tạo thành công |
| Failed | Tạo thất bại |

---

# 13. Nguyên tắc thiết kế

- Áp dụng RBAC cho toàn bộ hệ thống.
- Mọi thay đổi dữ liệu phải được ghi nhận Audit Log.
- Không cho phép xóa dữ liệu đã phát sinh giao dịch.
- AD chỉ được tạo khi nhân sự được Active.
- Nhân sự phải thuộc một đơn vị tổ chức hợp lệ.
- Khoa hoặc phòng ban đang có nhân sự không được ngừng sử dụng.

---

# 14. Tài liệu liên quan

| Tài liệu | Mô tả |
|-----------|--------|
| Business_Rules.md | Quy tắc nghiệp vụ |
| Data_Model.md | Mô hình dữ liệu |
| RBAC.md | Phân quyền hệ thống |
| Employee_Lifecycle.md | Vòng đời nhân sự |
| Organization_Management.md | Quản lý cơ cấu tổ chức |
| Employee_Transfer.md | Điều chuyển nhân sự |
| AD_Integration.md | Tích hợp Active Directory |
| Onboarding_Process.md | Quy trình Onboarding |
