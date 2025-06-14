# Kali_Linux
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
