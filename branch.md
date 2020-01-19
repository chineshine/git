# 分支相关内容
## remote
remote 指的是远程仓库
### 查看
```
  git remote -v
```
### 添加远程仓库地址
```
  git remote add {{name}} {{repo-address}}
```
### 删除远程仓库
```
  git remote remove {{name}}
```
### 重命名 remote 名称
```
  git remote rename {{old-name}} {{new-name}}
```

## branch

### 查看本地分支
```
  git branch     
```
### 查看所有分支 包括远程
```
  git branch -a   
```
### 从远程拉个分支到本地
```
  git checkout -b {{customer-branch}} origin/{{remote-branch}}
```
### 切换分支
```
  git checkout {{branch}}   
```
### 创建分支
```
  git branch {{branch-name}}
```   
### 上传分支
```
  git push --set-upstream {{remote}} {{branch}}

#  创建远程分支可在本地创建分支后上传到远程  
#  此处也可用于上传本地分支到指定远程的指定分支
```
### 删除本地分支
```
  git branch -d {{local-branch}}
```
### 强制删除本地分支
```
  git branch -D {{local-branch}}
```
### 删除远程仓库的分支
```
  git push {{remote}} --delete {{remote-branch}}
```
### 远程分支被删除,本地仍能看到远程的分支,清除远程已经不存在分支
```
  git remote prune {{remote}}  # 方式一

  git fetch -p                 # 方式二
```
### 给本地分支重命名
```
  git branch -m {{old-branch}} {{new-branch}}

#  重命名远程分支 => 删除远程,重命名本地,推送本地分支至远程
```
### 本地分支无远程追踪,让其与远程分支进行追踪关联
```
  git branch --set-upstream-to={{remote}}/{{remote-branch}} {{local-branch}}
```
### 本地查看分支却发现远程有些分支查看不到
```
  git fetch && git branch -a
```
### 创建一个空白分支
1. 创建一个孤儿分支, `--orphan` 会在创建分支时不包含原分支的所有提交信息
```
  git checkout --orphan {{ new-branch }}
```
2. 删除新建分支下所有内容
```
  git rm -rf .
```
3. 提交并上传到远程  
参考上面的命令
