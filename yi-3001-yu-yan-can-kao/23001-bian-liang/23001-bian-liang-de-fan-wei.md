## 变量的范围

---

### 局部变量

变量的作用范围在上下文中，大部分的 PHP 变量只有一个单独的范围。这个单独的范围跨度同样包含了 include 和 require 引入的文件。例如：

```
<?php
$a = 1;
include 'b.inc';
?>
-------------------------------------------------------

<?php
$a = 1; /* global scope */

function Test()
{
    echo $a; /* reference to local scope variable */
}

Test();
?>
```

这个脚本不会有任何输出，因为 echo 语句引用了一个局部版本的变量$a，而且在这个范围内，它并没有被赋值。你可能注意到 PHP 的全局变量和 C 语言有一点点不同，在 C 语言中，全局变量在函数中自动生效，除非被局部变量覆盖。这可能引起一些问题，有些人可能不小心就改变了一个全局变量。PHP 中全局变量在函数中使用时必须声明为 global。

### 全局变量

global 全局关键字，也可以使用$GLOBALES;

```
<?php

$a  = 1;
$b = 2;

function Sum() {
    global $a , $b;
    $b = $a + $b;
}
Sum();
echo $b; #结果3

#另外一种
$a = 1;
$b = 2;

function Sum() {
    $GLOBALS['b'] = $GLOBALS['a'] + $GLOBALS['b'];
}
Sum();
echo $b;
```



