# 一、概念

![img](https://wx3.sinaimg.cn/mw2000/008rcJvVgy1h4n2woszzbj30ou0a3q7e.jpg)





# 二、分支的基本操作



![img](https://wx3.sinaimg.cn/mw2000/008rcJvVgy1h4n2y3k3h8j30rc08swg7.jpg)



## 2.1、查看已有的分支

> git branch -v

```shell
$ git branch -v
* master c84009e 这是我的第一次提交
```

## 2.2、创建分支

> git branch 分支名

```shell
$ git branch hot-fix

$ git branch -v
  hot-fix c84009e 这是我的第一次提交
* master  c84009e 这是我的第一次提交
```

## 2.3、切换分支

> git checkout 指定分支名

```shell
$ git checkout hot-fix
Switched to branch 'hot-fix'

$ vim hellogit.txt
$ git add hellogit.txt
$ git commit -m "hot-fix 的第一次分交" hellogit.txt

```

![img](https://wx2.sinaimg.cn/mw2000/008rcJvVgy1h4n387xz3kj30vz05vwky.jpg)

![img](https://wx1.sinaimg.cn/mw2000/008rcJvVgy1h4n3ekd6wjj30w404178c.jpg)

## 2.4、在本分支下切换历史版本

> git reflog   //查出历史版本信息及其对应的版本号
>
> git reset --hard 历史版本号

## 2.5、合并分支

即将指定的分支合并到当前分支

> git merge 指定分支名