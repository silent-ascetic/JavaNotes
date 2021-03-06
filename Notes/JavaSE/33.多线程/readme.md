# 线程

## 程序、进程、线程

**程序：**  
    程序是为了完成特定任务，用某种语言编写的一组指令的集合，是一段静态代码。（程序是静态的）

**进程：**  
    进程是程序的一次执行过程，正在执行的一个程序。进程作为资源分配的单位，在内存中会为每个进程分配不同的内存区域，进程是一个动态过程。  
    电脑中每一个运行的软件都是一个进程。

**线程：**  
    线程是一个程序内部的一条执行路径。线程是进程中的一个执行单元，负责当前进程中的程序执行，一个进程中至少有一个线程。线程是CPU的最小调度单位。

## 并行与并发

**并行：** 两个或多个事件在同一时段发生  
**并发：** 两个或多个事件在同一时刻发生

在操作系统中，安装了多个程序，**并发**指的是在一段时间内宏观上有多个程序同时运行，这在单 CPU 系统中，每一时刻只能有一道程序执行，即微观上这些程序是分时
的交替运行，只不过是给人的感觉是同时运行，那是因为分时交替运行的时间是非常短的。  
而在多个 CPU 系统中，则这些可以并发执行的程序便可以分配到多个处理器上（CPU），实现多任务并行执行，即利用每个处理器来处理一个可以并发执行的程序，这样多个程序便可以同时执行。目前电脑市场上说的多核 CPU，便是多核处理器，核越多，并行处理的程序越多，能大大的提高电脑运行的效率。

> 注意：单核处理器的计算机肯定是不能并行的处理多个任务的，只能是多个任务在单个CPU上并发运行。同理,线程也是一样的，从宏观角度上理解线程是并行运行的，但是从微观角度上分析却是串行运行的，即一个线程一个线程的去运行，当系统只有一个CPU时，线程会以某种顺序执行多个线程，我们把这种情况称之为线程调度。

## 线程调度

* 分时调度：所有线程轮流拥有CPU的使用权，平均分配每个线程占用CPU的时间
* 抢占式调度：优先让优先级高的线程使用CPU，如果线程的优先级相同，则随机选择。Java使用的是抢占式调度。
  * 详解:  
  大部分操作系统都支持多进程并发运行，现在的操作系统几乎都支持同时运行多个程序。比如：现在我们上课一边使用编辑器，一边使用录屏软件，同时还开着画图板，dos窗口等软件。此时，这些程序是在同时运行，“感觉这些软件好像在同一时刻运行着”。实际上，CPU(中央处理器)使用抢占式调度模式在多个线程间进行着高速的切换。对于CPU的一个核而言，某个时刻，只能执行一个线程，而 CPU的在多个线程间切换速度相对我们的感觉要快，看上去就是在同一时刻运行。其实，多线程程序并不能提高程序的运行速度，但能够提高程序运行效率，让CPU的使用率更高。
  * 设置线程优先级
  ![](../../../img/设置线程优先级.png)

