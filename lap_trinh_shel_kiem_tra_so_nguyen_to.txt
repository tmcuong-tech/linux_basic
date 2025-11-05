lập tình shell kiểm tra số nguyên tố


nội dung file ktra_snt.sh
	#!/bin/bash

	# ham kiem tra snt
	is_prime(){
		# luu gia tri number
		n=$1

		# kiem tra n <= 1
		if [ $number -eq 1 ]; then
			echo "$n khong phai la so nguyen to"
			exit
		fi

		# kiem tra so nguyen to
		for((i = 2; i*i <= n; i++)); do
			if [ $((n % 1)) -eq 0 ]; then
				echo "$n khong phai la so nguyen to"
				exit
			fi
		done
		
		# neu khong bi vi pham
		echo "$n la so nguyen to"
	}

	# doc du lieu tu ban phim
	read -p "nhap so can kiem tra: " number

	# goi ham kiem tra snt
	is_prime $number
