# Hướng Dẫn Demo Blockchain Chuỗi Cung Ứng (Supply Chain)

Tài liệu này hướng dẫn từng bước quy trình demo trọn vẹn vòng đời của ứng dụng Supply Chain Blockchain.

## 📋 Điều Kiện & Cài Đặt

### 1. Chuẩn Bị Ví Metamask
Để demo tính năng phi tập trung một cách chân thực nhất, bạn nên chuẩn bị **5 tài khoản Ethereum khác nhau** trên ví MetaMask.

| Tài khoản | Vai trò (Role) | Mô tả |
|-----------|----------------|-------|
| **Account 1** | **Owner (Chủ sở hữu)** | Triển khai hợp đồng, đăng ký các vai trò, tạo đơn hàng. |
| **Account 2** | **RMS** | Nhà cung cấp nguyên liệu thô (Raw Material Supplier). |
| **Account 3** | **MAN** | Nhà sản xuất (Manufacturer). |
| **Account 4** | **DIS** | Nhà phân phối (Distributor). |
| **Account 5** | **RET** | Nhà bán lẻ (Retailer). |

> **Lưu ý:** Mặc dù về mặt kỹ thuật bạn có thể dùng 1 ví cho tất cả vai trò, nhưng việc dùng 5 ví sẽ giúp buổi demo chuyên nghiệp và thực tế hơn.

---

## 🚀 Quy Trình Demo Từng Bước

### Giai đoạn 1: Đăng ký Vai trò (Account 1 - Owner)

1.  **Đăng nhập:** Chuyển MetaMask sang **Account 1 (Owner)**.
2.  **Truy cập:** Vào trang **"Register Roles"**.
3.  **Thực hiện:** Đăng ký cho 4 tài khoản còn lại.
    *   **RMS:** Chọn `Raw Material Supplier`, điền địa chỉ ví **Account 2**, Tên (vd: "Cung ứng A"), Địa điểm war. Nhấn **Register**.
    *   **Manufacturer:** Chọn `Manufacturer`, điền địa chỉ ví **Account 3**, Tên (vd: "Xưởng SX B"), Địa điểm. Nhấn **Register**.
    *   **Distributor:** Chọn `Distributor`, điền địa chỉ ví **Account 4**, Tên (vd: "Vận tải C"), Địa điểm. Nhấn **Register**.
    *   **Retailer:** Chọn `Retailer`, điền địa chỉ ví **Account 5**, Tên (vd: "Siêu thị D"), Địa điểm. Nhấn **Register**.
4.  **Kiểm tra:** Xem bảng "Registered Roles" ở cuối trang để đảm bảo số lượng tài khoản đã tăng lên.

### Giai đoạn 2: Đặt Hàng Nguyên Liệu (Account 1 - Owner)

1.  **Vẫn giữ đăng nhập Account 1 (Owner).**
2.  **Truy cập:** Vào trang **"Order Materials"**.
3.  **Thực hiện:** Tạo đơn hàng mới.
    *   **Name:** Nhập tên sản phẩm (vd: "Thuốc Panadol").
    *   **Description:** Nhập mô tả (vd: "Lô hàng tháng 10").
    *   Nhấn **Create Order**.
4.  **Kết quả:** Ghi nhớ **Medicine ID** vừa tạo (ví dụ: ID: 1). Trạng thái lúc này là **Ordered**.

### Giai đoạn 3: Xử Lý Chuỗi Cung Ứng (Chuyển Đổi Tài Khoản)

#### Bước 1: Cung Cấp Nguyên Liệu (Account 2 - RMS)
1.  **Chuyển MetaMask sang Account 2.**
2.  **Truy cập:** Vào trang **"Supply Materials"** (Supply Chain Flow).
3.  **Thực hiện:** Kéo xuống phần **Step 1: Supply Raw Materials**.
    *   Nhập **Medicine ID** (vd: 1).
    *   Nhấn **Supply**.
4.  **Kết quả:** Trạng thái chuyển thành `Raw Material Supplied`.

#### Bước 2: Sản Xuất (Account 3 - MAN)
1.  **Chuyển MetaMask sang Account 3.**
2.  **Truy cập:** Vào trang **"Supply Materials"**.
3.  **Thực hiện:** Kéo xuống phần **Step 2: Manufacture**.
    *   Nhập **Medicine ID**.
    *   Nhấn **Manufacture**.
4.  **Kết quả:** Trạng thái chuyển thành `Manufacturing`.

#### Bước 3: Phân Phối (Account 4 - DIS)
1.  **Chuyển MetaMask sang Account 4.**
2.  **Truy cập:** Vào trang **"Supply Materials"**.
3.  **Thực hiện:** Kéo xuống phần **Step 3: Distribute**.
    *   Nhập **Medicine ID**.
    *   Nhấn **Distribute**.
4.  **Kết quả:** Trạng thái chuyển thành `Distribution`.

#### Bước 4: Bán Lẻ (Account 5 - RET)
1.  **Chuyển MetaMask sang Account 5.**
2.  **Truy cập:** Vào trang **"Supply Materials"**.
3.  **Thực hiện:** Kéo xuống phần **Step 4: Retail**.
    *   Nhập **Medicine ID**.
    *   Nhấn **Retail**.
4.  **Kết quả:** Trạng thái chuyển thành `Retail`.

#### Bước 5: Đánh Dấu Đã Bán (Account 5 - RET)
1.  **Vẫn giữ hoặc chuyển về Account 5 (Retailer).**
    *   *Lưu ý: Chỉ nhà bán lẻ mới có quyền xác nhận sản phẩm đã được bán cho người tiêu dùng.*
2.  **Truy cập:** Vào trang **"Supply Materials"**.
3.  **Thực hiện:** Kéo xuống phần **Step 5: Mark as Sold**.
    *   Nhập **Medicine ID**.
    *   Nhấn **Mark as Sold**.
4.  **Kết quả:** Trạng thái chuyển thành `Sold`.

### Giai đoạn 4: Theo Dõi & Truy Xuất (Bất Kỳ Tài Khoản Nào)

1.  **Truy cập:** Vào trang **"Track Materials"**.
2.  **Thực hiện:** Nhập **Medicine ID** (vd: 1) và nhấn **Track**.
3.  **Kết quả:**
    *   Xem toàn bộ lịch sử hành trình sản phẩm với thông tin chi tiết từng bước.
    *   Quét mã **QR Code** được tạo ra để xác thực thông tin.

---

## ❓ Câu Hỏi Thường Gặp (FAQ)

**Q: Tôi có nhất thiết phải dùng 4 địa chỉ ví khác nhau không?**
**A:** Về mặt kỹ thuật là **KHÔNG**, một ví có thể đóng nhiều vai trò nếu bạn (Owner) đăng ký chính ví đó cho nhiều vai trò. Tuy nhiên, để **demo** cho người khác thấy tính bảo mật và kiểm soát quyền truy cập của Blockchain (ví dụ: Nhà sản xuất không thể làm việc của Nhà phân phối), bạn **NÊN dùng 5 ví riêng biệt** như hướng dẫn trên.
