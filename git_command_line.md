## Một số thao tác cơ bản :sunglasses:
Câu lệnh | Chức năng
--- | ---
`$ git init` | Tạo repository trong thư mục mong muốn
`$ git status`| Để hiển thị danh sách của file đã được chỉnh sửa
`$ git add <file>`| Để thêm những file mà bạn muốn commit
`$ git add .`| Để thêm tất cả file
`$ git commit -m <message-of-commit>`| Để tạo 1 commit lên nhánh hiện tại
`$ git diff`| Xem phần sai khác của file được chỉnh sửa
`$ git log`| Để xem commit log
`$ git show <commit>`| Để xác nhận chi tiết của commit
`$ git mv <old-file-name> <new-file-name>`| Để di chuyển, thay đổi tên thư mục và file
`$ git rm <file>`| Để xóa file
`$ git checkout -- <file>`| Phục hồi lại file ban đầu sau khi đã chỉnh sửa 
`$ git reset HEAD <file>`| Muốn bỏ file đã thêm trong Index
`$ git add -u`| Muốn đăng ký trong tất cả Index chỉ những file đã có commit trước đó
`$ git log` | Muốn hiển thị các commit trước đó
`$ git clone <repository-url>` | Để tải về sourcecode của remote repository, tạo thành local repository ở máy mình <br/> Ví dụ: `*git clone https://github.com/hoihmy/git-study.git*`
`$ git pull or git pull origin <branch-name>` | Để cập nhật sourcecode mới nhất cho local repository từ remote repository
`$ git push origin <branch-name>` | Để chia sẽ lịch sử thay đổi của local repository mà bản thân đang có bằng remote repository, cần phải upload lịch sử thay đổi trong local repository

## Một số thao tác trên nhánh (branch)
Câu lệnh | Chức năng
--- | ---
`$ git branch`| Muốn hiển thị danh sách của branch
`$ git branch <branch-name>`| Tạo nhánh mới nhưng chưa chuyển qua nhánh đó, vẫn ở nhánh hiện tại
`$ git checkout <branch>`| Chuyển nhánh
`$ git checkout -b <branch-name`| Tạo nhánh mới và chuyển qua nhánh mới luôn
`$ git branch -m <old-branch> <new-branch>`| Muốn thay đổi tên nhánh
`$ git branch -d <branch-name>`| Xóa nhánh
`$ git merge <branch>`| Merge nhánh, nhánh đã chỉ định sẽ được đưa vào nhánh đang chỉ định của HEAD (Merge này là merge fast-forward)

## Một số thao tác tag
Câu lệnh | Chức năng
--- | ---
`$ git tag` | Muốn hiển thị danh sách của tag
`$ git tag <tag-name>` | Muốn tạo tag
`$ git tag -a <tag-name>` | Muốn tạo tag có gắn kèm chú thích
`$ git tag -d <tag-name>` | Muốn xóa tag

## Những cách khắc phục nhầm lẫn trong Git
Câu lệnh | Chức năng
--- | ---
`$ git config user.name "new-name"`<br/>`$ git config user.email "new-email"`<br/>`$ git commit --amend --reset-author` | Thay đổi tên tác giả của commit