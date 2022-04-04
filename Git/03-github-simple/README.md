---
title: README
date: 2022-04-03 20:49
---
## 添加远程仓库

`git remote add <remote_name> <url_address>`

> eg. `git remote add origin git@github.com:username/repository.git`
## delete remote repository
- `git remote remove <repository_name>`
## 推送至远程仓库

`git push -u origin master`
> -u参数可以在推送的同时，将origin仓库的master分支设置为本地仓库当前分支的upstream（上游）。添加了这个参数，将来运行git pull命令从远程仓库获取内容时，本地仓库的这个分支就可以直接从origin的master分支获取内容
> 如果`origin master`不存在的话，则会创建

git push origin HEAD:<remote_branch>
> 将当前的 head 推送到 remote 到 `<branch>`上面
> git push -u origin <remote_branch>

## 从远程仓库获取

### clone

- `git clone <url_address>`
- `git clone -b <b_name> <url>`
> clone the specified branch

> 执行git clone命令后我们会默认处于master分支下，同时系统会自动将origin设置成该远程仓库的标识符。

- pull

`git pull origin feature-D`

> 将远程的`feature-D`拉取到本分支
> 
> In its default mode, git pull is shorthand for git fetch followed by git merge FETCH_HEAD.

- `git pull <url> <branch_name>`
## exercise

- 添加上游仓库

- add remote
`git remote add upstream <url>`
- fetch
`git fetch upstream`
- merge
`git merge upstream/master`


