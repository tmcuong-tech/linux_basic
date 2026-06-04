LỆNH TÌM KIẾM TẬP TIN - find
lệnh find
- lệnh tìm kiếm mạnh nhất với nhiều tham số nhưng thường tốn thời gian hơn các lệnh khác
cú pháp: find [vị trí] [tiêu chuẩn tìm]

Tiêu chuẩn tìm kiểm	Tùy chọn			Mô tả
Tên			-name pattern			Tìm các tệp hoặc thư mục có tên khớp với mẫu pattern.
Timestamp		-atime, -mtime, -ctime		Tìm các tệp dựa trên thời gian truy cập (atime), sửa đổi (mtime), hoặc tạo (ctime).
Quyền			-perm mode			Tìm các tệp có quyền truy cập khớp với mode.
Kích thước		-size n				Tìm các tệp có kích thước bằng n.
Group			-gid GID			Tìm các tệp thuộc nhóm với GID chỉ định.
User ID			-uid UID			Tìm các tệp thuộc người dùng với UID chỉ định.
Cấp thư mục con	-maxdepth levels		Xác định cấp độ tối đa của thư mục con để tìm kiếm (theo số levels).



Tìm file với kích thước xác định
cú pháp: find -type f -size +1M

'+': Lớn hơn kích thước chỉ định.
'-': Nhỏ hơn kích thước chỉ định.
'c': Chính xác kích thước chỉ định.
'k': Kích thước được đo bằng kilobyte.
'M': Kích thước được đo bằng megabyte,
'G': Kích thước được đo bằng gigabyte.
'+10k': Tệp có kích thước lớn hơn 10 kilobyte.
'-100M': Tệp có kích thước nhỏ hơn 100 megabyte.
'c20': Tệp có kích thước chính xác là 20 byte.
ví dụ: find -type f -size +10M -size -100M


Tìm file theo thời gian
'-mtime' : Tìm kiếm file theo thời gian sửa đổi
'-ctime' : Tìm kiếm file theo thời giai thay đổi trạng thái
'-atime' : TÌm kiếm file theo thời gian truy cập
ví dụ: find /path/to/directory/ -type f -atime -7


Sử dụng toán tử '-exec' để thực thi một số lệnh khác cho từng flie được tìm thấy 

find . -size +10M -size -100M -exec ls -lh {} \;

find /etc -size +10k -exec cp {} /data \;


In thông tin kết quả tìm kiếm

find-size +10M -size -100M -printf "%f %s\n"

'%a' : Quyền truy cập của file.
'%b' : Số lương block được sử dụng bởi file.
'%c' : Thời gian file được thay đổi lần cuối (sửtháng 1 năm 1970).
'%d' : Loại file (dấu hiệu thiết bị thư mục).
'%f' : Tên file.
'%g' : Nhóm sở hữu file.
'%h' : Liên kết tượng trưng (nếu có).
'%i' : Số inode của file.
'%k' : Kích thước file (byte).
'%l' : Số liên okết đến file.
'%m' : Thời gian file được sửa đổi lần cuối (chuỗi thời gian).
'%n' : Tên file (không bao gồm đường dẫn).
'%o' : Quyền truy cập của file (chế độ octal).
'%p' : Đường dẫn đầy đủ đến file.
'%s' : Kích thước file (đơn vị human-readable).
'%t' : Thời gian file được truy cập lần cuối.
'%u' : Chủ sở hữu file.
'%y' : Loại file (dấu hiệu thiết bị/thư mục).
'%%' : Dấu phần trăm (%).

