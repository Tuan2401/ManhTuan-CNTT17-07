🎯 Mục tiêu 
  - Phát triển một hệ thống truyền file theo mô hình Client-Server, trong đó:
  - File gốc được chia nhỏ, mã hóa, ký số, sau đó truyền đi theo từng phần.
  - Đảm bảo tính bảo mật, toàn vẹn dữ liệu và xác thực nguồn gửi.

🎯 Mục đích
  - Giúp sinh viên hiểu rõ quy trình bảo mật dữ liệu trong môi trường mạng.
  - Thực hành lập trình các kỹ thuật:
  ✅ Mã hóa đối xứng (DES),
  ✅ Mã hóa bất đối xứng (RSA),
  ✅ Chữ ký số,
  ✅ Xác minh toàn vẹn bằng Hash.
  - Rèn luyện kỹ năng xây dựng ứng dụng web đơn giản bằng Flask, kết hợp giữa frontend và backend.
    
🏗️ Thành phần hệ thống
1. Người gửi (Sender)
  - Giao diện web cho phép người dùng chọn file để gửi.
  - Chia file thành 3 phần bằng thuật toán nội bộ.
  - Mã hóa nội dung từng phần bằng DES (CFB Mode).
  - Ký số từng phần bằng RSA (SHA-512).
  - Gửi lần lượt các phần tới Receiver qua HTTP POST.
![image](https://github.com/user-attachments/assets/381f44c0-e13d-49bd-ab86-97f3d111be23)

2. Người nhận (Receiver)
  - Lắng nghe cổng nhận dữ liệu từ Sender.
  - Nhận Handshake, Metadata, và từng phần dữ liệu.
  - Xác minh chữ ký, kiểm tra toàn vẹn, giải mã.
  - Khôi phục file gốc sau khi nhận đủ.
![image](https://github.com/user-attachments/assets/a354d740-da2e-4217-aa25-a3e31d160c3e)

🔒 Công nghệ bảo mật được áp dụng
  - Mã hóa khóa phiên: RSA
  - Mã hóa dữ liệu: DES - CFB Mode
  - Chữ ký số: RSA với thuật toán băm SHA-512
  - Kiểm tra toàn vẹn: SHA-512 Hashing

✅ Kết luận
  - Hệ thống đã mô phỏng thành công một quy trình truyền file an toàn qua mạng, bao gồm: mã hóa, ký số, chia phần, truyền từng phần, xác thực, giải mã và khôi phục dữ liệu.
  - Giúp người học nắm rõ ứng dụng thực tế của các thuật toán bảo mật như: RSA, DES, SHA-512.
  - Khả năng mở rộng: Có thể nâng cấp hệ thống để hỗ trợ nhiều định dạng file, nhiều phần chia hơn, hoặc thêm xác thực người dùng qua username/password.
  - Hệ thống là một nền tảng tốt cho việc học tập và nghiên cứu sâu hơn về an toàn thông tin và mạng máy tính.




