## stripslashes

反引用一个字符串

语法：

```
string stripslashes ( string $str )
```

参数：

$str 需要反转义的字符串

返回：

返回一个去除转义反斜线后的字符串（_\'_转换为_'_等等）。双反斜线（_\\_）被转换为单个反斜线（_\_）。

