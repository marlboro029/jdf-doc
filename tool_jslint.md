#jslint

##使用说明

* 方法1：在当前文件夹下，使用 `jdf jslint` 可直接检查当前文件夹下的所有js文件
* 方法2：在当前文件夹下，使用 `jdf jslint xxx.js` 可检查当前文件夹下的xxx.js

##检测说明

jslint可快速检测js代码的书写错误，比如 `test.js` 的内容如下：

    function test() {
      var a = 1
    }

运行 `jdf jslint test.js` 命令之后，会看到以下提示信息：

    #1
    >> line: 4, column: 12
    >> msg: Expected ";" and instead saw "}".
    >> at:   var a = 1
    #2
    >> line: 4, column: 7
    >> msg: Unused "a".
    >> at:   var a = 1
很明显，在此js文件中有两个问题：

* 问题1：在代码 `var a = 1` 结尾处没有加分号
* 问题2：a变量只是被定义了，却没有被使用