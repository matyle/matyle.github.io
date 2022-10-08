## git rebase
- git rebase是一个非常有用的命令，但知道和用的人非常少，今天介绍一下其作用


### git rebase -i 
- 作用：常用来合并多个相同目的的提交。
- 交互式有下面几个命令，常用命令

| 命令 | 作用                                    |
| ---- | --------------------------------------- |
| p    | 使用 commit                             |
| r    | 使用 commit，并修改提交信息             |
| e    | 编辑 commit，用于需要修改 commit 文件时使用，进入 edit 之后，然后修改文件或添加文件 |
| s    | 使用最多的命令，用来合并上一个提交      |

```bash
# Commands:
# p, pick <commit> = use commit
# r, reword <commit> = use commit, but edit the commit message
# e, edit <commit> = use commit, but stop for amending
# s, squash <commit> = use commit, but meld into previous commit
```

#### 命令行操作
<img src="https://raw.githubusercontent.com/matyle/tupic/master/img/20220911111505.png" style="zoom:50%;" />
#### lazygit 操作
- 对应 lazygit 在提交信息栏，按 x 可以查看对应命令
<img src="https://raw.githubusercontent.com/matyle/tupic/master/img/20220911110455.png" style="zoom:30%;" />
![]()


### git rebase branch
- 模拟场景
	- dev 开发完合并到了 master
	- 然后 dev2 开发完再去合并 master，我们可以看到 commit 2c8284ac出现分支，并且显示 Merge branch ‘dev2’
	- 此时我们想去掉这个分支
<img src="https://raw.githubusercontent.com/matyle/tupic/master/img/20220911104042.png" style="zoom:30%;" />

- 使用`git rebase dev2` 或者在 lazygit 光标放在 `dev2` 上面按 `r` (不清楚命令可以通过 x 查看)

<img src="https://raw.githubusercontent.com/matyle/tupic/master/img/20220911104147.png" style="zoom:30%;" />

- 最后效果就是一个分支，非常优雅

<img src="https://raw.githubusercontent.com/matyle/tupic/master/img/20220911104211.png" style="zoom:30%;" />





### git pull --rebase

- 当我们从远程拉代码的时候如果使用：git pull --rebase，则会以rebase的方式进行更新，而不是默认的merge。
- 有时远程 rebase 过，那么拉的时候也需要 rebase

