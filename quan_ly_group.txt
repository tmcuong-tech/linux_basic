các leemjh quản lý group 



tạo nhóm
- lệnh groupadd: tạo nhóm
- cấu trúc lênh: groupadd [options] group
- options: -g GID: định nghĩa nhóm với mã nhóm GID
- group: tên nhóm định nghĩa

ví dụ: tạo nhóm user
	#groupsadd user

tạo nhóm accounting với GID = 200
	#groupadd -g 200 accounting
	

sửa thông tin nhóm

- lệnh groupmod: sửa thông tin nhóm
- cấu trúc câu lệnh: droupmod [options] group
- options:
	-g GID: sửa mã nhóm thành mã GID
	-n group_name: sửa tên nhóm thành group_name
- group: tên nhóm cần chỉnh sửa

ví dụ: 
- sửa gid cảu nhóm users thành 201
	#groupmood -g 201 users

- đổi tên nhóm accounting thành accountant
	#groupmod -n accouunting accountant
	
	
	
xóa nhóm
- lệnh groupdel: dùng để xóa nhóm
- cấu trúc lệnh: groupdel group

ví dụ:
- xóa nhóm testgroup
	#groupdel testgroup
	

