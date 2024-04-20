# Learn-Java
<body>

  <h3>Introduction to Java</h3>

Welcome to the world of Java programming!

Programming languages enable humans to write instructions that a computer can perform. With precise instructions, computers coordinate applications and systems that run the modern world.

Sun Microsystems released the Java programming language in 1995. Java is known for being simple, portable, secure, and robust. Though it was released over twenty years ago, Java remains one of the most popular programming languages today.

One reason people love Java is the Java Virtual Machine, which ensures the same Java code can be run on different operating systems and platforms. Sun Microsystems’ slogan for Java was “write once, run everywhere”.

Java Virtual Machine running Java on three different platforms

Programming languages are composed of syntax, the specific instructions which Java understands. We write syntax in files to create programs, which are executed by the computer to perform the desired task.

Let’s start with the universal greeting for a programming language. We’ll explore the syntax in the next exercise.


<h3>Hello Java File!</h3>

Java runs on different platforms, but programmers write it the same way. Let’s explore some rules for writing Java.

In the last exercise, we saw the file HelloWorld.java. Java files have a .java extension. Some programs are one file, others are hundreds of files!

Inside HelloWorld.java, we had a class:

```
public class HelloWorld {
  
}
```

We’ll talk about classes more in the future, but for now think of them as a single concept.

The HelloWorld concept is: Hello World Printer. Other class concepts could be: Bicycle, or: Savings Account.

We marked the domain of this concept using curly braces: {}. Syntax inside the curly braces is part of the class.

Each file has one primary class named after the file. Our class name: HelloWorld and our file name: HelloWorld. Every word is capitalized.

Inside the class we had a main() method which lists our program tasks:

```
public static void main(String[] args) {

}
```


Like classes, we used curly braces to mark the beginning and end of a method.

public, static, and void are syntax we’ll learn about in future lessons. String[] args is a placeholder for information we want to pass into our program. This syntax is necessary for the program to run but more advanced than we need to explore at the moment.

Our program also displayed the text "Hello World" on the screen. This was accomplished using a print statement:

```
System.out.println("Hello World");
```

We’ll learn more about print statements in the next exercise!



<h2>Print Statements</h2>

Let’s take a closer look at this instruction from our previous program:

```
System.out.println("Hello World");
```

Print statements output information to the screen (also referred to as the output terminal). Let’s break this line of code down a little more. Don’t worry if some of the terms here are new to you. We’ll dive into what all of these are in much more detail later on!

System is a built-in Java class that contains useful tools for our programs.
out is short for “output”.
println is short for “print line”.
We can use System.out.println() whenever we want the program to create a new line on the screen after outputting a value:

```
System.out.println("Hello World");
System.out.println("Today is a great day to code!");
```

After "Hello World" is printed, the output terminal creates a new line for the next statement to be outputted. This program will print each statement on a new line like so:

```
Hello World
Today is a great day to code!
```

We also can output information using System.out.print(). Notice that we’re using print(), not println(). Unlike System.out.println(), this type of print statement outputs everything on the same line. For example:

```
System.out.print("Hello ");
System.out.print("World");
```

The above code will have the following output:

```
Hello World
```

In this example, if you were to use print() or println() again, the new text will print immediately after World on the same line. <strong>It’s important to remember where you left your program’s “cursor”</strong>. If you use println() the cursor is moved to the next line. If you use print() the cursor stays on the same line.

Note: Going forward after this exercise, all exercises will use System.out.println() to output values. You will get to practice using System.out.print() statements in the Checkpoints below, however.








<h2>Introduction to Classes</h2>

All programs require one or more classes that act as a model for the world.

For example, a program to track student test scores might have Student, Course, and Grade classes. Our real-world concerns, students and their grades, are inside the program as classes.

We represent each student as an instance, or object, of the Student class.

This is object-oriented programming because programs are built around objects and their interactions. An object contains state and behavior.

<img src= "https://content.codecademy.com/courses/learn-java/revised-2019/diagram%20of%20an%20object-01.png"> 


Classes are a blueprint for objects. Blueprints detail the general structure. For example, all students have an ID, all courses can enroll a student, etc.

An instance is the thing itself. This student has an ID of 42, this course enrolled that student, etc.

Let’s review with another example, a savings account at a bank.

What should a savings account know?

The balance of money available.
What should a savings account do?

Deposit money.
Withdraw money.

<img src= "https://content.codecademy.com/courses/learn-java/revised-2019/diagram%20of%20an%20object-02.png">


Imagine two people have accounts that are instances of the SavingsAccount class. They share behavior (how they deposit and withdraw) but have individual state (their balances), and even with the same balance amount these accounts are separate entities.











</body>
