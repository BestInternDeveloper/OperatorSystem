# OperatorSystem
操作系统 精髓与设计原理 课后复习题
地址寄存器：用于确定下一次读/写的存储器地址
指令寄存器：处理器的一个寄存器放着取到的指令
寄存器：与处理器交换数据
辅存：二级存储器，存取可见的文件和记录
命中率：较快存储器的访问次数与对所有存储器的访问次数的比值
可编程I/O：I/O状态执行请求设置I/O状态寄存器中相应的位，它不会通知处理器或中断处理器。因此处理器会定期检查I/O状态

### 1.1列出并简要定义计算机的4个主要组成成分
系统总线：在处理器，内存，输入输出模块之间提供通信的设施
处理器:处理数据
内存:存储数据
输入输出模块：在计算机与外部之间移动数据

### 1.2定义处理器寄存器两种主要类别
地址寄存器 确定下一次读/写存储器的地址
缓冲寄存器 存放要写入存储器的数据或从存储器中读取的数据

### 1.3 一般而言，一条机器指令能指定的4种不同操作是什么
处理器-存储器：数据可以从处理器传送到存储器，或从存储器传送到处理器
处理器-I/O:通过处理器和I/O模块间的数据传送，数据可以输出到外部设备，或从外部设备向处理器输入数据。
数据处理：处理器可以执行很多与数据相关的算术操作或逻辑操作。
控制：某些指令可以改变顺序。

### 1.4 什么是中断
中断是用来提高处理器执行效率的一种手段，处理器可以在I/O操作过程中执行其他指令。

### 1.5多个中断处理方式
（1）在处理一个中断的时候，禁止再发生中断
（2）定义中断优先级，根据优先级处理中断，高优先级的打断低优先级的中断

### 1.6 内存层次各个元素间的特征是什么
存取时间越快，每“位”价格越高
容量越大，每“位”的价格越低
容量越大，存取速度越慢

### 1.7 什么是高速缓存
处理器和内存间提供一个容量小且速度极快的存储器

### 1.8 多处理器系统和多核系统的区别是什么？
多核：两个或多个处理器在一块硅上
多处理器：一条系统总线上有多个处理器

### 1.9 空间局部性和时间局部性间的区别是什么？

### 1.10 开发空间局部性和时间局部性的策略是什么？

### 2.1 操作系统设计的三个目标是什么
方便：操作系统使计算机易于使用。
有效：操作系统以更有效的方式使用计算机系统资源
扩展能力：在构造操作系统时，应允许在不妨碍服务得前提下，有效地开发，引入和测试新的系统功能

### 2.2 什么是操作系统内核
包含操作系统最常用的功能

### 2.3 什么是多道程序设计
内存空间可以容得下操作系统和两个或多个用户程序，且在它们之间来回切换

### 2.4 什么是进程
一个正在执行的程序
计算机中正在运行的程序的一个实例
可分配给处理器并由处理器执行的一个实体
由一个单一顺序线程、一个当前状态和一组相关的系统资源所表征的活动资源

### 2.5 操作系统是怎样使用进程上下文的
给每个进程分配了一块存储器区域，并且在由操作系统建立和维护的进程表中进行记录

### 2.6 列出并简要介绍操作系统的5种典型存储管理职责
进程隔离：操作系统必须保护独立的进程，防止互相干扰各自的存储空间，包括数据和指令。
自动分配和管理：程序应该根据需要在存储层次见动态地分配，分配对程序员是透明的。因此程序员无须关心与存储限制有关的问题，操作系统会有效地实现分配问题，可仅在需要时才给作业分配存储空间。
支持模块化程序设计：程序员应该能够定义程序模块，并动态地创建、销毁模块，动态地改变模块的大小
保护和访问控制：不论在存储层次中的哪一级，存储器的共享都会存在一个程序访问另一个程序的潜在可能性。当某个程序需要共享时，这是可取的，但在其它时候，它可能会威胁到程序的完整性，甚至操作系统。因此操作系统必须允许一部分内存由各种用户以各种方式访问。
长期存储：许多应用程序需要在关机后长时间的保存信息。

### 2.7 实地址和虚地址的区别是什么？
实地址：
虚地址：

### 2.8 描述时间片轮转调度技术
时间片，在一段固定的时间间隔内，进程队列中先入先出，队列中进程强占当前进程，进入进程队列末尾。

