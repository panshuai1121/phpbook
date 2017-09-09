## 整型

是集合 ℤ = {..., -2, -1, 0, 1, 2, ...} 中的某个数。

整型值可以使用十进制，十六进制，八进制或二进制表示，前面可以加上可选的符号（- 或者 +）。

```
<?php
$a = 1234; // 十进制数
$a = -123; // 负数
$a = 0123; // 八进制数 (等于十进制 83)
$a = 0x1A; // 十六进制数 (等于十进制 26)
$a = 0b11111111; // 二进制数字 (等于十进制 255)
?>
```

### 整数溢出

如果给定的一个数超出了[integer](http://php.net/manual/zh/language.types.integer.php)的范围，将会被解释为[float](http://php.net/manual/zh/language.types.float.php)。同样如果执行的运算结果超出了[integer](http://php.net/manual/zh/language.types.integer.php)范围，也会返回[float](http://php.net/manual/zh/language.types.float.php)。

