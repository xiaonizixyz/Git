## 1、连接远程仓库

- 添加远程仓库，重命名为`origin`

  ```c
  # git remote add origin https://github.com/xxxx
  ```

## 2、提交本地仓库

```c
# git add . #添加所有文件，.表示所有，如若只提交单个文件写文件名即可
```

## 3、提交远程仓库

提交到远程仓库的`master`分支，`origin`是添加远程仓库时的重命名

```c
# git push -u origin master  #把本地的文件提交到远程仓库
```

## 4、删除远程仓库文件

```
# git rm -r --cached 要删除的文件  # cached不会把本地的文件也删除

# git commit -m "提交删除文件的说明"

# git push -u origin master       # 更新远程仓库
```

## 5、删除远程仓库连接

```c
# git remote remove origin
```

