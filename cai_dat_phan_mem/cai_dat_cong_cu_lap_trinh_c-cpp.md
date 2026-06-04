cài đặt công cụ lập tình c/c++

- cài đặt bộ công cụ biên dịch c/c++:
	sudo apt update
	sudo apt install build-essential

- bộ công cụ build-essential bao gồm các công cụ cần thiết như gcc, g++, make,...

biên dịch và chạy chương trình
- biên dịch và chạy chương trình c/c++:
	g++ /path/to/name_file.cpp -o name_file
	-c (output) : in ra

- xem được nội dung đã chực thi file c/c++:
	tại thư mục có cùng name_file.cpp và name_file
		./name_file
	cat /path/to/name_file
