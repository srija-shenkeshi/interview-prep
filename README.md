# Java FAQs

## Instance Variable:----->
A class variable without a static modifier known as an instance variable is typically shared by all instances of the class. 
These variables can have distinct values among several objects. 
The contents of an instance variable are completely independent of one object instance from another because they are related to a specific object instance of the class.

## Class Variable:----->
Class Variable can be declared anywhere at the class level using the keyword static. 
These variables can only have one value when applied to various objects. These variables can be shared by all class members since they are not connected to any specific object of the class.

## static variable:----->
The static keyword is used to share the same variable or method of a given class. 
Static variables are the variables that once declared then a single copy of the variable is created and shared among all objects at the class level.

## difference between the methods sleep() and wait()----->



| Sleep()                                                    |                                                                    Wait() |
| :--------------------------------------------------------- | ------------------------------------------------------------------------: |
| The sleep() method belongs to the thread class.            |      Wait() method belongs to the object class. |
| Sleep wont release the lock that the current thread holds. |     wait() release the lock which allows other threads to acquire it. |
| This method is a static method.                            |      This method is not a static method. |
| Sleep() does not throw an InterruptedException.            | will throw InterruptedException when thread is interrupted while waiting. |
| used to delay a thread for some time duration.             |           Mainly used to pause a thread until notified by another thread. |


## differences between StringBuffer and StringBuilder----->

