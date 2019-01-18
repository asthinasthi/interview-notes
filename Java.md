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

