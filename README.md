# learnGit


### 基本操作

#### 1. 从远程库克隆代码
> ###### git clone https://github.com/cosmosev/learnGit

#### 2. 初始化
> ###### git init

#### 3. 放到暂存区
> ###### git add .(file)

#### 4. 把暂存区文件提交到当前分支
> ###### git commit -m "message"

#### 5. 关联远程库
> ###### git remote add origin https://github.com/cosmosev/learnGit

#### 6. 本地内容推动到远程库
> ###### git push (-u) origin master
> *首次推送master分支时，加  -u*

#### 7. 回退版本
> ###### git reset --hard HEAD^(commit id)
> *HEAD^(上一个版本) ------  HEAD^(上上个版本)  ------  HEAD~100(往上100个版本)*
>
> *可通过git log, git reflog 获取commit id*

#### 8. 撤销修改
> ###### git checkout -- README.md(file)
> *回到最近一次git commit或git add时的状态*
>
> *本质是用版本库里的版本替换工作区的版本*

#### 9. 删除文件
> ###### rm README.md(file)
> *未commit前可用git checkout -- README.md(file)恢复文件*
> ###### git rm README.md(file)
> *不可用git checkout恢复*

---------------------------------------------

### 查询操作
#### 1. 查看文件内容
> ###### cat README.md(file)

#### 2. 查看状态
> ###### git status
> *可查看冲突状态*

#### 3. 查看工作区和版本库的区别
> ###### git diff HEAD -- README.md(file)

#### 4. 查看commit历史记录
> ###### git log (--pretty=oneline) (--abbrev-commit)
> *单行显示加  --pretty=oneline*
>
> *可查看合并分支情况*

#### 5. 命令历史操作查询
> ###### git reflog

----------------------------------------------

### 分支

#### 1. 创建分支
> ###### git branch dev(name)

#### 2. 切换分支
> ###### git checkout dev(name)

#### 3. 快速创建并切换
> ###### git checkout -b dev(name)

#### 4. 查询分支
> ###### git branch

#### 5. 分支合并
> ###### git merge dev(name)
> *快速合并*
> ###### git merge --no-ff -m "message" dev(name)
> *提交新的commit，合并分支有迹可循*

#### 6. 删除分支
> ###### git branch -d dev(name)
> *删除未合并过的分支，可通过git branch -D dev(name)强行删除*

-----------------------------------------------

### BUG策略

#### 1. 储藏工作现场
> ###### git stash

#### 2. 查看工作现场
> ###### git stash list

#### 3. 恢复工作现场
> ###### git stash apply
> *还需要删除工作现场*
> ###### git stash pop
> *恢复同时删除stash内容*

#### 4. 删除工作现场
> ###### git stash drop

-----------------------------------------------

### 标签管理

#### 1. 创建标签
> ###### git tag v1.0(版本号) (commit id)
> *commit id 选填，不填表示最近一次commit*

#### 2. 查看标签
> ###### git tag

#### 3. 查看标签信息
> ###### git show v0.9(版本号)

#### 4. 创建带有说明的标签
> ###### git tag -a v0.1 -m "version 0.1 released" (commit id)
> *-a 指定标签名*
>
> *-m 指定说明文字*

#### 5. 删除标签
> ###### git tag -d v1.0(版本号)

#### 6. 推送标签到远程
> ###### git push origin v1.0(版本号)/--tag(全部)

#### 7. 删除远程标签
> ###### git push origin:refs/tags/v1.0(版本号)
> *先本地删除*

-------------------------------------------------













