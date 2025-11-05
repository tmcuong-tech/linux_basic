khởi động và run levels

thiết lập
- thiết lập Multi-user.target mặc định khi khởi động:
	#systemctl set-default multi-user.target
- thiết lập Graphical.target mặc định khi khởi động:
	#systemctl set-deddalt graphical.target
- chuyển đỏi các levels:
	từ graphical sang command mode:
		#systemctl isolate multi-user.target
	từ command mode sang graphical:
		#systemctl isolate graphical.target

init
lệnh init
- init là tiến trình đầu tiên được khởi chạy sau khi hệ thống đã được khởi động và là tiến trình cha của tất của các tiến trình khác trong hệ thống

	- run level 0 (init 0): chế độ tắt máy
	- run level 1 (init 1): chế độ này chỉ  sư dụng được 1 người dùng
	- run level 2 (init 2): chế độ đa người dùng nhưng không có dịch vụ NFS
	- run level 3 (init 3): chế độ đa người dùng, có đầy đủ các dịch vụ
	- run level 4 (init 4): chưa được sử dụng
	- run level 5 (init 5): chế độ đồ họa
	- run level 6 (init 6): khởi động lại máy
	- cú pháp: # init


