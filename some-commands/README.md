# Các lệnh git cơ bản

##### 1. git init

- Tác dụng : Khởi tạo 1 git repository 1 project mới hoặc đã có.
- Cách sử dụng: git init trong thư mục gốc của dự án.

##### 2. git clone

- Tác dụng: Copy 1 git repository từ remote source.
- Cách sử dụng: git clone <:clone git url:>

##### 3. git status

- Tác dụng: Để check trạng thái của những file bạn đã thay đổi trong thư mục làm việc. VD: Tất cả các thay đổi cuối cùng từ lần commit cuối cùng.
- Cách sử dụng: git status trong thư mục làm việc.

##### 4. git add

- Tác dụng: Thêm thay đổi đến stage/index trong thư mục làm việc.
- Cách sử dụng: git add

##### 5. git commit

- Tác dụng: commit nghĩa là một action để Git lưu lại một snapshot của các sự thay đổi trong thư mục làm việc. Và các tập tin, thư mục được thay đổi đã phải nằm trong Staging Area
- Ngoài ra trong Git bạn cũng có thể khôi phục lại tập tin trong lịch sử commit của nó để chia cho một branch khác, vì vậy bạn sẽ dễ dàng khôi phục lại các thay đổi trước đó.
- Cách dùng: git commit -m ”description”

##### 6. git push/git pull

- Tác dụng: Push hoặc Pull các thay đổi đến remote. Nếu bạn đã added và committed các thay đổi và bạn muốn đẩy nó lên remote hoặc remote của bạn đã update và bạn apply tất cả thay đổi đó trên code của mình.
- Cách dùng:
  - git pull <:remote:> <:branch:>
  - git push <:remote:> <:branch:>

##### 7. git checkout

- Tác dụng: Chuyển sang branch khác
- Cách dùng:
  - git checkout <: branch:>
  - git checkout -b <: branch:> nếu bạn muốn tạo và chuyển sang một chi nhánh mới.

##### 8. git remote

- Tác dụng: Để check remote/source bạn có hoặc add thêm remote
- Cách dùng:
  - git remote để kiểm tra và liệt kê.
  - git remote add <: remote_url:> để thêm.

##### 9. git branch

- Tác dụng: liệt kê tất cả các branch (nhánh).
- Cách dùng:
  - git branch
  - git branch -a

##### 10. git merge
