Due to race condition (data race), meaning both threads are modifying the global variable "i", without any sync. mechanism, it becomes unpredictable which value the variable holds for each iteration, making the end result not 0, as we would expect.

Mutexes are used specificaly for the concept of shared owership of a variable, since it allows for only one thread to access the resource at a time. The reason for this is the ownership status, which means that the thread that locked the mutex is the owner and only it can access and modify the variable. Semaphore on the other hand does not have ownership, but rather allows for more general purposes of limiting concurrent access to variables. 




