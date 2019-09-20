git操作流程:
  1. git init：新建一个git库(本地路径)
  2. git status：查看目前状态
  3. git add <文件名>：添加文件从工作区到暂存区（. 为添加全部）
  4. git commit -m “提示信息”：从暂存区提交到代码仓库（最好加上提示信息，这样方便后期维护）
  5. git log：查看提交commit的信息
  6. git remote add origin https://github.com/try-git/try_git.git : 添加远程指针（远程仓库，就是github。第需要执行6 7命令后面不需要在执行）
  7. git push -u origin master：将本地的master分支推送到远程origin主机，-u参数表示记住对应关系，下次可以直接git push推送。
  8. git pull origin master：将远程主机origin的代码取回本地，与本地的master分支合并
  
  9. git diff HEAD：查看与上一次commit的区别
  
  
 当有多人共同维护一个项目的时候，文件容易发生冲突：
  1.	git status (看一下就行，大致修改涉及的有哪些文件)
  2.  git stash (把本地代码暂存到git缓存栈里，保持分支干净，为了下一步拉取代码)
  3.  git pull origin master (拉取master的远程代码)
  4.  git stash pop (把缓存的代码释放出来，git自动进行merge)
  5.  有冲突的话解决冲突
  6.  git add . (可能会有不需要提交的文件，可以使用git reset HEAD 文件名    取消文件的提交)
  7.  git commit -m "****"
  8.  git push origin (提交到自己分支的远程)
