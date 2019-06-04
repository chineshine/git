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
  git checkout -b {{customer-branch-name}} origin/{{remote-branch-name}}
```
#### 切换分支
```
  git checkout {{branch-name}}   
```
### 创建远程分支
#### 创建分支
```
  git branch {{branch-name}}
```   
#### 上传分支
```
  git push origin {{branch-name}}
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
  git push origin --delete {{remote-branch}}
```
#### 删除没有与远程分支相对应的本地分支
```
  git remote prune origin
或 :  
  git fetch -p
```
#### 给本地分支重命名
```
  git branch -m {{old-branch}} {{new-branch}}
@Note :
  重命名远程分支=>删除远程,重命名本地,推送本地分支至远程
```
