# Git summary

## Quay lại một commit:
1. git reset --hard [SHA]
2. git push -f origin [branch]

Git là một hệ thống quản lý phiên bản phân tán (Distributed Version Control System – DVCS), nó là một trong những hệ thống quản lý phiên bản phân tán phổ biến nhất hiện nay. Git cung cấp cho mỗi lập trình viên kho lưu trữ (repository) riêng chứa toàn bộ lịch sử thay đổi.
================================================================================
1. git cherry-pick
2. git stash
================================================================================
## 1. Branch
  - Các Branch (nhánh) đại diện cho các phiên bản cụ thể của một kho lưu trữ tách ra từ project chính của bạn.

  - Branch cho phép bạn theo dõi các thay đổi thử nghiệm bạn thực hiện đối với kho lưu trữ và có thể hoàn nguyên về các phiên bản cũ hơn.

## 2. Commit
  - Một commit đại diện cho một thời điểm cụ thể trong lịch sử dự án của bạn. Sử dụng lệnh commit kết hợp với lệnh git add để cho git biết những thay đổi bạn muốn lưu vào local repository.

## 3. Checkout
  - Sử dụng lệnh git checkout để chuyển giữa các branch. Chỉ cần nhập git checkout theo sau là tên của branch bạn muốn chuyển đến hoặc nhập git checkout master để trở về branch chính (master branch).

## 4. Fetch
  - Lệnh git fetch tìm nạp các bản sao và tải xuống tất cả các tệp branch vào máy tính của bạn. Sử dụng nó để lưu các thay đổi mới nhất vào kho lưu trữ của bạn. Nó có thể tìm nạp nhiều branch cùng một lúc.

## 5. Merge
  - Lệnh git merge kết hợp với các yêu cầu kéo (pull requests) để thêm các thay đổi từ nhánh này sang nhánh khác.

## 6. Pull
  - Pull requests thể hiện các đề xuất thay đổi cho nhánh chính. Nếu bạn làm việc với một nhóm, bạn có thể tạo các pull request để yêu cầu người bảo trì kho lưu trữ xem xét các thay đổi và hợp nhất chúng.

## 7. Push
  - Lệnh git push được sử dụng để cập nhật các nhánh từ xa với những thay đổi mới nhất mà đã commit.

---
# Các lệnh git cơ bản
## 1. git init
  - Tác dụng : Khởi tạo 1 git repository 1 project mới hoặc đã có.
  
  - Cách sử dụng: git init trong thư mục gốc của dự án.

## 2. git clone
  - Tác dụng: Copy 1 git repository từ remote source.
  
  - Cách sử dụng: git clone <:clone git url:>

## 3. git status
  - Tác dụng: Để check trạng thái của những file bạn đã thay đổi trong thư mục làm việc. VD: Tất cả các thay đổi cuối cùng từ lần commit cuối cùng.
  
  - Cách sử dụng: git status trong thư mục làm việc.

## 4. git add
  - Tác dụng: Thêm thay đổi đến stage/index trong thư mục làm việc.
  
  - Cách sử dụng: git add

## 5. git commit
  - Tác dụng: commit nghĩa là một action để Git lưu lại một snapshot của các sự thay đổi trong thư mục làm việc. Và các tập tin, thư mục được thay đổi đã phải nằm trong Staging Area
  - Ngoài ra trong Git bạn cũng có thể khôi phục lại tập tin trong lịch sử commit của nó để chia cho một branch khác, vì vậy bạn sẽ dễ dàng khôi phục lại các thay đổi trước đó.
  
  - Cách dùng: git commit -m ”description”

## 6. git push/git pull
  - Tác dụng: Push hoặc Pull các thay đổi đến remote. Nếu bạn đã added và committed các thay đổi và bạn muốn đẩy nó lên remote hoặc remote của bạn đã update và bạn apply tất cả thay đổi đó trên code của mình.

  - Cách dùng: 
    + git pull <:remote:> <:branch:>
    + git push <:remote:> <:branch:>

## 7. git checkout
  - Tác dụng: Chuyển sang branch khác

  - Cách dùng: 
    + git checkout <: branch:> 
    + git checkout -b <: branch:> nếu bạn muốn tạo và chuyển sang một chi nhánh mới.

## 8. git remote
  - Tác dụng: Để check remote/source bạn có hoặc add thêm remote

  - Cách dùng:
    + git remote để kiểm tra và liệt kê.
    + git remote add <: remote_url:> để thêm.

## 9. git branch
  - Tác dụng: liệt kê tất cả các branch (nhánh).

  - Cách dùng: 
    + git branch
    + git branch -a

## 10. git merge


