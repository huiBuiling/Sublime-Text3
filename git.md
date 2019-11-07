### Git

##### Git常规操作

1. 初始化
    git config --global user.name "xxx"
    git config --global user.email "xxx@gmail.com"

2. 获取git配置信息
    git config --list

3. 创建版本库
     mkdir testgit && cd testgit
     git init

4. 把文件添加到版本库
     touch readme.md
     git add readme.md

5. 把文件提交到仓库
    git commit -m 'xxxx'

5. 克隆
    直接克隆master: git clone https://github.com/huiBuiling/dva-musics.git
    对应分支克隆:git clone -b dev(分支名) https://github.com/huiBuiling/dva-musics.git

6. 查看修改状态
    git status

7. 查看修改
    查看对应文件修改内容: git diff readme.md
    工作区和版本库里面最新版本: git diff HEAD -- readme.md

8. 查看版本记录
     全部：git log
     近到远：git log --pretty=oneline

9. 版本回退
      上一个版本: git reset --hard HEAD^(上上一个版本就是HEAD^^, ...)
      回退对应版本： git reset --hard 2e70fdf(git log 查询出的commit id，取后几位即可)

10. 记录你的每一次命令
        git reflog

11. 丢弃工作区的修改(撤销, 即回到最近一次git commit或git add时的状态)
        git checkout -- readme.md
        git reset

12. 删除文件
        rm readme.md

13. 生成SSH key：
        ssh-keygen -t rsa -C "email"

15. 创建且切换分支
        创建分支：git branch dev
        切换分支：git checkout dev
        ------------------------
        git checkout命令加上-b参数表示创建并切换：git checkout -b dev

16. 查看当前分支
        当前: git branch
        远程: git branch -r
        所有: git branch -a

18. 合并分支(dev -> master)
        切换：git checkout master
        合并：git merge dev（合并指定分支到当前分支）

19.  删除分支
         git branch -d dev

21. 提交冲突，暂存缓存区(暂时将未提交的变化移除，稍后再移入)

        # 增
        git stash   # 存储代码，压入代码堆栈
        git stash save "message"  # 推荐

        # 查
        git stash list  # 查看现有记录
        git stash show  # 检查不一样的地方

        # 删
        git stash pop  # 恢复最新保存的工作进度
        git stash drop stash@{1} # 删除
        git stash clear  # 删除所有

22. 