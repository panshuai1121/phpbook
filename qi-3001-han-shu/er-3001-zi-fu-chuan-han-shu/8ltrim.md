## ltrim

语法：

```
string ltrim ( string $str [, string $character_mask ] )
```

参数：

str 输入的字符串

character\_mask : 你也可以指定想要删除的字符，简单地列出你想要删除的所有字符即可

返回值：

此函数返回字符串`str`去除最左边空白字符后的结果。**如果不指定第二个参数**，l**trim\(\)  **将去除这些字符：

> * " " \(ASCII 32 \(0x20\)\)，普通空格符。
> * "\t" \(ASCII 9 \(0x09\)\)，制表符。
> * "\n" \(ASCII 10 \(0x0A\)\)，换行符。
> * "\r" \(ASCII 13 \(0x0D\)\)，回车符。
> * "\0" \(ASCII 0 \(0x00\)\)，空字节符。
> * "\x0B" \(ASCII 11 \(0x0B\)\)，垂直制表符。



```
$text = "\t\tThese are a few words :) ...  ";
$binary = "\x09Example string\x0A";
$hello  = "Hello World";
var_dump($text, $binary, $hello);

print "\n";


$trimmed = ltrim($text);
var_dump($trimmed);

$trimmed = ltrim($text, " \t.");
var_dump($trimmed);

$trimmed = ltrim($hello, "Hdle");
var_dump($trimmed);

// 删除 $binary 开头的 ASCII 控制字符
// (从 0 到 31，包括 0 和 31)
$clean = ltrim($binary, "\x00..\x1F");
var_dump($clean);
```



