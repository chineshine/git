## some issues I met and the way to solve it

### error: src refspec master does not match any
way:   
初始化提交的时候没写提交信息  
先建立 README 文件
```
echo 'hello' > README.md
```
再提交:
```
git add README.md
git commit -m "first commit"
```
push 上去
```
git push -u origin master
```

### error: cannot stat 'file': Permission denied
在切换分支的出现这个错误:
way:
  关掉所有打开了的文件夹和编辑器,与项目有关的
  然后再 checkout 就好了

### fatal: refusing to merge unrelated histories
在代码仓库建立一个项目,由于项目会初始化有 `README.md` 文件,所以 `pull` 时报错  
way:  
```
  git pull --allow-unrelated-histories
```

### 本地处于无分支状态,进行状态追踪
```
   git branch --set-upstream-to=origin/<branch> master
```

### 本地看不到远程分支
```
  git fetch
  git branch -a
```