### 2.9 解释单体内核和微内核的区别
单体内核是作为一个进程实现的，所有元素都共享相同的地址空间。
微内核 只给内核分配一些最基本的功能，其它操作系统服务则由运行在用户模式且与其它类似的进程提供

### 2.10 什么是多线程
执行一个应用程序的进程划分为可以同时运行的多个线程

### 2.11 列出对称多处理操作系统设计时要考虑的关键问题
并发进程或线程
调度
同步
内存管理
可靠性和容错性

### 3.1 什么是指令跟踪？
处理器用来确定指令的下一步动作

### 3.2 哪些常见事件会触发进程的创建？		
1. 新的批处理作业
2.交互登录
3.为提供服务而由操作系统创建
4.由现有进程派生

### 3.3 简要定义图3.6所示进程模型中的每种状态
运行态：正在运行的进程。
就绪态：随时可以运行的进程。
新建态：刚刚创建的进程。
阻塞态：进程在某个事件发生前不能执行，一直等待事件发生。
退出态：线程停止执行或者因某种原因被取消。

### 3.4 抢占一个进程是什么意思
把当前一个运行状态的进程挂起，让就绪态的进程上处理器

### 3.5 什么是交换，其目的是什么？
把内存中某个进程的一部分或全部移到磁盘中。

### 3.6 为何图3.9（b）中有两个阻塞态？
操作系统可以进行转换，将阻塞态的一部分置出内存，释放内存空间。当需要时，再置入内存，并转换为挂起/阻塞态。

### 3.7列出挂起态进程的4个特点
1.该进程不能立即执行。
2.该进程可能在也可能不在等待一个时间。若在等待一个时间，那么阻塞条件不依赖于挂起条件，阻塞事件的发生不会使进程立即执行。
3.为阻止该进程执行，通过代理使其置于挂起态，代理可能来自父进程，也可能是操作系统。
4.除非代理显示命令系统转换，否则该进程无法从这一状态转移。

### 3.8 操作系统会为哪类实体维护信息表？
内存表，I/O表，进程表，文件表
内存，设备，进程，文件

### 3.9 列出进程控制块中的三类信息
·进程标识信息
·进程状态信息
·进程控制信息

### 3.10 为什么需要两种模式（用户模式和内核模式）？
保护操作系统和重要的操作系统表不受用户控制的干扰

### 3.11 操作系统创建一个新进程的步骤是什么？
1.为新进程分配一个唯一的进程标识符。
2.为进程分配空间。
3.初始化进程控制块。
4.设置正确的链接。
5.创建或扩充其他数据结构。

### 3.12 中断和陷阱有何区别
中断：与当前运行线程无关，与其某种外部事件有关
陷阱：与当前运行线程产生的错误和异常有关

### 3.13 中断的3个例子
1.时钟中断
2.I/O中断
3.内存失效

### 3.14 模式切换和进程切换有何区别？
模式切换：可在不改变运行态进程的状况下出现
进程切换：要保存上下文，设置进程状态，更新内存管理数据结构。

### 4.1 表3.5列出了无线程操作系统中进程控制块的基本元素。对于多线程系统，这些元素中的哪些可能属于线程控制块，哪些可能属于进程控制块？

###  4.2 请给出线程间的状态切换比进程间的状态切换开销更低的原因

### 4.3 线程中两个独立无关的特点是什么？
资源所有权：进程包括存放进程映像的虚拟地址空间
调度/执行：进程执行时采用一个或多程序的执行路径，不同进程的执行过程会交替进行。

### 4.4 给出在单用户多处理系统中使用线程的4个例子
1.前台和后台工作：例如，在电子表格程序中，一个线程可以显示菜单并读取用户输入，而另一个线程执行用户命令并更新电子表格。
2.异步处理：例如，为避免掉电带来的损失，可以创建一个任务是周期性地进行备份的线程，该线程由操作系统直接调度。
3.执行速度：在多处理器系统中，同一进程中的多个线程可同时执行。这样，即使一个线程在读取数据时被I/O操作阻塞，另一个线程仍然可以继续运行。
4.模块化程序结构：涉及多种活动或多种输入/输出源和目的地程序，更容易实现。

### 4.5 哪些资源通常被一个进程中的所有线程共享？
容纳进程映像的虚拟地址空间。
对处理器、其他进程、文件和I/O资源的受保护访问。

### 4.6 列出用户级线程相对于内核线程的三个优点
1.所有线程管理数据结构都在一个进程的用户地址空间中，线程切换不需要内核模式特权，节省了两次状态转换的开销。
2.调度因应用程序的不同而不同。可以做到为应用程序量身定做调度算法。
3.ULT可在任何操作系统中运行，不需要对地城内核进行修改以支持ULT。

