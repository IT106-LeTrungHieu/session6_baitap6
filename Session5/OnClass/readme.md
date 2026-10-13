# User Story 1

Là một quản trị viên hệ thống (Admin),

Tôi muốn tìm kiếm và xóa tài khoản của người dùng đã không còn hoạt động hoặc vi phạm quy định,

Để giải phóng tài nguyên hệ thống và loại bỏ các dữ liệu rác không còn sử dụng.

## Acceptance Criteria

### Kịch bản 1: Xoá tài khoản người dùng thành công

- Given: Quản trị viên đăng nhập thành công tài khoản quản trị và đang ở trang quản lí người dùng
- When: Quản trị viên tìm kiếm tài khoản người dùng cần xoá và ấn nút xoá và ấn xác nhận
- Then: Hệ thống kiểm tra quyền quản trị của tài khoản đang thực hiện xoá và chuyển trạng thái is_delete từ false thành true, thu hồi quyền sử dụng hệ thống của người dùng đó, sau đó trả thông báo thành công

### Kịch bản 2: Xoá tài khoản của 1 Quản trị viên khác hoặc xoá chính mình

- Given: Quản trị viên đang ở màn hình danh sách các tài khoản
- When: Quản trị viên nhìn vào các tài khoản Quản trị khác hoặc tài khoản của chính mình
- Then: Nút xoá bị làm mờ, chuyển con trỏ thành disable và không cho phép ấn, hoặc trả về 403 khi quản trị viên vẫn cố tình xoá quá gọi API thủ công

# User Story 2

Là một người dùng (sinh viên đang sử dụng hệ thống),

Tôi muốn chủ động yêu cầu xóa tài khoản cá nhân của chính mình kèm xác nhận mật khẩu,

Để bảo vệ quyền riêng tư và xóa bỏ toàn bộ thông tin cá nhân khỏi hệ thống khi tôi không còn nhu cầu học tập.

### Kịch bản 1: Người dùng nhập đúng mật khẩu

- Given: Người dùng
