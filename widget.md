# widget组件

## 生态圈

* 核心: 如果每人每天贡献出一个模块，如果每个项目贡献出一个模块，日积月累，那么开发时，只需要引入对应模块并在此基础上稍微修正，就可以以非常快的速度开发出一个复杂布局，多栏，多屏的页面.

* 生态循环
	* 依赖: jdf
	* 单一提交流程
		* 可复用widget提交 ==> 审核 ==> 接入公共库 

	* 引用提交循环流程
		* 开发项目 ==> 查看公共库是否有可用widget ==> 引用(仅一行代码) ==> 编入自己的工程 ==> 复用 ==>修正为新的widget ==> 可复用widget提交 ==> 审核 ==> 接入公共库

## widget定义
* widget模块是可复用并且能独立提供功能的页面片段，可以在单个项目里面使用，也可以发布贡献出来供其它项目使用

## 组成形式
* 可复用的vm/tpl片断
* 可复用的js片断
* 可复用的css片断

## 引用方法
* 在页面中统一引入

		{%widget name="test"%}

此时当前widget文件夹下的vm,tpl编译到页面上,js和css也加载至页面上


* 在页面中单独引入widget的vm文件

		{%widget name="test" type="vm"%}

* 在页面中单独引入widget的tpl文件

		{%widget name="test" type="vm"%}

* 在页面中单独引入widget的js文件

		{%widget name="test" type="js"%}

* 在页面中单独引入widget的css文件

		{%widget name="test" type="css"%}		

* widget输出文件名配置
	* 在引入页面增加widgetOutputName
	
			{%widgetOutputName="mywidget"%}

	* 或在config.json里面配置统一的配置项

			 widgetOutputName: widgetoutput

* widget引入时注释配置
	* 在页面中引入，不带文件路径注释

			{%widget name="test" comment="false"%}

	* 或在config.json里面配置统一的配置项 

			build: {
				widgetIncludeComment:true //默认为true，不带可以设置成false
			}


## 开发目录

	widget //组件目录，包括模板组件，js组件，css组件
	  └── test
			├── test.vm //模板文件
			├── test.css //css文件
			├── i/ //等待上线的图片文件夹
			├── images/ //素材图片文件夹
			└── test.js //js文件
	
## 页面输出

	<!-- js，css -->
	<link type="text/css" rel="stylesheet"  href="/widget/test/test.css" source="widget"/>
	<script type="text/javascript" src="/widget/test/test.js" source="widget"/></script>

	<!-- tpl -->
	<div class="test">this is test</div>

## 编译输出
* 所有widget模块中css文件合并为widget.css
* 所有widget模块中js文件合并为widget.js
* 所有widget模块中images文件输出对应目录

## 相关命令

* widget -all  	preview all widget //预览所有项目中所有widget
* widget -preview xxx 	preview a widget //预览一个widget模块
* widget -install xxx 	install a widget to local //安装一个widget模块到当前工程
* widget -publish xxx 	publish a widget to server //发布一个widget模块到服务端
* widget -create xxx 	create a widget to local //在本地项目新建一个widget,会生成widget文件夹和vm,css,js,json文件
* widget -list  	get widget list from server //取得服务端所有widget列表

