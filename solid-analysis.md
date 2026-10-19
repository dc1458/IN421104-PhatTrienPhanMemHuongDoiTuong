1. Vi Phạm quy tắc S trong SOLID
* Ở cấp độ Class (ClubManager): Class này đang đóng quá nhiều vai trò: quản lý danh sách CLB \& thành viên, xử lý ghi log ra file, gửi thông báo (Email, Slack) và kiêm luôn việc xuất báo cáo.
* Hàm CreateClub: Làm tới 3 việc cùng lúc: Kiểm tra hợp lệ dữ liệu (Validate) -> Lưu thông tin -> Gửi thông báo email.
* Hàm AddMemberToClub: Vừa xử lý nghiệp vụ kiểm tra số lượng thành viên (tối đa 50) và thêm vào danh sách, vừa gửi Email chào mừng và gửi tin nhắn Slack.

