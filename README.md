需要保留的文件需要放在source目录下

_config.yml
根目录下，主要包含 Hexo 本身的配置
主题目录下，这份配置由主题作者提供，主要用于配置主题相关的选项

需要特别注意的地方是，冒号后面必须有一个空格，否则可能会出问题
Hexo 本身的配置
# Hexo Configuration
## Docs: https://hexo.io/docs/configuration.html
## Source: https://github.com/hexojs/hexo/

# Site 网站
title: 嘟嘟独立博客		#网站标题
subtitle: 爱生活爱编码		#网站副标题
description: hello,every body!~	#网站描述
author: Tengj Jun		#您的名字
language: zh-CN			#网站使用的语言
timezone:			#网站时区。Hexo 默认使用您电脑的时区

# URL 网址
## 如果您的网站存放在子目录中，例如 http://yoursite.com/blog，则请将您的 url 设为 http://yoursite.com/blog 并把 root 设为 /blog/。
url: http://tengj.github.io
root: /
permalink: :year/:month/:day/:title/
permalink_defaults:

# Directory 目录配置
source_dir: source	 #源文件夹，这个文件夹用来存放内容。
public_dir: public	 #公共文件夹，这个文件夹用于存放生成的站点文件。
tag_dir: tags		 #标签文件夹
archive_dir: archives	 #归档文件夹
category_dir: categories #分类文件夹
code_dir: downloads/code #nclude code 文件夹
i18n_dir: :lang		 #国际化（i18n）文件夹
skip_render:		 #跳过指定文件的渲染，您可使用 glob 表达式来匹配路径。

# Writing 文章
new_post_name: :title.md # 新建文章默认文件名
default_layout: post     # 默认布局
titlecase: false # Transform title into titlecase
external_link: true # 在新标签中打开一个外部链接，默认为true
filename_case: 0    #转换文件名，1代表小写；2代表大写；默认为0，意思就是创建文章的时候，是否自动帮你转换文件名，默认就行，意义不大。
render_drafts: false  #是否渲染_drafts目录下的文章，默认为false
post_asset_folder: false #启动 Asset 文件夹
relative_link: false	#把链接改为与根目录的相对位址，默认false
future: true		#显示未来的文章，默认false
highlight:	#代码块的设置
  enable: true
  line_number: true
  auto_detect: false
  tab_replace:

# Category & Tag 分类和标签的设置
default_category: uncategorized		#默认分类
category_map:				#分类别名
tag_map:				#标签别名

# Date / Time format
## Hexo uses Moment.js to parse and display date
## You can customize the date format as defined in
## http://momentjs.com/docs/#/displaying/format/
date_format: YYYY-MM-DD
time_format: HH:mm:ss

# Pagination 分页
## Set per_page to 0 to disable pagination
per_page: 10	#每页显示的文章量 (0 = 关闭分页功能)
pagination_dir: page	#分页目录

# Extensions
## Plugins: https://hexo.io/plugins/
## Themes: https://hexo.io/themes/
theme: jacman

# Deployment
## Docs: https://hexo.io/docs/deployment.html
deploy:
  type: git
  repository: https://github.com/tengj/tengj.github.com.git
  branch: master
  
  



主题配置

##### Menu
menu:
  首页: /
  归档: /archives
  标签: /tags
  分类: /categories
## you can create `tags` and `categories` folders in `../source`.
## And create a `index.md` file in each of them.
## set `front-matter`as
## layout: tags (or categories)
## title: tags (or categories)
## ---

#### Widgets
widgets: 
- github-card
- category
- tag
- archive
- tagcloud
- rss
  ## provide eight widgets:github-card,category,tag,rss,archive,tagcloud,links,weibo



#### RSS 
rss: /atom.xml ## RSS address.

#### Image
imglogo:
  enable: true             ## display image logo true/false.
  src: img/logo.png        ## `.svg` and `.png` are recommended,please put image into the theme folder `/jacman/source/img`.
favicon: img/favicon.ico   ## size:32px*32px,`.ico` is recommended,please put image into the theme folder `/jacman/source/img`.     
apple_icon: img/jacman.jpg ## size:114px*114px,please put image into the theme folder `/jacman/source/img`.
author_img: img/author.jpg ## size:220px*220px.display author avatar picture.if don't want to display,please don't set this.
banner_img: #img/banner.jpg ## size:1920px*200px+. Banner Picture
### Theme Color 
theme_color:
    theme: '#2ca6cb'    ##the defaut theme color is blue

