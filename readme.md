##Git命令

#####安装git后配置全局参数
```
$ git config --global user.name "Your Name"
$ git config --global user.email "email@example.com"
```

#####查看版本号
```
git --version
```

#####创建版本库
```
$ mkdir git-demo
$ cd git-demo
$ pwd // 显示当前目录
E/github/git-demo
$ git init // 初始化仓库
```

#####把文件添加到仓库
```
$ git add readme.md
$ git add file1.txt file2.txt // 可添加多个文件
```

#####把文件提交到仓库
```
$ git commit -m "新增readme.md文件" // -m后面输入的是本次提交的说明
```

#####查看工作区状态
```
$ git status
```

#####查看文件的不同处
```
$ git diff // 查看所有文件不同的地方
$ git diff readme.md // 查看 readme.md 文件的不同处，按 Q 键退出查看模式
```

#####关联一个远程库
`git remote add origin git@server-name:path/repo-name.git`

#####第一次推送 master 分支的所有内容
`git push -u origin master`

#####推送最新修改
`git push origin master`


#####查看分支
`git branch`

#####创建分支
`git branch <name>`

#####切换分支
`git checkout <name>`

#####创建+切换分支
`git checkout -b <name>`

#####合并某分支到当前分支
`git merge <name>`

#####删除分支
`git branch -d <name>`

####命令可以看到分支合并图
`git log --graph`

git log --graph --pretty=oneline --abbrev-commit

git merge --no-ff -m "merge with no-ff" dev
