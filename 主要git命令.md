git config --global user.name "bruno"

设置用户名

git config --global user.email 839768702@qq.com

设置邮箱

git config --global credential.helper store

永久存储用户名和邮箱

git config --global --list

查看当前用户名，邮箱以及他们的状态

git init 【仓库名】   OR    git clone   url.git

创建仓库，名字省略则在当前文件夹创建仓库，有名字则在当前文件夹创建一个仓库名文件夹，然后在该文件夹霞创建仓库

git add  , git commit , git reset , git rm ， git checkout

add 添加到暂存区， commit暂存区到本地仓库，reset 暂存区到已经修改的状态，rm 是还没修改的文件改成为跟踪的状态，checkout 回退版本，从已经修改带未被修改

 git commit -m "第一次提交" ：“。。。。。。”内是提交的描述信息

 -am 可以不用add，直接更新到版本库中

git diff 【HEAD】：【xxx】可以不写，表示前后两次提交工作区和暂存区，版本库的差异

.gitignore文件：里面记录的文件名可以被忽视，修改控制不用被add，commit相应控制，但只适用于.gitignore被添加后被记录的文件，里面可以放隐私文件，编译中间文件等，可以用通配符，

忽略文件夹  temp/



ssh链接github远程仓库加入的5行，意思是当访问github时使用图片中的rsa密钥

git push, git pull:推送和拉取远程仓库 git pull默认拉取远程仓库的主分支到本地，后面可加[仓库名] [分支名] 来拉取指定分支，会自动进行一次合并同步，如果不同会冲突，需要手动解决

git fetch也可以拉取远端仓库，不过只会获取修改的内容，而且不会自行同步本地和远端不同的修改，需要手动解决冲突

git remote add <shortname><url>:关联本地和远程仓库； <shortname>是远程仓库别名

git branch -M master ：指定分支的名称为master

git push -u origin master:master :把本地的master分支和远程的origin分支关联起来 -u是-upstream的缩写

git rebase  [branch-name]:把当前分支的修改记录与[branch-name]的共同修改起始节点提交到当前等职末尾修改链表节点提交放到[branch-name]的修改记录链表提交的后面，形成一条修改提交链表，建议个人使用修改的仓库使用
