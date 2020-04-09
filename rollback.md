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
2. 修改打开的文件信息,将要合并的 commit 修改为 squash
3. 保存,退出

## 修改最后一次提交的 commit 的提交信息
```
  git commit -ammend -m "提交信息"
```

## 撤销 push 到远程的 commit
1. 查看提交日志,查找 commit
```
  git log    # 退出日志按 q
```
2. 回滚到指定 commit
```
  git reset --hard {{commit-id}}  # 1
  git reset --soft {{commit-id}}  # 2
#1 回滚到指定 commit,该 commit 之后的修改消失
#2 回滚到指定 commit,该 commit 之后的修改将留在本地,并可重新 commit
```
