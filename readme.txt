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
