## git学习 
### git add --> git commit 提交到本地仓库
#### git add . 

#### git add xx命令可以将xx文件添加到暂存区，如果有很多改动可以通过 git add -A .来一次添加所有改变的文件。注意 -A 选项后面还有一个句点。 git add -A表示添加所有内容，git add . 表示添加新文件和编辑过的文件不包括删除的文件; git add -u 表示添加编辑或者删除的文件，不包括新添加的文件

#### git commit -m "提交注释"

#### git push origin  分支名称，一般使用：git push origin master
### 版本穿梭
#### --hard  工作区 暂存区  本地库 都移动
#### git relog --> git reset --hard 加上索引值 随意穿梭版本
#### git relog --> git  reset --hard HEAD^^^ 后退三个版本
#### git relog --> git reset --hard HEAD~3 后退三个版本

#### --sorf （工作区 暂存区）不移动  本地库移动
#### 语法一致
#### --mixed 工作区不移动  本地库 暂存区 都移动

### git分支学习
#### master 主干
#### 创建分支 git branch blue（分支名）
#### 查看分支 git branch -v
#### git checkout blue (分支名)
#### 合并分支 1.切换到要合并的分支
#### git merge blue 将blue分支的修改合并到 master上
#### 解决同一文件的冲突 1删除特殊符号 2 修改文件保存 3 git add 文件名标记冲突已解决 4 git commit -m""

### git与github连接，本地仓库与远程仓库的连接

#### 创建远程库，在github上进行操作
#### git remote -v  --查看git项目的别名
#### git remote add 别名 分支 --创建别名
#### git push 别名 分支 --推送到远程库
#### git clone 地址 