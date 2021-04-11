# What are the components of Java Architecture?

Below mentioned pointers will be our topics of discussion:

- What is Java Architecture?
- Components of Java
- How is Java platform independent?
- JIT in Java

Let us begin by understanding what exactly is Java Architecture?

### What is Java Architecture?

Here, I will explain you the java architecture in simple steps.

- In Java, there is a process of compilation and interpretation.
- The code written in Java, is converted into byte codes which is done by the Java Compiler.
- The byte codes, then are converted into machine code by the JVM.
- The Machine code is executed directly by the machine.

This diagram illustrates the internal working of a Java code, or precisely, Java Architecture!

<img src="sources/1.png" width="350" height="350">

## Components of Java Architecture

There are three main components of Java language: JVM, JRE, and JDK.

Java Virtual Machine, Java Runtime Environment and Java Development Kit respectively.

Let me elaborate each one of them one by on.


### Java Virtual Machine:

Ever heard about WORA? (Write once Run Anywhere).  Well, Java applications are called WORA because of their ability to run a code on any platform. This is done only because of JVM. The JVM is a Java platform component that provides an environment for executing Java programs. JVM interprets the bytecode into machine code which is executed in the machine in which the Java program runs.

So, in a nutshell, JVM performs the following functions:

- Loads the code
- Verifies the code
- Executes the code
- Provides runtime environment

Now, let me show you the JVM architecture. Here goes!

<img src="sources/2.png" width="350" height="350">

## Explanation:

<b>Class Loader:</b> Class loader is a subsystem of JVM. It is used to load class files. Whenever we run the java program, class loader loads it first.

<b>Class method area:</b> It is one of the Data Area in JVM, in which Class data will be stored. Static Variables, Static Blocks, Static Methods, Instance Methods are stored in this area.

<b>Heap:</b> A heap is created when the JVM starts up. It may increase or decrease in size while the application runs.

<b>Stack:</b> JVM stack is known as a thread stack. It is a data area in the JVM memory which is created for a single execution thread. The JVM stack of a thread is used by the thread to store various elements i.e.; local variables, partial results, and data for calling method and returns.

<b>Native stack:</b> It subsumes all the native methods used in your application.

## Execution Engine:

- JIT compiler
- Garbage collector

<b>JIT compiler:</b> The Just-In-Time (JIT) compiler is a part of the runtime environment. It helps in improving the performance of Java applications by compiling bytecodes to machine code at run time. The JIT compiler is enabled by default. When a method is compiled, the JVM calls the compiled code of that method directly. The JIT compiler compiles the bytecode of that method into machine code, compiling it “just in time” to run.

<b>Garbage collector:</b> As the name explains that Garbage Collector means to collect the unused material. Well, in JVM this work is done by Garbage collection. It tracks each and every object available in the JVM heap space and removes unwanted ones.
Garbage collector works in two simple steps known as Mark and Sweep:

- Mark – it is where the garbage collector identifies which piece of memory is in use and which are not
- Sweep – it removes objects identified during the “mark” phase.

<b>Java Runtime Environment:</b>
The JRE software builds a runtime environment in which Java programs can be executed. The JRE is the on-disk system that takes your Java code, combines it with the needed libraries, and starts the JVM to execute it. The JRE contains libraries and software needed by your Java programs to run. JRE is a part of JDK (which we will study later) but can be downloaded separately.

<b>Java Development Kit:</b>
The Java Development Kit (JDK) is a software development environment used to develop Java applications and applets. It contains JRE and several development tools, an interpreter/loader (java), a compiler (javac), an archiver (jar), a documentation generator (javadoc) accompanied with another tool.

<img src="sources/3.png" width="350" height="350">

The blue area shown in the diagram is JDK. Now, let me elaborate the development tools to you all.

<b>java :</b> it is the launcher for all the java applications.
<b>javac :</b> complier of the java programming languages.
<b>javadoc:</b> it is the API documentation generator.
<b>jar:</b> creates and manage all the JAR files.

Moving ahead with Java architecture, let us understand how Java platform is independent?

## How is Java platform independent?

When is any programming language called as platform-independent? Well, if and only if it can run on all available operating systems with respect to its development and compilation.
Now, Java is platform-independent just because of the bytecode. Let me tell you what exactly is a bytecode? In simple terms,
Bytecode is a code of the JVM which is machine-understandable.
Bytecode execution in Java proves it is a platform-independent language.
Here, I will show you the steps involved in the process of java bytecode execution.

<img src="sources/4.png" width="350" height="350">

Below is the explanation of the steps involved:

```
sample.java → javac (sample. class) → JVM(sample.obj) → final output
```

First source code is used by java compiler and is converted in .class file. The class file code is in byte code form and that class file is used by JVM to convert into an object file. After that, you can see the final output on your screen.


Moving ahead in Java architecture article, let us understand the concept of JIT in Java.

## JIT in Java
Just In Time compiler commonly known as JIT, is basically responsible for performance optimization of java based applications at run time. The performance of an application is dependent on a compiler.
Here is a simple diagram showing you the internal process going on.

<img src="sources/5.png" width="350" height="350">

The JIT compiler compiles the byte code of the method into machine code, compiling it “Just In Time” to run. When a method is compiled, the JVM calls the compiled code of that method directly.
Let’s dive deeper:
The byte code has to be interpreted or compiled to proper machine instructions depending on the instruction set provided. Also, these can be directly executed if the instruction architecture is byte code based. Interpreting the byte code affects the speed of execution.
In order to improve performance, JIT compilers interact with the Java Virtual Machine (JVM) at run time and compile suitable bytecode sequences into native machine code (as shown in the diagram). While using a JIT compiler, the hardware is able to execute the native code, as compared to having the JVM interpret the same sequence of bytecode repeatedly and incurring overhead for the translation process.

With this, I have reached towards the end of this article on Java Architecture. I hope the above-discussed topics added value to your Java knowledge. Stay tuned for more articles!

Now that you have understood basics of Java, check out the Java Training by Edureka, a trusted online learning company with a network of more than 250,000 satisfied learners spread across the globe. Edureka’s Java J2EE and SOA training and certification course is designed for students and professionals who want to be a Java Developer. The course is designed to give you a head start into Java programming and train you for both core and advanced Java concepts along with various Java frameworks like Hibernate & Spring.

Got a question for us? Please mention it in the comments section of this “Java Architecture and its components” blog and we will get back to you as soon as possible.# java-architecture
