## git commit 回退
### 作为本地弄清楚三个点
* 工作区（working tree）： 本地编辑器
* 暂存区（index）：git add操作后进入暂存区，可用git status查看
* 本地仓库（repository）：git commit 后进入本地仓库

### 修改commit
> 当我们第一次提交后，发现还有修改没有提交，通常我们想的是在add/commit一次，这样存在的问题呢就是会有一些扰乱我们的commit信息。比如我们第二次commit提交信息可能是“删除上次提交的debugger”
> 其实我们两次提交内容的目的都是同一个，比如修改bug,第一次提交时忘了删除我们调试时留下的debugger。然后就删除提交第二次，第二次的提示信息就很不友好。我们怎么来将两个commit合为一个呢？
* git commit --amend   // 把上一次的commit记录去除，修改commit信息。
第一次提交：
第二次提交
查看commit log
回退
查看commit log
> 只有一次提交记录
### 回退commit
* git reset --soft   // 回退到指定commit，该commit之后的提交内容，保留工作目录，并把重置 HEAD 所带来的新的差异放进暂存区
* git reset --hard   // 回退到指定commit，该commit之后的提交内容，工作区和暂存区的内容都被抹掉
 


