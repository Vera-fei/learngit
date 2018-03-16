# record my learning git.

1. git add .      
2. git commit -m "msg"
3. git push



- git status    #查看状态
- git diff xxx
- git log       #查看历史版本
- git log --graph --pretty=oneline --abbrev-commit
- git reset --hard HEAD^  #回退到上个版本
- git reflog   #查看每一次命令
- git checkout -- readme.txt #丢弃add的修改
- git reset
- git rm xxx  #从版本库中删除

工作区：文件夹
.git:   Git的版本库
	stage 暂存区


## 先有本地库 本地仓库和远程仓库关联 
- git remote add origin git@github.com:Vera-fei/learngit.git

## -u是第一次把本地master和远程master关联起来
- git push -u origin master

## 从远程克隆工程到本地
- git clone xxx


## 创建dev分支，然后切换到dev分支
- git checkout -b dev
- git branch dev
- git checkout dev

## 查看当前分支
- git branch

## master下合并dev分支
- git merge dev

## 准备合并dev分支，请注意--no-ff参数，表示禁用Fast forward
- git merge --no-ff -m "merge with no-ff" dev


## 删除dev分支
- git branch -d dev

## 强行删除
- git branch -D dev


## git add后，保存现场，可以停止手头工作，修复新到的bug
- git stash

## 查看保存的内容
- git stash list

## 恢复现场，并删除保存区
- git stash pop

## 查看远程仓库信息
- git remote
- git remote -v  #详细


## 推到远程master
- git push origin master

## 推到远程dev
- git push origin dev

## 另一个小伙伴clone master后，可在本地创建远程相同的分支
- git checkout -b dev origin/dev


## 从远程拉取最新文件，同步
- git pull

## 本地和远程分支关联
- git branch --set-upstream-to=origin/dev dev

## 给分支打标签
- git tag v1.0

## 查看所有标签
- git tag

## 给提交的id 打标签
git tag v0.9 6224937

## 查看标签内容
- git show v1.0

## 删除标签
- git tag -d v0.1

## 推送标签
- git push origin v1.0

## 一次性推送所有标签
- git push origin --tags

## 删除远程标签
- git push origin :refs/tags/v1.0