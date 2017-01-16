# CDrrrWinThread

## 前言
目前，因为一个小项目的原因重新使用MFC，但是我发现对于线程的封装MFC比较弱，它的目的似乎是在UI线程上，而不是工作线程。因此，我只能重复造轮子。目标是想实现一个快速的工程线程类Task，然后派生出一个Check类。

## 目标
* Task类：CTaskThread，一次性的执行任务，线性，重载虚函数Run即可完成，可以随时检查线程状态。
* Check类：CCheckThread，派生子CTaskThread，用于执行检查任务，循环执行。重载虚函数ThreadBody()即可完成。另外有InitialThread()用于线程开始前申请资源，Cleanup()用于线程结束前清场。
2017年1月26日前提交0.1版本
