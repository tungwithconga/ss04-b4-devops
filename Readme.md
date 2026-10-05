# Bài 4 - Quản lý .gitignore và Git Amend

## 1. Tình huống

File `credentials.txt` chứa thông tin nhạy cảm đã bị commit nhầm vào Git.

## 2. Gỡ file khỏi Git

Sử dụng lệnh:

git rm --cached credentials.txt

Lệnh trên gỡ `credentials.txt` khỏi sự theo dõi của Git nhưng vẫn giữ file vật lý trên máy.

## 3. Cấu hình .gitignore

Thêm vào file `.gitignore`:

credentials.txt

Sau đó Git sẽ bỏ qua file này trong các lần thay đổi tiếp theo.

## 4. Sửa commit gần nhất

Sử dụng:

git commit --amend -m "Add project files with secure gitignore configuration"

Lệnh `--amend` cho phép chỉnh sửa commit gần nhất thay vì tạo một commit mới.

## 5. Kiểm tra

Kiểm tra trạng thái:

git status

Kiểm tra commit gần nhất:

git log -n 1

Kiểm tra các file Git đang theo dõi:

git ls-files

Kết quả: `credentials.txt` vẫn tồn tại trên máy nhưng không còn được Git theo dõi.