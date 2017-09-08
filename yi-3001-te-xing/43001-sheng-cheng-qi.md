## 生成器

生成器允许你在 [foreach](http://php.net/manual/zh/control-structures.foreach.php) 代码块中写代码来迭代一组数据而不需要在内存中创建一个数组, 那会使你的内存达到上限，或者会占据可观的处理时间。相反，你可以写一个生成器函数，就像一个普通的自定义 [函数](http://php.net/manual/zh/functions.user-defined.php)一样, 和普通函数只[返回](http://php.net/manual/zh/functions.returning-values.php)一次不同的是, 生成器可以根据需要[yield](http://php.net/manual/zh/language.generators.syntax.php#control-structures.yield)多次，以便生成需要迭代的值。

---

### 生成器的优势





