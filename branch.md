## git 分支 相关操作
#### 查看所有分支
```
git branch -a   
```
#### 查看本地分支
```
git branch     
```
#### 切换分支
也可用于在本地新建一个分支
```
git checkout -b <branchname> origin/<branchname>
```
#### 切回 master
```
git checkout master   
```
### 创建远程分支
#### 创建分支
```
git branch <分支名称>
```   
#### 上传分支
```
git push origin <分支名称(同上)>  
```
#### 删除本地分支
```
git branch -d <本地分支名称>
```
#### 强制删除本地分支
```
git branch -D <本地分支名称>
```
#### 删除远程仓库的分支
```
git push origin --delete <远程仓库的分支名称>
```
#### 删除没有与远程分支相对应的本地分支
```
git remote prune origin
或 :  
git fetch -p
```
#### 给本地分支重命名
```
git branch -m <本地分支名称> <新名称>
@Note :
  重命名远程分支=>删除远程,重命名本地,推送本地分支至远程
```
