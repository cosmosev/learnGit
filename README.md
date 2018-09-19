# learnGit



#### 从远程库克隆代码

> git clone https://github.com/cosmosev/learnGit



#### 初始化

> git init



#### 放到暂存区

> git add .(file)



#### 把暂存区文件提交到当前分支

> git commit -m "message"



#### 查看状态

> git status



#### 查看工作区和版本库的区别

> git diff HEAD -- README.md(file)



#### 关联远程库

> git remote add origin https://github.com/cosmosev/learnGit



#### 本地内容推动到远程库

> git push (-u) origin master

> 首次推送master分支时，加  -u



#### 查看commit历史记录

> git log (--pretty=oneline)

> 单行显示加  --pretty=oneline



#### 回退版本

> git reset --hard HEAD^(commit id)

> HEAD^(上一个版本)    HEAD^(上上个版本)    HEAD~100(往上100个版本)
> 可通过git log, git reflog 获取commit id



####命令历史操作查询

> git reflog