# 代码高亮主题
# available: default | night
highlight_theme: default

#### index post is expanding or not 
index:
  expand: true           ## default is unexpanding,so you can only see the short description of each post.
  excerpt_link: Read More  

close_aside: false  #close sidebar in post page if true
mathjax: false      #enable mathjax if true

### Creative Commons License Support, see http://creativecommons.org/ 
### you can choose: by , by-nc , by-nc-nd , by-nc-sa , by-nd , by-sa , zero
creative_commons: none

#### Author information
author:
  intro_line1:  "程序员上辈子都是折翼的天使"    ## your introduction on the bottom of the page
  intro_line2:  "This is my blog,Try to do better."  ## the 2nd line
  weibo:      ## e.g. wuchong1014 or 2176287895 for http://weibo.com/2176287895
  weibo_verifier: b3593ceb    ## e.g. b3593ceb Your weibo-show widget verifier ,if you use weibo-show it is needed.
  tsina:      ## e.g. 2176287895  Your weibo ID,It will be used in share button.
  douban:     ## e.g. wuchong1014 or your id for https://www.douban.com/people/wuchong1014
  zhihu:      ## e.g. jark  for http://www.zhihu.com/people/jark
  email:      ## e.g. imjark@gmail.com
  twitter:    ## e.g. jarkwu for https://twitter.com/jarkwu
  github: tengj    ## e.g. wuchong for https://github.com/wuchong
  facebook:   ## e.g. imjark for https://facebook.com/imjark
  linkedin:   ## e.g. wuchong1014 for https://www.linkedin.com/in/wuchong1014
  google_plus:    ## e.g. "111190881341800841449" for https://plus.google.com/u/0/111190881341800841449, the "" is needed!
  stackoverflow:  ## e.g. 3222790 for http://stackoverflow.com/users/3222790/jark
## if you set them, the corresponding  share button will show on the footer

#### Toc
toc:
  article: true   ## show contents in article.
  aside: true     ## show contents in aside.
## you can set both of the value to true of neither of them.
## if you don't want display contents in a specified post,you can modify `front-matter` and add `toc: false`.

#### Links
links:
#### Comment
duoshuo_shortname: 嘟嘟MD   ## e.g. wuchong   your duoshuo short name.
disqus_shortname:    ## e.g. wuchong   your disqus short name.

#### Share button
jiathis:
  enable: false ## if you use jiathis as your share tool,the built-in share tool won't be display.
  id:    ## e.g. 1889330 your jiathis ID. 
  tsina: ## e.g. 2176287895 Your weibo id,It will be used in share button.

#### Analytics
google_analytics:
  enable: false
  id:        ## e.g. UA-46321946-2 your google analytics ID.
  site:      ## e.g. wuchong.me your google analytics site or set the value as auto.
## You MUST upgrade to Universal Analytics first!
## https://developers.google.com/analytics/devguides/collection/upgrade/?hl=zh_CN
baidu_tongji:
  enable: true
  sitecode: e6d1f421bbc9962127a50488f9ed37d1 ## e.g. e6d1f421bbc9962127a50488f9ed37d1 your baidu tongji site code
cnzz_tongji:
  enable: false
  siteid:    ## e.g. 1253575964 your cnzz tongji site id

#### Miscellaneous
ShowCustomFont: true  ## you can change custom font in `variable.styl` and `font.styl` which in the theme folder `/jacman/source/css`.
fancybox: true        ## if you use gallery post or want use fancybox please set the value to true.
totop: true           ## if you want to scroll to top in every post set the value to true


#### Custom Search
google_cse: 
  enable: false
  cx:   ## e.g. 018294693190868310296:abnhpuysycw your Custom Search ID.
## https://www.google.com/cse/ 
## To enable the custom search You must create a "search" folder in '/source' and a "index.md" file
## set the 'front-matter' as
## layout: search 
## title: search
## ---
baidu_search:     ## http://zn.baidu.com/
  enable: false
  id:   ## e.g. "783281470518440642"  for your baidu search id
  site: http://zhannei.baidu.com/cse/search  ## your can change to your site instead of the default site
  
tinysou_search:     ## http://tinysou.com/
  enable: false
  id:  ## e.g. "4ac092ad8d749fdc6293" for your tiny search id