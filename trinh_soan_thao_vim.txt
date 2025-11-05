trình soạn thảo vim(vi)

vim(vi)
trình soạn thảo vi
- vim là một trình soạn thảo văn bản hướng màn hình
- cho phép người dùng sử dụng các lệnh bàn phím đẻ điều hướng tài liệu, sửa đổi và lưu các thay đổi
- tất cả đều dựa trên văn bản. không có giao diện GUI.

tạo tập tin mới từ vi
cú pháp: vi fileName
- nếu không có nội dung trong file và thoát, file mới sẽ không được tạo ra

các chế độ làm việc của vi
- command mode: ở chế độ này ta sẽ sử dụng các lệnh để làm việc
- nếu muốn chỉnh sửa văn bản ta phải chuyển sang chế độ Text mode
- để chuyển từ chế độ Command mode sang Texr  mode ta bấm phím "i" hoặc "a" hoặc "insert"
- để chuyển từ chế độ Text mode sang Commmand mode ta bấm phím "esc"
- để thoát khỏi vi ta phải ở chế độ command mode và thực hiện lệnh thoát:
	+ thoát và không lưu cấc thay đổi ta dùng lệnh: ":q!"
	+ thoát và lưu: ":x: hoặc ":wq"


các câu lệnh cần nhớ (tối thiểu)
- ":set nu": hiểm thị số dòng cảu file (set number)
- ":set nonu": không hiểm thị số dòng của file 
- "dd": xóa dòng ngay vị trí con trỏ
- dG: xóa từ vị trí con trỏ đến cuối file (G: tổ hợp phím shift + g)
- sử dụng các phóm mũi tên để duy chuyển con trỏ chuột
- ":n": di chuyển con trỏ đén dòng số n
- "u": undo (khôi phục), quay lại các thao tác trước đó
- "/text": tìm kiếm từ text trong file, dùng phím "n" (text) để xem quả kết tiếp


nhóm lệnh:
1. chèn đoạn văn bản
	i: trước dáu con trỏ
	l: trước ký tự đầu tiên trên dòng
	a: sau dáu con trỏ
	A: sáu ký tự đầu tiên trên dòng
	o: dưới dòng lệnh hiện tại
	O: trên dòng hiện tại
	r: thay thé 1 ký tự hiện hành
	R: thay thế cho đến khi nhấn

2. các nhóm lệnh di chuyển con trỏ
	h: sang trái 1 space
	e: sang phải 1 space
	w: sang phải 1 từ
	b: sang trái 1 từ
	k: lên 1 dòng
	j: xuống một dòng
	): cuối câu
	(: dầu câu
	}: đầu đoạn văn
	{: cuối đoạn vân

3. nhóm lệnh xóa
	dw: xóa 1 từ
	d^: xóa ký tự từ con trỏ đến đầu dòng
	d$: xóa ký tự từ con trỏ đến cuối dòng
	3dw: xóa 3 từ
	dd: xóa dòng hiện hành
	5dd: xóa 5 dòng
	x: xóa ký tự
	cw: thay thế 1 từ
	3cw: thay thế 3 từ
	cc: xóa dòng hiện hành

4. nhóm lệnh tìm kiếm
	?: tìm trở lên
	/: tìm trở xuống
	*/and: thêm từ kế tiếp của and
	*?and: tìm từ kết thúc là and
	*/nThe: tìm dòng kế bắt đầu bằng The
	n: tìm hướng xuống
	N: tìm hướng lên

5. nhóm lệnh tim kiếm và thay thế
	:s/text1/text2/g : thay thế text1 bằng text2
	:1.$s/tập_tin/thư_mục : thay thế tập tin bằng thư mục từ bằng 1
	:g/one/s/1/g : thay thế one bằng 1

6. nhóm lệnh copy, paste, undo
	y: copy
	p: paste
	y$: copy từ vị trí hiện tại của cursor đến cuối cùng
	yy: copy toàn bộ dòng tại vị trí cursor
	3yy: copy 3 dòng liên tiếp
	u: undo lại thao tác trước đó

7. thao tác trên tập tin
	:w : ghi vào tập tin
	:x : lưu và thoát khỏi chế độ soạn thảo
	:wq : lưu và thoát khỏi chế độ soạn thảo
	:w : lưu vào tập tin mới
	:q : thoát nếu không có thay đổi
	:q! : thoát không lưu
	:r : mở tập tin đọc

