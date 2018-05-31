git 命令整理

cd 打开本地文件目录
git init
git add README.md　 
git add . 提交新文件(new)和被修改(modified)文件，不包括被删除(deleted)文件git add -A  提交所有变化
git add -u  提交被修改(modified)和被删除(deleted)文件，不包括新文件(new)

git commit -m "first commit"

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


git remote -v　查看远程地址

git rm -r --cached dirname //删除远程文件夹，但保留本地文件夹 
git commit -m ‘say something’ //提交操作，并添加描述 
git push origin master //推送


git config  user.name "maxsu" //设置用户名
git config user.email "yiibai.com@gmail.com"　//设置邮箱

git config --list

git clone　　//克隆一个仓库到一个新目录

git branch -r //查看远程分支
git branch -a　//查看所有分支

