# 🌐 Thiết Kế & Triển Khai Hệ Thống Mạng Doanh Nghiệp

**Đồ án môn học:** Mạng máy tính nâng cao  
**Học kỳ - Năm học:** Học kỳ 1 (2025 - 2026)  
**Trường:** Đại học Sư phạm Kỹ thuật TP.HCM (HCMUTE)  
**GVHD:** T.S Huỳnh Nguyễn Chính

---

## 📝 Giới thiệu dự án

Đồ án thiết kế, triển khai và quản trị hệ thống mạng doanh nghiệp quy mô lớn, bao gồm **Trụ sở chính (HQ)** và **Chi nhánh (Branch)**, được mô phỏng và kiểm thử toàn diện trên **Cisco Packet Tracer**.

Hệ thống áp dụng mô hình phân cấp 3 lớp (Core – Distribution – Access) kết hợp các giải pháp bảo mật chuyên sâu và kết nối liên vùng qua VPN Site-to-Site.

### Nội dung triển khai:

**Hạ tầng Layer 2 / Layer 3:**
- Phân vùng VLAN theo phòng ban (Kế toán, Kinh doanh, Kỹ thuật, Management)
- Inter-VLAN Routing tại Core Switch Layer 3
- EtherChannel / LACP Trunking tăng băng thông và dự phòng
- DHCP Server phân tách HQ và Branch; DNS Server nội bộ

**Bảo mật & An ninh mạng:**
- Firewall ASA phân vùng Inside / DMZ / Outside (Security Level)
- Static NAT xuất bản Web Server & Email Server ra Internet qua DMZ
- ACL kiểm soát truy cập giữa các phân vùng
- Port Security, DHCP Snooping, Layer 2 Hardening tại Access Switch
- SSH quản trị từ xa trên tất cả thiết bị
- Xác thực WiFi tập trung qua Radius Server

**Kết nối liên vùng:**
- VPN Site-to-Site (IPsec) giữa Firewall HQ và Firewall Branch
- OSPF định tuyến động liên vùng
- NAT/PAT cho truy cập Internet tại cả hai site

**Bài 2 – Thiết kế hệ thống nâng cao:**
- Tách biệt WiFi khỏi mạng nội bộ
- Quản trị tập trung thiết bị
- Bổ sung Application Server & Database Server nội bộ
- Cân bằng tải và bảo mật DMZ

## 🛠️ Công cụ & Giao thức sử dụng

- **Phần mềm:** Cisco Packet Tracer 8.x
- **Thiết bị:** Cisco Catalyst Switch (Core/Distribution/Access), Cisco Router, Cisco ASA Firewall
- **Giao thức:** OSPF, VLAN, Inter-VLAN Routing, EtherChannel (LACP), HSRP, DHCP, DNS, NAT/PAT, IPsec VPN Site-to-Site, ACL, SSH, DHCP Snooping, Radius

## 📐 Kiến trúc tổng thể

```
[Internet / ISP]
       |
[Firewall Branch] ←─ IPsec VPN ─→ [Firewall HQ]
       |                                   |
  [Branch LAN]          ┌──────────────────┤
  3 phòng ban           |                  |
                   [Core Switch L3]    [DMZ Zone]
                   (Inter-VLAN)       Web / Email Server
                   /         \
          [DistSW1]       [DistSW2]
          Building 2      Building 3
              |                |
         [AccessSW]        [AccessSW]
         End Users         End Users
```

## 🚀 Hướng dẫn thực nghiệm

1. Cài đặt **Cisco Packet Tracer 8.x** trên máy tính
2. Mở file `topology/network_topology.pkt`
3. Kiểm tra kết nối ping giữa các VLAN và giữa HQ ↔ Branch qua VPN
4. Tham khảo báo cáo để xem chi tiết từng bước cấu hình

## 📁 Cấu trúc thư mục

```
enterprise-network-design/
├── topology/
│   └── network_topology.pkt    # File mô phỏng Cisco Packet Tracer
└── docs/
    └── report.pdf               # Báo cáo đồ án đầy đủ
```

## 📊 Tài liệu dự án

- 📜 **[Báo cáo môn học (PDF)](docs/report.pdf)**

---