### 4.7 列出用户级线程相对于内核级线程的两个缺点
1.系统调用会引起阻塞。因此，在执行ULT时，阻塞一个线程会导致所有线程都被阻塞。
2.在纯ULT策略中，多线程应用程序不能用做多处理技术。

### 4.8 什么是套管技术
把一个产生阻塞的操作系统调用转换为一个非阻塞的系统调用。

### 5.1 列出与并发相关的4个设计问题
1.操作系统必须能够跟踪不同的进程。
2.操作系统必须为每个活动进程分配和释放各种资源。
3.操作系统必须保护每个净化才能的数据和物力资源，避免其他进程的干扰。
4.一个京城的功能和输出必须与执行速度无关

### 5.2 产生并发3种上下文是什么？
+ 多应用程序：多道程序设计技术允许在多个活动的应用程序动态共享处理器时间。
+ 结构化应用程序：作为模块化设计和结构化程序设计的扩展，一些应用程序有效地设计一组并发进程。
+ 操作系统结构：同样的结构化程序设计有点适用于系统程序，且我们已知操作系统常常作为一组进程实现。


### 5.3执行并发进程最基本的要求？


### 5.4 列出进程间的三种互相知道的程度，并简要给出各自的定义。
+ 进程之间相互不知道对方的存在
+ 进程间接知道对方的存在
+ 进程直接知道对方的存在

### 5.5 竞争进程和合作进程间有何区别
两个或更多的进程在它们的执行过程中需要访问一个资源，每个进程并不知道其他进程的存在，且每个进程也不受其他进程的影响
进程间的资源是共享等待，共同维护数据的完整性。

### 5.6 列出与竞争相关的三个控制问题
死锁：两个线程互相等待对方，永远得不到资源
互斥：一个不可共享资源，一次只能一个进程在临界区中，进程之间产生竞争资源的关系
饥饿：高优先级的进程频繁调用，导致低优先级的进程无限延时处理。

### 5.7 列出对互斥的要求
1.必须强制实施互斥，一次只能有一个进程在临界区。
2.一个在非临界区停止的进程不能干涉其他进程。
3.绝不会允许非临界区需要访问时被无限延迟的情况，既不会死锁也不会饥饿。
4.没有进程在临界区中时，需要访问时可以立刻进入。
5.对相关进程的执行速度和处理器的数量没有任何要求。
6.一进程主流在临界区中的时间是有限的

### 5.8 在信号量上可以执行什么操作
1.一个信号量可以初始化成非负数。
2.semWait操作使信号量减1。若值编程负数，则阻塞执行semWait()的进程，否则进程操作继续执行。
3.semSignal操作信号量加1.若值小于等于0，则被semWait()阻塞的进程解除阻塞。

### 5.9 二元信号量和一般信号量有何区别
二元信号量
1.二元信号量可以初始化为0或1。
2.sewWaitB操作检查信号的值。若值为0，则进程执行semWaitB就会受阻。若值为1，将值改为0，并继续执行该进程。
3.semSignalB操作检查是否有任何进程在该信号上shouzu.ruo有进程受阻，则通过semWaitB操作，受阻的操作会被唤醒；若没有进程受阻，则值设置为1。

### 5.10 信号量和弱信号量有何区别？
强信号量：被阻塞时间最久的京城最先从队列释放。
弱信号量：没有规定进程移出顺序的信号量。

### 5.11 什么是管程？
由一个或多个过程、一个初始化队列和局部数据组成的软件模块。

### 5.12 关于消息，阻塞和无阻赛有何区别？
阻塞send，阻塞receive，一对一，两个被阻塞，直到消息完成投递。
无阻塞send，阻塞receive 多对一，发送者可以发送多条消息，但接受者继续工作前必须接收到消息的进程将被阻塞，直到该消息的到达。
无阻塞send，无阻塞receive 多对多，不要求任何一方等待。

### 5.13 与读者/写者问题先关的条件通常有哪些？
1.任意数量的读进程可同时读这个文件。
2. 一次只有一个写进程可以写文件。
3.若一个写进程正在写文件，则禁止任何读进程读文件。

### 6.1 可重用资源和可消耗资源的例子
可重用资源的例子包括处理器、I/O通道、内存和外存
可消耗资源的例子有中断、信号、消息和I/O缓冲区

