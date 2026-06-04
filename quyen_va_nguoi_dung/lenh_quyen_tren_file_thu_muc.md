các lệnh về quyền trên file và thư mục


lệnh chmod
- lệnh chmod: thay đổi quyền truy xuất trên thư mục/tập tin
- cấu trúc lệnh: chmod [options] Mode file
- options: 
	-R: áp dụng đối với thư mục làm cho lệnh chmod có tác dụng trên cả các thư mục con (đệ quy).
	Mode: quyền truy xuất mới tên tập tin
	

Mode: quyền truy xuất mới trên tập tin
- quyền truy xuất mới có thể gán cho từng nhóm quyền bằng cách sử dụng:
	u: đại diện cho quyền của người sở hữu (owner)
	g: đại diện cho quyền của nhóm (group)
	0: đại diện cho quyền của mọi người dùng khác (others)
- ký tự:
	"+": có ý nghĩa gán thêm quyền
	"-": có ý nghĩa tút bớt quyền
	"=": có ý nghĩa là gám
	

ví dụ:
g+w: thêm quyền ghi cho nhóm
o-rwx: loại bỏ tất cả các quyền cảu mọi người dùng khác
u+X: thêm quyền thực thi cho người sở hữu
+x: thêm quyền thực thi cho tất cả (mọi người)
a+rw: thêm quyền ghi đọc cho tất cả
ug+r: thêm quyền đọc cho owner và group
0=x: chỉ cho quyền thực thi với mọi người

ví dụ:
chmnod a-x passwd : xóa bỏ quyền thực thi (execute) của tất cả 
	chmod: lệnh thay đổi quyền truy xuất trên thư mục/tập tin
	a: (all) là tất cả các quyền (bao gồm owner, group, others)
	-: giảm bót quyền
	x: (execute) quyền thực thi
	passwd: tập tin passwd

chmod ug+x passwd: thêm quyền thực thi (x: execute) file passwd cho owner/user (u: owner) và nhóm (g: group)
	chmod: lệnh thay đổi quyền truy xuất trên thư mục/tập tin
	u: (user/owner) là người sở hữu
	g: (group) nhóm
	+: thêm quyền
	x: (execute) quyền thực thi
	passwd: tập tin passwd

chmod o-rwx passwd: xóa bỏ toàn quyền (không được truy xuất) của người dùng khác (others) đối với tập tin passwod
	chmod: lệnh thay đổi quyền truy xuất trên thư mục/tập tin
	o: (other) người dùng khác
	-: bớt quyền
	r: (read) quyền đọc
	w: (write) quyền ghi
	x: (execute) quyền thực thi
	passwd: tập tin passwd


lệnh chown
- lệnh chown: thay đổi người sở hữu thư mục/tập tin
- cấu trúc lệnh: chown [option] owner file
- options:
	-R: áp dụng đối với thư mục làm cho lệnh chmod có tác dụng trên cả các thư mục con (đệ quy)
	owner: người sở hữu mới trên tập tin
	
ví dụ
chown fedora hello: thay đổi chủ sở hữu mới cho một file
	chown: lệnh thay đổi người sở hữu thư mục/tập tin
	fedora: tên người sở hữu mới
	file: tên tập tin hoặc thư mục muốn đổi người sở hữu



lệnh chgrp:
- lệnh chgrp: thay đổi nhóm sở hữu thư mục/tập tin
- cấu trúc lệnh: chgrp [options] group file
- options:
	-R: áp dụng đối với thư mục làm cho lệnh chmod có tác dụng trên cả các thư mục con (đệ quy)
	group: nhóm sở hữu mới trên tập tin
	

ví dụ: thay đổi nhóm của tập tin
chgrp fedora hello: thay đổi nhóm sở hữu tập tin
	chgrp: lệnh thay đổi nhóm sở hữu
	fedora: tên nhóm sở hữu mới
	hello: tập tin hoặc thư mục muốn đổi nhóm sở hữu mới


