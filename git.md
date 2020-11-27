git version

git config --global user.name "yangjiachang"

git config --global user.email "dockerc@163.com"

查看配置的选项 cat ~/.gitconfig

初始化git仓库 git init

查看git仓库状态 git status

添加文件到暂存区 git add <file>

回退上一状态 git rm --cached README.md

添加所有文件 git add -A， 大A是 all的意思

查看所有文件，包含隐藏文件 ll -la，这时候可以看到.git，它是一个目录，cd .git进入这个目录有一个index文件，cat index查看这个文件

提交文件 git commit -m "add README.md"   -m参数是message的意思

```
git config --global user.name “用户名”
git config --global user.email “邮箱”

执行生成公钥和私钥的命令：  ssh-keygen -t rsa 并按回车3下
执行查看公钥的命令：   cat ~/.ssh/id_rsa.pub
```

连接github

在github创建一个新仓库，根据命令提示连接远程仓库git remote add origin git@github.com:yangjiachang/git-tutorial.git

注意origin是这个远程仓库的名字，这个名字是可以自定义的，但是一般都使用origin，这是约定俗成的，不建议修改

可以通过 git remote -v查看连接

推送到远程仓库 git push -u origin master，加上-u参数后以后再提交就可以直接用 git push来推送

克隆仓库，并起一个别名 git clone https://github.com/yangjiachang/git-tutorial.git git-demo

拉取到本地仓库 git pull origin master，origin：远程连接的名字，master：分支的名字