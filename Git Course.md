
# Git 教程
[toc] 
<center></center>

[本教程由云主页提供](https://ZhuYe.Cloud/) &nbsp; 


# Git 全局配置及初始化仓库
> 空白区右击，选择“Git Bash Here”。
## 1. 配置
```
git config --global user.name "200"
git config --global user.email "whgreatmap@qq.com"
```

[![License](https://img.shields.io/badge/license-GPL_V3.0-yellowgreen.svg)](https://github.com/wisp-x/lsky-pro/blob/master/LICENSE)
[![PHP](https://img.shields.io/badge/PHP->=5.6-orange.svg)](http://php.net)
[![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/wisp-x/lsky-pro.svg)](https://github.com/wisp-x/lsky-pro)

## 2. 初始化
```shell
mkdir studygit  #创建目录
cd studygit  #切换目录
git init  #初始化
ls -al  #查看目录详情
```

# 创建文件
```
echo "# -java-" >> readme.md
```
# 提交本地代码
## 1. git add 添加到缓冲区
### 提交部分
```shell
git add readme1.md readme2.md #指令可以添加一个文件，也可以添加多个文件。
```
### 提交全部
```shell
$ git add .  
```

## 2. 提交至版本库
```shell
$ git commit -m "注释内容"
```










## 3. 查看当前状态
```
$ git status
```
### 1. On branch master
> 显示当前分支是master。


### 2. Changes not staged for commit
> 说明已跟踪文件的内容发生变化,但还没有放到暂存区，要暂存这次更新，需要运行 git add 命令。
> 
> 查看具体更改了什么，使用 git diff 命令，
+号 绿色表示新增，
-号 红色表示删除，
Q 键退回到命令行输入。

## 4. 创建.gitignore文件
```
touch .gitignore

*.class  #忽略所有.class文件

!/bin/*.java  #不要忽略根目录下bin文件夹中.java文件
```

# 查看提交记录
```
$ git log #显示所有提交过的版本信息
$ git log --pretty=oneline #只显示版本号和提交时的备注信息

$ git reflog #查找到所有分支的所有操作记录，包括删除的以及reset的内容！
```
# 版本回退
```
$ git reset --hard^ 版本号
```

# 克隆线上仓库到本地
```
$ git clone https://github.com/appstack/Git.git 
```

## 拉取线上仓库
```
$ git pull
```

## 提交到线上仓库
```
$ git push
```

> 如果提示403，permission等字样表示权限不够，修改./.git/config文件。

```
[core]
	repositoryformatversion = 0
	filemode = false
	bare = false
	logallrefupdates = true
	symlinks = false
	ignorecase = true
[remote "origin"]
	url = https://github.com/appstack/Git.git
	fetch = +refs/heads/*:refs/remotes/origin/*
[branch "master"]
	remote = origin
	merge = refs/heads/master
```
改为：
```
url = https://appstack:password@github.com/appstack/Git.git #appstack:password表示账号和密码
```
















# 分支
```shell
$ git branch #查看当前分支

$ git branch branchName #创建新分支

$ git checkout branchName #切换到新分支

$ git checkout -b branchName #创建新分支并切换

$ git merge dev #合并分支，把dev分支合并到当前分支中

$ git branch -d dev #删除dev分支










```


# 解决冲突
1. 先Git pull，git会自动将冲突合并到本地readme.txt中！


# 忽略文件
> .gitignore的格式规范
> 
> a #忽略所有 .a 结尾的文件
> 
> !lib.a  #但lib.a 除外
> 
> /TODO  #仅仅忽略项目根目录下的 TODO 文件，不包括 subdir/TODO
> 
> build/  #忽略build/ 目录下的所有文件
> 
> doc/.txt  #会忽略 doc/notes.txt 但不包括 doc/server/arch.txt



```
$ touch .gitignore #创建忽略文件

$ git check-ignore #规则检查

```







注意：请不要使用记事本打开修改，修改完成后保存即可。


# 联系我

- QQ：
- Email: 
- Blog：[ZhuYe.Cloud](https://ZhuYe.Cloud/)

# 鸣谢



开源许可
=

[GPL 3.0](https://opensource.org/licenses/GPL-3.0)

Copyright (c) 2020 [ZhuYe.Cloud](https://ZhuYe.Cloud/).
 
