## bin2hex

bin2hex 函数把包含的二进制字符串转换成十六进制值

```
string bin2hex ( string $str )
```

把二进制的参数`str`转换为的十六进制的字符串。转换使用字节方式，高四位字节优先

参数：

str 二进制字符串

返回值

返回指定字符串的十六进制表示。

```
<?php

$str = 10010011;
echo bin2hex($str);
```



