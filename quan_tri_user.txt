quản trị user

- trên linux có 2 loại tài khoản:
	+ tài khoản user hệ thống
	+ tìa khoản user người dùng

user hệ thống:
- dùng để thực thi các module, script cần thiết phục vụ cho hệ điều hành

user người dùng:
- tài khoản để login để sử dụng hệ điều hành.
- trong các tìa khoản user thì các tài khoản user root (superuser) là tài khoản quan trọng nhất.
- tài khoản này (root) được từ động tạo ra khi cài đặt linux.
- tài khoản này (root) không thể đổi tên hay xóa bỏ.
- user root còn được gọi là superuser vì có toàn quyền trên hệ thống.
- chỉ làm việc với tài khoản user root khi muốn thực hiện công tác quản trị hệ thống, trong các trường hợp khác chỉ nên làm việc với tài khoản user bình thường


mỗi user có các đặc điểm sau:
- tên mỗi user là duy nhất, chỉ có thể đặt tên chữ thường, chữ hoa.
- mỗi user có một max định danh tuy nhất (uid).
- mỗi user có thể thuộc về nhiều nhóm
- tìa khoản superuser có uid = gid = 0


file /etc/paswd:
- là file văn bản chứa thông tin về các tài khoản user trên máy. mọi user đều có thể đọc tập tin này nhưng chỉ có root mới có quyền thay đổi
- để xem nội dung của file ta dùng lệnh: #cat /etc/passwd
- cấu trúc của file gồm các hàng, mỗi hàng là thông tin của 1 user. dòng đầu tiên của tập tin mô tả thông tin cho user root (có ID = 0), tiếp theo là các tìa khoản khác của hệ thống, cuối cùng là các tài khoản người dùng thường. mỗi hàng được chia làm 7 cột các nhau bằng dấu ":".

ví dụ:
juser:x:3119:1000:J.Random User:/home/juser:/bin/bash

login name: juser
passwd: x
user ID: 3119
group ID: 1000
real name (GECOS): J.Random User
home directory: /home/juser
shell: /bin/bash



file /etc/shadow
- là tập tin văn bản chứa thông tin về mật khẩu của các tài khoản user trên máy. chỉ có root mới có quyền đọc tập tin này. user root có quyeenf reset mật khẩu của bất kỳ user nào trên máy

- mỗi dòng trong tập tin chứa thông tin về mật khẩu của user, định dạng của dòng gồm nhiều cột giá trị, dấu ":" được sử dụng để phân cách các cột

ví dụ
	user1:$1$bYFL1/.1$to.KQF0duniRnFEkgl/:13871:0:99999:7:::

user name: user1
encrypted password: $1$bYFL1/.1$toSr0.KQF0duniRnFEkgl/
lastchg days: 139871
mindays: 0
maxdays: 99999
warmdays: 7
inactive days: trống
disabled days: trống
not used: trống


ý nghĩa các cột giá trị như sau:
- cột 1: trên người sử dụng, tên này cũng giống vwois tên trong /etc/passwd
- cột 2: mật khẩu đã được mã hóa. để trống - không có mật khẩu, dấu "*" - tài khoản bị tạm ngưng (disable)
- cột 3: số ngày kể từ lần cuối thay đổi mật khẩu (tính từ 1/1/1970)
- cột 4: số ngày trước khi có thể thay đổi mật khẩu, giá trị 0 có nghĩa có thể thay đổi batas kỳ lúc nào
cột 5: số ngày mật khẩu có giá trị. 99999 có nghĩa mật khẩu có giá trị vô thời hạn
cột 6: số ngyaf cảnh bóa user trước khi mật khẩu hết hạn
cột 7: số ngày sau khi mật khẩu hết hạng tài khoản sẽ bị xóa. thường có giá trị 7 (một tuần)
cột 8: số ngày kể từ khi tài khoản bị khóa (tính từ 1/1/1970)



