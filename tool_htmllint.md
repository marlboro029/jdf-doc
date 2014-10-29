#htmllint

##使用说明

* 方法1：在当前文件夹下，使用 `jdf htmllint` 可直接检查当前文件夹下的所有html文件
* 方法2：在当前文件夹下，使用 `jdf htmllint xxx.html` 可检查当前文件夹下的xxx.html
* 方法3：可直接使用 `jdf htmllint http://www.jd.com` 检查在线页面（注意：url前必须加上http）

##检测说明

htmllint可以快速检测html代码的书写错误，比如 `test.html` 的内容如下：

    <div id="box"></div>
    <div id="box"></div>
    
    <input type=text>

运行 `jdf htmllint test.html` 命令之后，会看到以下提示信息：

    jdf htmllint:  test/test.html
    #1
    >> line: 9, column: 2
    >> msg: the id "box" is already in use
    #2
    >> line: 10, column: 2
    >> msg: the "type" attribute is not double quoted

很明显，在此hmtl文件中存在两个问题：

* 问题1：页面中有两个元素使用了重复的id
* 问题2：`input` 元素的 `type` 属性值没有加双引号
