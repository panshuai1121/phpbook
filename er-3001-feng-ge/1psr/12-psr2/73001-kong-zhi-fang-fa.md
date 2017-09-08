## 控制方法

控制结构的基本规范如下：

* 控制结构关键词后 **必须 **有一个空格。
* 左括号`(`后 **一定不可 **有空格。
* 右括号`)`前也 **一定不可**有空格。
* 右括号`)`与开始花括号 `{`间 **必须 **有一个空格。
* 结构体主体 **必须 **要有一次缩进。
* 结束花括号 `}`**必须 **在结构体主体后单独成行。

每个结构体的主体都**必须**被包含在成对的花括号之中， 这能让结构体更加结构话，以及减少加入新行时，出错的可能性。

### 1、if else

```
<?php
namespace Vendor\Package;

abstract class ClassName
{
    protected static $foo;
    abstract protected function zim();
    final public static function bar()
    {
        if ($expr1) {
            // if body
        } elseif ($expr2) {
            // elseif body
        } else {
            //else body;  
        }
    }
}
```

**应该 **使用关键词 `elseif`代替所有 `else if`，以使得所有的控制关键字都像是单独的一个词。

### 2、swith 和 case

标准的`switch`结构如下代码所示，留意括号、空格以及花括号的位置。`case`语句**必须**相对`switch`进行一次缩进，而`break`语句以及`case`内的其它语句都**必须**相对`case`进行一次缩进。

如果存在非空的`case`直穿语句，主体里**必须**有类似`// no break`的注释。

```
<?php
switch ($expr) {
    case 0:
        echo "Fist case ,with a break ";
        break;
    case 1:
        echo "second case ,with falls through";
        // no break
    case 2:
    case 3:
    case 4:
        echo "third case return instaead of break";
        return;
    default:
        echo "default case";
        break;  
}
```

### 3、while 和 do while

一个规范的 while 语句应该如下表示，注意其括号、空格以及花括号的位置。

```
while ($expr) {
    //body
}

do {

} while ($expr);
```

### 4、for

```
for ($i = 0; $i < 10; $i++) {
    //
}
```

### 5、foreach

```
foreach ($iterable as $key => $value) {
    //
}
```

### 6、try catch





