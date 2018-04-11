## Git命令

##### 安装git后配置全局参数
```
$ git config --global user.name "Your Name"
$ git config --global user.email "email@example.com"
```

##### 查看版本号
```
git --version
```

##### 创建版本库
```
$ mkdir git-demo
$ cd git-demo
$ pwd #显示当前目录
E/github/git-demo
$ git init #初始化仓库
```

##### 把文件添加到仓库
```
$ git add readme.md
$ git add file1.txt file2.txt #可添加多个文件
```

##### 把文件提交到仓库
```
$ git commit -m "新增readme.md文件" #m后面输入的是本次提交的说明
```

> git commit 不输入 -m 以及后面的内容会进入vim模式 <br/>
> vi & vim 有两种工作模式：
> * 命令模式：接受、执行 vi & vim 操作命令的模式，打开文件后的默认模式；
> * 编辑模式：对打开的文件内容进行 增、删、改 操作的模式； 在编辑模式下按下 ESC 键，回退到命令模式。
> ##### 创建、打开文件：$ vi [filename]
> * 使用 vi 加 文件路径（或文件名）的模式打开文件，如果文件存在则打开现有文件，如果文件不存在则新建文件，并在终端最下面一行显示打开的是一个新文件。
> * 键盘输入字母 “i”或“Insert”键进入最常用的插入编辑模式。
> ##### 保存文件：
> * 在插入编辑模式下编辑文件。
> * 按下 “ESC” 键，退出编辑模式，切换到命令模式。
> * 在命令模式下键入"ZZ"或者":wq"保存修改并且退出 vi 。
> * 如果只想保存文件，则键入":w"，回车后底行会提示写入操作结果，并保持停留在命令模式。
> ##### 放弃所有文件修改：
> * 放弃所有文件修改：按下 "ESC" 键进入命令模式，键入 ":q!" 回车后放弃修改并退出vi。
> * 放弃所有文件修改，但不退出 vi ，即回退到文件打开后最后一次保存操作的状态，继续进行文件操作：按下 "ESC" 键进入命令模式，键入 ":e!" ，回车后回到命令模式。
 
> 把文件往Git版本库里添加的时候，是分两步执行的：
> * 第一步是用git add把文件添加进去，实际上就是把文件修改添加到暂存区；
> * 第二步是用git commit提交更改，实际上就是把暂存区的所有内容提交到当前分支。

##### 查看工作区状态
```
$ git status
```

##### 查看文件的不同处
```
$ git diff #查看工作区(work dict)和暂存区(stage)的区别
$ git diff --cached #查看暂存区(stage)和分支(master)的区别
$ git diff HEAD #查看工作区和版本库里面最新版本的区别
$ git diff readme.md #查看 readme.md 文件的不同处，按 Q 键返回命令行
```

##### 查看文件
```
$ cat readme.md
```

##### 查看提交日志
```
$ git log
$ git log --pretty=oneline #每次记录显示在一行
$ git log --graph
$ git log --graph --pretty=oneline --abbrev-commit
$ git merge --no-ff -m "merge with no-ff" dev
```

##### 回退版本
```
$ git reset --hard HEAD^ #上一个版本，HEAD指向的版本就是当前版本
$ git reset --hard HEAD^^ #上上个版本
$ git reset --hard ec32933 #回滚到指定版本
```

##### 查看命令历史
```
$ git reflog
```

##### 关联一个远程库
```
$ git remote add origin git@server-name:path/repo-name.git
```

##### 第一次推送 master 分支的所有内容
```
$ git push -u origin master
```

##### 推送最新修改
```
$ git push origin master
```


##### 查看分支
```
$ git branch
```

##### 创建分支
```
$ git branch <name>
```

##### 切换分支
```
$ git checkout <name>
```

##### 创建+切换分支
```
$ git checkout -b <name>
```

##### 合并某分支到当前分支
```
$ git merge <name>
```

##### 删除分支
```
$ git branch -d <name>
```