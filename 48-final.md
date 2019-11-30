# Garbage Collection
- In java destruction of object from emory is done aytomatically by the JVM.
- No delete keyword in java
- when there is no reference to an object, then that object is assumed to be no longer needed and the memory occupied by the object are released this is known as garbage collection done by JVM.

## JVM threads
whenever we run a java program, JVM has 3 threads namely:-
- main threads.
  The task of main thread is to execute the main method.
- thread scheduler
the task of thread scheduler is to schedule the threads.
- garbage collector
The task of garbage collector thread is to sweep abandoned objects from the heap memory.

## Finalize Method
- That means clean up operations which you have kept in the finalize method are executed before an object is destroyed from the memory.
- Garbage collector thread calls finalize method only once for one object.
- there are no distructors in java.
- finalize() method is a protected an non-static method of java.lang.Object class.
-` protected void finalize() throws Throwable{
	...// Syntax goes same ....
}`
- Garbage collector thread before sweeping out an abandoned object it calles finalize() method of that object.
- We can call finalize method explicitly on an object before it is abandoned.
- When we call only operations kept in finalize() method are performed on an object.
- Object will not be destroyed from the memory.
- Exceptions occured in finalize method are not propagated . they are ignored by the garbage collector.
- finalize methods are not chained like constructors ie there is no calling statement to super class finalize method inside the subclass . You need to explicitly call suyper class finalize method.

# Graphical User interface.
There are two sets of java API for graphics programming 
- Abstract Window Toolkit
- Swing.
### Classes in AWT
- GUI component classes as Button ,TextField, Label
- GUI container classes ( frame, panel, dailog and ScrollPane)
- Layout managers ( FlowLayout, BorderLayout and Grid Layout)
- Custom graphics classes (such as graphics, color and font)

