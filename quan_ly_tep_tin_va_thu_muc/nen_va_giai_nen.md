nén và giải nén

nén: gzip
gzip
cú pháp: gzip [options] [files...]
các tùy chọn quan trọng:
	-c, --stdout: in ra két quả nén trên màn hình thay vì ghi đè lên tệp tin gôc
	-d --decompress: giải nén tệp tin được nén
	-f, --force: bắt buộc nén tệp tin mà không hỏi lại người dùng
	-r, --recursive: nén tất cả các tệp tin trong thư mục và các thư mục con


giải nén: gupzip
gunzip
cú pháp: gunzip [options] [files...]
tùy chọn:
	-c, --stdout: in ra két quả nén trên màn hình
	-f, --force: bắt buộc nén tệp tin mà không hỏi lại người dùng
	-r, --recursive: nén tất cả các tệp tin trong thư mục và các thư mục con
	
nén và giải nén bằng lệnh tar
tar
cú pháp: tar [options] [files...]
các cú pháp phổ biến:
	-c hoặc --create: tạo một tệp tin nén mới
	-x hoặc --extract: giải nén một tệp tin đã tồn tại
	-f hoặc --file: xác định tên của tệp tin nén
	-v hoặc --verbose: hiểm thị thông tin chi tiết về quá trình làm việc
	-z hoặc gzip: sử dụng nén gzip khi tạo hoặc giải nén
	-j hoặc bzip2: sử dụng nén bzip2 khi tạo hoặc giải nén
	-r hoặc --append: thêm các tệp tin vào tệp tin nén đã tồn tại
	-t hoặc --list: liệt kê nội dung của tệp tin nén mà không giải nén
	

