## git commit 回退
### 作为本地弄清楚三个点
* 工作区（working tree）： 本地编辑器
* 暂存区（index）：git add操作后进入暂存区，可用git status查看
* 本地仓库（repository）：git commit 后进入本地仓库

### 修改commit
> 当我们第一次提交后，发现还有修改没有提交，通常我们想的是在add/commit一次，这样存在的问题呢就是会有一些扰乱我们的commit信息。比如我们第二次commit提交信息可能是“删除上次提交的debugger”
> 其实我们两次提交内容的目的都是同一个，比如修改bug,第一次提交时忘了删除我们调试时留下的debugger。然后就删除提交第二次，第二次的提示信息就很不友好。我们怎么来将两个commit合为一个呢？
* git commit --amend   // 把上一次的commit记录去除，修改commit信息。

