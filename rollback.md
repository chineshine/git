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
