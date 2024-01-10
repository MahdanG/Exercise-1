Exercise 1 - Theory questions
-----------------------------

### Concepts

What is the difference between *concurrency* and *parallelism*?

Parallelism involves performing multible tasks at the same time in parallell. Concurrency however involves performing multible task at once but not nesseseraly at the same time. It often involves switching between steps within the tasks.

What is the difference between a *race condition* and a *data race*? 

Both issues with concurrent programming, where data race is a type of race condition. Data race means that multible tasks tries to acces the same piece of data without propper synchronization, as a result the data might be altered by one of the tasks, corrupting the data for the other tasks, leading to unwanted behavior. Race conditions is a broader term refering to issues where the outcome depends on the sequence or timing of uncontolable events.

*Very* roughly - what does a *scheduler* do, and how does it do it?

A scheduler is a component that decides which processes or threads should run at a given time. It works by allocating CPU time to each process, aiming to optimize overall system performance, minimize response time, and ensure fair access to resources. The scheduler constantly switches between processes, a process known as context switching, to effectively manage system resources and keep the computer running smoothly.


### Engineering

Why would we use multiple threads? What kinds of problems do threads solve?

Multithreading is used to improve performance and efficiency. By using multiple threads, a program can handle several tasks simultaneously, such as processing data while staying responsive to user input. This is particularly beneficial in multi-core processors where threads can operate in parallel, leading to better CPU utilization. Additionally, threads can share resources within the same process, making resource management more efficient. Common applications include responsive user interfaces, concurrent processing in web servers, and background tasks like file I/O operations. However, proper thread management is crucial to prevent issues like data corruption and performance bottlenecks.

Some languages support "fibers" (sometimes called "green threads") or "coroutines"? What are they, and why would we rather use them over threads?

They are programming constructs that provide concurrency similar to threads but with a key difference: they are managed at the application level rather than the operating system level. This makes them more  efficient, as they require less overhead for context switching compared to traditional threads. They are useful for tasks that involve a lot of waiting, like I/O operations, as they allow for more tasks to be handled concurrently without the overhead of OS-managed threads. Developers often prefer them over threads in scenarios where high performance with a large number of concurrent operations is required, as they offer more control over how tasks are scheduled and executed.

Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?

Creating concurrent programs can be both easier and harder for programmers. On one hand, concurrency can improve performance and responsiveness in applications, particularly in handling multiple tasks simultaneously or leveraging multi-core processors effectively. On the other hand, it introduces complexity, as developers must carefully manage the interactions between concurrent threads or processes. This can lead to challenging issues like race conditions, deadlocks, and debugging difficulties. Therefore, while concurrency has its benefits, it also requires a deeper understanding and more careful programming to ensure correct and efficient implementation.

What do you think is best - *shared variables* or *message passing*?

Choosing between shared variables and message passing in concurrent programming depends on the application's needs. Shared variables are efficient for closely related processes or threads in a single system, but they require careful synchronization to avoid issues like race conditions. Message passing, on the other hand, is more suitable for distributed systems or loosely coupled architectures, as it avoids direct sharing of data and can reduce complexity. However, it might introduce more overhead due to data being packaged and sent across processes. Each method has its strengths, so the best choice varies based on factors like system architecture, performance requirements, and the complexity of synchronization needed.


