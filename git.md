### tag
展示当前分支的最近的 tag
git describe --tags --abbrev=0

### blame 
查看某段代码是谁写的
git blame <file-name>

### whatchanged  
查看两个星期内的改动
git whatchanged --since='2 weeks ago'

### log
commit 历史中显示 Branch1 有的，但是 Branch2 没有 commit
git log Branch1 ^Branch2