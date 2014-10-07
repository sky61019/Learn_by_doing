Git Learning
============================
记录学习Git的笔记

# Git操作
## 忽略特殊文件
为了避免每次git status都会显示“Untracked files ...”。解决方案：
1. 在Git工作区的根目录下创建一个特殊的.gitignore文件
2. 把要忽略的文件名填进去，Git就会自动忽略这些文件
不需要从头写.gitignore文件，GitHub已经为我们准备了各种配置文件，只需要组合一下就可以使用了。所有配置文件可以直接在线浏览：[https://github.com/github/gitignore](https://github.com/github/gitignore)
