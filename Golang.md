1. make和new的区别
	>new只分配内存，make用于slice，map，和channel的初始化

2. 闭包 
	 >闭包是一个可以引用其作用域之外变量的函数,闭包是一个内部函数，它可以访问创建它的范围内的变量。即使外部函数完成执行并且作用域被破坏，依然可以访问

3. map底层原理
	>它是一个指针，占用8字节，指向一个hmap结构体,hmap包含了若干个结构为bmap的数组，每个bmap结构底层采用的是链表结构，bmap一般称其bucket

4. channel底层原理
	>Go 语言的 Channel 在运行时使用hchan结构体表示，结构体中的五个字段 `qcount`、`dataqsiz`、`buf`、`sendx`、`recv` 构建底层的循环队列
	>- `qcount` — Channel 中的元素个数；
	>- `dataqsiz` — Channel 中的循环队列的长度；
	>- `buf` — Channel 的缓冲区数据指针；
	>- `sendx` — Channel 的发送操作处理到的位置；
	>- `recvx` — Channel 的接收操作处理到的位置；