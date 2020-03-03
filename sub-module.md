# sub-module
## remove sub-module
1. 删除子模块目录及其目录下所有东西
```
  rm -rf {{ sub-module}}
```
2. 删除 `.gitmodules` 下所要删除的子模块的内容
```
  vi .gitmodules
```
3. 删除 `.git/config` 文件内所有与子模块相关的内容
```
  vi .git/config
```
4. 删除 `.git/module` 下与子模块有关的内容
```
  rm .git/module/{{sub-module}}
```
5. 缓存清理
```
  git rm --cached {{ sub-module }}
```
6. 上传
```
  git push
```
