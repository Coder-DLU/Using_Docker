# Lệnh Docker exec, lưu container thành image với commit, xuất image ra file
## 1:

![Container](aa.PNG)

- Cài đặt ping: root@ubuntu1:/# apt install iputils-ping
-  Chạy lệnh ping: root@ubuntu1:/# ping google.com
- Cài đặt Vim : root@ubuntu1:/# apt install vim
##1.1 Commit container thành Image:


![Container](aa1.PNG)

- tiến hành commit: Vào thư mục màn hình desktop bằng lệnh cd


![Container](aa2.PNG)

-  Bây giờ ngoài màn hình desktop sẽ có thư mục myImage.tar chúng ta vừa commit.
-  Chúng ta có thể sử dụng file Image này để chia sẽ cho nhiều máy tính.
-  Để sử dụng file image này chúng ta dùng lệnh: docker load -i myImage.tar
-  Chúng ta có thể đặt tên Repository và tag cho Image bằng lệnh sau: 
    docker tag IMAGE ID Tên_Repository:Tag 
# Cách chia sẻ dữ liệu từ máy host cho container và giữa các container với nhau.
- Bây giờ chúng ta tạo một folder Dulieu  chứa tập tin test.txt trong tập tin này chứa nội dung là xin chào.
- Để container truy cập được dữ liệu này cũng như ghi được dữ liệu vào file này và sau đó chúng ta xóa container đi và thư mục này vẫn còn tồn tại trên máy host: 
   + Chúng ta tạo một container chứa trong images ubuntu-vim 
   docker run -it -v pathHost:pathContainer Imageid
   
![Container](aa3.PNG)

- có thể sử dụng lện vi tenFile: để xem nội dung trong file 

 
