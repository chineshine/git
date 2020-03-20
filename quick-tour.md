# quick tour
新手常用命令快速上手指南

## 新手操作基本指令
- 基本设置
```
# 设置用户名和邮箱  
  git config --global user.email "you@email.com"
  git config --global user.name "Your Name"
```

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
  git add {{file-or-dir}}
```
3. 提交  
```
  git commit -m "此处填写提交时的备注信息"

   -m : 参数必需,为所提交的事物的说明信息
```

- 推送到远程仓库(如: github,gitlab 等)  
```
  git push

#  建议每次推送前,如果不确认远程仓库是否变动,先执行 git pull
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
```
# 在当前分支下
  git merge {{branch}}

# 建议学习  git rebase
```

- 覆盖本地单个文件
```
  git checkout {{file}}
```

- 强制覆盖本地所有变动
```
  git checkout -f
```
