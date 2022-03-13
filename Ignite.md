Scanning Nmap
![1-Nmap](https://user-images.githubusercontent.com/81396319/158060816-5100b39f-aa9b-4818-9e16-d46b928ec933.PNG)
Phát hiện port 80 chạy dịch vụ http sau đó truy cập thử vào web và phát hiện trang web là giao diện fuel cms và sau khi duyệt web ta phát hiện được user default của cms này
![2-truycapweb](https://user-images.githubusercontent.com/81396319/158060869-326e35f2-2baa-4dbd-9d07-34053a3823e4.PNG)
Thử điền thông tin và ta truy cập được thành công
![3-login thanhcong](https://user-images.githubusercontent.com/81396319/158060889-fb6f5e1a-ae05-439b-818e-f7ade8bdff91.PNG)
Sau đó ta thực hiện tìm các lỗi cve của CMS này bằng công cụ searchploit ta phát hiện cms này có các lỗi RCE
![4-searcploit](https://user-images.githubusercontent.com/81396319/158060916-922ef8da-f0c8-4bc4-ad61-9fadb9df2ebf.PNG)
Sau đó ta sẽ copy code exploit và thử khai thác để lấy shell
![5-rce](https://user-images.githubusercontent.com/81396319/158060954-28383a39-00c2-46a8-b8b1-e81065a563fc.PNG)
Sau đó ta tạo file revershell và chạy python webserver và trên máy nạn nhân ta sẽ down file đó về qua lỗi rce và thục thi file để lấy shell
![6-shell](https://user-images.githubusercontent.com/81396319/158061004-259cf127-53b2-43de-b8d2-aa29684f0d09.PNG)
Sau khi download thành công ta thực thi và nhận được shell trả về 
![7-getrevshell](https://user-images.githubusercontent.com/81396319/158061026-4e0391de-c6c8-4658-8204-8170f7f4dafc.PNG)
Sau đó quay lại trang giao diện chính ta phát hiện được dường dẫn lưu database được đề cập trên đó
![8-goiy](https://user-images.githubusercontent.com/81396319/158061060-d3236de1-4659-471e-bc0d-c002703cf1e9.PNG)
ta thử truy cập theo đường dẫn và ta được 1 số file như hình sau
![9-findfile](https://user-images.githubusercontent.com/81396319/158061073-976c3fe6-23d0-4a8f-96a0-0ab9cc2dfc91.PNG)
Sau đó ta mở các file lên xem và phát hiện được file database.php có chưa thông tin của user
![10 findsuccess](https://user-images.githubusercontent.com/81396319/158061143-a4518ea9-2687-453b-80c1-275362cea122.PNG)
Sau đó ta thử truy cập user root bằng thông tin ta vừa tim được và thành công lấy đuộc phiên đăng nhập
![11-getflag](https://user-images.githubusercontent.com/81396319/158061173-f1491b89-cbad-4aee-9a13-f6cf991be1ee.PNG)