### 6.2 产生死锁的三个必要条件是什么？
1.互斥。
2.占有且等待。
3.不可抢占。

### 6.3 产生死锁的4个条件是什么？
1.互斥
2.占有且等待
3.不可抢占
4.循环等待

### 6.5 如何防止占有且等待条件？
可以要求进程一次性请求所有资源，并阻塞这个进程直到所有请求都同时满足。

### 6.6 如何防止循环等待条件？
定义资源类型的线性顺序来预防

### 6.7 死锁避免、检查和预防之间的区别是什么？
死锁预防：通过防止发生三个必要条件中的一个间接完成。
死锁避免：允许三个必要条件，但通过明智选择，永远不会到死锁点。
死锁检查：操作系统周期性地执行一个算法来检测前面的条件。

### 内存管理需要满足哪些需求？
+ 重定位
+ 保护
+ 共享
+ 逻辑组织
+ 物理组织

### 7.1 为何需要重定位进程的能力？
进程换出到磁盘中后，下次换入换出前相同的内存区域很困难，我们需要把进程重定位到内存的不同区域。

### 7.2 为何不能在编译时，实施内存保护？
因为操作系统不能预测违法的内存访问，即使可以预测，也非常耗时

### 7.3 允许两个或多个进程访问内存某一特定区域的原因是什么？
多个进程合作比一个进程执行有优势

### 7.4 在固定分区方案中，使用大小不等的分区有何好处？
大程序用大分区，小程序用小分区
提高内存的利用率非常低

### 7.5 内部碎片和外部碎片有何区别？
内部碎片：由于装入的数据块小于分区的大小，因而导致内部存在空间浪费
外部碎片：随着时间的推移，内存中形成了越来越多的碎片，内存的利用率随之下降。

### 7.6 逻辑地址、相对地址和物理地址有何区别？
逻辑地址：是指与当前数据在内存中的物理分配地址无关的访问地址
相对地址：相对于某些已知点的存储单元
物理地址：数据在内存中的实际地址

### 7.7 页和页框有何区别？
进程中分成同样大小的小块，进程中称为页，内存中称为页框

### 7.8 页和段有何区别？
分段类似于动态分区

### 8.1 简单分页与虚拟内存分页有何区别？
简单分页：进程运行时，它的所有页必须都在内存中， 除非使用了覆盖技术。
虚存分页：进程运行时，并非所有页都须在内存页框中。仅在需要是才读入页。

### 8.2 什么是抖动？
当操作系统读取一块时，要换出内存中的一块。若此时那块内存正好要用，操作系统又要将它取回。处理器大部分的时间都用于交换块而非执行命令。

### 8.3 为何使用虚拟内存时，局部性原理至关重要？
它可以对将来引用的块进行猜测，从而避免系统抖动。

### 8.4 哪些元素时页表项中能找到的典型元素？简单定义每个元素。
页号：虚拟地址的页号部分。
进程标志符：使用该页的进程。
控制位：该域包含一些标记
链指针：若某项没有链项，则该域为空。否则，该域包含链中下一项的索引值。

### 8.5 转换检测缓冲区的目的是什么？
每次虚存访问可能会引起两次物理访问，一次取页表项，另一次取需要的数据，因此，简单的虚拟内存方案会导致内存访问时间加倍。

### 8.6 简单定义两种可供选择的页面读取策略？
1.请求分页：只有放访问到某页中的一个单元时才将该页取入内存。
2.预先分页：若一个进程的页连续储存在辅存中，则一次读取许多连续的页。

### 8.7 驻留集管理和页面置换策略有何不同？
置换策略
+ 给每个活动进程分配多少页框。
+ 计划置换的页集是局限于那些产生缺页中断的进程，还是局限于所有页框都在内存中的进程。
+ 在计划置换的页集中，选择置换出哪一页。

驻留集管理
分配一个进程页框，用于保存该进程的工作集，从分配给该进程的页框中选择被置换的页。

### 8.8 FIFO和时钟页面置换算法有何联系
FIFO隐含的逻辑是置换驻留在内存中时间最长的页

### 8.9 页缓冲实现了什么功能？
已修改的页按簇写回，而不是一次只写一页，因此大大减少了I/O操作的数量，进而减少了磁盘访问时间。

### 8.10 为什么不能把全面置换策略和固定分配策略组合起来？
如果组合起来，内存中所有未被锁定的页都要分配一个固定的页框数，会非常耗时，甚至内存溢出。

