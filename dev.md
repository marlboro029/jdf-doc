# 开发流程

## 新建工程目录
* 在svn主干上新建分支，名称为testitem，比如svn根目录/product/index/branches/testitem
* 或者直接在主干新建项目文件夹，比如svn根目录/product/index/trunk/
* 或者在某个目录新建项目文件夹，同时配置projectPath

## 初始化工程目录
* 从命令行下进入当前目录
* 执行 jdf install init，生成标准化的项目文件夹

## 项目开发
* 在html，app/js/，app/css/等文件夹中新建相应文件
* 在widget文件夹新建,规划抽离好的widget模块

## 项目本地调试
* jdf build 在浏览器中查看构建后的当前工程，包括less，sass编译，widget编译等
* jdf release 在浏览器中查看release后的工程，包括所有widget中js，css合并后效果

## 项目输出
* jdf output 输出项目文件夹，包括压缩合并后的css，js，images，静态资源加cdn前缀，同时压缩所有png图片
* jdf output -html 输出项目文件夹时包括了html文件夹，供联调使用
* jdf output app/js/test.js，app/css 自定义输出自己需要的文件或文件夹

## 项目联调和发布
* jdf upload 发布至远端机器，供产品，设计师查看效果，以及后端工程师联调
	
## 项目备份
* jdf output -backup 备份app目录至tags文件夹，供和已线上版本对比
