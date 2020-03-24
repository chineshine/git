# some operation for rollback

## 覆盖本地文件
- 单个文件覆盖
```
  git checkout {{ filedir/file }}
```
- 强制覆盖本地所有
```
  git checkout -f
```

## 撤销 `git add ` 操作
```
  git reset HEAD {{ file }}
```

## 恢复 误删 分支
1. 显示所有的 commit
```
  git reflog
```
2. 恢复被删除的分支
```
  git branch {{ branch-name }} HEAD@{$NUM}
```

## 合并最近几次的 commit
1. 如: 合并最近3次的 commit
```
  git rebase -i HEAD~3
```
2. 修改打开的文件信息,将最近的一次 commit 修改为 squash
3. 保存,退出

## 修改最后一次提交的 commit 的提交信息
```
  git commit -ammend -m "提交信息"
```
