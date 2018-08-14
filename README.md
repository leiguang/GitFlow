# [GitFlow](https://github.com/leiguang/GitFlow)


### 参考：
1. [聪神](https://github.com/ManitoYu) 的面对面指点
2. [my-git](https://github.com/xirong/my-git/blob/master/git-workflow-tutorial.md)
3. [3.6 Git 分支 - 变基](https://git-scm.com/book/zh/v2/Git-分支-变基)
...

### Note:
1. *所有的*Git操作都会有记录，即使git log、sourcetree界面上看不到，都可以通过git reflog 找回。
2. revert 提交回滚，回滚 某个提交节点所做的文件更改，并不会删除之前的提交记录，而是在当前基础上产生一个新的commit。注意！！！只会回滚该节点的提交更改。
3. reset 重置，重置到某个提交节点，中间的提交记录都会被删除，有三种选择，soft - 相当于恢复到add状态、mix - 相当于恢复到stash状态、hard - 丢掉所有改变。
4. cherry pick 遴选，只会合并 该次commit所做的更改，该次commit之前的 commit记录 所做的修改并不会被合并。
5. rebase [变基](https://git-scm.com/book/zh/v2/Git-分支-变基)，遵守一条金科玉律：“不要对在你的仓库外有副本的分支执行变基”。 
在sourcetree上，若要将feature分支的更改 合并到dev上，需要先checkout到dev，然后在feature上 右击 -> 将当前变基变更到feature；或者先在feature分支上 rebase dev，然后再checkout dev 并merge feature。 
6. 将dev合到master时，可以不需要做变基操作，master上保留dev所有的提交记录也是ok的。
7. hotfix，从master上checkout出hotfix，然fix完毕后合并回master，然后把master上的修改合并回dev。（hotfix和master相关联，master和dev相关联）
