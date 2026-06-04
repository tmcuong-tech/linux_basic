lập trình shell lẹnh nhập xuất

giới thiệu
- lập trình shell là viêc viết các lệnh thực thi các công việc trên hệ điều hành Unix/Linux
- trong shell script, chúng ta có thể thực hiện các phép tính đơn giản và tương tác với người dùng trông qua lệnh nhập /xuất

lệnh echo
	1. in chuỗi
		echo "hello, world!"
	kết quả: 'hello, world!'
	trường hợp này 'echo' đơn giản là in ra chuỗi được đặt trong dấu '" "'

	2. in giá trị của biến
		name="alice"
		echo "hello, $name!"
	kết quả: 'hello, alice!'
	biến $name' được thay thế bằng giá trị cảu nó khi in ra màn hình

	3. in chuỗi chứa dấu "
		echo "she said, \"hello!\""
	kết quả: 'she said, "hello!"
	dấu '\' dược dùng để thoát khỏi dấu '"' trong chuỗi, tránh việc kết thúc chuỗi khi gặp dấu '"'.

	4. in chuỗi có chứa dấu '
		echo 'she said, "hello"'
	kết quả: 'she said, "hello!"'
	khi sử dụng dấu ('), các ký tự bên trong được xem như là chuỗi và không được phân tích

	5. sử dụng lệnh echo trong các biểu thức
		echo "today is $(date)"
	kết quả: 'today ís <ngày hiện tại>
	các dấu '$(...)'được sử dụng để thực hiện một biểu thức và chàn kết quà của biểu thức đó vào trong chuỗi được in ra

	6. sử dụng dấu backticks(') thay cho %()
		echo 'today is 'date'"
	kết quả: 'today is <ngày hiện tại>
	dấu backticks(') cũng thực hiện chức năng tương tự như '$(...)' đề chèn kết quả của một biểu thức vào trong chuỗi được in ra

	
	
lệnh read
- lênh read trong shell script được sử dụng để đọc sẽ liệu từ bàn phím và lưu nó vào các viến
	
cú pháp:
	read [options] [variable...]
		options: các tùy chọn để chỉnh cách 'read' hoạt động
		variable...: danh sách các biến mà giá trị đọc từ bàn phím sẽ được gán vào
	
ví dụ:
	echo "nhâp tên của bạn: "
	read name
	echo "xin chào, $name!"
	
	
	1. -p --prompt
	cho phép chỉ định một câu thông báo để hướng dẫn người dùng nhập dữ liệu
		read -p "nhập tên của bạn: " name
	
	2. -s --silent
	cho phép nhập mật khẩu mà không hiểm thị dữ liệu đang nhập trên màn hình
		read -s -p "nhập mật khẩu: " password
	
	3. -r --raw
	đọc dữ liệu mà không thực hiện xử lý escape sequences (như \ và $)
		read -r line
	
	4. -a --array
	đọc dữ liệu và lưu vào một mảng
		read -a names
	tùy chịn kết hợp
		các tùy chọn có thể được kết hợp để đáp ứng nhu cầu cụ thể của người dùng
			read -rsp "nhập mật khẩu: " password
	
	
	

