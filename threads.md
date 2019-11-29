# What is Thread
- A thread is an independent path of execution within a program.
- Many threads can run concurrently within a program.
- Multithreading refers to two or more tasks executing concurrently within a single program.
- Every thread in java is created and controlled by the java.lang.Thread class.
- There are two ways to create a thread in java.
  - By extending the Thread Class.
  - implement the runnable interface.
## Threads using Runnable Interface
- `public interface Runnable{ void run(); }`
- implement runnable inerface and then instantiate an object of the class.
- we need to override the run() method into our class which is the only method that needs to be implemented.
- Steps to implement:-
  - An object of thread class is created by passing a runnable object as argument to the thread constructor. the thread object now has a runnable object that implements the run() method.
  - The start() method is invoked on the thread object created in the previous step. The start() method returns immediately after a thread has been spawned.
  - thread ends when the run() method ends either by normal completion or by throwing an uncaught exception.

## By extending the thread class
- `public class example extends Threads{ public void run(){...} }`
- all points are same its just that there is no multiple inheritance in java so cannot extend more than one class.

## Thread States
### New
- A thread is in this sate when the instantiation of a thread object creates a new thread but does not start it running.
- A thread starts life in the ready to run state.
- you can call only the start() or stop() methods when the thread is in this state.
- calling any mehod besides start() or stop() causes an Exception.
### Runnable
- when the start method is invoked on a new thread it gets to the runnable state or running state by calling the run() method.
- a runnable thread may actually be running or may be awaiting its turn to run.
### Non-Runnable
- When sleep(int ms) method is invoked and it sleeps for a specified amount of time
- when suspend() method is invoked.
- when the wait() method is invoked and the thread waits for notification of a free resource or waits for the completion of another thread or waits to acquire a lock of an object.
- the thread is blocking on io and waits for irs completion.
### Dead
thread enters this state twhen the run method has finished executing or when the srop method is invoked . Once in this state, the thread cannot ever run again.
## Thread Priority
we can specify priority of each threads and ones with higher priority get greater access to available resources than lower ones.
- setPriority() method is used to modify threads priority at any time.
- getPriority() method is used to retrieve thread priority value.
- Higher the priority first it will run.
## Thread Synchronisation
When we start two or more threads within a program there may be a situation when multiple threads try to access the same resource.
` synchronized (objectidenitfier){
    //Access shared variables and other shared resources.
}