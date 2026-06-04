lập tình shell mảng dữ liệu

mảng
- trong lập trình shell, mảng là một cấu trúc dữ liệu linh hoạt cho phép lưu trữ miền giá trị trong một biến. mảng trong shell không cần phải được khai báo với kích thước cố định và có thể chứa các loại sữ liệu khác nhau, bao gồm chuỗi, số nguyên và số thực


khai báo mảng:
# cách 1: khai báo bằng cách gán các giá trị trực tiếp
	my_array=("apple" "banana" "cherry")

# cách 2: khai báo mảng dựa trên kết qủa của một lệnh hoặc biến
	numbers=(1 2 3 4 5)
	file=(*.txt)



truy cập vào phần tử của mảng:
	# truy cập phần tử đầu tiên của mảng
	echo $(my_array[0]) # output: apple

	# truy cập vào phần tử thứ n của mảng
	echo $(my_array[2]) # output: cherry

	# truy cập vào tất cả các phần tử cảu mảng
	echo $(my_array[@]) # output: apple banana cherry

	# đếm số phần tử trong mảng
	echo $(#my_array[@]) # output: 3


xóa phần tử của mảng:
	# xóa phần tử tại vị trí cụ thể
	unset my_array[2]

	# xóa toàn bộ mảng
	unset my_array



duyệt qua mảng:
	# dùng vòng lặp for
	for element in "$(my_array[@])"; do
		echo $element
	done


	# dùng vòng lặp while
	i=0
	while [ $i -lt $(#my_array[@]) ]; do
		echo $(my_array[$i])
		((++i))
	done
