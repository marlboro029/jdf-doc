#csslint

##使用说明
* 方法1：默认csslint功能是关闭状态，可以通过config.json的{{build.csslint}}键值设置为true进行开启，这样在 `jdf build` 下会自动检测
* 方法2：在当前文件夹下，使用 `jdf csslint` 可直接检查当前文件夹下的所有css文件
* 方法3：在当前文件夹下，使用 `jdf csslint xxx.css` 可检查当前文件夹下的xxx.css

##检测说明
csslint可以快速检测css的书写错误，比如 `btn.css` 内容如下：
	
	.btn{
		colo: #fff
		border:1px solid red;
	}

很明显 `.btn` 样式存在两个问题

* 问题1： `colo` 属性是不存在的，可能应该为 `color`
* 问题2： `colo: #fff` 后和 `border:1px solid red;` 前少了一个分号 `;`

此时jdf命令行下会有如下提示，方便查找问题所在

	jdf csslint: There are 2 problems in lib/csslint.css

	#1 warning at line 2, col 2
	Unknown property 'colo'.
		colo: #fff

	#2 error at line 3, col 8
	Expected RBRACE at line 3, col 8.
		border:1px solid red;

注意：less/scss文件需要编译成css后才能检测，否则提示会不准确。

##原理浅析

csslint可用于检查CSS取值和潜在问题，使用了Nicholas大神的npm模块parser-lib作为css解析器，并按照parser-lib给出的API来编写检查规则。
csslint的每一个规则都是通过监听parser-lib给出的事件来进行相应的判断：

* startrule为规则开始
* property为找到一个属性时的事件 
* endrule为一个规则结束

一旦规则结束并且没有统计到任何property，则说明规则为空。
