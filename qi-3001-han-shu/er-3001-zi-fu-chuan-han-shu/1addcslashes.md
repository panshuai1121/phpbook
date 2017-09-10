## addcslashes

— 以 C 语言风格使用反斜线转义字符串中的字符

语法：

```
string addcslashes ( string $str , string $charlist )
```

参数：

$str: 需要转义的字符串

$charlist: 符合转义字符串的规则，区间，需要注意的是，需要转移内容的范围 比如说 出现\n \t ，奖以C语言风格转换，另外如果第二个参数的结束字符ASCII高于开始字符，则不会创建区间

返回值：

返回转义后的字符串

```
$str = "My name is Phper, i'm study .. ";

echo addcslashes($str,'A..z');
```



