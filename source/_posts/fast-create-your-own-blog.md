---
title: fast build your own Blog website in 30 minutes （hexo && github pages）
date: 2016-09-19 14:48:05
tags: initBlog
author: AppariTT
---

### mac环境配置（windows 可能并不适用）

    1.先安装 node.js, （附上链接 https://nodejs.org/en/）
    2.再安装 git， （附上链接 https://git-scm.com/）， 如果有xcode 就跳过此步了；

### 安装 hexo， 再进行本地化服务器测试
    
    无脑在命令行中敲入如下命令
    1.$ npm install -g hexo-cli --no-optional
    此安装为默认位置， 现在你可以调整hexo的位置
    2.$ cd 到你需要的文件夹路径 
    3.$ hexo init  这是转移刚才安装的hexo 到你的路径
    4.$ npm install 继续添加依赖
       
    然后可以说已经完成1/2了。。。
    测试下是不是已经生成博客了，
    a. hexo g 这是常用命令 表示根据源文件生成内容到指定的地方， 一般改了内容都需要进行此步骤
    b. hexo s 这是在本地部署blog， 它会给一个地址 为 http://localhost:4000/ , 如果出现 hexo页面则为成功了； 如果没有看到的话请需要检查下之前有哪一步遗漏了
    
### github pages 配置， 将独立博客保存在github上， 让外网能够访问到 默认个人域名为 用户名.github.io
    
    #### 登陆你的github帐号 则没有进行注册
    #### 创建一个代码库（repository） 名字为你的 [用户名.github.io]
    #### 这一步需要添加你电脑的 SSH公钥 到 Account settings -> SSH Keys -> Add SSH Key
       ##### 如何获取公钥呢？？？让我细细道来 
       ###### git config --global user.email "你的登陆邮箱"
       ###### git config --global user.name "你的用户名" 
       ###### ssh-keygen -t rsa -C "你的登陆邮箱" 生成公钥
              
              出现以下字样表示需要输入需要保存密钥的路径， 直接回车在默认位置生成，稍后会有提示

Generating public/private rsa key pair.
Enter file in which to save the key (//.ssh/id_rsa): 

出现这个的时候 自己设置个密码 用于之后的配置使用
Enter passphrase (empty for no passphrase):
Enter same passphrase again:

之后会出现公钥的位置

Your public key has been saved in xxx\xxx\ssh.pub.

复制这一段路径到finder找到文件位置 取出内容  或者直接 vim xxx\xxx\ssh.pub. 然后复制全部的内容

       ###### 到你的github上面找到 Account settings -> SSH Keys -> Add SSH Key，添加成功！
    #### 然后更改一下hexo 的配置文件 让它知道你需要把源文件保存在哪个github上面
       ###### 如果你没有更改之前的命令行位置的话 直接vim _config.yml 然后拉到最下面进行下面的配置,不要多加一个空格或者删除一个空格

deploy:
  type: github      
  repository: git@github.com:用户名/用户名.github.io.git
  branch: master 


       ###### hexo d -g 此命令意思为生成内容并布局到刚才你的库中， 然后显示在github page中， 域名为： 用户名.github.io ， 然后别人就能通过这个域名对你的blog进行访问了
   

 
##oke！ 至此大功告成！， 新发博文 和 主题的更换， 之后再说吧！








