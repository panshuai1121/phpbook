## stripcslashes

stripcslashes 用于 反转义 addcslashes 转义后的字符串

语法：

```
string stripcslashes ( string $str )
```

参数：

$str addcslashes转义后的字符串

返回：

转义后的字符串

```
$str = "My na me is Phper, i'm s t udy .. ";
$aStr = addcslashes($str,'A..z');
echo stripcslashes($aStr);
```



