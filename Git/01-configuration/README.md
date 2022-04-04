---
title: README
date: 2022-04-03 00:35
---
# git configuration

## git
- name-and-mail

```bash
​​git config --global user.name "Firstname Lastname" git config --global user.email "your_email@example.com"​​
```

> 会在“～/.gitconfig”中以如下形式输出设置文件。

```txt
​​[user]   name = Firstname Lastname   email = your_email@example.com​​
```

- better print

```bash
git config --global color.ui auto​​
```

> “～/.gitconfig”中会增加下面一行

```txt
​​[color]   ui = auto​​
```

## github

### ssh

- generate key
```bash
ssh-keygen -t rsa -C "your_email@example.com"
```

> 最好直接`enter`，设置密码会导致提交到时候总要密码
> 
> id_rsa文件是私有密钥，id_rsa.pub是公开密钥。

- test

```bash
ssh -T git@github.com
```




