### 1.9 线程

- 1.什么是线程？能解决什么问题。

>多任务：同一时刻运行多个程序的能力。每一个任务称为一个线程。可以同时运行一个以上线程的程序称为多线程程序。

>Java编写程序都运行在在Java虚拟机（JVM）中，在JVM的内部，程序的多任务是通过线程来实现的。每用java命令启动一个java应用程序，就会启动一个JVM进程。在同一个JVM进程中，有且只有一个进程，就是它自己。在这个JVM环境中，所有程序代码的运行都是以线程来运行。

>一般常见的Java应用程序都是单线程的。比如，用java命令运行一个最简单的HelloWorld的Java应用程序时，就启动了一个JVM进程，JVM找到程序程序的入口点main()，然后运行main()方法，这样就产生了一个线程，这个线程称之为主线程。当main方法结束后，主线程运行完成。JVM进程也随即退出 。
>对于一个进程中的多个线程来说，多个线程共享进程的内存块，当有新的线程产生的时候，操作系统不分配新的内存，而是让新线程共享原有的进程块的内存。因此，线程间的通信很容易，速度也很快。不同的进程因为处于不同的内存块，因此进程之间的通信相对困难。

>进程是指一个内存中运行的应用程序，每个进程都有自己独立的一块内存空间，一个进程中可以启动多个线程。比如在Windows系统中，一个运行的exe就是一个进程。

>线程是指进程中的一个执行流程，一个进程可以运行多个线程。比如java.exe进程可以运行很多线程。线程总是输入某个进程，进程中的多个线程共享进程的内存。

>Java中线程是指java.lang.Thread类的一个实例或线程的执行。使用java.lang.Thread或java.lang.Runnable接口编写代码定义、实例化、启动新线程。
>Java中每个线程都有一个调用栈，即使不在程序中创建任何新的线程，线程也在后台运行。main()方法运行在一个线程内，称为主线程。一旦创建一个新的线程，就产生一个新的调用栈。
线程分为两类：用户线程和守候线程。当所有用户线程执行完毕后，JVM自动关闭。但是守候线程却不独立与JVM，守候线程一般是有操作系统或用户自己创建的。


- 2.Java中创建线程的2种方式。

> [点击查看答案](https://www.cnblogs.com/tzc1024/p/6005580.html)

- 3.给我说说线程的生命周期。

> [点击查看答案](https://www.cnblogs.com/sunddenly/p/4106562.html)

- 4.线程死锁的原因 & 举个栗子 & 如何避免死锁。

> [点击查看答案](https://www.cnblogs.com/xiaoxi/p/8311034.html)
> [如何避免死锁](https://www.cnblogs.com/vinozly/p/5240204.html)

- 5.Synchronized放在静态方法和非静态方法上的锁对象分别是什么？

> Synchronized放在静态方法上时，锁对象为当前类对应的字节码对象class。
> Synchronized放在非静态方法上时，锁对象是this指针指向的当前对象。

- 6.如何停止掉一个线程？

> [点击查看答案](https://www.cnblogs.com/of-fanruice/p/7522201.html)

- 7.给我说说线程池的种类 & 特点 & 内部原理 & 平时当中使用案例。

> [点击查看答案](https://www.cnblogs.com/aaron911/p/6213808.html)

- 8.给我谈谈你是如何保证线程数据安全问题的？

> 这里笔者不提供答案。具体讲讲消费者生产者问题，Synchronized的使用以及如何避免死锁即可。

- 9.wait()和sleep()的区别？

> [点击查看答案](https://www.cnblogs.com/ccliekkas/p/5001611.html)

- 10.什么是公平锁&非公平锁&区别？

> [点击查看答案](https://www.cnblogs.com/qifengshi/p/6831055.html)

- 11.给我讲讲线程间通信

> [点击查看答案](https://www.cnblogs.com/hapjin/p/5492619.html)

- 12.volatile关键字是如何使用的？原理是什么

> [volatile使用](https://www.cnblogs.com/sunrunzhi/p/3930297.html)
> [volatile原理](https://www.cnblogs.com/dolphin0520/p/3920373.html)

- 13.说说使用5个线程去计算一个数组之和的思路。

> 这个题目实际在考察你的思维和多线程数据安全问题。首先将这个数组分为5组，分别交给5个线程，此外还需要有一个变量记录和值，那么问题来了，这个记录和值的变量肯定会被5个线程进行读取和修改，那么就一定存在数据安全问题，所以问题还是回到第8题如何保证线程数据安全问题。

- 14.谈谈线程阻塞的原因有哪些？

> [点击查看答案](https://www.cnblogs.com/ou-pc/p/9522369.html)

- 15.谈谈你对notify的理解？

> [点击查看答案](https://www.cnblogs.com/hapjin/p/5492645.html)

- 16.你觉得Lock和Synchronized的区别是什么？

> [点击查看答案](https://www.cnblogs.com/nsw2018/p/5821738.html)

- 17.谈谈你对ReentrantLock的认识。

> [点击查看答案](https://www.cnblogs.com/zhimingyang/p/5702752.html)

- 18.调用run()和start()的区别？

> [点击查看答案](http://www.cnblogs.com/changekyq/p/4308537.html)

- 19.transient关键字的用法 & 作用 & 原理。

> [点击查看答案](https://www.cnblogs.com/duanxz/p/4919147.html)

- 20.ThreadPoolExecutor的工作策略有哪些？

> [点击查看答案](https://www.cnblogs.com/lic309/p/4564507.html)

- 21.ThreadLocal了解吗？说说原理。

> [点击查看答案](https://www.cnblogs.com/xujian2014/p/5777849.html)

- 22.权衡多线程的性能。

> 这题答案没有标答了，主要就是和面试官说说你对多线程性能的认识。
> 参考回答：
>
> **多线程的优点：**
>
1. 方便高效的内存共享
1. 多进程下内存共享比较不便，且会抵消掉多进程编程的好处
1. 较轻的上下文切换开销
1. 不用切换地址空间，不用更改CR3寄存器，不用清空TLB
1. 线程上的任务执行完后自动销毁

>**多线程的缺点：**
>
1. 开启线程需要占用一定的内存空间(默认情况下,每一个线程都占512KB)
1. 如果开启大量的线程,会占用大量的内存空间,降低程序的性能
1. 线程越多,cpu在调用线程上的开销就越大
1. 程序设计更加复杂,比如线程间的通信、多线程的数据共享


>综上得出，多线程不一定能提高效率，在内存空间紧张的情况下反而是一种负担，因此在日常开发中，应尽量
>
1. 不要频繁创建，销毁线程，使用线程池
1. 减少线程间同步和通信（最为关键）
1. 避免需要频繁共享写的数据
1. 合理安排共享数据结构，避免伪共享（false sharing）
1. 使用非阻塞数据结构/算法
1. 避免可能产生可伸缩性问题的系统调用（比如mmap）
1. 避免产生大量缺页异常，尽量使用Huge Page
1. 可以的话使用用户态轻量级线程代替内核线程

- 23.如何理解同步和异步，阻塞和非阻塞。

> [点击查看答案](https://www.cnblogs.com/mhq-martin/p/9035640.html)
