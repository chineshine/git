#### 查看远程仓库地址
```
  git remote -v
```

#### 项目太大,上传不了
```
# 将上传缓存设置大一些
  git config http.postBuffer 524288000
```

#### 建立仓库后初始化提交
```
git init
git add .
git commit -m "init"
git remote add origin <remote-address>
git push -u origin master
```

#### 删除不下被托管,但已托管的文件
```
# 此方式不会删除本地文件
   git rm -r --cache file
```
