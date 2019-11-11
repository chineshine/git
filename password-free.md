# 不想输入用户名和密码
## 使用 ssh
生成 ssh 公钥和私钥  
```
windows:
  ssh-keygen -t rsa -C "{{email}}"
linux:
  ssh-keygen
```
上传公钥至 github 或 gitlab 等仓库网站上  
- {{email}} 邮箱地址  

## 设置记住密码缓存，默认 15分钟
```
  git config –global credential.helper cache
```
## 或自定义时间，如 1个小时
```
  git config credential.helper ‘cache –timeout=3600’
```
## 长期存储密码
```
  git config –global credential.helper store
```
