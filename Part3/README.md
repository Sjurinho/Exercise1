# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to your groups repository to complete the task.

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > Concurrency involves performing several tasks within the same time frame. Parallelism involves using several processors to achieve concurrency. Thus parallelism is a means to achieve concurrency, whilst one can achieve concurrency without parallelism, for example with task switching. 
 
 ### Why have machines become increasingly multicore in the past decade?
 > Machines have become increasingly multicore because:
 - It provides you with increased multitasking. Even though a single core can exploit concurrency to multi task to a certain extent, it has it limits. Although more complex architecture, several cores can all exploit concurrency to massively increase the multitasking possible, depending not only on sheer clockspeed.
 - Since it is hard to increase clockspeed even further, several cores can provide the same effect, thus making it possible to still follow Moore's law.
 - It is easier to detect HW errors in cores. By comparing the different cores to each other, one can easily detect and warn about HW errors in one of the cores. The same does not go for SW, since they all run the same SW.
 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > Seperate and independent processes to be executed simultaneously
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > 
 
 ### What are the differences between processes, threads, green threads, and coroutines?
 > Both processes and threads are independent sequences of execution, but the difference between them is that processes do not have a shared memory space, whilst threads do. Green threads are like threads, except they are scheduled by a runtime library or a virtual machine. Coroutines are cooperative, control is switched between functions that run dependently of each other. Thus it is not concurrent?
 
 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > pthread_create() creates a thread, threading.Thread() creates a thread object, go creates a goroutine, running the function concurrently with the callerfunction.
 
 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > GIL locks python objects s.t. only one thread can access them at a time.
 
 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > The multiprocessing package, it utilizes subprocesses instead of threads.
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > Sets the maximum number of CPUs that can be running simultaneously and returns the previous setting.  
