# 一、常用命令

![img](https://wx3.sinaimg.cn/mw2000/008rcJvVgy1h4n10g0qopj30re0dpn2f.jpg)

## 1.1、设置用户签名

[(74条消息) git---全局设置用户名、密码、邮箱_feifeidata的博客-CSDN博客_git设置全局用户名和邮箱](https://blog.csdn.net/fei321321/article/details/117730779)



![img](https://wx3.sinaimg.cn/mw2000/008rcJvVgy1h4n152azo8j317c0iytik.jpg)



## 1.2、初始化本地库

> **git init**



## 1.3、查看本地库状态

> **git status**

![img](https://wx3.sinaimg.cn/mw2000/008rcJvVgy1h4n1moj0xcj30xj0hz12t.jpg)

## 1.4、添加暂存区

> **git add 待暂存的文件**
>
> **git rm --cached 待移除的文件**

![img](https://wx2.sinaimg.cn/mw2000/008rcJvVgy1h4n1srsxccj30tm0jxn84.jpg)

![img](https://wx4.sinaimg.cn/mw2000/008rcJvVgy1h4n1uk4eisj30y60kek35.jpg)

记：`git rm --cached file`只是将文件从暂存区中去除，而在工作区中该文件仍然存在



## 1.5、提交本地库

> **git commit -m "your commit message" fileName**

![img](https://wx4.sinaimg.cn/mw2000/008rcJvVgy1h4n219khghj30yw0kq1az.jpg)

**注意提交后的状态变化**

![img](https://wx1.sinaimg.cn/mw2000/008rcJvVgy1h4n22v3itqj30x906daff.jpg)



## 1.6、修改后版本迭代

例如重新编辑了hellogit.txt文件，**此时即应重新添加至暂存区并再次提交**

![img](https://wx1.sinaimg.cn/mw2000/008rcJvVgy1h4n2d65723j31200jvtq3.jpg)



## 1.7、历史版本穿梭

> **git reflog  //查看版本信息**
>
> **git log //查看版本详细信息**



> **git reset --hard 历史版本号**

![img](https://wx3.sinaimg.cn/mw2000/008rcJvVgy1h4n2o4pburj30xo0fuk7z.jpg)

**原理**

![img](https://wx2.sinaimg.cn/mw2000/008rcJvVgy1h4n2lspji9j30ow0cadhs.jpg)

![img](https://wx4.sinaimg.cn/mw2000/008rcJvVgy1h4n2qurz9sj316t0kmtfs.jpg)

