# IndianRail-Eficiency
Here for the rquired project, we are supposed to use the code done using C programming
usinglocksand condition variables

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
