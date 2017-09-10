## trim

trim 去除字符串首尾处的空白字符（或者其他字符）

语法：

```
string trim ( string $str [, string $character_mask = " \t\n\r\0\x0B" ] )
```

此函数返回字符串`str`去除首尾空白字符后的结果。**如果不指定第二个参数**，**trim\(\)  **将去除这些字符：

> * " " \(ASCII 32 \(0x20\)\)，普通空格符。
> * "\t" \(ASCII 9 \(0x09\)\)，制表符。
> * "\n" \(ASCII 10 \(0x0A\)\)，换行符。
> * "\r" \(ASCII 13 \(0x0D\)\)，回车符。
> * "\0" \(ASCII 0 \(0x00\)\)，空字节符。
> * "\x0B" \(ASCII 11 \(0x0B\)\)，垂直制表符。

参数：

$str

需要处理的字符串

$character\_mask

一般要列出所有希望过滤的字符，也可以使用..列出一个字符范围

返回值：

过滤后的字符串

```
$str = " \r my name is xiao ming  ai ya \t sssfi \n aiyou\n\r\t"; #注意单引号不解析
echo trim($str,"a");
```



