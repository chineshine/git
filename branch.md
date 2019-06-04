# git branch

## git 分支相关操作

# 基本操作
#### 查看所有分支 包括远程
```
  git branch -a   
```
#### 查看本地分支
```
  git branch     
```
#### 从远程拉个分支到本地
```
  git checkout -b {{customer-branch}} origin/{{remote-branch}}
```
#### 切换分支
```
  git checkout {{branch}}   
```
#### 创建分支
```
  git branch {{branch-name}}
```   
#### 上传分支
```
  git push --set-upstream {{remote}} {{branch}}
@NOTE
  创建远程分支可在本地创建分支后上传到远程
  此处也可用于上传分支到指定远程的指定分支
```
#### 删除本地分支
```
  git branch -d {{local-branch}}
```
#### 强制删除本地分支
```
  git branch -D {{local-branch}}
```
#### 删除远程仓库的分支
```
  git push {{remote}} --delete {{remote-branch}}
```
#### 删除没有与远程分支相对应的本地分支
```
  git remote prune {{remote}}
或 :  
  git fetch -p
```
#### 给本地分支重命名
```
  git branch -m {{old-branch}} {{new-branch}}
@NOTE
  重命名远程分支=>删除远程,重命名本地,推送本地分支至远程
```
#### 本地分支无远程最终,让其与远程分支进行追踪关联
```
  git branch --set-upstream-to={{remote}}/{{remote-branch}} {{local-branch}}
```
#### 本地查看分支却发现远程有些分支查看不到
```
  git fetch && git branch -a
```
