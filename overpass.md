Scanning bằng công cụ nmap ta phát hiện được 2 port là 8- chạy http và 22 chạy ssh
![1-nmap](https://user-images.githubusercontent.com/81396319/158061351-6a1fc0be-e335-4496-abf9-f84b26f966ed.PNG)
Sau đó ta truy cập vô web và thử chạy công cụ dirsearch phát hiện được đường dẫn login.js
![3-dirsearch](https://user-images.githubusercontent.com/81396319/158061442-3cb79766-461c-4ddf-816e-dee6aa87b7b3.PNG)
Sau đó ta truy cập folder login.js và thấy đoạn code xử lý login
![2-loginjs](https://user-images.githubusercontent.com/81396319/158061375-9b2166ad-4310-41dc-88ac-9687f8ddd29c.PNG)
Đoạn code trong hình ngay chõ else cho ta thấy khi ta set cookie  SessionToken:statusOrCookie thì nó sẽ chuyển ta đến folder admin ở đây mình sẽ dùng công cụ curl để khai thác hoặc bạn có thể làm nó trực tiếp trên trình duyệt của mình
![4-thanhcong](https://user-images.githubusercontent.com/81396319/158061494-b0919a8c-365f-4deb-85ac-cb911cac8877.PNG)
Khi khai thác thành công ta phát hiện được 1 ssh key
Ta sẽ thử crack tài khoản ssh này bằng công cụ jhon ta tìm được password ssg 
![5-crackpass](https://user-images.githubusercontent.com/81396319/158061626-a4864d1a-89c7-42b6-a6db-8f2ab1f5a111.PNG)
  
