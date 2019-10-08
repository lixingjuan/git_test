## git常用操作 🎀
### 查看git信息

```bash
# 查看用户名
git config --global user.name
# 查看邮箱
git config --global user.email
# 修改全局用户名
git config --global user.name '李幸娟'
# 修改当前项目用户名
git config user.name '李幸娟'
```

### 查看git 状态
```bash

```

- 

- 
1. 创建分支
2. `git reflog`: 查看历史记录 
3. `git reset --soft e79fcfb`: 回退到某次提交，并且把commit的内容撤回到暂存区 >> ？？
4. `git stash [save "msg"]`：储藏当前暂存的文件，[并提交储藏信息] >> 切换分支可能会提醒
   1. `git stash list`: 储藏列表 >> 
   2. `git stash apply stash@{0}`: 应用某次储藏(不会删除那一次)
   3. `git stash pop`: 应用并弹出栈顶的储藏 >> ？？
5. `git status`：查看git当前的状态，在哪条分支上 >> ？？
6. `git clone <remote_url>`:克隆代码仓库
7. `git add <file_name>`: 暂存变动文件
8. `git commit -m 'commit information`: 提交变动文件
9. `git pull orign <remote branch>`: 拉取最新代码 >> remote branch是？，然后orign作用是？
<br>`git fetch`: 从远程获取最新到本地,不会自动merge
9. `git branch`: 查看本地分支
<br>`git branch -r`: 查看远程分支
10. `git checkout -b <newBranch>`: 切换分支
<br>`git branch test`: 创建分支test
11. 拉取分支代码(develop是分支代码)
`git clone -b develop XXX ` 
12. 撤销git commit 但是不删除代码：`git reset --soft HEAD^`,完成这个操作后，就恢复到了上次一的commit 状态
 - 参数：
 - --mixed:不删除工作空间改动代码，撤销commit和git add,操作这个是默认参数，git reset --mixed HEAD^和git reset HEAD^效果相同
 - --soft:不删除工作空间改动代码，撤销commit,不撤销git add
 - --hard: 删除工作空间改动代码，撤销commit,撤销git add

 13. 查看git 仓库的位置
.git>config>
url = https://rdc.hand-china.com/gitlab/25037/todoList-dva-react.git