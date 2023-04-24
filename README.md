# Git Summary

Git là một hệ thống quản lý phiên bản phân tán (Distributed Version Control System – DVCS), nó là một trong những hệ thống quản lý phiên bản phân tán phổ biến nhất hiện nay. Git cung cấp cho mỗi lập trình viên kho lưu trữ (repository) riêng chứa toàn bộ lịch sử thay đổi.

#### [I. Các lệnh git cơ bản](https://github.com/shounoop/git-summary/tree/master/some-commands)

#### II. Move Git commit between branches.

In Git, if you want to move a commit from one branch to another branch, you can use a combination of cherry-pick, reset, and checkout commands. Here's a step-by-step guide:

1. Note the commit hash: Before starting, take note of the commit hash you want to move. You can do this by using git log to view the commit history and find the hash associated with the commit.
2. Checkout the target branch: Switch to the branch where you want to move the commit using the git checkout command:

   ```
   git checkout target-branch
   ```

3. Cherry-pick the commit: Use the git cherry-pick command to apply the desired commit from the source branch to the target branch:
   ```
   git cherry-pick <commit-hash>
   ```
   Replace <commit-hash> with the hash of the commit you noted in step 1.
4. Checkout the source branch: Now, switch back to the source branch using the git checkout command:

   ```
   git checkout source-branch
   ```

5. Remove the commit from the source branch: To remove the commit from the source branch, use the git reset command followed by the commit hash of the previous commit:
   ```
   git reset --hard <previous-commit-hash>
   ```
   Replace <previous-commit-hash> with the hash of the commit immediately before the one you moved. This will move the branch pointer back to the previous commit, effectively removing the commit you moved from the source branch.
6. Verify the changes: Finally, check the commit history in both branches using git log to ensure that the commit has been moved successfully.

Keep in mind that this process will rewrite history, so use it with caution, especially when working with shared repositories. If you've already pushed the changes to a remote repository, you'll need to force-push the changes using git push --force. However, this can cause issues for other collaborators, so communicate with your team before making these changes.

#### III. Quay lại một commit.

1. git reset --hard [SHA]
2. git push -f origin [branch]

#### IV. git stash