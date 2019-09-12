﻿# 练习1

##题目
```
2、程序实现目标：把一段字符串中的第一个空格和最后一个空格去掉。

实例：源字串：" asd bsdf   df "，目的字串："asd bsdf   df"
```
##解题思路
1. 如何从标准入力接收带有空格的字符串？ 
  - scanf:遇到空格就会结束，默认使用空格作为入力的分隔符。
  - gets:接收字符串直到遇到回车，并且接收回车字符，然后将回车字符转成字符串结束符`'\0'`保存。
2. 去字符串前后空格，可以使用指针，从前往后，如果是空格指针向后移动一个字符，直到找到第一个非空格字符。从后往前查找空格，如果是空格，就将该空格置换为字符串结束符`'\0'`。