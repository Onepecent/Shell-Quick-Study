# Shell-Quick-Study
Shell脚本语言光速入门<br />
https://www.bilibili.com/video/BV1WY4y1H7d3?p=76&spm_id_from=pageDriver&vd_source=619f2ea84d097d616020f74d1643c8f1

----

通过shell修改配置文件：<br />
http://t.zoukankan.com/jinglangyan-p-7505268.html<br />
https://www.cnblogs.com/songxingzhu/p/7402833.html<br />

----

三剑客：https://www.jianshu.com/p/cfd7633b86e2 <br />
使用小结:<br />
grep、sed、awk都可以过滤行记录，但过滤行记录时优先选择grep，其过滤行的效率最高。<br />
sed主要用于对文件内容做出各种修改(增加、替换等)。<br />
awk主要用于对文件内容取行列操作。<br />

----

Linux系统中wc（Word Count）命令的功能为统计指定文件中的字节数、字数、行数，并将统计结果显示输出。
wc [options] 文件...或者通过管道的方式 |<br />
　　-c　  统计字节数

　　-l　   统计行数

　　-m　 统计字符数。这个参数不能与 -c 参数一起使用。

　　-w　 统计字数。一个字被定义为空白、跳格或换行字符分隔的字符串。

　　-L　 打印最长行的长度

　　--help 　  显示帮助信息

　　--version  显示版本信息

  ----

  在Linux中，sort命令用于对文本文件进行排序。sort命令的具体实现可能因不同的Linux发行版而有所不同，但一般会使用快速排序（quicksort）算法作为默认的排序算法。

快速排序是一种常见的排序算法，它通过选择一个基准元素（pivot），将待排序的序列分割成两部分，并递归地对这两部分进行排序，直到整个序列有序。快速排序的平均时间复杂度为O(nlogn)，是一种高效的排序算法。

除了快速排序，某些Linux发行版的sort命令也可以使用合并排序（mergesort）或堆排序（heapsort）等其他排序算法，这取决于具体的实现。有时，sort命令还会根据输入数据的大小和特点来选择最优的排序算法。


Red Hat 是一个知名的 Linux 发行版，其 sort 命令通常使用的是合并排序（mergesort）算法来进行排序。

合并排序是一种分治策略的排序算法，它将待排序的序列递归地切分成更小的子序列，然后将这些子序列逐步合并起来，直到整个序列有序。合并排序的时间复杂度为O(nlogn)，在处理大规模数据时表现较好。
