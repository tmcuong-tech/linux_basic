ngày và thời gian

date
lệnh date
mục đích: xem ngày và giờ của hệ thống
ví dụ: 
- date
- date + "%Y-%m-%d %H:%M:%S"

%D: ngày hiểm thị dưới dạng mm/đ/yy
%Y: Năm
%m: tháng (01-12)
%B: tên tháng viết đầy đủ (ví dụ: November)
%b: tên tháng viết tắt (ví dụ: Nov)
%d: ngày trong tháng (ví dụ: 01)
%j; ngày trong năm (001-366)
%u: ngày trong tuần (1-7)
%A: tên đầy đủ các ngày trong tuần (ví dụ: Friday)
%a: tên ngày trong tuần viết ngắn (ví dụ: Fri)
%H: giờ (00-23)
%I: giờ (01-12)
%M: phút (00-59)
%S: giây (00-60)


timedatectl
lệnh timedatectl
- hiểm thị thời gian hiện tại:
- thiết lập thời gian:
	+ sudo timedatectl set-time "YYYY-MM-ĐD HH:MM:SS"
	+ sudo timedatectl set-time "2024-02-22 09:30:00"
- thiết lập múi giờ:
	+ sudo timedatectl set-timezone [múi_giờ]
	+ sudo timedatectl set-timexone Asia/Ho_Chi_Minh
- bật/tắt tự động đồng bộ hóa thời gian với máy chủ NTP:
	+ sudo timedatectl set-ntp true (hoặc false)
- kiểm tra trạng thái đồng bộ hóa: timedatectl status

