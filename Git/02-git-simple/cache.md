---
title: cache
date: 2022-04-04 12:0
---
- 取消文件跟踪

> 如果文件被 commit，那么就是 commit
> 如果文件被 add，则可以取出，再添加到`.gitignore`生效

```bash
git rm -r --cached
vim .gitignore
git add .
```
