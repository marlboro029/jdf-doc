# ui和unit组件

## 引用方法
* js引用方法

		<script type="text/javascript" src="/app/js/main.js"></script>

* css引用方法

		<script type="text/javascript" src="/app/js/main.js"></script>

* ui和unit组件引用方法

		seajs.use(['jdf/1.0.0/unit/event/1.0.0/event.js'],function(event){ 
			//todo
		})

* 项目内js引用方法

		seajs.use(['/app/a.js','/app/b.js'],function(a,b){ 
			//todo
		})	

* widget引用方法

		{%widget name="header"%}

* widget输出文件名处理,这样每个示例html文件就可以生成自己的widget css和js了,也在config.json里面单独配置
		
		{%widgetOutputName="mywidget"%}

## 公共base引用

	<link rel="stylesheet" type="text/css" href="http://misc.360buyimg.com/lib/skin/2013/base.css" media="all" />
	<script type="text/javascript" src="http://misc.360buyimg.com/jdf/lib/jquery-1.6.4.js"></script>
	<script type="text/javascript" src="http://misc.360buyimg.com/jdf/1.0.0/unit/base/1.0.0/base.js"></script>


## 页面头尾初始化
* 标准头尾
		
		seajs.use('jdf/1.0.0/unit/globalInit/1.0.0/globalInit',function(globalInit){
			globalInit();
		});

* 非标准头尾

	* 需要单独配置

## 本地调试
* 在页面后面增加?isdebug那么页面中所有js文件就不会combo合并
* 使用jdf工具,则可以不压缩静态文件直接上传至测试服务器,中间仅增加了路径引用

		jdf upload -debug 


## 最佳实践
项目核心js顶部首先配置alias,如下

	seajs.config({
		alias:{
			'globalInit':'jdf/1.0.0/unit/globalInit/1.0.0/globalInit',
			'event':'jdf/1.0.0/unit/event/1.0.0/event.js'
		}
	})

项目页面引用时直接用alias来代替

	seajs.use('jdf/1.0.0/unit/globalInit/1.0.0/globalInit',function(globalInit){
		globalInit();
	});
	seajs.use('event',function(event){})

这样做的目的:

* 方便对所用到了的组件统一管理
* 后续升级只要修改一处即可


