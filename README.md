# Code C demo thuật toán AES theo chế độ ECB:

Nhắc lại cách thức hoạt chế độ ECB:
------
Mã hóa:

![alt text](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d6/ECB_encryption.svg/601px-ECB_encryption.svg.png)

Giải mã:

![alt text](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e6/ECB_decryption.svg/601px-ECB_decryption.svg.png)

Mô tả:
------
#### Đầu vào: 
- bản rõ: chuỗi ký tự không giới hạn.
- khóa: chuỗi ký tự có độ dài thỏa mãn dưới 32 byte.
         
#### Xử lý:   
- khóa nếu không đủ độ dài 128/192/256 bit sẽ được thêm các bit 0 ở cuối cho đến độ dài tối thiểu để tạo khóa.
- bản rõ nếu có độ dài khác bội của 128 bit sẽ được thêm các bit 0 ở cuối rồi sau đó được chia thành các khối 128 bit.
- từng khối được đưa vào quá trình mã hóa và giải mã.

#### Đầu ra:  
- bản mã: chuỗi ký tự ban đầu đã được mã hóa.

#### Ngoài ra để tiện cho việc tìm hiểu thuật toán sinh khóa, trong quá trình mã hóa giải mã cũng hiển thị đầu vào dưới dạng mảng byte và các khóa con được sinh ra trong quá trình sinh khóa.

#### Để kiểm tra kết quả có thể thử lại với trang: http://aes.online-domain-tools.com/

Demo:
------
![alt text](https://image.prntscr.com/image/Xd77nDPaTjWFFBIMI-rW5w.png)
