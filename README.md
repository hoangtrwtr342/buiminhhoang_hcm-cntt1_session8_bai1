Bài 1 : Xử lý Log máy chủ dung lượng lớn


Phần 1: Phân tích

Notepad có thể bị Not Responding vì phải nạp và hiển thị một tệp 800 MB. Việc xử lý văn bản lớn có thể dùng thêm bộ nhớ và làm giao diện bị quá tải.

Lệnh cat không chạy trong CMD truyền thống vì CMD không có lệnh đó. Trong PowerShell, cat là alias của Get-Content, nên lệnh được nhận diện ở đó. Tuy vậy, cat file vẫn cố in toàn bộ nội dung; với log lớn, nên xem theo trang hoặc chỉ lấy phần cần thiết.


Phần 2: Lệnh PowerShell

Xem toàn bộ tệp theo từng trang : Get-Content .\server_log_800MB.log | more

Nhấn Space để sang trang tiếp theo, hoặc Enter để xem thêm một dòng.

Xem 10 dòng cuối : Get-Content .\server_log_800MB.log -Tail 10
