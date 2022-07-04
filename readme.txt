Git is a version control system.
Git is free softwar
我来改一下
vi 是git的进入文件方法
git status命令可以让我们时刻掌握仓库当前的状态
git diff可以查看修改了什么
git log命令显示从最近到最远的提交日志
git reset可以更改文件版本 输入参数为--hard + 上一个版本就是HEAD^，上上一个版本就是HEAD^^，当然往上100个版本写100个^比较容易数不过来，所以写成HEAD~100
需要回以前的版本的话就 把--hard后面的改成你想回的版本的id就行了
git reflog用来记录你的每一次命令
git checkout -- 文件名；意思就是，把readme.txt文件在工作区的修改全部撤销，这里有两种情况：
一种是readme.txt自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；
一种是readme.txt已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。
总之，就是让这个文件回到最近一次git commit或git add时的状态。

场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令git checkout -- 文件名

场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令git reset HEAD 文件名
就回到了场景1，第二步按场景1操作。
 git checkout -- 文件名 可以丢弃工作区的修改

 rm 文件名 可以直接删除文件，但是git版本库中还有你的文件缓存
 现在你有两个选择，一是确实要从版本库中删除该文件，那就用命令git rm删掉，并且git commit
 另一种情况是删错了，因为版本库里还有呢，所以可以很轻松地把误删的文件恢复到最新版本
 git checkout -- 文件名
 注意：从来没有被添加到版本库就被删除的文件，是无法恢复的！

 要关联一个远程库，使用命令git remote add origin git@<server-name>:path/repo-name.git；
关联一个远程库时必须给远程库指定一个名字，origin是默认习惯命名；
关联后，使用命令git push -u origin master第一次推送master分支的所有内容；
此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改


git clone git@github.com:自己的用户名/gitskills.git  这样就能远程克隆仓库

查看分支：git branch

创建分支：git branch <name>

切换分支：git checkout <name>或者git switch <name>

创建+切换分支：git checkout -b <name>或者git switch -c <name>

合并某分支到当前分支：git merge <name>

删除分支：git branch -d <name>

小结
当Git无法自动合并分支时，就必须首先解决冲突。解决冲突后，再提交，合并完成。

解决冲突就是把Git合并失败的文件手动编辑为我们希望的内容，再提交。

用git log --graph命令可以看到分支合并图
nwainwaeugvbawebvewauivewauvaweu
