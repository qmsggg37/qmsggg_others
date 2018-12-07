## 删除本地git的远程分支和远程删除git服务器的分支
在项目中使用git管理代码后，有些时候会创建很多不同名称的分支，以此区分各个分支代码功能。 而随着代码的合并，以前的分支就可能不再需要保存了，所以就要对没有用的分支进行删除，包括紧急回滚时从中抽取某一个版本记录所创建的临时分支。 这时候就可以使用下面的命令：

- 列出本地分支：
  ```
  git branch
  ```
- 删除本地分支：
  ```
  git branch -D BranchName
  ```
  其中`-D`也可以是`--delete`，如：
  ```
  git branch --delete BranchName
  ```
- 删除本地的远程分支：
  ```
  git branch -r -D origin/BranchName
  ```
- 远程删除git服务器上的分支：
  ```
  git push origin -d BranchName
  ```
  其中`-d`也可以是`--delete`，如：
  ```
  git push origin --delete BranchName
  ```
*注意：git命令区分大小写，例如-D和-d在不同的地方虽然都是删除的意思，并且它们的完整写法都是--delete，但简易写法用错大小写会执行失败。*
