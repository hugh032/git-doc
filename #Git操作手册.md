# Using Git

## 配置工具

~~~shell
#对所有本地仓库的用户信息进行配置
#######################################
$ git config --global user.name "[name]"
#对你的commit操作设置关联的用户名

$ git config --global user.email "[email address]"
#对你的commit操作设置关联的邮箱地址

$ git config --global color.ui auto
#启用有帮助的彩色命令行输出
~~~

## 创建仓库

~~~shell
#当着手于一个新的仓库时，你只需创建一次。要么在本地创建，然后推送到 GitHub；要么通过 clone 一个现有仓库。
#######################################
$ git init

#在使用过 git init 命令后，使用以下命令将本地仓库与一个 GitHub 上的空仓库连接起来：

$ git remote add origin [url]

#将现有目录转换为一个 Git 仓库

$ git clone [url]

#Clone（下载）一个已存在于 GitHub 上的仓库，包括所有的文件、分支和提交(commits)
~~~

## .gitignore 文件

```shell
有时一些文件最好不要用 Git 跟踪。这通常在名为 .gitignore 的特殊文件中完成。你可以在 github.com/github/gitignore 找到有用的 .gitignore 文件模板。
```

## 分支

```shell
#分支是使用 Git 工作的一个重要部分。你做的任何提交都会发生在当前“checked out”到的分支上。使用 git status 查看那是哪个分支。
#######################################
$ git branch [branch-name]

#创建一个新分支

$ git checkout [branch-name]

#切换到指定分支并更新工作目录(working directory)

$ git merge [branch]

#将指定分支的历史合并到当前分支。这通常在拉取请求(PR)中完成，但也是一个重要的 Git 操作。

$ git branch -d [branch-name]

#删除指定分支
```

## 同步更改

```shell
#将你本地仓库与 GitHub.com 上的远端仓库同步
#######################################
$ git fetch

#下载远端跟踪分支的所有历史

$ git merge

#将远端跟踪分支合并到当前本地分支

$ git push

#将所有本地分支提交上传到 GitHub

$ git pull

#使用来自 GitHub 的对应远端分支的所有新提交更新你当前的本地工作分支。git pull 是 git fetch 和 git merge 的结合
```