### 8.11 驻留集和工作集有何区别？

### 8.12 请求式清除和预约式清除有何区别？
请求式清除：只有当一页被选择用于置换时才被写回辅存。
预约式清除：将这些已修改的多页需要使用它们所占的页框之前成批写回辅存。

### 9.1 简要秒速三种类型的处理器调度
1.长程调度 决定加入待执行进程池
2.中程调度 决定加入部分或全部位于内存中的进程集合
3.短程调度 决定处理器执行哪个可运行进程

### 9.2 在交互式操作系统中，通常最重要的性能或要求是什么？
相应时间

### 9.3 周转时间和响应时间有何区别？
周转时间：指一个进程从提交到完成之间的时间间隔，包括实际执行的时间和等待资源的时间。
相应时间：对于一个交互系统来说，提出请求到开始接受响应的时间间隔。

### 9.4 对于进程调度，较小的优先级值是表示较低的优先级还是表示较高的优先级？
表示较高的优先级

### 9.5 抢占式调度和非抢占式调度有何区别？
非抢占式：一旦进程处于运行状态，就不会不断执行知道终止，进程要么因为等待I/O，要么因为某些系统服务而阻塞自己。
抢占式：当前运行的进程可能被系统中断，并转换为就绪态。

### 9.6 简单定义FCFS调度？
每个进程就绪后，进入就绪队列，当前运行的进程停止运行，选择等待时间长的进程运行。

### 9.7 简单定义轮转调度？
周期性产生时钟中断。
根据时间片，固定时间间隔，对进程进行处理。

### 9.8 简单定义最短进程优先调度？
下次选择预计处理时间最短的进程，短进程将会越过长作业，跳到队列头。
扫描就绪队列中，选择最短的进程上处理器调度。

### 9.9 简单定义最高响应比优先调度。
最高相应比：周转时间和实际服务时间的比值
希望这个值小，所有进程的平均值也最小

### 9.10 简单定义反馈调度。
根据反馈情况，优先调度等待时间间隔长的进程
调度基于抢占原则（按时间片）并使用动态优先级机制。对等待服务时间较长的进程，暂时提高优先级。

### 10.1 列出并简单定义5中不同级别的同步粒度？
细粒度：单指令流中固有的并行。
中等粒度：一个单独应用中的并行处理或多任务处理。
粗粒度：多道程序环境中并发进程的多处理。
极粗粒度：在网络结点上进行分布式处理，形成一个计算环境。
无约束：多个无关进程。

### 10.2 列出并简单定义线程调度的4种技术。
+ 负载分配：进程不分配到某个特定的处理器。
+ 组调度：一组相关的线程基于一对一的原则。
+ 专用处理器分配：它通过把线程指定到处理器来定义隐式的调度。
+ 动态调度：在执行期间，进程的线程数量可以改变。

### 10.3 简单定义三种版本的负债均衡。
+ 先来先服务：一个作业到达时，其所有线程被连续地放在共享队列末尾。一个处理器空闲时，选择下一个就绪线程进行处理。
+ 最少线程数优先：共享就绪队列被组织成一个优先级队列，一个作业包含的未调度线程的数量最少是，给它指定最高的优先级。具有相同优先级按照FCFS。
+ 可抢占的最少线程数优先：最高优先级给予具有最少未被调度线程数的作业。

### 10.4 硬实时任务和软实时任务有何区别？
硬实时任务：必须满足最后期限，不然会给系统带来不可接受的破坏。
软实时任务：也有一个最后期限，并不强制满足这一需求。

### 10.5 周期性实时任务和非周期性实时任务有何区别？
非周期性实时任务：有约束条件，有个开始和结束期限。
周期性性实时任务：每隔周期T执行一次。

### 10.6 列出并简单定义实时操作系统的5方面要求。
+ 可确定性
+ 可相应性
+ 用户控制
+ 可靠性
+ 故障弱化处理

### 10.7 列出并简单定义4类实时调度算法。
+ 静态表调度发：执行关于可行调度的静态分析。
+ 静态优先级抢占调度法：传统的基于优先级的抢占式调度程序。
+ 基于动态规划的调度法：在运行时动态地确定可行性，而不是在开始运行前离线地确定。
+ 动态尽力调度法：不执行可行性分析。系统试图满足所有的最后期限，并终止任何运行但错过最后期限的进程。

### 10.8 一个任务哪些信息在实时调度时非常有用？
优先级
