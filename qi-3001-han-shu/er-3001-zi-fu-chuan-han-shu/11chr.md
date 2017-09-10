## chr

chr 返回指定的字符

语法：

```
string chr ( int $ascii )
```

返回相应ascii 所指定的单个字符。此函数与 ord互补。

参数：

ascii 码

返回值：

返回规定的字符

```
$str = "The string ends in escape: ";
$str .= chr(27); /* 在 $str 后边增加换码符 */
```



