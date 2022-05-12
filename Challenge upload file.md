Level 1
Đầu tiên ta xem source code và phát hiện là server sẽ lấy file từ người dùng mà không kiểm tra lúc này ta có thể upload file php và thực thi shell
![lv-1](https://user-images.githubusercontent.com/81396319/168017463-d10b72b5-87b9-4b2c-b513-803668eb03fc.PNG)
Sau đó ta tiến hành uplaod file shell
![image](https://user-images.githubusercontent.com/81396319/168017841-2eee512d-41ba-43e1-9e65-7685f0423c11.png)
Thành công ta truy cập vô file theo dường dẫn và lấy được shell
![image](https://user-images.githubusercontent.com/81396319/168017880-af145a18-297c-41e8-9bac-5d67c0aa6549.png)

Level 2
Level 2 đầu tiên ta sẽ mở source và phát hiện lần này server đã filter extension file php nhưng lại chỉ lấy phần đầu extension vd shell.php.abc thì server chỉ kiểm tra đoạn php được tách ra bằng dấu "." 
![image](https://user-images.githubusercontent.com/81396319/168018199-d7bac4da-f0e4-47dd-abfc-fcc1bb2f92a0.png)
Để bypass ta chỉ cần thay double extension lên vd shell.php -> shell.jpg.php
![image](https://user-images.githubusercontent.com/81396319/168018587-2cc395bb-e3e9-43db-9678-8b7cae2513c7.png)
Thành công upload và thực thi shell
![image](https://user-images.githubusercontent.com/81396319/168018734-c6359857-ab15-469b-aeba-a5f16c5863a0.png)

Level 3
Ta mở source và phát hiện web lần này sẽ lấy phần cuối của đoạn chuỗi tách ra vd shell.php.abc -> nó sẽ lấy cuối cùng là abc và kiểm tra nếu là php sẽ bị filter
![image](https://user-images.githubusercontent.com/81396319/168019001-8f125bc3-a805-4dff-96c1-ff16ec19c0bd.png)
Để bypass ta chỉ cần thay extension khác chữ php nhưng vẫn thực thi code php , ở đây mình sẽ dùng phtml
![image](https://user-images.githubusercontent.com/81396319/168019207-e8e56431-3785-4f0a-9900-072847ed1f5e.png)
Thành công upload và thực thi shell
![image](https://user-images.githubusercontent.com/81396319/168019320-7001f05b-fed1-49a0-bde3-bff62dff46af.png)

Level 4
Level này web sẽ filter 3 extension là php phtml phar nhưng vẫn còn một số extension khác như php5 hay php7
![image](https://user-images.githubusercontent.com/81396319/168020102-510e653a-2192-49dc-ba2f-18063e9b6fe4.png)
Nhưng khi mình upload thì file của mình trở thành file text thay vì file php
![image](https://user-images.githubusercontent.com/81396319/168020272-be56fc48-c911-4c81-bbf4-8b3fad640576.png)
Điều này có thể do file htacces của server do đó mình sẽ thử 1 cách khác là upload file htaccess để thay đổi cấu hình file htacces webserver
![image](https://user-images.githubusercontent.com/81396319/168020533-dacff544-cd96-4cfd-8a0f-929df8ded48e.png)
![image](https://user-images.githubusercontent.com/81396319/168020671-e49e6e76-1c4a-4834-b5cd-ac40515bb564.png)
File đó sẽ thực thi file shell.jpg như một file php bình thường
![image](https://user-images.githubusercontent.com/81396319/168021289-78c5e261-b079-4537-9ffa-6aa3b14d21e4.png)
![image](https://user-images.githubusercontent.com/81396319/168021341-92918eeb-b09a-417c-9a04-9a55b4fecff6.png)



