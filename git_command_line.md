## Một số thao tác cơ bản :sunglasses:
Câu lệnh | Chức năng
--- | ---
`$ git init` | Tạo repository trong thư mục mong muốn
`$ git status` | Để hiển thị danh sách của file đã được chỉnh sửa
`$ git add <file>` | Để thêm những file mà bạn muốn commit
`$ git add .` | Để thêm tất cả file
`$ git commit -m <message-of-commit>` | Để tạo 1 commit lên nhánh hiện tại
`$ git diff` | Xem phần sai khác của file được chỉnh sửa
`$ git log` | Để xem commit log
`$ git show <commit>` | Để xác nhận chi tiết của commit
`$ git mv <old-file-name> <new-file-name>` | Để di chuyển, thay đổi tên thư mục và file
`$ git rm <file>` | Để xóa file
`$ git checkout -- <file>` | Phục hồi lại file ban đầu sau khi đã chỉnh sửa 
`$ git reset HEAD <file>` | Muốn bỏ file đã thêm trong Index
`$ git add -u` | Muốn đăng ký trong tất cả Index chỉ những file đã có commit trước đó
`$ git log` | Muốn hiển thị các commit trước đó
`$ git clone <repository-url>` | Để tải về sourcecode của remote repository, tạo thành local repository ở máy mình <br/> Ví dụ: *`$ git clone https://github.com/hoihmy/git-study.git`*
`$ git pull or git pull origin <branch-name>` | Để cập nhật sourcecode mới nhất cho local repository từ remote repository
`$ git push origin <branch-name>` | Để chia sẽ lịch sử thay đổi của local repository mà bản thân đang có bằng remote repository, cần phải upload lịch sử thay đổi trong local repository

## Một số thao tác trên nhánh (branch)
Câu lệnh | Chức năng
--- | ---
`$ git branch` | Muốn hiển thị danh sách của branch
`$ git branch <branch-name>` | Tạo nhánh mới nhưng chưa chuyển qua nhánh đó, vẫn ở nhánh hiện tại
`$ git checkout <branch>` | Chuyển nhánh
`$ git checkout -b <branch-name` | Tạo nhánh mới và chuyển qua nhánh mới luôn
`$ git branch -m <old-branch> <new-branch>` | Muốn thay đổi tên nhánh
`$ git branch -d <branch-name>` | Xóa nhánh
`$ git merge <branch>` | Merge nhánh, nhánh đã chỉ định sẽ được đưa vào nhánh đang chỉ định của HEAD (Merge này là merge fast-forward)

## Một số thao tác tag
Câu lệnh | Chức năng
--- | ---
`$ git tag` | Muốn hiển thị danh sách của tag
`$ git tag <tag-name>` | Muốn tạo tag
`$ git tag -a <tag-name>` | Muốn tạo tag có gắn kèm chú thích
`$ git tag -d <tag-name>` | Muốn xóa tag
`$ git push origin <tag-name>` | Muốn push single tag
`$ git push origin --tags` | Muốn push all tags

## Những cách khắc phục nhầm lẫn trong Git
Câu lệnh | Chức năng
--- | ---
`$ git config user.name "new-name"` <br/> `$ git config user.email "new-email"` <br/> `$ git commit --amend --reset-author` | Thay đổi tên tác giả của commit
`$ git reset <file-name>` | Muốn "undo" thay đổi trên một file cố định trước khi commit, có thể dùng lệnh *reset*
`$ git reset --soft HEAD~1` | Nếu muốn undo hẳn một commit (do đã lỡ commit xong rồi) và giữ lại những thay đổi hiện tại (chưa commit)
`$ git reset --hard HEAD~1` | Nếu muốn bỏ cả 1 commit trước đó và những phần đang thay đổi hiện tại <br/> Có thể thay đổi theo *HEAD~<số commit cần reset>*
`$ git commit --amend` | Để sửa lại commit vừa mới commit trước đó, có thể thay đổi commit message
`$ git add <file-name>` <br/> `$ git commit --amend` | Nếu nội dung muốn thay đổi không chỉ là message mà gồm cả thiếu file, thì đơn giản có thể add lại file và dùng amend
`$ git clean --force` | Khi branch đang làm việc có quá nhiều file mới (chưa được add), và mình muốn clean hết, thì có thể dùng một câu lệnh
`$ git stash save "stash-message"` | Để lưu lại những thay đổi ở hiện tại nhưng chưa muốn commit
`$ git stash save -u` or `git stash save --include-untracked` | Cũng có thể lưu trữ các tệp không được theo dõi
`$ git stash list` | Để hiển thị tất cả cách danh sách của stash
`$ git stash apply stash@{số stash}` | Apply stash theo id của nó <br/> Ví dụ apply stash thứ 2: *`$ git stash apply stash@{1}`*
`$ git stash drop stash@{số stash}` | Xóa stash theo id được chỉ định
`$ git stash show -p` | Xem toàn bộ những sự khác biệt