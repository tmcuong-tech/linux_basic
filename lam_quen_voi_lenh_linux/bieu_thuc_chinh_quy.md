BIỂU THỨC CHÍNH QUY - REGULAR EXPRESSION - REGEX
- Là một chuỗi ký tự đặc biệt được sử dụng để mô tả một mẫu chuỗi.
- Mục đích: Regex thường được sử dụng trong các hoạt động tìm kiếm, thay thế, xử lý văn bản.

ký hiệu 		mô tả
. 		Ký tự bất kỳ.

[] 		[..] Mô tả một tập hợp các ký tự, các mẫu. Còn [^...] là phủ định của [], phù hợp nếu không có ký tự nào trong [^].
		Đặc biệt:
		\w [a-zA-Z0-9_] (từ)
		\W=[^\w] [^a-zA-Z0-9_]
		\d [0-9]
[^] : 		\D[^0-9] [^d]
		\s=[\t\n\f\r\p{Z}] (các ký tự trắng tab, space, return...
		\s = [^] (không phải ký tự trắng)
		\b = phân cách các từ
		\B = không phải phân cách các từ
'*' 		Lặp lại 0 đến nhiều lần.
'+' 		Lặp lại 1 hoặc nhiều lần
'?' 		Tùy chọn có hay không cho mẫu phía trước đều được.
'?!...' 		Lookahead. (non-capture) Kết quả trả về khi ở trong chuỗi gốc, nó đứng trước chuỗi thỏa mãn lookahead.
{min, max) 	Độ dài. {min, } độ dài tối thiểu, {number} độ dài chính xác.
(xyz) 		Capture group. Biểu diễn nhóm mẫu và nhớ kết quả trả về.		
'|'		Thay thế (phép toán or, hoặc)
'\'		Dùng để biểu diễn ký tự đặc biệt [ ] ( ) { } . * + ? ^ $ \ '|'
'^'		Điểm bắt đầu của dòng.
\A		Điểm bắt đầu của chuỗi input.
'$'		Điểm kết thúc của dòng
\z		Điểm kết thúc chuỗi input

ví dụ:
mật khẩu tối thiểu 9 ký tự, bao gồm các ký tự bất kỳ
đáp án: .{8,}
giải thích:
'.' : ký tự bất kỳ
{8,} : tối thiểu là 8

có ít nhất 1 chữ hoa
đáp án: ^(?=.*[A-Z]).{8,}$
giải thích:
'^' : bắt đầu của 1 chuỗi
'?=.' : bắt đầu chuỗi bằng dấu '.' có hãy không cũng được
[A-Z] : phải có ít nhất 1 ký tự viết hoa từ A-Z
.{8,} : tối thiểu là 8 ký tự
'$' : kết thúc 1 chuỗi

Ví dụ
Email: ^[a-zA-Z0-9_]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$
'^': Bắt đầu của chuỗi.
[a-zA-Z0-9-]+: Một hoặc nhiều ký tự từ a đến z (viết thường hoặc viết hoa), số từ 0 đến 9 hoặc các ký tự đặc biệt như . hoặc
'@': Kỳ tự @.
'[a-zA-Z0-9.-]+': Một hoặc nhiều ký tự từ a đến z (viết thường hoặc viết hoa), số từ 0 đến 9 hoặc dấu gạch ngang.
'\': Dấu chấm.
'[a-zA-Z]{2,}': Ít nhất hai ký tự từ a đến z (viết thường hoặc viết hoa) cho phần mở rộng tên miền.
'$': Kết thúc của chuỗi.

Ví dụ
Biểu thức chính quy sau để kiểm tra số điện thoại với mã quốc gia +84 và sau đó là 9 chữ số, với hoặc không có dấu ngoặc đơn và khoảng trắng sau nó:
			^\(\+84\)\s{0,1}\d{9}$

Giải thích:
'^': Bắt đầu của chuỗi.
'\(': Dấu ngoặc đơn mở.
'\+84\': Mã quốc gia +84.
'\)\s{0,1}': Dấu ngoặc đơn đóng và sau đó là một khoảng trắng hoặc không có khoảng trắng.
'\d{9}': Chính xác chín chữ số sau đó.
'$': Kết thúc của chuỗi.

