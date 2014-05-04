# jdf doc

## 关于jdf

* jdf为前端开发集成解决方案:
* 目的是合理，快速和高效的解决前端开发中的工程和项目问题；
* 核心提供了前端开发必备的基础的UI和业务组件，并集成调试，构建，布署，代码生成，文档生成，编辑器插件等一系列开发工具；
* 同时提供了前端模块的安装，下载，发布，提交，预览．

## 功能介绍

* 跨平台:完美支持windows、mac、linux等系统
* 项目配置:支持为项目创建一个配置文件，按选项统一编译
* 错误提示:在编译过程中如果遇到语法的错误，在控制台可以输出错误信息，方便定位代码错误位置
* 支持volicity模板编译，可供前后端共享模板
* 支持本地，联调，线上三种开发流程
* 支持公共widget的引用，预览，安装和发布
* 可生成标准化的项目文件夹
* 支持给所有静态资源添加CDN域名前缀或后缀戳
* 支持css引用的所有链接生成combo格式
* 支持文件夹或者单独文件css和js文件压缩
* 支持less，sass实时监听文件，当文件改变时自动执行编译成css
* 支持cmd模块自动提取文件id和dependencies，压缩时保留require关键字
* 支持备份当前工程文件
* 内置png图片压缩插件，支持将png24压缩为png8
* 内置本地开发调试服务器，支持html和静态文件预览，以及当前目录浏览
* 支持文件监听，保存后文件即可在浏览器即时预览
* 支持上传到远端服务器，利用文件监听，即实现本地文件保存后可上传至远端服务器
* 编码统一化，即无论当前文件格式是gbk，gb2312，utf8，utf8-bom，统一输出utf8
* 多条命令，可满足不同的开发需求

## 安装使用

* jdf基于nodejs
	* [nodejs安装](http://nodejs.org/download/)
	* node版本需要 >=0.8.0
* 安装jdf
	* npm install jdf **-g** --save-dev
* 安装测试
	* 执行 jdf -v 如果出现版本号则说明你已安装成功
* 更新jdf
	* npm update jdf **-g**

## 示例演示
* [示例安装](demo.md#示例安装)
* [示例演示](demo.md#示例演示)

## 开发流程
* [新建工程目录](dev.md#新建工程目录)
* [项目开发](dev.md#项目开发)
* [项目本地调试](dev.md#项目本地调试)
* [项目输出](dev.md#项目输出)
* [项目联调和发布](dev.md#项目联调和发布)
* [项目备份](dev.md#项目备份)
* [工作流程对比](compare.md)

## 方案规范
* [项目目录规范](dir.md#项目目录规范)
	* 项目目录
	* 输出目录
	* 上线目录
* [ui和unit组件目录规范](dir.md#ui和unit组件目录规范)
	* ui和unit目录
* [widget目录规范](dir.md#widget目录规范)
	* widget目录
	* widget目录细化	


## widget组件
*  [生态圈](widget.md#生态圈)
*  [widget定义](widget.md#widget定义)
*  [组成形式](widget.md#组成形式)
*  [引用方法](widget.md#引用方法)
*  [开发目录](widget.md#开发目录)
*  [页面输出](widget.md#页面输出)
*  [编译输出](widget.md#编译输出)
*  [相关命令](widget.md#相关命令)

## js组件
* [组件类型](js.md#组件类型)
* [组件写法](js.md#组件写法)
* [引用方法](js.md#引用方法)
* [公共base引用](js.md#公共base引用)
* [页面头尾初始化](js.md#页面头尾初始化)
* [本地调试](js.md#本地调试)
* [最佳实践](js.md#最佳实践)
* [依赖管理方案](depend.md)

##vm模板
* [设计原则](vm.md#设计原则)
* [velocity模板引挚](vm.md#velocity模板引挚)
* [目录结构](vm.md#目录结构)
* [引用方法](vm.md#引用方法)
* [velocity基本语法](vm.md#velocity基本语法)
* [velocity语法详解](vm.md#velocity语法详解)
* [数据源举例](vm.md#数据源举例)

##集成工具使用
* [LiveReload](https://github.com/putaoshu/jdf-doc/blob/master/livereload.md)

## 配置API
* [配置API](config.md)

## 命令手册
* [命令手册](api.md)

## 编译器插件
* [Sublime Text2 插件](https://sublime.wbond.net/packages/Jdf%20-%20Tool)
