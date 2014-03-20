# 方案规范

## 目录规范
* 项目文件夹

		├──jdf_demo
		|	└──index   
		|		  └── branches 
		|		  	   └── jdf_demo_2014
		|		  	   		├── app //静态文件目录
		|					|	├── css //css文件夹
		|					|	|	└── i //图片文件夹
		|					|	└── js //js文件文件夹
		|		  	   		├── html //预览页面html
		|		  	   		├── img //预览页面中示例图片
		|		  	   		├── widget //模块化目录,包括模板组件,js组件,css组件
		|					|	└── header
		|					|		├── header.tpl //模板文件
		|					|		├── header.source //tpl的数据源文件		
		|					|		├── header.css //css文件
		|					|		├── header.js //js文件
		|					|		└── header.png //图片文件
		|		  	   		└── config.json //配置文件

* 输出文件夹

		├──jdf_demo
		|	└──index   
		|		├── css //css文件目录
		|		├── html //预览页面html
		|		├── js //js文件目录
		|		└── widget //模块化目录

* 上线文件夹

		├──jdf_demo
		|	└──index   
		|		├── css //css文件目录
		|		└── widget //模块化目录		

注意: 

* jdf_demo/index/branches/app仅作为项目文件夹路径,项目编译输出时会把branches/app忽略掉,直接取jdf_demo/index做静态资源文件前缀
* 如果你在config.json中配置了 "projectPath" 即工程目录前缀,那么会直接取projectPath的值


## widget规范
* widget文件夹
* widget安装
* widget预览
* widget发布

## 版本规范
* UI和Unit组件规范

		├──	jdf
		|	└──1.0.0
		|		├── build //编译输出文件目录
		|		├── html //预览页面html
		|		├── ui //ui组件化目录
		|		|	├── dialog //dialog组件
		|		|	|	└── 1.0.0
		|		|	|		├── dialog.css
		|		|	|		├── dialog.png
		|		|	|		└── dialog.js
		|		|	└── switchable //switchable组件
		|		|		└── 1.0.0
		|		|			├── switchable.css
		|		|			└── switchable.js
		|		├── unit //ui组件化目录
		|		|	├── login //登陆注册组件
		|		|	|	└── 1.0.0
		|		|	|		└── login.js
		|		|	└── search //搜索组件
		|		|		└── 1.0.0
		|		|			└── search.js		
		|		└── config.json //配置文件
