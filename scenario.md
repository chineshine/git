# git command -- some base use

## 全局初始化用户和邮箱
```
  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"
```

## 项目太大,上传不了
设置上传缓存  
```
  git config http.postBuffer 524288000
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
如 maven 的 target, 不想上传到仓库但已经上传上去了
```
   git rm -r --cache {{file/dir}}
@NOTE
  该操作不会删除本地文件
```

## 合并某个特定 commit 并提交到远程合并
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

## 新手操作基本指令
- 克隆仓库
```
  git clone {{git-repository-url}}
```
- 拉取
```
  git pull
```
- 提交
1. 先查看本地修改
```
  git status
```
2. add
```
  git add {{file/dir}}
```
3. 提交
```
  git commit -m "此处填写要提交的信息"
```
- 推送到远程
建议每次推送前,如果不确认远程仓库是否变动,先执行 `git pull`
```
  git push
```
- 切换分支
```
  git checkout {{branch}}
```
- 创建分支
```
  git branch {{branch-name}}
```
- 合并分支内容  
在当前分支下
```
  git merge {{branch}}
```
建议学习 `git rebase`
- 覆盖本地单个文件
```
  git checkout {{file}}
```
- 强制覆盖本地所有变动
```
  git checkout -f
```
