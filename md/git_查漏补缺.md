# git 查漏补缺

#### git diff

```
$ git diff // unstage VS local repo

$ git diff --staged // staged vs local repo

$ git diff master..dev  // master branch VS dev branch
$ git diff master dev  // master branch VS dev branch

$  git diff c2967e..da363d // commit c2967 VS commit da363d
$  git diff c2967e da363d // commit c2967 VS commit da363d


```

#### git log 

```
$ git log -p  // display detail modified message
```

#### git stash

```
$ git stash // stash staged file

$ git stash -u(--include-untracked) // stash unstaged and staged file

$ git stash -a(--all) // stash unstaged and staged file and ignored file 

$ git stash list // list all stash 

$ git stash save "<commit>" // stash file with commit "<commit>"

$ git stash pop stash@{n} //  set back to stash@{n}

$ git stash drop stash@{n} // clean up stash stash@{n}

$ git stash clear // clean up all stash

$ git stash show // show diff stash
$ git stash show -p // show full diff stash
```

#### git clean
```
	$git clean  // reset untracked file note include unstaged file

	-n //
	-f //force clean
	-i //交互式
	-x // 包含ingored files
	-d //删除 == git clean 

```

#### 修改commit message
```
$ git commit --amend //修改commit message


```


#### git 撤销 staged file

```
$ git reset --mixed  // git 撤销 staged file
```
#### git 撤销 unstaged file

```
$ git checkout <filename/dirname>  // git 撤销 未staged file
```
#### git 撤销 untracked file

```
$ git clean <filename/dirname>  // git 撤销 未 tracked file
```

#### git 撤销 staged file

```
$ git reset <filename/dirname>  // git 撤销  staged filename file, 不改变workplace 和工作树
```


## Reference
<https://www.atlassian.com/git/tutorials/inspecting-a-repository>


#### git 缩写术语

```
先说下我常见／常用的：

WIP   Work In Progress 开发中
LGTM Looks Good To Me Riview 完别人的 PR ，没有问题
PTAL Please Take A Look 帮我看下，一般都是请别人 review 自己的 PR
CC 是好像是通知别人的意思，不知道是什么的缩写
搜到一篇相关文章： What do cryptic Github comments mean?

LGTM  —  looks good to me
ACK  —  acknowledgement, i.e. agreed/accepted change
NACK/NAK — negative acknowledgement, i.e. disagree with change and/or concept
RFC  —  request for comments, i.e. I think this is a good idea, lets discuss
WIP  —  work in progress, do not merge yet
AFAIK/AFAICT  —  as far as I know / can tell
IIRC  —  if I recall correctly
IANAL  — “ I am not a lawyer ”, but I smell licensing issues
```


