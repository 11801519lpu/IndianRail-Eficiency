# IndianRail-Eficiency
Here for the rquired project, we are supposed to use the code done using C programming
using locksand condition variables

 IndianRail has decided to improve its efficiency by automating not just its trains but also its passengers. Each passenger and each train is controlled by a thread. You have been hired to write synchronization functions that will guarantee orderly loading of trains.

Locks are methods of synchronization used to prevent multiple threads from accessing a resource at the same time. Usually, they are advisory locks, meaning that each thread must cooperate in gaining and releasing locks. More difficult to implement and less common, mandatory locks actually prevent any other thread from accessing a resource, and issue an exception if this occurs.

There are only two operations that can be applied to a condition variable: wait and signal. When a thread executes a wait call on a condition variable, it is immediately suspended and put into the waiting queue of that condition variable. Thus, this thread is suspended and is waiting for the event that is represented by the condition variable to occur. Because the calling thread is the only thread that is running in the monitor, it "owns" the monitor lock. 


One common lock mechanism is the semaphore.

lock_init(struct lock* lock)

lock_acquire(struct lock* lock)

lock_release(struct lock* lock)

cond_init(struct condition* cond)

cond_wait(struct condition* cond, structlock * lock)

cond_signal(struct condition* cond, structlock * lock)

cond_broacast(struct condition* cond, structlock * lock)

We do this withonly these functions 
Firstly we assume that there is never more than one train in the station at once, and that all trains (and all passengers) are going to the same destination.
This code allows multiple passengers to board simultaneously.

And this dosen't result busy waiting