| StringBuffer                                                        |                                            StringBuilder |
| :------------------------------------------------------------------ | -------------------------------------------------------: |
| StringBuffer provides functionality to work with the strings.       | StringBuilder is a class used to build a mutable string. |
| It is thread-safe                                                   |             It is not thread-safe |
| (two threads can't call the methods of StringBuffer simultaneously) |          (two threads can call the methods concurrently) |
| Comparatively slow as it is synchronized.                           |         Being non-synchronized, implementation is faster |

mutable- changed
immutable- unchanged

## Which among String or String Buffer should be preferred when there are a lot of updates required to be done in the data?
The string is preferred over StringBuffer as StringBuilder is faster than StringBuffer,
but StringBuffer objects are the preferred over as it provides more thread safety.

## What are the various access specifiers in Java?----->
Access specifiers are the keywords which are used to define the access scope of the method, class, or a variable. 

Public - The classes, methods, or variables which are defined as public, can be accessed by any class or method.
Protected - Protected can be accessed by the class of the same package, or by the sub-class of this class, or within the same class.
Default-  Default are accessible within the package only. By default, all the classes, methods, and variables are of default scope.
Private - The private class, methods, or variables defined as private can be accessed within the class only.


## Class------>
A class in Java is a set of objects which shares common characteristics/ behavior and common properties/ attributes. 
It is a user-defined blueprint or prototype from which objects are created.

## What is an object?----->
The Object is the real-time entity having some state and behavior.
Object is an instance of the class having the instance variables as the state of the object and the methods as the behavior of the object. 
The object of a class can be created by using the new keyword.

## What is the constructor?
The constructor can be defined as the special type of method that is used to initialize the state of an object. 
It is invoked when the class is instantiated

## What is an Interface?
It is a collection of static final variables and abstract methods.
Any class that implements an interface is required to implement a specific set of methods.
->all variables are final and static by default
->all methods are public abstract by default

## What is a marker interface?
An Interface is recognized as an **empty interface** (no field or methods) it is called a marker interface. 
Examples of marker interfaces are Serializable, Cloneable, and Remote interfaces. 
primarily used to mark or flag classes with specific characteristics or behaviors without adding any methods or fields. 
It provides a way to convey information to the compiler or runtime about the intended behavior of a class

## What are the differences between abstract class and interface?

| Abstract Class                                                            |                                           Interface Class |
| :------------------------------------------------------------------------ | --------------------------------------------------------: |
| Both abstract and non-abstract methods may be found in an abstract class. |             The interface contains only abstract methods. |
| Abstract Class supports Final methods.                                    |       The interface class does not support Final methods. |
| Multiple inheritance is not supported by the Abstract class.              |    Multiple inheritances is supported by Interface Class. |
| Abstract Keyword is used to declare Abstract class.                       | Interface Keyword is used to declare the interface class. |
| extend keyword is used to extend an Abstract Class.                       |    implements Keyword is used to implement the interface. |
| Abstract Class has members like protected, private, etc.                  |                  All class members are public by default. |


## data encapsulation
it bundles data and methods that operate on that data within a single unit. 
Encapsulation is achieved by declaring the instance variables of a class as private, which means they can only be accessed within the class.

## Inheritance.
When an object that belongs to a subclass acquires all the properties and behavior of a parent object that is from the superclass, it is known as inheritance.
Inheritance provides code reusability.

## Polymorphism?
the ability to take more than one form.
It is of two types namely, Compile time polymorphism or method overloading- a function called during compile time.
Run time polymorphism or method overriding- links during run time.

## What is method overriding?
also known as run time polymorphism is one where the child class contains the same name and parameters as the parent class.

## Method Overloading in Java
When a class has two or more methods by the same name but different parameters

## Can we override the static method?
No, as static methods are part of the class rather than the object so we can't override them.

## Can we override the overloaded method?
Yes, since the overloaded method is a completely different method in the eyes of the compiler. 
Overriding isn't the same thing at all. The decision as to which method to call is deferred to runtime.

## What is Abstraction?
act of representing essential features without including background details. The detailed information or the implementation is hidden.

## When Abstract methods are used?
when we want to use a method but want to child classes to decide the implementation in that case we use Abstract methods with the parent classes.

## What is Collection Framework in Java?
collection framework is a set of interfaces and classes that are used to represent and manipulate collections of objects in a variety of ways. 
The collection framework contains classes(ArrayList, Vector, LinkedList, PriorityQueue, TreeSet) and multiple interfaces (Set, List, Queue, Deque) 
where every interface is used to store a specific type of data.

## Map
used for mapping values in the form of a key-value form. The map contains all unique keys.

One-to-one mapping occurs in map().
One-to-many mapping occurs in flatMap().


## HashMap: 
HashMap is not synchronized. One key can be a NULL value. faster

Unordered: The HashMap does not guarantee any specific order of the keys or values.

Allows nulls: HashMap allows one null key and multiple null values.

Non-synchronized: It is not thread-safe. If multiple threads access a HashMap concurrently and at least one of the threads modifies the map structurally, it must be synchronized externally.


## Set
don't store duplicate elements. They don't keep any order of the elements. 

## HashSet: 
stores the elements in a has table which provides faster lookups and faster insertion. HashSet is not ordered.
## LinkedHashSet: 
implementation of HashSet which maintains the insertion order of the elements.
## TreeSet: 
stores the elements in a sorted order that is determined by the natural ordering of the elements.

## difference between Comparable and Comparator?

| Comparable                                              |                            Comparator (functioanl interface)     |
| :------------------------------------------------------ | ---------------------------------------------------------------: |
| The interface is present in java.lang package.          |                   The Interface is present in java.util package. |
| Provides compareTo() method to sort elements.           |                   Provides compare() method to sort elements.    |
| It provides single sorting sequences.                   |                    It provides multiple sorting sequences.       |
| Method sorts the data according to fixed sorting order. | Method sorts the data according to the customized sorting order. |
| It affects the original class.                          |                    It doesn't affect the original class.         |



## difference between Set and Map?

|               Set                                                       |     Map                        |
| :-------------------------------------------------------- | ----------------------------------------------: |
| The Set interface is implemented using java.util package. | The map is implemented using java.util package. |
| It can extend the collection interface.                   |    It does not extend the collection interface. |
| It does not allow duplicate values.                       |                     It allows duplicate values. |
| The set can sort only one null value.                     |          The map can sort multiple null values. |

## Exception Handling?
An Exception is an Event that interrupts the normal flow of the program and requires special processing.

try: The block of code that might throw an exception.

catch: The block of code that handles the exception.

finally: The block of code that executes regardless of whether an exception was thrown or not.

throw: Used to explicitly throw an exception.

throws: Declares that a method can throw an exception.

**Built-in exceptions:** These exceptions can be further divided into two subcategories i.e., checked and unchecked Exceptions.
Below are some of the built-in exceptions in Java:
ArrayIndexOutOfBoundsExceptions, ClassNotFoundException, FileNotFoundException, IOException
NullPointerException, ArithmeticException, InterruptedException, RuntimeException

**User-defined exceptions:** are defined by the programmers themselves to handle some specific situations or errors which are not covered by built-in exceptions.
To define user-defined exceptions a new class that extends the appropriate exception class must be defined.

## Difference between an Error and an Exception.

|                Errors                                                     |            Exceptions             |
| :--------------------------------------------------------- | --------------------------------------------------------------: |
| Recovering from Errors is not possible.                    |              Recovery by try-catch block or throwing exceptions |
| Errors are all unchecked types in Java.                    | It includes both checked as well as unchecked types that occur. |
| Errors are mostly caused by the environment while running. |       The program is mostly responsible for causing exceptions. |
| Errors can occur at compile time as well as run time.      |     checked exceptions at compiler time & unchecked at runtime. |

Compile Time: Syntax Error, Run Time: Logical Error.


Examples: java.lang.StackOverflowError, java.lang.OutOfMemoryError            |Checked Exceptions: SQLException, IOException Unchecked 
                                                                                 Exceptions:ArrayIndexOutOfBoundException, NullPointerException, ArithmeticExceptio

## difference between Checked Exception and Unchecked Exception?

Checked Exceptions are the exceptions that are checked during compile time of a program. 
In a program, if some code within a method throws a checked exception, then the method must either handle the exception 
or must specify the exception using the throws keyword. 

Unchecked are the exceptions that are not checked at compile time of a program. Exceptions under Error and RuntimeException classes are 
unchecked exceptions, everything else under throwable is checked.

## Multithreaded program?
Multithreaded programs in Java contain threads that run concurrently instead of running sequentially
advantages: Resource Sharing, scalability, Better Communication, Minimized system resource use

## What are the two ways in which Thread can be created?
By extending the Thread class
By implementing a Runnable interface.

## What is a thread?
Threads in Java are subprocess with lightweight with the smallest unit of processes and also has separate paths of execution.
These threads use shared memory but they act independently hence if there is an exception in threads that do not affect the working of other threads
despite them sharing the same memory.

## What is a daemon thread?
A daemon thread in Java is a low-priority thread that is used to perform background operations or tasks 
which are used to perform continuously. such as Garbage collection

## Garbage Collection is necessary in Java?
Garbage collection is necessary to avoid memory leaks which can cause the program to crash and become unstable. 
There is no way to avoid garbage collection in Java. 


### JAVA 8 features

## Lambda Expressions
Lambda expression helps us to write our code in functional style.
It provides a clear and concise way to implement SAM interface(Single Abstract Method) by using an expression.

## Method References
shorthand notation of a lambda expression to call a method.

Each time when you are using lambda expression to just referring a method, you can replace your lambda expression with method reference.

## Functional Interface
An Interface that contains only one abstract method is known as functional interface. 
It can have any number of default and static methods. 
It can also declare methods of object class.
Functional interfaces are also known as Single Abstract Method Interfaces (SAM Interfaces).

## forEach
Java provides a new method forEach() to iterate the elements. It is defined in Iterable and Stream interfaces.
It is a default method defined in the Iterable interface. Collection classes which extends Iterable interface can use forEach() method to iterate elements.

## Stream API
Stream API is introduced in Java 8 and is used to process collections of objects with the functional style of coding using the lambda expression.
It performs lazy computation. So, it executes only when it requires.

## Optional
Java introduced a new class Optional in Java 8. It is a public final class which is used to deal with NullPointerException in Java application. 
We must import java.util package to use this class. It provides methods to check the presence of value for particular variable.

## Default Methods
Java provides a facility to create default methods inside the interface. 
Methods which are defined inside the interface and tagged with default keyword are known as default methods. 
These methods are non-abstract methods and can have method body.

Default methods allow interfaces to have methods with a default implementation that can be overridden by implementing classes.

## Singleton design pattern
define a class that has only one instance and provides a global point of access to it
In other words, a class must ensure that only single instance should be created and single object can be used by all other classes.

There are two forms of singleton design pattern
Early Instantiation: creation of instance at load time.
Lazy Instantiation: creation of instance when required.

## How to create Singleton design pattern?
Static member: It gets memory only once because of static, it contains the instance of the Singleton class.

Private constructor: It will prevent to instantiate the Singleton class from outside the class.

Static factory method: This provides the global point of access to the Singleton object and returns the instance to the caller.

public class Singleton {
    // Eagerly created instance of Singleton
    private static final Singleton instance = new Singleton();

    // Private constructor prevents instantiation from other classes
    private Singleton() {}

    // Public method to provide access to the instance
    public static Singleton getInstance() {
        return instance;
    }
}


## Interfaces Diamond problem Multiple inheritance

 Resolving the conflict by overriding the start method
    @Override
    public void start() {
        // We can choose to call one of the default methods explicitly
        Vehicle.super.start();
+
