---
author: hxl
comments: true
date: 2015-08-09 16:31:37+00:00
layout: post
slug: githug-playing
title: Githug闯关记
tagline: githug-playing
wordpress_id: 957
categories:
- 技术之路
tags:
- git
- 版本控制
---

黄历上说今天不宜写代码（其实是想偷懒。。。），在网上闲逛，发现<a href="https://github.com/Gazler/githug" target="_blank">Githug</a>这个游戏。  
官方的介绍是Githug is designed to give you a practical way of learning git. It has a series of levels, each requiring you to use git commands to arrive at a correct answer.简单的说，就是一款帮助你学习使用Git的游戏。  
废话少说，按提示创建好git_hug文件夹，开始游戏！  

### 第一关，初始化一个git库
`A new directory, ' git_hug ', has been created; initialize an empty repository in it.`  
这个简单，`git init`，搞定。  

### 第二关，设置名字和email
`Set up your git name and email, this is important so that your commits can be identified.`  
我去。。忘了，使用`git help`命令也没有看到相关的命令，只好看看git的官方指南，得知一个用`git config`命令。  
于是，git help config，查看帮助后尝试`git config name Xianglong He`。。诶？报错！再次查看帮助，发现少了`user.`  
`git config user.name Xianglong He`  
`git config user.email qwgg9654@gmail.com`  
再次运行githug，要求输入名字和邮箱，输入后，提示不正确。百思不得其解，遂查看git_hug的.git目录下的config文件，发现设置的名字只有Xianglong，He不见了。。重新做githug尝试，成功。  
然后尝试重新设置名字，发现需要加引号，git config user.name "Xianglong He"  

### 第三关，添加文件到git版本控制中  
`There is a file in your folder called 'README', you should add it to your staging area`  
这个简单，git add *  

### 第四关，提交更改
`The 'README' file has been added to your staging area, now commit it.`  
这个也简单，`git commit`  
然后在弹出的txt文件中根据提示添加提交日志。  

### 第五关，clone一个repo
`Clone the repository at https://github.com/Gazler/cloneme.`  
这个也简单，`git clone https://github.com/Gazler/cloneme`  

### 第六关，clone一个repo到一个目录  
`Clone the repository at https://github.com/Gazler/cloneme to 'my_cloned_repo'.`  
这个不会，看看帮助，`git help clone`  
然后发现我想复杂了，`git clone https://github.com/Gazler/cloneme my_cloned_repo`  

### 第七关，忽略一个扩展名的文件  
`The text editor 'vim' creates files ending in '.swp' (swap files) for all files that are currently open.  We don't want them creeping into the repository.  Make this repository ignore '.swp' files.`  
我知道可以直接编辑.gitignore文件来实现这个，但是觉得这个题不会是让我怎么做的，尝试`git help`，没有发现什么；尝试`git ignore`，提示没有这个命令。于是，查看文档，发现我想多了，的确要编辑`.gitignore`，没有什么特殊的命令。  
尝试向该文件添加一行`.swp`，但githug提示回答错误，添加`*.swp`，正确。  

### 第八关，忽略一个扩展名，并添加一个例外
`Notice a few files with the '.a' extension.  We want git to ignore all but the 'lib.a' file.`  
不会，查看文档后得知，向`.gitignore`添加两行`*.a`和`!lib.a`。  

### 第九关，查看哪个文件没有列入版本控制
`There are some files in this repository, one of the files is untracked, which file is it?`  
不废话，`git status`（我老是忘记最后的s）  
把`Untracked files:`的文件名复制，在运行githug是输入即可  

### 第十关，查看有多少等待提交的文件
`There are some files in this repository, how many of the files will be committed?`  
由于我用的git shell直接在目录后显示了目录的变动信息，使用自己把新增、修改、删除的文件相加，输入即可。  
`git status`也有相关信息。  

### 第十一关，从版本库中移除一个文件
`A file has been removed from the working tree, however the file was not removed from the repository.  Find out what this file was and remove it.`   
先`git status`查看到`deleteme.rb`这个文件已经被移除。  
尝试`git add *`，不对。  
`git help`和，得知应该`git rm deleteme.rb`  

### 第十二关，从暂存区移除一个文件
`A file has accidentally been added to your staging area, find out which file and remove it from the staging area.  *NOTE* Do not remove the file from the file system, only from git.`  
首先还是`git status`，看到文件名   
然后查看帮助，`git help rm`  
然后尝试`git rm deleteme.rb`，不对，遂尝试`git rm deleteme.rb --cached`，成功  

### 第十三关，暂存工作区
`You've made some changes and want to work on them later. You should save them, but don't commit them.`  
然而完全不记得这个命令，查看文档得知，`git stash`  

### 第十四关，重命名文件
`We have a file called 'oldfile.txt'. We want to rename it to `newfile.txt` and stage this change.`  
`git mv oldfile.txt newfile.txt`  

