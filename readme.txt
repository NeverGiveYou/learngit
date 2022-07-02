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

