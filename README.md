1. Mục tiêu của phần này là theo dõi mọi thay đổi trái phép đối với các file quan trọng trong thư mục C:\Wazuh_Lab.
2. Tôi đã cấu hình file agent.conf để kích hoạt tính năng quét thời gian thực nhằm phản ứng tức thì với các thay đổi và đẩy báo cáo chi tiết các thay đổi về nội dung file lên Dashboard.

<img width="447" height="57" alt="{E6D7C25A-9A65-4318-BBCC-D63C95D2CB14}" src="https://github.com/user-attachments/assets/b053aa25-b223-4163-9ffe-7c0e2c60cb0f" />


Kịch bản thực hiện
Tạo file: Tạo new text document.txt và test.txt.
Chỉnh sửa: Thay đổi nội dung bên trong test.txt.
Xóa: Xóa file để kiểm tra khả năng phát hiện mất dữ liệu.

<img width="508" height="363" alt="{4CBBA7B1-BFA5-496E-A4F2-6DCE23180DE3}" src="https://github.com/user-attachments/assets/b04b51cd-be30-49de-8053-d7e0c2e057be" />

Phân tích kết quả
Dựa trên Dashboard của Wazuh, hệ thống đã ghi nhận chính xác 5 sự kiện (hits) trong khoảng thời gian từ 01:30 đến 01:45:

syscheck.event: added: Ghi nhận khi file mới được tạo.
syscheck.event: modified: Ghi nhận khi nội dung file bị can thiệp.
syscheck.event: deleted: Ghi nhận khi file bị xóa khỏi thư mục giám sát.

