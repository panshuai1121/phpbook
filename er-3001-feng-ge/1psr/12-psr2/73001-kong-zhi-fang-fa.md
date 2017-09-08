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



