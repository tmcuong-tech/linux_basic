hard link và symbolic link


links
- trong hệ điều hành linux, các liên kết (links) là một khái niệm quan trọng trong việc quản lý file system

ví dụ:
- giả sử chúng ta có một tệp có tên là "myfile" nằm trong thư mục "/home/user/documents". chúng ta có tể tạo một liên kết dến tập này trong một thư mục khác, chẳng hạn như "/home/user/desktop".


taị sao dùng link?
- tiết kiệm không gian lưu trữ: bằng cách tạo các liên kết, người dùng có thể chia sẻ cùng một dữ liệu giữ nhiều vị trí khác nhau mà không cần sao chép dữ liệu thực sự. điều này giúp tiết kiệm không gian lưu trữ, đặc biệt là khi có nhu cầu sử dụng nhiều bản san của cùng một tập tin hoặc thư mục
- dễ dàng tổ chức dữ liệu: sử dụng liên kết, người dùng có thể tổ chức và quản lý dữ liệu một cách linh hoạt. ví dụ, có thể tạo cấc liên kết giữa các tập tin và thư mục liên quan chức năng với nhau, giúp việc truy cập dữ liệu trở nên thuận tiện hơn


các chức năng của link
- chuyển cấc hướng và tổ chức tệp
- lập phiên bản và sao lưu tệp
- thư viện chia sè 
- cấu hình và tùy chỉnh hệ thống
- quản lý kho lưu trữ tệp lớn
- truy cập tệp từ xa
- tệp tham chiếu chéo
- lưu trữ trang web
- chia sẻ tệp và công tác
- giảm sử dụng dung lượng đĩa
- khả năng tương thích đa nền tảng


inode (index node)
- trên hệ thống linux, các tệp dược lưu trữ dưới dạng các khổi có kích thước nhất định. nếu một tệp lớn hơn kích thước được xác định trước này, nó sẽ được chia thành cấc phần và được lưu trữ trong các khối trống bất cứ  nơi nào chúng có sẵn trên ổ đĩa. với sự gia tăng số lượng tệp, điều này có thể dễ dàng gây nhầm lẫn. Inodes giúp hệ thống tổ chức dữ liệu


câu lệnh xem vị trí inode của các tệp tin
	ls -i hoặc ls -li


hard link
- hard link là một liên kết trực tiếp tới một inode trong hệ thống tệp của linux. khi bạn tạo một hard link cho một tệp, thực ra bạn đang tạo ra một bản sao trực tiếp của inode, cho phép nhiều tên file trỏ tới cùng một dữ liệu

file_goc (take inode from cell_memory: 1111) ------> cell_memory (inode of cell_memory: 1111) <------- file_hardlink (take inode from cell_memory: 1111)


cách tạo một hard link
- ban đầu file_goc có vị trí inode là: 1111
- tạo một hard link trỏ với inode của file_goc
	ln file_goc file_hardlink
		ln: (link) liên kết
		file_goc: file ban đầu trỏ tới inode của ô nhớ là: 1111
		file_hardlink: file cùng trỏ tới inode ô nhớ là: 1111
- sau khi tạo file_hardlink cũng sẽ có inode là: 1111
- khi file_goc bị xóa hoặc bị mất thì dữ liệu trong file_hardlink không vị ảnh hưởng (vần giữ nguyên)


lưu ý về hard link
- không thể tạo hard link cho thư mục: hard link chỉ hoạt động với các tệp, không thể tạo liên kết đến thư mục.
- khi xóa một hard link, dữ liệu vẫn tồn tại cho dến khi không có liên kết nào trỏ tới nó nữa
- khi thay đổi nội dung của tệp thông qua một hard link, thực chất bạn đang thay đổi đữ liệu trong inode mà tất cả các hard link trỏ tới. do đó, bất kỳ thay đổi nào thực hiên sẽ được phản ánh trên tất cả các hard link khác cùng trỏ với inode đó


khi nào sử dụng hard link
- khi cần tiết kiệm không gian đĩa và không gian muốn sao chép dữ liệu thưc sự
- khi muốn duy trì các phiên bản và sao lưu dữ liệu một cách hiện quả
- khi bạn cần truy cập nhanh chóng đến các tệp với nhiều tên khác nhau



symbilic link, hay còn được gọi là soft link
- symbolic link, hay còn được gọi là soft link, là một loại liên kết đặc biệt trong hệ thống tệp tin của linux. symbolic link tạo ra một liên kết từ một đường dẫn tới một tệp hoặc một thư mục khác, giúp tạo ra một "biến thể" của đường dẫn gốc.

file_softlink (take inode from file_goc: 2222) -------> (inode of file_goc: 2222) file_goc (take inode from cell_memory: 1111) -------> (inode of cell_memory: 1111) cell_memory

tạo soft link
- ban đầu file_goc chứa vị trí inode là: 1111
- tạo một soft link:
	ln -s file_goc file_softlink 
		ln: (link) liên kết
		-s: (symbolic) liên kết bằng symbolic
		file_goc (inode của file_goc: 1111): file ban đầu chứ inode của ô dữ liệu mà file_goc trỏ tới: 1111 | inode của file_goc: 2222
		file_softlink (inode của file_softlink: 2222): file trỏ tới inode của file_goc
sau khi tạo file_softlink
	+ inode của file_softlink: 2222 - vị trí ô nhớ của file_goc
	+ inode của file_goc: 1111 - vị trí ô nhớ của ô dữ liệu mà file_goc trỏ tới 


* lưu ý về symbolic link
- symbolic link cho phép tạo liên kết tới các tệp và thư mục ở các vị trí khác nhau trong hệ thống tệp
- người dùng có tể dễ đàng tạo, xóa hoặc si chuyển symbolic link mà không ảnh hưởng đến tệp gốc
- symbolic link có thể trỏ đến các tệp và thư mục trên các ổ đĩa khác nhau
- khi tệp hoặc thư mục gốc bị xóa, symblolic sẽ trở thành "có vấn đề" hoặc "hỏng"
- khi sử dụng symbolic link, hệ thống cần thực hiện một số thao tác để theo dõi đường dẫn, vì vậy truy cập thông qua symbolic link có thể chậm so với truy cập trực tiếp vào tệp gốc




khi nào sử dụng symbolic link
- khi cần tạo liên kết giữa các tệp và thư mục ở các vị trí khác nhau trong hệ thống tệp
- khi muốn tạo ra các biến thể hiện đường dẫn gốc mà không làm ảnh hưởng đến tệp gốc
- khi cần tạo liên kết giữa các ổ đĩa hoặc phân vùng khác nhau trên hệ thống 
