cài đặt và gỡ bỏ ứng dụng

cài đặt ứng dụng kho lưu trữ
- sử dụng apt để cài đặt ứng dụng từ kho lưu trữ debian
- sudo apt update - cập nhạt các gói mới nhất trong kho ứng dụng (chỉ cập nhật nhưng chưa cài đặt)
- sudo apt install <tên_ứng_dụng> - tải các gói ứng dụng về máy



cài đặt từ file.deb
- cài đặt:
	sudo dpkg -i /path/to/package.deb
	sudo apt install -f - nếu cần cài đặt các gói phụ thuộc bị thiếu

tải file bằng lệnh wget:
	wget -O /path/to/save/file<URL_ứng_dụng>

gỡ bỏ ứng dụng
	sudo <tên_gói_đã_cài_dặt_ứng_dụng_cần_xóa_trước_đó> -r <tên_ứng_dụng>
	-r (remove> : xóa

