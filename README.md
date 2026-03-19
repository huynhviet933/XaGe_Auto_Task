# XaGe_Auto_Task
Auto Task
================================================================================
HƯỚNG DẪN CÀI ĐẶT VÀ SỬ DỤNG TOOL AUTO XAGE (NODE.JS) - BẢN FIX NODE 22
================================================================================

1. YÊU CẦU HỆ THỐNG:
   - Đã cài đặt Node.js (Khuyên dùng bản mới nhất hoặc v22+).
   - Thư mục chạy tool nên nằm ở ổ đĩa dễ truy cập (Ví dụ: D:\Zerg).

2. CÀI ĐẶT THƯ VIỆN (Mở CMD tại thư mục Tool và chạy lệnh):
   npm install axios https-proxy-agent@5.0.1 colors uuid

3. CHUẨN BỊ CÁC FILE DỮ LIỆU (Tạo cùng thư mục với file p1.js):
   - p1.js          : File mã nguồn Tool (Copy code đã fix ở trên).
   - Cookie.txt      : Mỗi dòng 1 Cookie (Dạng: connect.sid=s%3A...).
   - proxy.txt       : Mỗi dòng 1 Proxy (Dạng: http://user:pass@ip:port hoặc ip:port).
   - User_agents.txt : Mỗi dòng 1 User-Agent trình duyệt thật.
   - profiles.json   : (Tool tự tạo) Lưu UUID và UA cố định cho từng ví.

4. CƠ CHẾ HOẠT ĐỘNG CỦA TOOL (ANTI-BAN):
   - Bước 1: Login tài khoản, kiểm tra ví và số dư hiện tại.
   - Bước 2: Lấy danh sách nhiệm vụ chưa hoàn thành.
   - Bước 3 (QUAN TRỌNG): 
     + Nhận nhiệm vụ -> Nghỉ 15 giây (Giả lập mở web).
     + Verify -> Nghỉ 15 giây (Để server ghi nhận thời gian chờ).
     + Claim điểm -> Gửi API /complete.
   - Bước 4: Sau khi Claim thành công, nghỉ ngẫu nhiên 30-90 giây.
   - Bước 5: Nghỉ thêm 10 giây trước khi sang nhiệm vụ tiếp theo.
   - Bước 6: Sau khi xong 1 ví, nghỉ 30-60 giây mới chuyển sang ví mới.

5. CÁCH CHẠY TOOL:
   Mở CMD/Terminal và gõ lệnh: node p1

6. MỘT SỐ LƯU Ý QUAN TRỌNG:
   - Cookie: Không được bấm "Logout" trên trình duyệt sau khi lấy Cookie, nếu không Cookie sẽ bị hủy.
   - Proxy: Nên dùng Proxy chất lượng để tránh bị Server chặn IP (Rate limit).
   - Log: 
     + [Màu Xanh]: Thao tác thành công/Đang xử lý.
     + [Màu Tím]: Số điểm nhận được (+ 1500 $XAGE).
     + [Màu Đỏ]: Lỗi (Cookie die, Task lỗi hoặc mạng yếu).
   - Chỉnh sửa: Có thể sửa file proxy.txt ngay khi tool đang chạy, tool sẽ đọc proxy mới khi chuyển tài khoản.

7. XỬ LÝ LỖI PHỔ BIẾN:
   - Lỗi "ERR_PACKAGE_PATH_NOT_EXPORTED": Do bản https-proxy-agent không khớp. 
     => Khắc phục: Cài đúng bản 5.0.1 (npm install https-proxy-agent@5.0.1).
   - Lỗi "Task not started/Too fast": Do thời gian nghỉ quá ngắn. 
     => Khắc phục: Tool hiện tại đã set 30s tổng cộng, rất an toàn.

================================================================================

Tham Gia NHóm tele : https://t.me/HVchannelss

Tham Gia Discor ( Vip ) : https://discord.gg/gKxvTNu5

Tham gia NHóm VIp Với Chi Phí 8u/1thang Lợi ích tham gia nhóm ViP Sẽ được cấp keey sử dụng các tool vip trong discor hỗ trợ Và tham khao Code các tool dự án mà các bạn đề xuất

Gửi Phí tháng vào đây và chụp hình gửi trực tiếp cho tôi tại discor để xác nhận Role VIp ☕ https://huynhviet933.github.io/donate_viet_mmo/ Có thể tặng tôi ít cafe tại đây
