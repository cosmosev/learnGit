# learnGit

### 从远程库克隆代码

> git clone https://github.com/cosmosev/learnGit

### 初始化

> git init

### 放到暂存区

> git add .(file)

### 把暂存区文件提交到当前分支
> git commit -m "message"

### 关联远程库
> git remote add origin https://github.com/cosmosev/learnGit

### 本地内容推动到远程库
> git push (-u) origin master
  * 首次推送master分支时，加-u

### 查看commit历史记录
> git log (--pretty=oneline)
