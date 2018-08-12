# [GitFlow](https://github.com/leiguang/GitFlow)


### Note:
1. revert 提交回滚，回滚 某个提交节点所做的文件更改，并不会删除之前的提交记录，而是在当前基础上产生一个新的commit。注意！！！只会回滚该节点的提交更改。
2. reset 重置，重置到某个提交节点，中间的提交记录都会被删除，有三种选择，soft - 相当于恢复到add状态、mix - 相当于恢复到stash状态、hard - 丢掉所有改变。
3. cherry pick 遴选，只会合并 该次commit所做的更改，该次commit之前的 commit记录 所做的修改并不会被合并。
4. rebase 变基，不仅可以将分支merge后 的提交记录整合为一条线性提交历史， 带参数的 rebase -i 可以将单条分支的多条commit记录的文件变更合并为一条（对应于sourcetree上的交互式变基）。 
      在sourcetree上，若要将feature分支的更改 变基到dev上，需要先checkout到dev，然后在feature上 右击 -> 将当前变基变更到feature。 
5. 将dev合到master时，可以不需要做变基操作，master上可以保留dev所有的提交记录。
6. hotfix，从master上checkout出hotfix，然fix完毕后合并回master，然后把master上的修改合并回dev。（hotfix和master相关联，master和dev相关联）
