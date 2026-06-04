lập trình shell thực hiện phép tính

tính toán trong shell
sử dụng expr
cú pháp: expr op1 phép_toán op2
ví dụ:
	expr 1 + 3
	expr 2 - 1
	expr 20 / 2
	expr 20 % 3
	expr 10 \* 3
	echo 'expr 6 \+ 3'

sử dụng let
ví dụ:
	let "z=$z+3"
	let "z += 3"
	let "z=$m*$n"
	
sử dụng $((...))
ví dụ:	
	z=$((z+3))
	z=$(($m*$n))

chú ý khi sử dụng dấu nháy:
": nháy kép bất cứ gì nằm trong nháy kép được xem là những ký tự riêng biệt
': nháy đơn những gì nằm trong dấu nháy đơn có ý nghĩa không đổi
': nháy ngược thực thi lệnh


1. 'expr':
- 'expr' là một tiện ích dòng lệnh được sử dụng để thực hiện các phép toán số học và các phép toán chuỗi
- kết quả của 'expr' được in ra stdout (standard output)
- cú pháp: 'expr <biểu_thức>'
'expr' yêu cầu các toán hạng và toán tử được đặt trong dấu nháy cách
ví dụ:
	'result=$(expr $a + $b)'
	
	
2. 'let':
- 'let': là một lệnh dành rieeng cho shell script để thực hiện các phép tính số học
- kết qủa của 'let' được gán vào một biến
- cú pháp: 'let <biến> = <biểu_thức>'
- 'let" không yêu cầu dấu cách giữa cấc toán hạng và toán tử
ví dụ:
	'let result=a+b'
	
3. '$(())'
- '$(())' là cú pháp trong bash shell để thực hiện các phép tính số học
- kết quả của '$(())' có thể được gán vào một biến hoặc in ra màn hình
- cú pháp: '$(<biểu_thức>)'  hoặc '$((<biểu_thức>))'
- '$(())' không yêu cầu dấu cách giữa các toán hạng và toán tử


sự khác biệt:
- 'expr' và 'let' cả 2 là các lệnh dành riêng cho shell script, trong khi '$(())' là một cú pháp của bash shell
- 'expr' yêu cầu dấu cách giữa các toán hạng và toán tử, trong khi 'let' và '$(())' không yêu cầu điều này
- 'let' gán kết quả vào biến, trong khi 'expr' và '$(())' có thể gán kết quả vào biến hoặc in ra stdout
- 'let' chỉ hỗ trợ các biến nguyên, trong khi 'expr' và '$(())' có thể xử lý cả biến nguyên và biến thực (floating point)






