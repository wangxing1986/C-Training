﻿# 练习3

##题目
```
3、程序实现目标：输入n个字符串，将各个字符串排序后的结果按顺序输出。

实例：n = 4，
输入："abhhhhddffg"
      "sd23354675"
      "adssfdhsafs"
      "sdabc"

输出："sdabc"
      "sd23354675"     
      "adssfdhsafs"
      "abhhhhddffg"
```
##解题思路
1. 因为需要排序的字符串个数不确定，所以需要动态分配空间用来保存入力的字符串。
  - char *ptrStr[MAX_PAHT]:字符指针数组，用来指向每一个入力的字符串空间的首地址。排序的时候，只需要调整这些指针在数组中顺序。
  - malloc: 动态分配入力字符串的保存空间。需要注意的是，malloc的参数，必须制定想要分配的空间的byte个数。
  - scanf和gets：又是这两个stdin入力获取函数，哈哈。再强调一点，scanf会以空格和回车划分入力内容，并且不返回回车符，回车符和剩下的入力内容会残留在stdin缓存中，下次scanf和gets之类的入力读取函数调用时，会直接从stdin缓存中读到。