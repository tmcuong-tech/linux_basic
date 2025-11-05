lập trình shell xây dựng hàm

xây dựng hàm
- trong shell script, hàm là một khối mã được tổ chức để thực hiện các tác vụ cụ thể
- hàm có thể được gọi bất kỳ đâu trong chương trình và thực hiện một loạt các câu lệnh được định nghĩa nó
- hàm trong shell script thường được sử dụng để tái sử dụng mã

	# định nghĩa hàm in thông điệp mặc định
	print_default_manage() (
		echo "dây là một thông điệp mặc định"
	)

	# gọi hàm mà không truyền tham số
	print_defeult_manage

output:
	đây là một thông điệp mặc định
