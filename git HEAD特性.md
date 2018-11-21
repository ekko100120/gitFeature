## git HEAD特性


##### 1. 将HEAD与branch分类，指向父父commit(commit A)

```shell

 //方法1
 $ git checkout HEAD~3
 
 //方法2
 $ git checkout HEAD^^^
 
 // 方法3
 $ git checkout <commit A>

```

#### 2. git branch -f master HEAD~3 让分支指向另一个提交

```
$ git branch -f master HEAD~3

```

#### 总结根据`git checkout <commit A>` 和 `git branch -f master HEAD~3`可以快速把某个分支指向某个特定的commit上
