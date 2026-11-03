**Phần 1:**
Hiện tượng CSS không cập nhập: Do trình duyệt sử dụng cache phiên bản cũ của file CSS và khi An bấm phím F5 (Normal Refresh) tải thường thì mọi thứ vẫn  không cập nhật được CSS.
**Phiên đăng nhập bị mất khi đóng trình duyệt:**
Session Cookies (Cookie tạm thời): Khi mã nguồn cấp phát (cookie) mà không thiết lập thuộc tính Max-Age hoặc Expires, trình duyệt sẽ hiểu đây là một Session Cookie. Loại cookie này chỉ tồn tại trong suốt phiên làm việc và sẽ bị xóa tự động ngay khi người dùng đóng trình duyệt.

Persistent Cookies (Cookie bền vững): nếu được gán Max-Age hoặc Expires, cookie sẽ được ghi xuống ổ cứng và duy trì trạng thái vượt qua các phiên đóng/mở trình duyệt. Do thiếu hai thuộc tính này, An bị "văng" khỏi hệ thống mỗi lần mở lại trình duyệt.
**Phần 2: 2 giải pháp**
- Sử dụng phím tắt: Bấm tổ hợp phím Ctrl + F5 (hoặc Ctrl + Shift + R) trên Windows
hoặc Disable Cache trên F12
- Cấu hình thời gian sống cho Cookie: Tại đoạn mã thiết lập cookie định danh phiên trên server, An cần bổ sung thêm thuộc tính Max-Age (tính bằng giây) hoặc Expires.