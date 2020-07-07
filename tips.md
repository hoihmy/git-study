## Một số thao tác cơ bản

|Câu lệnh|Chức năng| 
|---|:---:|:---:|
|`$ git init`| Tạo repository trong thư mục mong muốn|
|`$ git status`| Để hiển thị danh sách của file đã được chỉnh sửa|
|`$ git add <file>`| Để thêm những file mà bạn muốn commit|
|`$ git add .`| Để thêm tất cả file|
|`$ git commit -m <message-of-commit>`| Để tạo 1 commit lên nhánh hiện tại|
|`$ git diff`| Xem phần sai khác của file được chỉnh sửa|
|`$ git log`| Để xem commit log|
|`$ git show <commit>`| Để xác nhận chi tiết của commit|
|`$ git mv <oldfilename> <newfilename>`| Để di chuyển, thay đổi tên thư mục và file|
|`$ git rm <file>`| Để xóa file|
|`$ git checkout -- <file>`| Phục hồi lại file ban đầu sau khi đã chỉnh sửa |
|`$ git reset HEAD <file>`| Muốn bỏ file đã thêm trong Index|
|`$ git add -u`| Muốn đăng ký trong tất cả Index chỉ những file đã có commit trước đó|

## Một số thao tác trên nhánh (branch)
|Câu lệnh|Chức năng|
|---:|:---:|---:|
|`$ git branch`| Muốn hiển thị danh sách của branch|
|`$ git branch <branchname>`| Tạo nhánh mới nhưng chưa chuyển qua nhánh đó, vẫn ở nhánh hiện tại|
|`$ git checkout <branch>`| Chuyển nhánh|
|`$ git checkout -b <branchname`| Tạo nhánh mới và chuyển qua nhánh mới luôn|
|`$ git branch -m <oldbranch> <newbranch>`| Muốn thay đổi tên nhánh|
|`$ git branch -d <branchname>`| Xóa nhánh|
|`$ git merge <branch>`| Merge nhánh, nhánh đã chỉ định sẽ được đưa vào nhánh đang chỉ định của HEAD (Merge này là merge fast-forward)|

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3