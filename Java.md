# interview-notes
Notes for Interviews

# Java
https://stackoverflow.com/questions/40480/is-java-pass-by-reference-or-pass-by-value
It's perfectly valid to follow an address and change what's at the end of it; that does not change the variable, however.
Priority Queue ?
- No multiple inheritance in Java because of diamond problem

## Composition
     - has a relationship
     
```
class Person { 
private Job job = new Job();
public int getSalary(){
   job.getSalary(); 
}}
```
  - Job salary class can change any time without affecting Person class. 

## Dependency Injection / IOC
- Spring like framework handles object creation instead of sending and passing around objects
https://stackoverflow.com/questions/9403155/what-is-dependency-injection-and-inversion-of-control-in-spring-framework

## Java8
- Interfaces can have static methods
- forEach method is in the Iterable interface
- forEach accepts a Consumer class
- static methods of Interfaces have to be overridden if multiple interfaces are being implemented

## Database/ORM
- Entity: Class representation of tables
- DAO: queries, findAll, persist etc.
- Controller/Service: Multiple queries or coordination between DAO's

## Java Memory
1. Stack : 
Local variables, Thread specific variables of a method etc.
Every method invocation gets its own stack
2. Heap :
Young Generation. Old Generation, etc. Store objects/instantiation of classes.
3. Permanent Generation: Static classes

## Threading & Parallelization
1. Single Lane Bridge Problem: https://orajavasolutions.wordpress.com/2014/05/03/single-lane-bridge-problem/
1. `t1.join()` Main Thread waits till thread completes. Thread might have already finished/died. If finished it will return immediately. Catch `InterruptedException` 
1. Runnable vs Callable: The Callable interface is similar to Runnable, in that both are designed for classes whose instances are potentially executed by another thread. A Runnable, however, does not return a result and cannot throw a checked exception.

## Exceptions
1. Unchecked/Runtime Exceptions : NullPointerException, Arithmetic Exception.
2. Checked Exceptions: Thrown or caught. 
```
           +-----------+
           | Throwable |
                   +-----------+
                    /         \
           /           \
          +-------+          +-----------+
          | Error |          | Exception |
          +-------+          +-----------+
       /  |  \           / |        \
         \________/      \______/         \
                            +------------------+
    unchecked     checked    | RuntimeException |
                    +------------------+
                      /   |    |      \
                     \_________________/
                       
                       unchecked
```

<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3169.0561694030494!2d-122.30943068463222!3d37.41214724071236!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x808fa71b47e4d187%3A0xba6e6955322acb04!2sEl+Corte+de+Madera+Creek+Preserve!5e0!3m2!1sen!2sus!4v1552763019593" width="600" height="450" frameborder="0" style="border:0" allowfullscreen></iframe>
