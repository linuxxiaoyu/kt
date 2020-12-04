# git cmd

## add

git add [file, path ...] 添加文件

## branch

git branch -d branch 删除branch分支

## cat-file

git cat-file -t 查看git文件类型

git cat-file -p

## checkout

git checkout -b newBranch 在当前分支基础上创建分支newBranch

## clone

git clone 克隆

## commit

git commit -m 'msg' 提交

## config

git config [--list] [--global, --local, --system] 获取git配置信息

git config user.name user 设置git用户名为user

git config user.email email 设置git邮箱为email

## diff

git diff 比较

## fetch

git fetch 从远端获取代码库

## init

git init [repository] 初始化仓库

## log

git log 查看git提交记录

## mv

git mv 移动文件

## pull

git pull 从远端下载代码

## push

git push 上传到远端

## remote

git remote -v  查看远端

git remote add name url  添加远端

git remote remove name 删除远端

## rebase

git rebase -i  变基

git rebase --contine 继续处理变基

pick reword squash

## reset

git reset HEAD 重置

## rm

git rm   删除文件

## stash

git stash   暂存

git stash list 显示暂存数据

git stash pop 从暂存中弹出

## status

git status 显示当前状态

## switch

git switch branch 切换到branch分支
