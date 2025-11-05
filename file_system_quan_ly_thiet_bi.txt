file system và quản lý thiết bị

linux file system
- ext4: đây là định dạng phần vùng mặc định trên hầu hết các bản phân phối linux hiện đại như ubuntu, fedora. nó hỗ trợ dung lượng lớn và các tính năng như journaling (ghi nhật ký) để bảo vệ dữ liệu trước sự cố mất điện

- XFS (XFS system): XFS là một hệ thống tệp có hiệu suất cao và hỗ trợ dung lượng lớn. nó dược sử dụng phổ biến trong các môi trường máy chủ và lưu trữ dữ liệu

- Btrfs (b-tree file system): Btrfs là một hệ thống tập phân tán mới có nhiều tính năng tiên tiến như snapshot, compression và đeuplication. nó cũng hỗ trợ phân vùng online, cho phép thay đổi kích thước phân vùng mà không cần khởi động lại hệ thống

- NTFS (New Technology File System): NTFS là một hệ thống tệp của window, nhưng linux cũng hỗ trợ đọc và ghi vào phân vùng NTFS. điều này cho phép người dùng chia sẻ dữ liệu hệ điều hành windows và linux

- FAT32 (File Allocation Table): FAT32 là một định dạng phổ biến cho các ổ đĩa di động và thẻ nhớ. nó hỗ trợ dung lượng nhỏ và có hạn chế về kích thước và dung lượng phân vùng

- exFAT (Extended File Allocation Table): exFAT là một phiên bản mở rộng của FAT32, hỗ trợ dung lượng lớn hơn và kích thước tệp lớn hơn

- Swap: phân vùng swap được sử dụng cho việc trao đổi trang và tăng hiệu suất của hệ thống linux bằng cách sử dụng không gian trên ổ cứng ddeerr làm bộ nhớ ảo khi bộ nhớ RAM không đủ.


một số lệnh dùng để quản lý ổ cứng
fdisk - đẻ phân chia partition của ổ cứng
mkfs - để format
mount - để gắn một partition đã format vào một mount poit


tham khảo bào viết:
https://funix.edu.vn/chia-se-kien-thuc/cach-quan-ly-phan-vung-dia-trong-linux-voi-fdisk/
https://quantrimang.com/cong-nghe/cach-mount-o-cung-phan-vung-bang-cach-su-dung-dong-len-linux-160276
