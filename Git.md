Git Learning
============================
记录学习Git的笔记

# Git操作
## 忽略特殊文件
为了避免每次git status都会显示“Untracked files ...”。解决方案：

1. 在Git工作区的根目录下创建一个特殊的.gitignore文件
2. 把要忽略的文件名填进去，Git就会自动忽略这些文件

不需要从头写.gitignore文件，GitHub已经为我们准备了各种配置文件，只需要组合一下就可以使用了。所有配置文件可以直接在线浏览：[https://github.com/github/gitignore](https://github.com/github/gitignore)

# Github 远程仓库
## Github远程仓库创建

1.	**创建SSH Key**用于本地Git仓库和Github仓库之间的传输。在用户主目录下，看看有没有.ssh目录，如果有，再看看这个目录下有没有id_rsa和id_rsa.pub这两个文件，如果已经有了，可直接跳到下一步。如果没有，打开Shell（Windows下打开Git Bash），创建SSH Key：

	> $ ssh-keygen -t rsa -C "youremail@example.com" 

	你需要把邮件地址换成你自己的邮件地址，然后一路回车，使用默认值即可，由于这个Key也不是用于军事目的，所以也无需设置密码。如果一切顺利的话，可以在用户主目录里找到.ssh目录，里面有id_rsa和id_rsa.pub两个文件，这两个就是SSH Key的秘钥对，id_rsa是私钥，不能泄露出去，id_rsa.pub是公钥，可以放心地告诉任何人。

2.    **设置username和email**，因为github每次commit都会记录他们。
>  $ git config --global user.name "your name"
   $ git config --global user.email "your_email@youremail.com"

3.    **克隆仓库**或将现有的本地仓库与Github上的仓库进行**关联**
> $ git clone https://github.com/your name/example.git
  或 $ git remote add origin https://github.com/your name/example.git