### 第十五关，移动文件
`You added some files to your repository, but now realize that your project needs to be restructured.  Make a new folder named 'src' and using Git move all of the .html files into this folder.`  
这个题我知道应该是用`git mv`，然而尝试`git mv *.html ./src/`失败，尝试`git mv index.html ./src`，直接把`index.html`重命名为了`sec`。。。然后使用`git reset`撤销失败，之后`githug reset`，重玩本关。  
这次不打算偷懒，直接一个个来。  
`git mv index.html ./src/index.html`  
但报错，查看文档后发现需要先建立src文件夹，建立和重试成功，剩下两个文件，一样的操作。
  
### 第十六关，查询最近的提交hash
`You will be asked for the hash of most recent commit.  You will need to investigate the logs of the repository for this.`  
直接`git log`，查看到hash。  

### 第十七关，添加一个tag  
`We have a git repo and we want to tag the current commit with 'new_tag'.`  
`git tag new_tag`，完成。  

### 第十八关，提交tag到服务器  
`There are tags in the repository that aren't pushed into remote repository. Push them now.`  
`git push`，完成  

### 第十九关，向之前的提交添加一个文件
`The 'README' file has been committed, but it looks like the file 'forgotten_file.rb' was missing from the commit.  Add the file and amend your previous commit to include it.`  
查看文档后，得知，先`git add`，再`git commit --amend`。  

### 第二十关，以未来的日期提交
`Commit your changes with the future date (e.g. tomorrow).`  
看到这个题目，我很想直接该系统时间。。然而忍住了，去看git commit的文档。  
`git commit --date=2016-01-01T00:00:00`  

### 第二十一关，从暂存区移除一个文件
`There are two files to be committed.  The goal was to add each file as a separate commit, however both were added by accident.  Unstage the file 'to_commit_second.rb' using the reset command (don't commit anything).`  
开始我理解错了，以为是要从已经提交的东西中去除一个文件，实际上是要从暂存区去除，这样就简单了（`git status`里也有提示）  
`git reset HEAD to_commit_second.rb`  

### 第二十二关，撤销最后的提交
`You committed too soon. Now you want to undo the last commit, while keeping the index.`  
查看`git reset`的文档，`git reset --soft HEAD^~`  

### 第二十三关，checkout一个文件
`A file has been modified, but you don't want to keep the modification.  Checkout the `config.rb` file from the last commit.`  
直接`git checkout config.rb`  

### 第二十四关，查询当前的远端名
`This project has a remote repository.  Identify it.`  
直接`git remote`。  

### 第二十五关，查询远端的url
`The remote repositories have a url associated to them.  Please enter the url of remote_location.`  
直接`git remote show remote_location`  
卧槽，直接粘贴到githug不对，尝试去掉末尾的斜杠，对了。坑爹啊！提交了个issus。  

### 第二十六关，从远端pull
`You need to pull changes from your origin repository.`  
尝试了`git pull`，不对，根据提示使用`git pull origin master`  

### 第二十七关，添加一个远端
`Add a remote repository called 'origin' with the url https://github.com/githug/githug`  
直接`git remote add origin https://github.com/githug/githug`  

