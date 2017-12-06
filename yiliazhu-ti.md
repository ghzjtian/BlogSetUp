#yilia主题

>GitHub: https://github.com/litten/hexo-theme-yilia

###* 1.git clone 主题.
###* 2.把主题放到 themes 下面.
###* 3.在 ```_config.yml``` 中把
```
#theme: landscape
theme: hexo-theme-yilia
```


###*[4.点击所有文章，但没显示,需要设置](#error_all_article)
###*[5.Zhen的_config.yml配置。](#theme_config)
###*6.在需要截断的地方，添加以下代码
```
<!-- more -->
```


***
***
***

###*4.点击所有文章，但没显示,需要设置<a name="error_all_article"/>
缺失模块。

* 1、请确保node版本大于6.2
* 2、在博客根目录（注意不是yilia根目录）执行以下命令：

```
npm i hexo-generator-json-content --save
```

3、在根目录_config.yml里添加配置：

```
  jsonContent:
    meta: false
    pages: false
    posts:
      title: true
      date: true
      path: true
      text: false
      raw: false
      content: false
      slug: false
      updated: false
      comments: false
      link: false
      permalink: false
      excerpt: false
      categories: false
      tags: true
```
***

###*5.Zhen的_config.yml配置。<a name="theme_config"/>

```
# Header

menu:
  主页: /

# SubNav
subnav:
#qq: "479375578"

rss: /atom.xml

# 是否需要修改 root 路径
# 如果您的网站存放在子目录中，例如 http://yoursite.com/blog，
# 请将您的 url 设为 http://yoursite.com/blog 并把 root 设为 /blog/。
root: 

# Content

# 文章太长，截断按钮文字
excerpt_link: more
# 文章卡片右下角常驻链接，不需要请设置为false
show_all_link: '展开全文'
# 数学公式
mathjax: false
# 是否在新窗口打开链接
open_in_new: false

# 打赏
# 打赏type设定：0-关闭打赏； 1-文章对应的md文件里有reward:true属性，才有打赏； 2-所有文章均有打赏
reward_type: 2
# 打赏wording
reward_wording: '谢谢你的奖赏，么么哒,我不会骄傲的。'
# 支付宝二维码图片地址，跟你设置头像的方式一样。比如：/assets/img/alipay.jpg
alipay: /assets/imgs/alipay.png
# 微信二维码图片地址
weixin: /assets/imgs/wechat.png

# 目录
# 目录设定：0-不显示目录； 1-文章对应的md文件里有toc:true属性，才有目录； 2-所有文章均显示目录
toc: 1
# 根据自己的习惯来设置，如果你的目录标题习惯有标号，置为true即可隐藏hexo重复的序号；否则置为false
toc_hide_index: true
# 目录为空时的提示
toc_empty_wording: '目录，不存在的…'

# 是否有快速回到顶部的按钮
top: true

# Miscellaneous
baidu_analytics: ''
google_analytics: ''
favicon: /favicon.png

#你的头像url
avatar: /assets/imgs/zhen.jpg

#是否开启分享
share_jia: true

#评论：1、多说；2、网易云跟帖；3、畅言；4、Disqus；5、Gitment
#不需要使用某项，直接设置值为false，或注释掉
#具体请参考wiki：https://github.com/litten/hexo-theme-yilia/wiki/

#1、多说
duoshuo: false

#2、网易云跟帖
wangyiyun: false

#3、畅言
changyan_appid: false
changyan_conf: false

#4、Disqus 在hexo根目录的config里也有disqus_shortname字段，优先使用yilia的
disqus: false

#5、Gitment
gitment_owner: false      #你的 GitHub ID
gitment_repo: ''          #存储评论的 repo
gitment_oauth:
  client_id: ''           #client ID
  client_secret: ''       #client secret

# 样式定制 - 一般不需要修改，除非有很强的定制欲望…
style:
  # 头像上面的背景颜色
  header: '#f08078'
  # 右滑板块背景
  slider: 'linear-gradient(200deg,#a0cfe4,#f08078)'

# slider的设置
slider:
  # 是否默认展开tags板块
  showTags: false

# 智能菜单
# 如不需要，将该对应项置为false
# 比如
#smart_menu:
#  friends: false
smart_menu:
  innerArchive: '所有文章'
  friends: '友链'
  aboutme: '关于我'

friends:
  友情链接:

aboutme: 毕业于华师，工作于广州<br><br>温柔可爱的<br>小女子一枚


```


