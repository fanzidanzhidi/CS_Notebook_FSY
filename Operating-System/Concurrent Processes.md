### Concurrent Processes 并发

#### Basic Concepts

- **atomic** means that variable on which read, modify and update happens at the same time/moment with no pre-emption
- **Concurrent** means, which occurs when something else happens.

![image-20220311171949044](C:\Users\zzk\Documents\OneDrive - Delft University of Technology\CS_Notebook_FSY\Images\Concurrent Processes\image-20220311171949044.png)

#### mutex 互斥量

- A **Mutex** is a lock that we set before using a shared resource and release after using it. When the lock is set, no other thread can access the locked region of code.
- 为协调共同对一个共享资源的单独访问而设计的。互斥量跟临界区很相似，比临界区复杂，互斥对象只有一个，只有拥有互斥对象的线程才具有访问资源的权限。

#### Semaphores 信号量

- 为控制一个具有有限数量用户资源而设计。它允许多个线程在同一时刻访问同一资源，但是需要限制在同一时刻访问此资源的最大线程数目。互斥量是信号量的一种特殊情况，当信号量的最大资源数=1就是互斥量了。

  优点：适用于对Socket（套接字）程序中线程的同步。