### 第二十八关，将本地分支与远程分支合并
`Your local master branch has diverged from the remote origin/master branch. Rebase your commit onto origin/master and push it to remote.`  
尝试了好久，没成功  
`git pull origin master`  
`git push origin master`  
这样不行，然后根据hint，看文档，又尝试了一会儿  
`hint：Take a look at 'git fetch', 'git pull', and 'git push'.`  
卧槽。。坑啊，[在网上看到的攻略](http://fancyoung.com/blog/githug-cheat-sheet/)完全不是这样啊。  
`git rebase origin/master`  
`git push`  

### 第二十九关，查看上一次被修改的行号
`There have been modifications to the 'app.rb' file since your last commit.  Find out which line has changed.`  
`git diff`查看变化，发现提示23行，试着输入，不对。然后因为显示的23下面4行是被修改的，尝试27，不对。  
遂查看源文件。。竟然是26。。。。  

### 第三十关，找出向文件添加敏感信息的人
`Someone has put a password inside the file `config.rb` find out who it was.`  
本想使用`git log`，看到日志里有个`add password`，以为是他。。结果不是。。  
查看hint，发现使用`git blame`可以查看每一行的作者，成功。  

### 第三十一关，建立分支
`You want to work on a piece of code that has the potential to break things, create the branch test_code.`  
直接`git branch test_code`  

### 第三十二关，建立并切换分支
`Create and switch to a new branch called my_branch.  You will need to create a branch like you did in the previous level.`  
直接`git branch my_branch`  
`git checkout my_branch`  

### 第三十三关，切换到一个tag
`You need to fix a bug in the version 1.2 of your app. Checkout the tag 'v1.2'.`  
直接`git checkout v1.2`  

### 第三十四关，在有相同名字分支的情况下切换到标签  
`You need to fix a bug in the version 1.2 of your app. Checkout the tag 'v1.2' (Note: There is also a branch named 'v1.2').`  
查看hint得知`git checkout tags/v1.2`  

### 第三十五关，在最后的一次提交之前建立分支
`You forgot to branch at the previous commit and made a commit on top of it. Create branch test_branch at the commit before the last.`  
先`git log`找到提交的hash  
开始尝试使用`start-point`，然而并不对  
按攻略，`git branch test_branch -v 07f5e43a04`  

### 第三十六关，删除一个分支  
`You have created too many branches for your project. There is an old branch in your repo called 'delete_me', you should delete it.`  
直接`git branch -d delete_me`  

### 第三十七关，push一个分支 
`You've made some changes to a local branch and want to share it, but aren't yetready to merge it with the 'master' branch.  Push only 'test_branch' to the remote repository`  
直接 `git push origin test_branch`  

### 第三十八关，合并分支
`We have a file in the branch 'feature'; Let's merge it to the master branch.`  
直接`git merge feature`  

### 第三十九关，获取远端分支的变动
`Looks like a new branch was pushed into our remote repository. Get the changes without merging them with the local repository`  
开始以为是要查看远端分支建立的分支的名字，结果不是这样，按hint，`git fetch`。  

### 第四十关，将一个分支rebase到master
`We are using a git rebase workflow and the feature branch is ready to go into master. Let's rebase the feature branch onto our master branch.`  
简直卧槽。我尝试过这些命令  
`git rebase`  
`git rebase -i`  
`git rebase feature`  
`git rebase feature -i`  
`git rebase master`  
都不对，然后上网找攻略，没有找到，hint里面也只是说要`git rebase`。  
突发奇想，先`git checkout feature`，再试试  
`git rebase master`，成功了。  

### 第四十一关，repack
`Optimise how your repository is packaged ensuring that redundant packs are removed.`  
完全没看懂，看hint，让我`git repack`，运行，不对。  
看了google翻译后，发现要把多余的包删除，于是`git repack -d`  

### 第四十二关，从一个分支中合并一个文件  
`Your new feature isn't worth the time and you're going to delete it. But it has one commit that fills in 'README' file, and you want this commit to be on the master as well.`  
首先直接尝试`merge`，发现有几个文件，但只需要一个，不对。  
切换到`new-feature`分支，`git blame README.md`  
找到相应提交的hash，切换回master  
本来想用`git checkout`，但是尝试失败，hint说要用`cherry-pick`  
`git cherry-pick ca32a6da`  

### 第四十三关，查找
`Your project's deadline approaches, you should evaluate how many TODOs are left in your code`  
完全不会，查看hint，`git grep TODO`  

### 第四十四关，修改错误的提交信息
`Correct the typo in the message of your first (non-root) commit.`  
不会，看攻略，`git rebase -i HEAD~2`  
然后根据提示，把要修改的行前面作reword标记，并修改  

### 第四十五关，合并提交
`You have committed several times but would like all those changes to be one commit.`  
根据hint，尝试`git log`获取第一次提交的hash，在`git rabse 05269a64 -i`，但是不对  
在看了下攻略，再参考rebase时的提示，发现合并提交需要将相应的提交前面作squash标记，成功  

### 第四十六关，合并一个分支上，仅作为一次提交
`Merge all commits from the long-feature-branch as a single commit.`  
我是先切换到那个分支，rebase，然后merge，然后再在主分支上merge  
而攻略提供了简单的办法  
`git merge --squash long-feature-branch`  
`git commit -a -m 'merge branch long-feature-branch'`  

### 第四十七关，调整两次提交的顺序
`You have committed several times but in the wrong order. Please reorder your commits.`  
`rebase -i`，文件中调整顺序。  

### 第四十八关，寻找BUG
`A bug was introduced somewhere along the way.  You know that running 'ruby prog.rb 5' should output 15.  You can also run 'make test'.  What are the first 7 chars of the hash of the commit that introduced the bug.`
这关完全看不懂，之后来看吧。  

## 后面还有几关，完全不会，等之后学了再搞搞吧。

<a href="http://creativecommons.org/licenses/by-nc-sa/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" alt="知识共享许可协议" /></a>  
Githug闯关记 由 <a href="https://tec.hxlxz.com/?p=957" rel="cc:attributionURL">何相龙</a> 创作，采用 <a href="http://creativecommons.org/licenses/by-nc-sa/4.0/" rel="license">知识共享 署名-非商业性使用-相同方式共享 4.0 国际 许可协议</a>进行许可。  
[在Wordpress站上浏览本文](https://tec.hxlxz.com/?p=957)