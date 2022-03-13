Đầu tiên ta sẽ scan bằng công cụ nmap
![1-scan-nmap](https://user-images.githubusercontent.com/81396319/158061885-e5751caf-4980-43b0-9e33-838d1068c0e8.PNG)
Sau đó ta phát hiện có chạy vụ web và ta truy cập vào web thì phát hiện được một vài param khả nghi
![2-truycapweb-clickvaolinkbatky](https://user-images.githubusercontent.com/81396319/158061902-cce73147-4f5f-430d-ae33-2d21c61ab69c.PNG)
Ta thử chèn một số payload lfi và phát hiện trang web này tồn tại lổ hổng
![3-docfileetc](https://user-images.githubusercontent.com/81396319/158061924-0c26d8ba-e2ea-41a8-aa96-073889a3c81d.PNG)
Ta viewsource nhìn kỹ hơn sẽ thấy có 1 dòng comment là một user
![4-viewsourcephathienuser](https://user-images.githubusercontent.com/81396319/158061950-954a1be5-50a6-4258-b0a6-06f788fe35c5.PNG)
Ta thủ truy cập user đó thông qua dịch vụ ssh mà ta đã quét ở bước 1 và thành công lấy được phiên đăng nhập
![5-ssh](https://user-images.githubusercontent.com/81396319/158061984-fdeeac8e-751c-4d6d-b3a3-704a986f0390.PNG)
Sau đó ta sẽ chạy lệnh sudo -l và phát hiện được file socat có thể chạy bằng sudo bằng user ta đang dùng
![6-sudoexploit](https://user-images.githubusercontent.com/81396319/158062103-0d380b09-9b06-4f2c-9607-91092b12ccf3.PNG)
Sau đó ta sẽ lên trang https://gtfobins.github.io/gtfobins/socat/ và phát hiện được cách khai thác và thành công nâng lên quyền root
![7-ketqua](https://user-images.githubusercontent.com/81396319/158062164-6b913dc4-1bad-45b3-80fc-6630ec090c7f.PNG)

