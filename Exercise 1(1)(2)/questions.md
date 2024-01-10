Exercise 1 - Theory questions
-----------------------------

### Concepts

What is the difference between *concurrency* and *parallelism*?

Parallelism involves performing multible tasks at the same time in parallell. Concurrency however involves performing multible task at once but not nesseseraly at the same time. It often involves switching between steps within the tasks.

What is the difference between a *race condition* and a *data race*? 

Both issues with concurrent programming, where data race is a type of race condition. Data race means that multible tasks tries to acces the same piece of data without propper synchronization, as a result the data might be altered by one of the tasks, corrupting the data for the other tasks, leading to unwanted behavior. Race conditions is a broader term refering to issues where the outcome depends on the sequence or timing of uncontolable events.

*Very* roughly - what does a *scheduler* do, and how does it do it?
> *Your answer here* 


### Engineering

Why would we use multiple threads? What kinds of problems do threads solve?
> *Your answer here*

Some languages support "fibers" (sometimes called "green threads") or "coroutines"? What are they, and why would we rather use them over threads?
> *Your answer here*

Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
> *Your answer here*

What do you think is best - *shared variables* or *message passing*?
> *Your answer here*


