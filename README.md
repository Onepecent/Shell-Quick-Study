要学会善用gpt
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

 ----

 1. | ，在Linux中 | 是作为管道符来使用的，将 ‘|’前面命令的输入当做后面命令的输入
2. || ，用 || 分割的命令具有短路效应，及如果前面的命令为真，在后面的命令不会执行，如果前面的命令为假，则继续执行后面的命令。
3. & ，用 & 连接的多个符号将同时执行，不管命令是否执行成功
4. && ，用&&连接的符号也具有短路效应，即当前面的命令执行的结果为假时，后面的命令将不会得到执行，只有当前面的命令执行结果为真时后面的命令才会得到执行

git提交代码的时候会出现LF文件无法提交的情况，只需要将回车方式改成CRLF就行，然后在git配置文件中将autocrlf = false


----

curl常用的命令行工具的用法
https://zhuanlan.zhihu.com/p/346026915?utm_id=0

----

在AWK中，有四个与分隔符相关的变量：RS、ORS、FS和OFS。它们的作用和区别如下：

1. RS（Record Separator）记录分隔符：
   - 默认值为换行符 `\n`。
   - 用于确定输入数据中记录（行）的结束位置。
   - AWK会根据RS的值将输入数据拆分成多个记录。

2. ORS（Output Record Separator）输出记录分隔符：
   - 默认值为换行符 `\n`。
   - 用于定义在输出时记录之间的分隔符。
   - 当AWK打印输出时，会在每个记录之后插入ORS的值。

3. FS（Field Separator）字段分隔符：
   - 默认值为连续的空格或制表符。
   - 用于确定输入数据中字段（列）的分隔位置。
   - AWK会根据FS的值将每个记录分割成多个字段。

4. OFS（Output Field Separator）输出字段分隔符：
   - 默认值为一个空格。
   - 用于定义在输出时字段之间的分隔符。
   - 当AWK打印输出时，会在每个字段之间插入OFS的值。

总结：
- RS和ORS是用于控制记录（行）的分隔和输出格式的变量。
- FS和OFS是用于控制字段（列）的分隔和输出格式的变量。

通过修改这些变量的值，可以自定义分隔符以适应不同的输入数据格式和输出需求。

----

要在一个Shell脚本中调用三个子Shell并等待它们完成后再执行第四个Shell，你可以使用`wait`命令来等待子Shell的结束。以下是一个示例Shell脚本：

```bash
#!/bin/bash

# 启动第一个子Shell
echo "启动第一个子Shell"
./first_script.sh &

# 启动第二个子Shell
echo "启动第二个子Shell"
./second_script.sh &

# 启动第三个子Shell
echo "启动第三个子Shell"
./third_script.sh &

# 等待第一个子Shell结束
wait

# 等待第二个子Shell结束
wait

# 等待第三个子Shell结束
wait

# 执行第四个Shell
echo "执行第四个Shell"
./fourth_script.sh
```

上面的脚本假设你有四个分别为`first_script.sh`、`second_script.sh`、`third_script.sh`和`fourth_script.sh`的Shell脚本文件。在脚本中，我们首先启动三个子Shell，然后使用`wait`命令等待它们的完成。最后，当所有三个子Shell都结束后，才执行第四个Shell。

----

CSH相关
http://www.pythonclub.org/_media/linux/csh/cshell-chinese.pdf
http://www.pythonclub.org/linux/start
