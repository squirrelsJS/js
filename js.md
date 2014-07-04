#技术架构

整理一下现在使用的开发环境和配置说明。
目前项目中有若干小项目，开发时间各不同，所以整理的配置都不太一样。

用到的插件和工具在后面会全部列出来，也可以点击这里直接跳转。


前期项目设计时，就打算将后端全部以接口的形式封装，供client通过ajax调用，所以将view视图层单独分离出来交给JS处理。这样导致相当一部分业务逻辑需要JS进行处理，工作量较大，所以需要使用了MVC模式，将JS代码拆分为model层（和php后端对接，本地缓存部分数据，部分业务逻辑处理），control层（处理dom），view层（模版，处理页面）。

##第一阶段：
###前端
一套自己开发的JS框架，使用了MVC模式，外加一些插件，包括jQuery、keyboardJS、iScroll、jSmart模版引擎等。
###后端
自己开发的php框架，包含model层和control层。
###数据库
MySQL

这个配置使用一段时间以后，自己开发的JS框架扩展性还是不太够，需求经常变动的情况下，修改非常痛苦。了解了一下主流的JS MVC框架后，决定换angularJS。

##第二阶段
###前端
angularJS，辅助以jQuery。其中基本上很少使用到jQuery。
###后端
PHP+MySQL

angularJS的优势在于可以实现双向数据绑定，同时配合指令的使用，基本上可以不用操作DOM，只需要处理业务逻辑即可。
但其实，理想化的情况和现实是比较遥远的。初次使用angularJS，有很多问题需要处理：

* 需要将原有的开发习惯，转换为指令的形式。有些需求在第一阶段非常容易实现，例如设置input元素的focus状态，但要使用angularJS的方式来解决问题就很麻烦。
* 性能问题。

这些问题只能依靠时间来逐步解决，之后有时间会单独总结一些经验发到这里。

##第三阶段
基本配置和之前一样，加入了bootstrap3.x以减轻页面设计的压力。编码方面，使用了coffeescript和less以提高效率。

##之后……
下一阶段打算将mysql数据库替换为mongoDB，后台将php替换为nodeJS，整个项目全部使用JS实现。
目前在尝试meteor+angularJS的组合，以后有时间再单独整理。


##工具和插件

### 百度前端集成解决方案fis
地址：https://github.com/fex-team/fis/wiki
用于打包合并JS、css，处理文件目录问题，打包代码到发布目录，实时检测代码变化并自动刷新浏览器。

### 键盘热键插件keyboardJS
地址：https://github.com/RobertWHurst/KeyboardJS

### 滚动插件iScroll
地址：http://cubiq.org

### 统计图表插件flotr2
地址：http://www.humblesoftware.com/flotr2/index

### angularJS
地址：http://www.angularjs.org

