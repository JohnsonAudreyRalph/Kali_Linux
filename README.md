# Kali Linux
<hr>

## Cài đặt và cập nhật phần mềm
* Thực hiện cập nhật danh sách gói phần mềm
```
sudo apt-get update
```
* Thực hiện nâng cấp tất cả gói đã cài lên phiên bản mới nhất
```
sudo apt-get update
```
* Thực hiện gỡ bỏ các gói phần mềm không cần thiết
```
sudo apt-get autoremove
```

## Cài đặt zerotier
* Bước 1: Cập nhật hệ thống
```
sudo apt update && sudo apt upgrade -y
```
* Bước 2: Cài đặt Zerotier
```
curl -s https://install.zerotier.com | sudo bash
```
* Bước 3: Bật dịch vụ ZeroTier
```
sudo systemctl start zerotier-one
sudo systemctl enable zerotier-one
```
* Bước 4: Tham gia mạng ZeroTier
```
sudo zerotier-cli join <network_id>
```
## Cấu hình VNC
* Bước 1: Cài đặt máy chủ VNC
```
sudo apt install tightvncserver
```
* Bước 2: Cài đặt môi trường đồ họa (nếu cần)
```
sudo apt install xfce4 xfce4-goodies
```
* Bước 3: Cấu hình VNC Server
Khởi động VNC server lần đầu để tạo file cấu hình
```
vncserver
```
Nhập mật khẩu VNC khi được yêu cầu (tối đa 8 ký tự). Bạn cũng có thể thiết lập mật khẩu xem-only nếu muốn.
* Bước 4: Khởi động VNC Server
```
vncserver :1
```
:1 là số hiển thị (display number), bạn có thể thay đổi (ví dụ: :2).
* Bước 5: Kết nối từ máy khách:
Kết nối đến địa chỉ IP của máy Kali kèm số hiển thị, ví dụ: 192.168.1.100:1 (thay IP của bạn).
