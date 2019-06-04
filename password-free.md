# 不想输入用户名和密码
## 使用 ssh
```
ssh-keygen -t rsa -C “<email>”
```
生成 ssh 公钥和私钥  
<email> 为注册 github 或 gitlab 等邮箱  
上传公钥至 github 或 gitlab 等仓库网站上

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
