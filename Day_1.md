# 1、本地库与远程库的交互方式

![img](https://wx4.sinaimg.cn/mw2000/008rcJvVgy1gyk9rbhzt8j30dc0i00ul.jpg)

![img](https://wx3.sinaimg.cn/mw2000/008rcJvVgy1gyk6npvd1nj30tv0fp41j.jpg)

![img](https://wx1.sinaimg.cn/mw2000/008rcJvVgy1gyk6lhimj2j30za0go789.jpg)

# 2、本地库操作

## 2.1、本地库初始化

* 命令行：git add

* 效果：

  ![img](https://wx3.sinaimg.cn/mw2000/008rcJvVgy1gyk76tb0mvj30hv05gtcc.jpg)

  注意：`.git`目录存放的是本地库相关的子目录和文件，不言删除也不要随意修改。

## 2.2、设置签名

* 形式：

  用户名：

  Email地址（只用来区分不同的开发人员）

  这里设置的签名和登录远程库（代码托管中心）的账号、密码没无关

* 命令：

  * 项目级别、仓库级别：仅在当前本地仓库范围内有效

    * `git config user.name tom_pro`

    * `git config user.email goodMorning_pro @atguigu.com`

    * 信息保存在：./.git/config文件中

      ![img](https://wx1.sinaimg.cn/mw2000/008rcJvVgy1gyk7vnoac7j30e606iwgi.jpg)

  * 系统用户级别：登陆当前操作系统的用户范围

    * `git config --global user.name tom_glb`

    * `git config --global goodMorning_pro @atguigu.com`

    * 信息保存在：`~./.git/config`文件中

      ![img](https://wx1.sinaimg.cn/mw2000/008rcJvVgy1gyk8458nscj30cp02sdgn.jpg)

  * 级别优先级：就近原则：项目优先级大于系统用户优先级，二者都有则是采用项目级别。但二者不能都没有

## 2.3、仓库状态

`$ git status`

![img](https://wx1.sinaimg.cn/mw2000/008rcJvVgy1gyk8d52dcgj30mg03ugnb.jpg)

------

`$ vim first.txt`

此时添加了一个文件，可以直接写入（退出时用Esc+Z+Z保存并退出）或者`Esc+:+w+q` 保存退出

此时再次查询Git状态

![img](https://wx2.sinaimg.cn/mw2000/008rcJvVgy1gyk8nyeuvej30nj05sgnv.jpg)

------

`$ git add first.txt`

添加后查询状态：

![img](https://wx3.sinaimg.cn/mw2000/008rcJvVgy1gyk8pi9hdpj30oj08mgqq.jpg)

------

`$ git rm --cached first.txt`

可以将文件从暂存区删除，但工作区不变动。

------

`$ git commit first.txt`

之后会弹出编辑输入说明后保存退出

![img](https://wx2.sinaimg.cn/mw2000/008rcJvVgy1gyk96e7byjj30m303l418.jpg)

![img](https://wx2.sinaimg.cn/mw2000/008rcJvVgy1gyk97yn2b7j30my057ju7.jpg)

-----

对文件进行修改：

````mysql
#	$ vim first.txt
肖恢浦@DESKTOP-L5ONVS0 MINGW64 /d/2022Winter/Git_Learning/WeChat (master)


#	$ cat first.txt
aaaaaaaa
bbbbbbbb
cccccccc
I made a change in this file!
肖恢浦@DESKTOP-L5ONVS0 MINGW64 /d/2022Winter/Git_Learning/WeChat (master)


#	$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   first.txt

no changes added to commit (use "git add" and/or "git commit -a")

````

![img](https://wx1.sinaimg.cn/mw2000/008rcJvVgy1gyk9lgboe8j30oi0c0k19.jpg)

```c
tips：
$ git commit -m "Commit Message" FileName.txt
这样省的打开编辑器
```

![img](https://wx3.sinaimg.cn/mw2000/008rcJvVgy1gyk9s2urr7j30j10fv42x.jpg)

### 2.3.4、查看历史版本

`$ git log`

多屏显示控制方式：

* 空格向下翻页
* b向上翻页
* q退出

`$ git log --pretty=oneline`

`$ git log --oneline`

`$ git reflog`

* HEAD@{移动到当前版本需要多少步}

![img](https://wx3.sinaimg.cn/mw2000/008rcJvVgy1gyk9vb4wknj30m7071n12.jpg)

* `commit f867a2bea6fb7e5963397ad398a847ba081b5d5d (HEAD -> master)`这里面的数字是哈希索引

![img](https://wx3.sinaimg.cn/mw2000/008rcJvVgy1gyka9lqexlj30s10odnd1.jpg)

