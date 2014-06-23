# 配置文档

* config.json需要放在项目根目录下, 可配置项如下：

		{
			"cdn":"http://www.cdn.com", 
			"jsPlace":"bottom",
	
			"cssDir" : "css",
			"imagesDir" : "css/i",
			"jsDir" : "js",
			
			"htmlDir" : "html",
			"widgetDir" : "widget",
	
			"buildDirName" : "html",
			"outputDirName:" : "build",
			"outputCustom:" : "a/,b/",
			"widgetOutputName": "widget",
			
			"projectPath" : "product/index/",
			"host" : "192.168.1.1",
			"serverDir" : "cdndir",
			"localServerPort" : "3000",
			"previewServerDir": "preview.com",
			
			"build":{
				"jsPlace": "insertHead", 
				"livereload":true, 
				"widgetIncludeComment":true, 
				"sass":true,
				"lass":true
			},
			"output":{
				"vm":true, 
				"compressJs":true,
				"compressCss:true,
				"compressPng":true
			},
			widget:{
				js:[
					'http://misc.360buyimg.com/jdf/lib/jquery-1.6.4.js',
					'http://misc.360buyimg.com/jdf/1.0.0/unit/base/1.0.0/base.js'
				],
				css:[
					'http://misc.360buyimg.com/lib/skin/2013/base.css'
				]
			}
		}
	
* 具体举例说明如下:

		cdn:'http://www.cdn.com', //静态cdn域名
		jsPlace:"bottom", //编译后js文件位置,位于header或者页面底部
	
		cssDir : 'css', //css文件夹名称
		imagesDir : 'css/i', //images文件夹名称
		jsDir: 'js', //js文件夹名称
		htmlDir: 'html', //html文件夹名称
		widgetDir: 'widget', //widget文件夹名称
	
		buildDirName:'html', //编译的文件夹名称
		outputDirName:'build', //输出文件夹名称
		outputCustom:'a/,b/', //自定义输出文件夹
		widgetOutputName: "widget", //输出的widget文件夹名称
		
		projectPath: 'product/index/', //工程目录前缀
		host:"192.168.1.1", //远端机器IP
		serverDir: 'cdndir', //上传至远端服务器文件夹名称
		localServerPort: 3000 //本地服务器端口

		previewServerDir: "preview.com", //html文件夹上传至服务器所在的文件夹名称

		build:{
			jsPlace: "insertHead", //调试时js文件位置 insertHead|insertBody
			livereload:true, //是否开启liveload
			widgetIncludeComment:true, //引用widget时是否带上文件路径注释
			sass:true,//是否开启sass编译
			lass:true//是否开启lass编译
		},

		output:{
			vm:true, //是否开启vm编译
			compressJs:true,//是否开启压缩js文件
			compressCss:true,//是否开启压缩css文件
			compressPng:true//是否开启压缩png图片
		},

		widget:{
			//widget预览所依赖的js
			js:[
				'http://misc.360buyimg.com/jdf/lib/jquery-1.6.4.js',
				'http://misc.360buyimg.com/jdf/1.0.0/unit/base/1.0.0/base.js'
			],
			//widget预览所依赖的css
			css:[
				'http://misc.360buyimg.com/lib/skin/2013/base.css'
			]
		}