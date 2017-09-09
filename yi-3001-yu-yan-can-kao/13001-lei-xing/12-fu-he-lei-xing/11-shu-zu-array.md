## 数组



![](http://upload-images.jianshu.io/upload_images/3012926-1f55932b7bdc86a6.png?imageMogr2/auto-orient/strip|imageView2/2/w/1240)

数组本质就是一个hashtable结构，左侧的0~nTablemask便是hash下标，而后面有一个双向链表，便是我们通常所说的hash冲突的链地址法。

而绿色的双向链表，则是foreach遍历用的，这个地方用双向链表，主要是为了逆序访问来用的，遍历的时候，就是从pListHead开始不断的next便可以遍历所有的元素。这样要比下标遍历hashtable快得多。

但是这个结构有很明显的缺点：

①. 每次插入/删除元素都要申请/释放内存，这样会严重的导致内存碎片化，降低内存的使用率。

②. 再者，每次插入元素的时候都要去申请内存，会有一次寻址的过程，时间效率低。

③. 指针结构很复杂，有大量的指针操作。

