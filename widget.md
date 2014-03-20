# widget

## widget命令使用介绍

* widget -preview name 预览一个widget模块
* widget -install name 安装一个widget模块到当前工程
* widget -publish name 发布一个widget模块

## widget模块依赖介绍

* widget模块是为了解决开发多个页面中有相同html结构，一页多屏html代码上等等问题。
* 引入类型：html，css，images
* 引入方式

		{%widget name="test"%}
    
* 开发目录

		widget/
	        widget/test/
	        widget/test/test.html
	        widget/test/test.css
	        widget/test/test.js
	        widget/test/test.png

* 本地测试输出

		<!-- js,css -->
		<link type="text/css" rel="stylesheet"  href="/widget/tes/tes.css" source="widget"/>
		<script type="text/javascript" src="/widget/tes/tes.js" source="widget"/></script>

		<!-- tpl -->
		<div class="test">this is test</div>

* 编译输出
	* 所有widget模块中css文件合并为widget.css
	* 所有widget模块中js文件合并为widget.js
	* 所有widget模块中images文件输出对应至目录