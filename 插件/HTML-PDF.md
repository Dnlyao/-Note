 ## 安装到centos phatomJS报错
 
 node 根据html生成PDF文件
 
报错内容
`
"html-pdf: Failed to load PhantomJS module. You have to set the path to the PhantomJS binary using \'options.phantomPath
`

解决方法

在服务器上全局安装 phantomJS
phantomjs --version -> O/p 2.1.1

进入项目的node-module，找到html-pdf
html-pdf -> lib -> pdf.js
在`"this.options = options || {}"`之后加上 服务器的phantomjs安装路径
`
this.options.phantomPath = "/usr/local/bin/phantomjs"
`
