 gitskills
Creating  a new branch is quick
git checkout -b dev (创建一个新的分支指向提交，并将HEAD指针指向dev切换当前分支为dev)
git merge (可能会出现冲突，冲突出现时Git先会尝试合并修改，合并不了则手动解决冲突)
git log(查看分支合并冲突)
git merge --no-ff 以非快进方式合并分支。
git stash 保存工作现场(包含工作树和暂存区)
git stash apply (取出暂存的工作树和暂存区但不删除stash list中内容)
git stash drop  (删除stash list中内容)
git stash pop (同时具备以上两个功能)
git stash list (显示暂存的内容)
