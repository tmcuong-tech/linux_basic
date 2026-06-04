lập trình shell bash


lập trình shell là gì?
- lập trình shell là việc viết các tập lệnh (script) để thực hiện các tác vụ trong môi trường dòng lệnh
- script shell thường được sử dụng để tự động hóa các công việc lặp đi lập lại hoặc để thực hiện các tác vụ phức tạp


cách loại shell thông dụng trên Unix/Linux
-sh (shell bourme): shell nguyên thủy có mặt trên hầu hết các hệ thống Unix/Linux... nó rất hữu dụng cho việc lập trình shell nhưng nó không sử lý tương tác người dùng như các shel khác...

- bash (bourme Again shell); đây là phần mở rộng của sh, nó kế thừa những gì sh đã có và phát huy những gì sh chưa có. dây là shell được cài đặt mặc định trên các hệ thóng Linux

- csh, tcsh và zsh: sử dụng cấu trúc lệnh của C, là shell thông dụng thứ 2 sau bash shell


sử dụng công cụ để soạn thảo
- vi / vim
- gedit
- nano


phân quyền thưc thi
- gán quyền thực thi cho script
	chmod a+x tên_script
		chmod - dùng để chuyển chế độ / phân quyền
		a - all: tất cả
		x - execute: thực thi
		tên_cript : tên file muốn được cập quyền

- thực thi
	./tên_cript


cấu trúc
	#!/bin/bash - đánh dấu bash sẽ thực thi script
	command ... - các câu lệnh shell
	exit 0 - thoát chương trình


cú pháp của script shell
- mỗi dòng lệnh script được viết trên một dòng riêng
- bắt đầu script bằng dòng shebang #!/bin/bash để chỉ định shell mà script sẽ sử dụng (trong trường hợp này là bash)
- kết thúc mỗi dòng lệnh này bằng dấu chấm phẩy ';' hoặc không cần dấu chấm phẩy nếu muốn lệnh được viết trên một dòng riêng


biến trong shell
- biển hệ thống (system variable): được tạo bởi linux. kiểu biến này được viết bằng ký tự in hoa
-  biến do người dùng định nghĩa
	- biến trong shell được sử dụng để lưu trữ dữ liệu như chuỗi, số hoặc kết quả của một lệnh
	- gán giá trị cho biến: tên_biến = giá_trị
	- sử dụng giá trị của biến: $tên_biến


một số quy đinh về biến trong shell:
	(1) tên biến bắt đầu bằng ký tự hoặc dấu gạch chân '_'
	(2) không được có khoảng trắng trước và sau dấu bằng khi gán giá trị cho biến
	(3) biến có phân biệt chữ hoa và chữ thường
	(4) có thể khai báo một biến có giá trị là NULL như sau: var01= hoặc var01=""
	(5) không dùng dấu '?', '*' để đặt tên biến
- để truy xuất giá trị biens, dùng cú pháp sau: $tên_biến

ví dụ:
n=10
echo $n
