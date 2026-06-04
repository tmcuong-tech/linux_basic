các lệnh quẩn lý user


tạo tài khoản user
useradd
- lệnh useradd: tạo tài khoản user
- cấu trúc lệnh: useradd [options] login_name
- options:
	-c: comment, tạo bí danh
	-u: set user ID. mặc định sẽ lấy số ID tiếp theo để gán cho user
	-d: chỉ định thư mục home
	-g: chỉ định nhóm chính
	-G: chỉ định nhóm phụ (nhóm mở rộng)
	-s: chỉ định shell cho user sử dụng

ví dụ:
tạo một user với tên mary và tên đầy đủ là Tung Le (tham so -c)
	#useradd -c "Tung Le" tungle
	#passwd tungle
	New UNIX password: *******
	Retype new UNIX password: *******


sửa thông tin tài khoản
usermod
sửa thông tin tài khoản 
- lệnh usermod: sẳ thông tin tài khoản
- cấu trúc lệnh: usermod [options] login_name
- options:
	-c: comment, tạo bí danh
	-l -d: thay đổi thư mục home
	-g: chỉ định nhóm chính
	-G: chỉ định nhóm phụ (nhóm mở rộng)
	-s: chỉ định shell cho user sử dụng
	-L: Lock account

ví dụ:
đổi tên tài khoản tungle thanh letung (tham số -l) với thư mục của user là /home/letung (tham số -d)

	#usermod -l letung -c "Jenny Barnes" -m -d /home/letung tungle


ví dụ 2:
tạo user với tên mary và tên đầy đủ Mary Smith (tham số -c), user thuộc về nhóm users và các nhóm wheel, sales

	#useradd -g usersletung -G wheel, sales -c "Mary Smith" mary
	$paswd mary
	New UNIX password: ******
	Retype new UNIX password: *******



xóa tài khoản user
- lệnh userdel: xóa tài khoản user
- cấu trúc lệnh: userdel [óptions] login_name
options: -r : xóa thư mục home của user

ví dụ: xóa tài khoản letung. 
	#userdel letung

- thư mục home của user không bị xóa khi sử dụng lệnh userdel, để xóa cả thư mục hơm của user, sử dụng tham số -r.

ví dụ: xóa tài khoản user letung và thư mục home của user. 
	#userdel -r letung

- khi xóa tài khoản user bằng userdek, dòng mô tả tương ứng cảu user trong các tập tin /etc/passwd và /etc/shadow cũng bị xóa


thiết lập các chính sách (policy) cho user
- lệnh chage: dùng để thiết lập các chín sách (policy) cho user
- cấu trúc lệnh: chage [options] login_name
- options:
	-l: xem chính sách của 1 user
	-E: thiết lập ngày hết hạn cho accout.
		ví dụ: chảng -E 6/30/2024 a1
	- l: thiết lập siis ngày bị khóa sau khi hết hạn mật khẩu
	-m: thiết lập số ngày tối thiểu được phép thay đỏi password
	-M: thiết lập số ngày tối đa đuqọc phép thay đổi password
	-W: thiết lập số ngày cảnh báo trước khi hểt hạn mật khẩu

ví dụ:
	chage -E "2030-04-30" -m 5 -M 90 -W 14 letung

- lệnh sẽ thiết lập mật khẩu hết hạn vào ngày 30/04/2030. ngoài ra, số ngày tối thiểu/tối đa giữa các lần thay đổi mật khẩu được thiết lập đến 5 và 90 tương ứng. một tin nhắn cảnh báo sẽ được gửi ra 14 ngày trước khi hết hạn mật khẩu



