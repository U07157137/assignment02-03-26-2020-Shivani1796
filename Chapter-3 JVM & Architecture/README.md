# Content

* [What is JVM?](#What-is-JVM-?)
* [How JVM Works?](#How-JVM-Works-?)



## What is JVM?
Java Virtual Machine (JVM) is a engine that provides runtime environment to drive the Java Code or applications. It converts Java bytecode into machines language. JVM is a part of Java Run Environment (JRE).
In other programming languages, the compiler produces machine code for a particular system. However, Java compiler produces code for a Virtual Machine known as Java Virtual Machine. 
It is :
1) A specification where working of Java Virtual Machine is specified. But implementation provider is independent to choose the algorithm. Its implementation has been provided by Oracle and other companies.
2) An implementation Its implementation is known as JRE (Java Runtime Environment).
3) Runtime Instance Whenever you write java command on the command prompt to run the java class, an instance of JVM is created.

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/master/Chapter-3%20JVM%20%26%20Architecture/jvm.png">
</p>

## How JVM Works?
First, Java code is complied into bytecode. This bytecode gets interpreted on different machines
Between host system and Java source, Bytecode is an intermediary language.
JVM is responsible for allocating memory space. When we compile a .java file, .class files(contains byte-code) with the same class names present in .java file are generated by the Java compiler. This .class file goes into various steps when we run it. These steps together describe the whole JVM.
<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/master/Chapter-3%20JVM%20%26%20Architecture/java-arch.png">
</p>

### Function :

**1) ClassLoader**

The class loader is a subsystem used for loading class files. It performs three major functions viz. Loading, Linking, and Initialization.It is mainly responsible for three activities.

- Loading
- Linking
- Initialization

**2) Method Area**

In method area, all class level information like class name, immediate parent class name, methods and variables information etc. are stored, including static variables. There is only one method area per JVM, and it is a shared resource.

**3) Heap**
All the Objects, their related instance variables, and arrays are stored in the heap. This memory is common and shared across multiple threads.

**4) JVM language Stacks**

Java language Stacks store local variables, and it’s partial results. Each thread has its own JVM stack, created simultaneously as the thread is created. A new frame is created whenever a method is invoked, and it is deleted when method invocation process is complete.

**5)  Program Counter (PC) Registers**

PC register store the address of the Java virtual machine instruction which is currently executing. In Java, each thread has its separate PC register.

**6) Native Method Stacks**

Native method stacks hold the instruction of native code depends on the native library. It is written in another language instead of Java.

**7) Execution Engine**

Execution engine execute the .class (bytecode). It reads the byte-code line by line, use data and information present in various memory area and execute instructions. It can be classified in three parts :-

- *Interpreter* : It interprets the bytecode line by line and then executes. The disadvantage here is that when one method is called multiple times, every time interpretation is required.

- *Just-In-Time Compiler(JIT)* : It is used to increase efficiency of interpreter.It compiles the entire bytecode and changes it to native code so whenever interpreter see repeated method calls,JIT provide direct native code for that part so re-interpretation is not required,thus efficiency is improved.

- *Garbage Collector* : It destroy un-referenced objects.For more on Garbage Collector,refer Garbage Collector.

**8) Native Method interface**

The Native Method Interface is a programming framework. It allows Java code which is running in a JVM to call by libraries and native applications.

**9) Native Method Libraries**

Native Libraries is a collection of the Native Libraries(C, C++) which are needed by the Execution Engine. 
