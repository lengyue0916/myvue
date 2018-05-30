git 命令整理

cd 打开本地文件目录
git init
git add README.md　 
git add . 提交新文件(new)和被修改(modified)文件，不包括被删除(deleted)文件git add -A  提交所有变化
git commit -m "first commit"
git add -u  提交被修改(modified)和被删除(deleted)文件，不包括新文件(new)
git remote add origin https://github.com/lengyue0916/vue.git
git push -u origin master

git　help 帮助命令
git reset
git reset HEAD 撤销最近的提交
git reset HEAD^　撤销上上次的提交

git reset --mixed
git reset --soft

HEAD 最近一个提交
HEAD^ 上一次提交
HEAD^ ^ 上一次的 上一次的提交（倒数第三次）
HEAD^^^ 倒数 第四次的 提交

HEAD~0 最近一个提交
HEAD~1 上一次提交
HEAD^2 上一次的 上一次的提交（倒数第三次）
HEAD^3 倒数 第四次的 提交


git pull origin master 将远程仓库里面的项目拉下来

dir  查看有哪些文件夹

git rm -r --cached file  删除file文件或文件夹
git commit -m '删除了target'  提交,添加操作说明
git push -u origin master 将本次更改更新到github项目上去
git remote -v　查看远程地址
