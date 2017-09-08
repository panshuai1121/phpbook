## 类和常量

类的常量和所有字母都 **必须 大写，词间使用下划线。**

**此处的「类」指代所有的类（class）、接口（interface）以及可复用代码块（traits）。**

```
<?php

namespace Vendor\Model;

class Foo
{
   const VERSION = 1.0 ;
   const DATE_APPROVED = "2017-09-01";
}
```

### **类的属性**

类的属性命名：

* 大写开头的驼峰 $StudlyCaps；
* 小写开头的驼峰$studlyCaps;
* 下划线分隔 $under\_score;

**无论哪种风格团队应该保持一致。**

### 方法：

方法必须符合 camelCase\(\) 小写驼峰开头

