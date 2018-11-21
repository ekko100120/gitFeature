### git rebase变基的关系问题


##### 1.两个分叉的feature分支feature1，feature2的变基过程如下，

1. **变基前**：feature1的commit是 A<--B<--C, feature2的 commit是A<--B<--D,

2. 首先切换到feature2分支上,然后rebase feature1

```shell
  $ git checkout feature2  //切换到feature2分支上
  $ git rebase feature1    //然后rebase feature1
  
  A---B---D
       \----C---D'
       
```
3. 变基完以后feature1处于C位置，feature2处于D'位置

```shell
  $ git checkout feature1
  $ git rebase feature2  //reabse feature2 保持feature1,feature2同步
```

4. 再切换到feature1，然后rebase feature2 保持同步

##### 以前的误区：

```shell

 $ git checkout feature2 & git reabse feature1 之后是 A<--B<--C'<--D，此乃误解
```


##### rebase的高级用法
