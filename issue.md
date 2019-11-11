# some issues I met and the way to solve it

## error: src refspec master does not match any
分析: 初始化提交的时候没写提交信息  
解决:  
先建立 README 文件: 
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

## error: cannot stat 'file': Permission denied
在切换分支的出现这个错误:
分析: 一般在 windows 系统上容易出现,主要是由于 windows 的文件权限问题
解决:
  关闭所有 与项目相关的 文件夹 编辑器
  然后再切换分支就好了,不必重启
```
  git checkout {{ branch }}
```

## fatal: refusing to merge unrelated histories
场景: 本地有文件未提交,但远程此时有同名文件,在 pull 时报错
解决:  
```
  git pull --allow-unrelated-histories
```
