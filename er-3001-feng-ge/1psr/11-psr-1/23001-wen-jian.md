## 文件

2.1 PHP标签

PHP 代码必须使用&lt;?php ?&gt; 长标签或&lt;?= ?&gt;段标签；**一定不可** 使用其它自定义标签。

2.2 字符编码

PHP代码 **必须** 且只可以使用 **不带BOM的UTF-8 **编码。

2.3 副作用

一个源文件中 **应该 只用来做声明（类 class 、函数 function、常量 constant 等）或者只用来做一些引起副作用的操作（例如：输出信息，修改.ini等 ）不建议两者同时存在。**

**副作用包含却不仅限于**：

* 生成输出 echo print\__r var\_dump\(\);_
* 直接使用 require 或 include
* 连接外部服务
* 修改ini配置
* 抛出错误或异常
* 修改全局或静态变量
* 读或写文件

需要避免的例子：

```
<?php
// 副作用：修改了ini配置
ini_set('error_reporting', E_ALL);

// 副作用：载入了文件
include "file.php";

// 副作用：产生了输出
echo "<html>\n";

// 声明
function foo()
{
    // 函数体
}

```

提倡的例子：

```
<?php
// 声明函数
function foo()
{
    // 函数主体部分
}

// 条件声明 **不** 属于「副作用」
if (! function_exists('bar')) {
    function bar()
    {
        // 函数主体部分
    }
}
```



