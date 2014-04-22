#基本语法

// ---------- 1、"#"用来标识Velocity的脚本语句，包括#set、#if 、#else、#end、#foreach、#end、#iinclude、#parse、#macro等，如:

		#if($info.images)
		<img src="$info.images">
		#else
		<img src="noPhoto.jpg">
		#end

// ---------- 2、"$"用来标识一个变量，如

		$i、$msg.errorNum

// ---------- 3、"!"用来强制把不存在的变量显示为空白

		$!msg

// ---------- 4、注释，如：

		## 这是一行注释，不会输出

#语法详解

具体更详细的语法可参考[官网] (http://velocity.apache.org/engine/devel/user-guide.html)



// ---------- 1.变量赋值输出------------
	
		Welcome $name to Javayou.com!
		today is $date.
		tdday is $mydae.//未被定义的变量将当成字符串

// -----------2.设置变量值,所有变量都以$开头----------------

		#set( $iAmVariable = "good!" )
		Welcome $name to Javayou.com!
		today is $date.
		$iAmVariable

//-------------3.if,else判断--------------------------

		#set ($admin = "admin")
		#set ($user = "user")
		#if ($admin == $user)
		Welcome admin!
		#else
		Welcome user!
		#end

//--------------4.迭代数据List ($velocityCount为列举序号，默认从1开始) -----------

		#foreach( $product in $allProducts )
			<li>$velocityCount $product $product.title</li>
		#end

// ------------5.迭代数据get key-----------------

		#foreach($key in $myProducts.keySet() )  
			$key `s value: $myProducts.get($key)
		#end

//-----------6.导入其它文件,可输入多个-----------

		#parse("vm_a.tpl")
		#parse("vm_b.tpl")

//-----------[todo多个文件用逗号隔开]--------------
