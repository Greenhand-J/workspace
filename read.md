### 1.设置机器的名字和email地址

```
git config --global user.name "your name"
git config --global user,email "your email"
```

### 2.创建版本库

```
+ cd /d                         #进入一个空目录
+ mkdir learngit cd learngit    #创建一个文件夹并进入
+ git init                      #使得该目录变成git可以管理的仓库
+ git branch <name>  #创建一个新的分支
```

### 3.添加

```
+  git add filename              #将文件由工作区加载到暂存区
+  git commit -m "discrible"     #将文件由暂存区加载到分支
```

### 4.查询

```
git log pretty=oneline单行输出参数 #查看提交的文件日志
cat filename                     #查看文件内容
git reflog                   	 #查看每个版本的版本号
git status    	        		 #查看当前状态
git diff HEAD-- filename 		 #查看工作区和版本库最新版本的区别
git branch                   	 #查看分支
git log  --graph --pretty=oneline --abbrev-commit   #查看分支合并图
```

### 5.版本回退

```
git reset--hard HEAD^  			#返回上个版本  HEAD^代表上个版本
git reset --hard commit_id       #跳转指定的版本
```

### 6.修改

```
git checkout -- filename      #撤销在工作区的修改
git reset HEAD filename       #将暂存区的修改退回到工作区
```

### 7.删除

```
git rm filename               #删除文件

git branch -d <name>          #删除分支
```

### 8.远程传输

```
git remote add origin git@github.com:username/learngit.git  #建立远程
git push -u origin master     #初次提交
git push origin master        #之后提交
```

### 9.仓库克隆

```
git clone github git@github.com:<username>/<pro-name.git>
```

### 10.分支其他操作

```
git checkout <name> / git switch <name>    #切换分支
git checkout -b <name> / git switch -c <name>  #创建并切换分支
git merge <name>          #合并某分支到当前分支
git merge --no-ff -m"merge with no-ff" <name> #禁用fast forwad合并
```

### 11.bug分支

```
git stash  #保存当前的工作内容
git stash list  #查看保存的地点
git stash apply <place> #指定恢复工作但不删除stash内容
git stash drop    #删除stash内容
git stash pop      #恢复且删除stash内容
git cherry-pick <branch-place>  #重复branch的操作并提交
git  branch -D <branch-name>  #强行删除未合并的分支
```

### 12.多人协作

```
git pull               										 #将最新的提交抓下
git branch --set-upstream branch-name origin/branch -name    #建立本地分支和远程分支的关联
git rebase  												 #将没有push的提交历史整理成直线
```
