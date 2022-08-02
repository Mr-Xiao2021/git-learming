

![img](https://wx2.sinaimg.cn/mw2000/008rcJvVgy1h4o7qkbsgzj30wv0k9n2g.jpg)



![img](https://wx3.sinaimg.cn/mw2000/008rcJvVgy1h4o7trcekvj31nx0uudxo.jpg)

[24_尚硅谷_Git_GitHub_团队内协作](https://www.bilibili.com/video/BV1vy4y1s7k6?p=24&spm_id_from=pageDriver&vd_source=fbab16b01174b8c671633151f543a4c7)

# 一、推送本地库到远程仓库

![img](https://wx3.sinaimg.cn/mw2000/008rcJvVgy1h4o8gf6r5jj311n0k747d.jpg)



> 查看当前所有远程地址别名

git remote -v

> 起别名

git remote add git-demo https://github.com/Mr-Xiao2021/git-demo.git

> 推送本地分支内容到远程仓库

git push git-demo master

或者直接 git push 仓库链接名

> 拉取远程到本地库

![img](https://wx3.sinaimg.cn/mw2000/008rcJvVgy1h4ro8kz3toj319n0gj0x9.jpg)

git pull git-demo master

> 克隆

git clone 仓库链接



> 邀请成员加入团队

![img](https://wx2.sinaimg.cn/mw2000/008rcJvVgy1h4rov864maj31hr0trgw9.jpg)

此时才可以使得成员在自己本地修改代码并提交之后github更新代码

> 跨团队

1. 先`fork`

2. 修改完后`push`到自己仓库后，提交申请给被fork``方

   ![img](https://wx3.sinaimg.cn/mw2000/008rcJvVgy1h4rp8jtojgj30wy0760uk.jpg)

   

   ![img](https://wx4.sinaimg.cn/mw2000/008rcJvVgy1h4rp9sztj0j31qb0xth51.jpg)

   

   

> ssh免密登录

[26_尚硅谷_Git_GitHub_SSH免密登录_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1vy4y1s7k6?p=26&spm_id_from=pageDriver&vd_source=fbab16b01174b8c671633151f543a4c7)

1. 在本机用户文件夹下打开`git bash`之后输入

   肖恢浦@DESKTOP-L5ONVS0 MINGW64 ~
   $ ssh-keygen -t rsa -C 3493602396@qq.com

   即生成`.ssh`文件夹，进入后打开并复制`id_rsa.pub`内容

2. ![img](https://wx2.sinaimg.cn/mw2000/008rcJvVgy1h4rpqtcixsj31qo107k7r.jpg)



就可以直接

![img](https://wx2.sinaimg.cn/mw2000/008rcJvVgy1h4rpulh904j314z0f2q9k.jpg)

$ git pull git@github.com:Mr-Xiao2021/git-demo.git master

$ git push git@github.com:Mr-Xiao2021/git-demo.git master

