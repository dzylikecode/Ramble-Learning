---
title: ignore
date: 2022-04-06 18:17
---
- 从未提交过的文件可以用.gitignore
> 该文件只能作用于未跟踪的文件（Untracked Files），也就是那些从来没有被 git 记录过的文件

- 已经推送（push）过的文件，想从git远程库中删除

> - `git rm --cached <file>`
> - edit `.gitignore`

- 已经推送（push）过的文件，想在以后的提交时忽略此文件
> - `git update-index --assume-unchanged <file>`
> - 枚举文件
> > `git ls-files | tr '\n' ' '`
