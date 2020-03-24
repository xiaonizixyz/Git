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

## 6、设置用户名和邮箱

```c
git config --global user.name "[name]"
git config --global user.email "[email dress]"
```

## 7、创建新的代码库

```c
git init [repository name]
```

## 8、获取远端代码库

```c
git clone [远端代码库url]
```

## 9、添加文件至`stage`(暂存区)

```
git add [file name]  -- 将指定文件添加至stage
git add *     -- 将多个文件添加至stage(暂存区)
```

## 10、显示文件变更

```c
git diff   --显示尚未添加至stage的文件的变更
    
git difff --staged     --显示添加到stage的文件与当前最新版本之间的差异
    
git diff [first branch] [second branch]  --显示两个分支之间的差异
```

## 11、从stage中撤出指定文件

```
git reset [file]  -- 将从stage中撤出指定的文件，但可以保留文件的内容

git reset [commit] -- 可以撤销指定提交之后的所有提交，并在本地保留变更

git reset --hard [commit] -- 将丢弃所有的历史纪录，并回滚到指定的提交
```

## 12、显示需要提交的文件

```c
git status --显示所有需要提交的文件
```

## 13、删除工作目录中的文件

```
git rm [file]   --删除工作目录中的文件，并将删除动作添加至stage
```

## 14、显示当前分支的版本历史记录

```
git log  --显示当前分支的版本历史记录

git log --follow[file]  --用于显示某个文件的版本历史记录，包括文件的重命名
```

## 15、显示指定提交的元数据及内容变更

```
git show [commit]  --显示指定提交的元数据及内容变更
```

## 16、给指定提交加标签

```
git tag [commit] --给指定的提交添加标签
```

## 17、显示当前代码库中所有本地分支

```
git branch   --显示当前代码库中所有的本地分支

git branch [branch name]  --创建一个分支

git branch -d [branch name]  --删除指定的分支
```

## 18、切换分支

```
git checkout [branch name]   --切换分支

git checkout -b [branch name]  --创建一个分支，并切换到新分支上
```

## 19、合并分支

```
git merge [branch name]   --将指定分支的历史记录合并到当前分支
```

## 20、获取远程仓库变更

```
git pull [Repository Link]   --获取远程服务器上的变更，并合并到你的工作目录
```

## 21、临时保存所有修改文件

```
git stash save  --临时保存所有修改的文件

git stash pop   --恢复最近一次stash(储存)的文件

git stash list   --显示stash的所有变更

git stash drop   --丢弃最近一次stash的变更
```

