学习笔记
### 作业
#### 问题
>基于 errgroup 实现一个 http server 的启动和关闭 ，以及 linux signal 信号的注册和处理，要保证能够一个退出，全部注销退出。

---
#### 分析解答
* http server使用channel进行监听，使用接口进行启动和关闭
* linux signal本身使用chan阻塞，有信号就会结束
* 