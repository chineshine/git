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
