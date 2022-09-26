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
