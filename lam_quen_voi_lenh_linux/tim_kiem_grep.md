CÂU LỆNH TÌM KIẾM GREP
lệnh grep:
- là công cụ tìm kiếm văn bản
- tìm kiếm chuỗi ký tự trong file haojc thư mục
- hỗ trợ biểu thức chính quy
tìm kiếm keyword trong 1 file
cú pháp: grep [option] pattern [file]
options thông dụng:
'-c': đếm số lần xuất hiện của string (count)
'-i': Bỏ qua phân biệt hoa thường
'-v': Lọc kết quả không khớp
'-n': hiển thị số dòng của từ tìm kiếm trong file

Ví dụ: tìm kiếm từ root trong file passwd
#grep 'root'/etc/passwd
