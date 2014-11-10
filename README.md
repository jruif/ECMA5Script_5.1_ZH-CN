ECMA5Script_5.1_ZH-CN
=====================

ECMAScript 5.1  中文版

创建项目介绍页地址：
https://help.github.com/articles/creating-project-pages-manually/

汉化总结下：

###　第一步：新克隆项目

例如：
```bash
$ git clone https://github.com/user/repository.git
```
上面的命令中user是你的昵称repository是你的项目名
大概会显示：
```bash
# Clone our repository
# Cloning into 'repository'...
# remote: Counting objects: 2791, done.
# remote: Compressing objects: 100% (1225/1225), done.
# remote: Total 2791 (delta 1722), reused 2513 (delta 1493)
# Receiving objects: 100% (2791/2791), 3.77 MiB | 969 KiB/s, done.
# Resolving deltas: 100% (1722/1722), done.
```
###　第二步：创建一个`gh-pages`分支

在上一步的基础上进行下面的命令
```bash
$ cd repository

$ git checkout --orphan gh-pages
# Creates our branch, without any parents (it's an orphan!)
# Switched to a new branch 'gh-pages'

$ git rm -rf .
# Remove all files from the old working tree
# rm '.gitignore'
```
注意：`$ git rm -rf .`会清空你新克隆项目下的所有文件，不过不用急，这是分支上的文件，不是主干上的文件

###  第三步：添加内容并上传

```bash
$ echo "My GitHub Page" > index.html
$ git add index.html
$ git commit -a -m "First pages commit"
$ git push origin gh-pages
```
已经有了自己的`index.html`的可以不用执行第一个命令，可以直接拷贝进入这个目录，使用第二个命令将文件添加到缓存区域,
第三个命令提交缓存，第四个提交本地`gh-pages`分支至远程分支。
