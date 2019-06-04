# git command
## 查看远程仓库地址
```
  git remote -v
```

## 项目太大,上传不了
```
# 将上传缓存设置大一些
  git config http.postBuffer 524288000
```

## push 到指定远程的指定分支
```
  git push --set-upstream {{remote}} {{branch}}
```

## 建立仓库后初始化提交
```
git init
git add .
git commit -m "init"
git remote add origin {{remote-address}}
git push -u origin master
```

## 删除不想被托管,但已托管的文件
```
# 此方式不会删除本地文件
   git rm -r --cache {{file}}
```

## 合并某个特定 commit 并提交远程给远程合并
1) 在自己的分支查看并查找想合并的 `commit-id`
```
  git log
```
2) 从远程拉个分支下来
```
  git checkout -b {{customer-branch-name}} origin/{{remote-branch}}
```
3) 在当前分支合并 commit
```
  git cherry-pick {{commit-id}}
```
4) 将分支推送到远程
```
  git push {{remote}} {{branch}}
```
5) 在远程操作合并,之后删除远程分支,本地分支
```
  git push origin --delete {{branch}}
  git branch -d {{branch}}
```

## 查看单个文件的提交历史
```
  git log --pretty=oneline {{file_path}}
  git log {{commit_id}}
```
