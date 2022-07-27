---
title: git版本控制工具
categories: 
	- 阶段三：JavaSE
	- git版本控制工具
tags: ["git","github","gitee"]
---

```
作者: 左岸小镇_梦归
企鹅: 2427419219
邮箱: publicfinal@163.com
博客: https://publicfinal.top/
备用: https://publicfinal.gitee.io/
```

# Git常见命令速查表

## git客户端的安装和配置

```apl
产看本地配置信息
git config --global -l
git config --global --list
用户名和邮箱设置
//仅对当前仓库有效
git config --local user.name "Your Name"
git config --local user.email "email@example.com"
//对当前用户的所有仓库有效
git config --global user.name "Your Name"
git config --global user.email "email@example.com"
```



## 创建版本库

```apl
git clone <url>  #克隆远程版本库
git init   # 初始化本地版本库
```

## 修改和提交

```apl
git status  #查看状态
git diff    #查看变更内容
git add .   #跟踪所有改动过的文件（将改动过的文件提交到暂存区）
git mv <old> <new> #文件改名
git rm <file> #删除文件  git commit -m "" 完成删除
	git checkout --abc.txt #错误删除文件恢复（其实是用版本库里的版本替换工作区的版本）
git rm --cached <file> # 停止跟踪文件但不删除
git commit -m "commit message" #提交所有更新过的文件
git commit --amend		#修改最后一次提交
```

## 查看提交历史

```apl
git log  #查看提交历史
git log --pretty=oneline  #精简信息查询:
git log -p  <file>  #查看指定文件的提交历史
git blame <file>    #以列表方式查看指定文件的提交历史
```

## 撤销

```apl
git reset --hard HEAD  #撤销工作目录中所有未提交文件的修改内容
    回退到上一个版本 git reset --hard HEAD^ 
    回退到上上一个版本 git reset --hard HEAD^^ 
    回退到上100个版本 git reset --hard HEAD~100
git checkout HEAD <file> #取消对文件内容的修改（让这个文件回到最近一次git commit或git add时的状态）
git revert <commmit> #撤销指定的提交
git reset --hard a1faca5  #切换到固定版本号
git reflog  #查看历史操作 （回退后第二天后悔，查询不到版本号可使用）
```

## 分支(branch)与标签(tag)

```apl
git branch     #显示所有本地分支
git checkout <branch/tag>   #切换到指定分支或标签
git branch <new-branch>		#创建新的分支
git branch -d <branch>    #删除本地分支
git tag					#列出所有本地标签
git tag <tagname>       #基于最新提交创建标签
git tag -d <tagname>    #删除标签
```

## 合并和衍合

```apl
git merge <branch>  #合并指定分支到当前分支
git rebase <branch> #衍合指定分支到当前分支
```

## 远程操作

```apl
git remote add <remote> <url>  #添加远程版本库
git remote -v #查看远程版本库信息
git remote show  <remote> #查看指定远程版本 库信息
git fetch <remote>  #从远程库获取代码
git pull <remote> <branch>  #下载代码及快速合并
git push <remote>  <branch> #上传代码及快速合并
git push <remote> :<branch/tag-name> #删除远程分支或标签
git push --tags  #上传所有标签
```

## Git的远程仓库

```apl
ssh-keygen -t rsa -C "你的邮箱地址"          #生成密钥  （C:\Users\Administrator\.ssh 目录下，里面有公匙和私匙）
```



