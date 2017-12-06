#Hexo搭建

>1.把 Hexo 博客发布到 GitHub 上面.
>2.注意 Hexo 的格式要求(:后预留空格).
>3.源文件都在 ```source```文件夹中,如果需要保存源文件(.md)，需要另起一个 GitHub 仓库去存储.

###[1.安装hexo](#install_hexo)
###[2.建站](#start_hexo)
###[3.发布](#hexo_deploy)
###[4.错误](#error_solve)
###[5.脚本](#script_write)
###[6.把 CNAME 添加到项目中](add_CNAME)
###[7.文章开头title](#title)

***
***
***


###1.安装hexo<a name="install_hexo"/>
>https://hexo.io/zh-cn/docs/
```
npm install -g hexo-cli
```
***

###2.建站<a name="start_hexo"/>

>参考:http://www.jianshu.com/p/834d7cc0668d

* 1.初始化仓库
```
hexo init yourname
cd yourname
npm install
```
* 2.修改 _config.yml 文件.
![](/assets/Snip20171111_8.png)

>记得要有缩进!:https://hexo.io/zh-cn/docs/deployment.html
>记得添加空格: https://github.com/hexojs/hexo/issues/1154

***

###3.发布<a name="hexo_deploy"/>

>参考:http://www.jianshu.com/p/834d7cc0668d

```
hexo clean
hexo g
hexo d
```

***

###4.错误<a name="error_solve"/>

* 1.发现错误```Deployer not found: git```,就算是像 '教程1' 说的那样，把 git 改为 github ,再运行```npm install hexo-deployer-git --save``` 也没用.
>教程1: https://github.com/hexojs/hexo/issues/1040
```
tiandeMacBook-Pro-2:myBlog tianzeng$ hexo d
ERROR Deployer not found: github
```

* 2.解决，原来是在出现错误后，运行
    * 1
     ```
    tiandeMacBook-Pro-2:MyBlog2 tianzeng$ hexo deploy
ERROR Deployer not found: git
tiandeMacBook-Pro-2:MyBlog2 tianzeng$ npm install hexo-deployer-git --save
    ```
    * 2
    ```
    tiandeMacBook-Pro-2:MyBlog2 tianzeng$ hexo d
INFO  Deploying: git
INFO  Setting up Git deployment...
    ```
这样就可以了.
![](/assets/Snip20171111_9.png)


***

###5.脚本<a name="script_write"/>

>参考: https://github.com/qinjx/30min_guides/blob/master/shell.md

* 把上传命令双击自动完成!
```
#!/bin/bash
CMD_PATH=`dirname $0`
cd $CMD_PATH
echo 'Begin---------------------------'
echo 'hexo clean:'
hexo clean
echo 'hexo generate:'
hexo generate
echo 'hexo deploy:'
hexo deploy
echo 'Finish--------------------------'
exit 0
```
![](/assets/Snip20171111_10.png)

***

###6.把 CNAME 添加到项目中<a name="add_CNAME"/>

>参考:http://webcache.googleusercontent.com/search?q=cache:Y4TSEfU_xUoJ:jeasonstudio.github.io/2016/05/26/Mac%25E4%25B8%258A%25E6%2590%25AD%25E5%25BB%25BA%25E5%259F%25BA%25E4%25BA%258EGitHub-Page%25E7%259A%2584Hexo%25E5%258D%259A%25E5%25AE%25A2/+&cd=2&hl=zh-CN&ct=clnk&gl=ph

* 1.把 CNAME 文件放到 /blog/themes/landscape/source 目录下即可(其他想同步到 github 上的文件也是同理).



***

###7.文章开头title<a name="title"/>
>标题,标签，种类,日期.

```
---
title: Hello World
tags: [tags]
categories: [categories]
date: 2017-11-11 11:46:19
---
```



