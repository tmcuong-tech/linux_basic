lập trình shell tìm giá trị nhỏ nhất


nội dung trong file timsonhonhat.sh
	#!/bin/bash

	# doc du lieu tu ban phim
	read -p "nhap vao cac so, cach nhau boi dau cach: " -a arr

	# luu so luong pha tu
	n=${#arr[@]}

	# in ra cach thanh phan trong mang
	echo "mang: ${arr[@]}"

	# bien luu gia tri nho nhat
	min=${arr[0]}

	# tim phan tu nho nhat
	for ((i = 1; i < n; i++)); do
		if [ ${arr[i]} -lt #min ]; then
			min=${arr[i]}
		fi
	done

	# in ra gia tri nho nhat
	echo "Min = $min"
