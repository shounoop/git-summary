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

#### IV. git cherry-pick

git cherry-pick is a Git command used to apply changes from a specific commit to the current branch. It allows you to extract a single commit from a branch and apply it to another branch. This is useful when you want to apply changes made in one branch to another branch without merging the entire branch.

Here's how to use git cherry-pick:

1. Switch to the branch where you want to apply the changes.
   ```
   git checkout <target-branch>
   ```
2. Identify the commit you want to apply. You can find the commit hash by using git log.
   ```
   git log
   ```
3. Run the git cherry-pick command, followed by the commit hash.

   ```
   git cherry-pick <commit-hash>
   ```

   This will apply the changes made in the specified commit to the current branch.

4. Resolve any conflicts that may arise.
   If there are any conflicts between the changes made in the specified commit and the current branch, Git will prompt you to resolve them. You can use Git's merge tools to resolve the conflicts or edit the files manually.

5. Commit the changes.
   After resolving any conflicts, commit the changes using git commit.
   ```
   git commit -m "message"`
   ```
   That's it! The changes made in the specified commit are now applied to
   the current branch.

#### V. git stash

git stash is a Git command that allows you to save the changes you've made to your working directory in a temporary location, so you can revert back to a clean working directory without losing your changes. It is useful when you are working on a branch but you need to switch to another branch or perform some other Git operation that requires a clean working directory.

Here's how to use git stash:

1. Make changes to your working directory.
   ```
   # Make changes to your files
   ```
2. Run the git stash command.
   ```
   git stash
   ```
   This will save your changes to a temporary location and revert your working directory to the last committed state.
3. Perform the Git operation you need to do.
   ```
   # Switch to another branch
   # Perform another Git operation
   ```
4. Retrieve the changes you stashed.

   ```
   git stash pop
   ```

   This will apply the changes you stashed back to your working directory. If you have multiple stashes, you can specify the stash you want to apply with git stash apply stash@{n}, where n is the index of the stash.

5. Commit the changes.
   After retrieving your stashed changes, you can commit them using git commit.
   ```
   git commit -m "message"
   ```

That's it! git stash is a powerful command that can help you save your changes and switch between Git operations without losing your progress
