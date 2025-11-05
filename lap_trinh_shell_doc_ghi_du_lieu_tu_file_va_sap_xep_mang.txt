lập trình shell đọc ghi dữ liệu từ file và sắp xếp mảng


nội dung file docghifile_sapxepmang.sh
	#!/bin/bash

	# khai bao file
	file_input="$1"
	file_output="$2"

	# kiem tra file input co ton tai khong
	if [ ! -f "$file_input" ]; then
		echo "file khong ton tai"
		exit
	fi

	# doc mang tu file
	read -r -a arr < "$file_input"

	# lay so luong phan tu trong mang
	n=${#arr[@]}

	# sap xep mang
	for ((i = 0; i < n-1; i++)); do
		for ((j = 0; j < n-2; j++)); do
			if [ ${arr[j} -lt ${arr[i]} ]; then
				temp=${arr[i]}
				arr[i] = ${arr[j]}
				arr[j] = $temp
			fi
		done
	done

	# xuat mang
	echo "${arr[@]}" > "$file_output"


lưu file và thoát
ở terminal
	echo "9 5 3 1 5 9 10" >> input.txt
	cat input.txt
	touch output.txt
	sudo chmod a+x docghifile_sapxepmang.sh
	./docghifile_sapxepmang input.txt output.txt

ouput:
1 3 5 5 9 9 10
