---
title: branch
date: 2022-04-03 18:10
---
# 分支的操作

## show the branch

- `git branch`
> git branch命令可以将分支名列表显示，同时可以确认当前所在分支
- `git branch -vv`
> the connection between local and remote
## create branch 

- `git checkout -b <branch_name>`

> 以当前的分支为基础创建新的分支，并且切换
> equals below

```bash
git branch <branch_name>
git checkout <branch_name>
```

- `git checkout -b <b> <remote_repository>/<remote_b>`
> 根据远程仓库的分支来新建分支

- `git branch <b_name> <hash_id>`

## delete

- `git branch -d <b_name>`
> delete local branch which has been merged
- `git branch -D <b_name>`
> delete local branch although it may not be merged yet
- `git push origin --delete <b_name>`
> delete remote branch



## switch branch

- `git checkout <branch_name>`
- `git checkout -`
> 用“-”（连字符）代替分支名，就可以切换至上一个分支

## merge

`git merge --no-ff <branch_name>`

> 首先切换到master分支
> 
> 然后 execute the command to合并feature-A分支
> 
> 为了在历史记录中明确记录下本次分支合并，我们需要创建合并提交。因此，在合并时加上--no-ff参数。
> 
> > --no-ff 是禁止快进式合并（fast-forward）,不加该参数，Git 合并两个分支时，如果顺着master走下去可以到达feature-A，就会简单的把HEAD指针移动到feature-A上，如果删除分支的话会导致丢失分支信息，这个过程没有创建commit。通俗的举例：10个人按照票号排队（master），现在突然出现第11个人（特性分支feature-A），不去拿票号就直接排在队伍后面（不加参数），会扰乱队伍的正常顺序（导致master提交历史混乱），加了参数，相当于他去拿票号（创建了一份commit）。
> [git merge和git merge --no-ff的区别](https://www.jianshu.com/p/418323ed2b03)


### conflict

```txt
<<<<<<< HEAD   current_branch content =======   merged_branch content >>>>>>> merged_branch_name
```
> =======以上的部分是当前HEAD的内容，以下的部分是要合并的被合并分支中的内容。
> 修改选择接受哪一部分，进行提交即可

## 修改名字

`git branch -m <oldName> <newName>`

## track

git branch --set-upstream-to=origin/<remote_branch> <local_branch>