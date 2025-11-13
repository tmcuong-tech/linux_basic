tắt và khởi động

renbot
- mục đích: khơi động lại server, máy tính
- cú pháp: reboot

shutdown
- cú pháp: shutdown [options] [time] [wall]
- options:
	-h: shutdown
	-r: restart
	-c: cancel pending shutdown
	time:
		now : thực hiện ngay lập tức
		hh:mm : ấn định thời gain thực hiện
		+m : sau m phút sẽ thực hiện
- wall: message thông báo
ví dụ: shutdown -r +10 "khoi dong lai may sau 10 phut"

