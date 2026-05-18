# 🌐 Enterprise Network Infrastructure Design & Management

**Đồ án môn học:** Mạng máy tính nâng cao  
**Học kỳ - Năm học:** Học kỳ 1 (2025 - 2026) | Năm 3  
**Trường:** Đại học Sư phạm Kỹ thuật TP.HCM (HCMUTE)

---

## 📝 Giới thiệu dự án
Dự án **Thiết kế, triển khai và quản trị hệ thống mạng doanh nghiệp** tập trung vào việc nghiên cứu, hoạch định và xây dựng một hạ tầng mạng toàn diện, có khả năng mở rộng, bảo mật cao và đảm bảo tính sẵn sàng (High Availability) cho một doanh nghiệp quy mô lớn (gồm Trụ sở chính và các Chi nhánh). 

Toàn bộ mô hình kiến trúc mạng được cấu hình, giả lập và kiểm thử chức năng trực quan trên nền tảng **Cisco Packet Tracer**.

### Các giải pháp và kỹ thuật triển khai cốt lõi:
- **Thiết kế mô hình phân lớp (Hierarchical Network Design):** Áp dụng mô hình chuẩn 3 lớp (Core - Distribution - Access) giúp tối ưu hóa hiệu năng truyền tải dữ liệu và quản lý tập trung.
- **Phân hoạch hạ tầng & Quy hoạch IP (VLAN & Subnetting):** Phân chia các phòng ban thành các vùng mạng (VLAN) độc lập (Kế toán, Nhân sự, IT, Giám đốc) kết hợp kỹ thuật chia subnet (VLSM) để tiết kiệm và tối ưu không gian địa chỉ IP.
- **Cấu hình định tuyến & Dự phòng (Routing & Redundancy):** Triển khai định tuyến động (OSPF) giữa các phân vùng mạng và thiết lập giao thức dự phòng cổng gateway mặc định (HSRP) kết hợp gộp băng thông (EtherChannel) nhằm đảm bảo hệ thống không bị gián đoạn khi xảy ra sự cố phần cứng.
- **Kiểm soát an ninh mạng (Network Security):** Triển khai danh sách kiểm soát truy cập (ACL) để chặn/cho phép lưu lượng mạng, thiết lập vùng phi quân sự (DMZ) bảo vệ cụm Server (Web, Mail, FTP) và cấu hình bảo mật cổng mạng (Port Security) ở lớp Access.

## 🛠️ Công nghệ & Công cụ sử dụng
- **Phần mềm giả lập:** Cisco Packet Tracer 8.x
- **Thiết bị mô phỏng:** Cisco Catalyst Switches (Core, Distribution, Access), Cisco Routers.
- **Giao thức triển khai:** OSPF, VLAN, Inter-VLAN Routing, EtherChannel, HSRP, NAT/PAT, DHCP, Standard/Extended ACL.
- **Quản lý mã nguồn:** Git & GitHub.

## 🚀 Hướng dẫn thực nghiệm (Lab Execution)

1. **Tải đồ án về máy:**
   ```bash
   git clone [https://github.com/an-ngnvi/enterprise-network-design.git](https://github.com/an-ngnvi/enterprise-network-design.git)
   cd enterprise-network-design