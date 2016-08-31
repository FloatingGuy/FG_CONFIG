## Git原理
> Git pro 第九章

### 9.1 .git目录结构

.git

    |- branches/
    |- hooks /      客户端或服务端钩子 脚本（第六章）
    |- info /       忽略的文件，但不在.gitignore中管理
    |- objects /    存储所有数据内容
    |- refs /       存储指向数据（分支）的提交对象的指针
    |- config       项目特有的配置选项
    |- description  GitWeb 使用
    |- <HEAD>       指向当前分支
    |- index        『暂存区』的信息

### Git 对象

1. 对象的类
    * blob对象
    * tree对象
    * commit对象

1.1 blob对象
blob对象是保存在 .git/objects 目录下的每个文件。
使用 底层命令 cat-file 和 hash-object 可以直接操作 blob对象。
```
   $ echo 'version 1' > test.txt
   $ git hash-object -w test.txt      #存储对象
    83baae61804e65cc73a7201a7252750c76066a30    (保存在.git/objects 目录的blob对象)

   $ git cat-file -p 83baae61804e65cc73a7201a7252750c76066a30 > test.txt  #查看对象
   $ cat test.txt
    version 1
```
![blob对象]()

1.2 tree对象
tree对象可以存储文件名, 仓库管理的所有内容都是通过tree和blob来保存的。

![tree对象]()


1.3 commit对象
该对象用来记录所有的提交信息
commit-tree 命令：
    使用该命令 可以为某个tree创建一个commit对象，该对象记录了当前时间戳、提交注释信息、作者/提交者等。
    返回一个commit对象的hash值。
```
$ echo 'first commit' | git commit-tree d8329f fdf4fc3344e67ab068f836878b6c4951e3b15f3d

$ git cat-file -p fdf4fc3
    tree d8329fc1cc938780ffdd9f94e0d364e0ea74f579
    author Scott Chacon <schacon@gmail.com> 1243040974 -0700 committer Scott Chacon <schacon@gmail.com> 1243040974 -0700

    first commit
```
















