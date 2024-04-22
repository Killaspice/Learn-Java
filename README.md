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


<h3>Classes: Review</h3>

Java is an object-oriented programming language where every program has at least one class. Programs are often built from many classes and objects, which are the instances of a class.

Classes define the state and behavior of their instances. Behavior comes from methods defined in the class. State comes from instance fields declared inside the class.

Classes are modeled on the real-world things we want to represent in our program. Later we will explore how a program can be made from multiple classes. For now, our programs are a single class.

```
public class Dog {
  String breed;
  boolean hasOwner;
  int age;
  
  public Dog(String dogBreed, boolean dogOwned, int dogYears) {
    System.out.println("Constructor invoked!");
    breed = dogBreed;
    hasOwner = dogOwned;
    age = dogYears;
  }
  
  public static void main(String[] args) {
    System.out.println("Main method started");
    Dog fido = new Dog("poodle", false, 4);
    Dog nunzio = new Dog("shiba inu", true, 12);
    boolean isFidoOlder = fido.age > nunzio.age;
    int totalDogYears = nunzio.age + fido.age;
    System.out.println("Two dogs created: a " + fido.breed + " and a " + nunzio.breed);
    System.out.println("The statement that fido is an older dog is: " + isFidoOlder);
    System.out.println("The total age of the dogs is: " + totalDogYears);
    System.out.println("Main method finished");
  }
}
```



<h2>Conditions & Control flow</h2>


<h3>If-Then-Else-If</h3>

The conditional structure we’ve learned can be chained together to check as many conditions as are required by our program.

Imagine our program is now selecting the appropriate course for a student. We’ll check their submission to find the correct course enrollment.

The conditional statement now has multiple conditions that are evaluated from the top down:

```
String course = "Theatre";

if (course.equals("Biology")) {

  // Enroll in Biology course

} else if (course.equals("Algebra")) {

  // Enroll in Algebra course

} else if (course.equals("Theatre")) {

  // Enroll in Theatre course

} else {

  System.out.println("Course not found!");

}

The first condition to evaluate to true will have that code block run. Here’s an example demonstrating the order:

int testScore = 72;

if (testScore >= 90) {

  System.out.println("A");

} else if (testScore >= 80) {

  System.out.println("B");

} else if (testScore >= 70) {

  System.out.println("C");

} else if (testScore >= 60) {

  System.out.println("D");

} else {

  System.out.println("F");

}
// prints: C
```

This chained conditional statement has two conditions that evaluate true. Because testScore >= 70 comes before testScore >= 60, only the earlier code block is run.

Note: Only one of the code blocks will run.





<h3>Nested Conditional Statements</h3>

We can create more complex conditional structures by creating nested conditional statements, which is created by placing conditional statements inside other conditional statements:


```
if (outer condition) {
  if (nested condition) {
    Instruction to execute if both conditions are true
  }
}
When we implement nested conditional statements, the outer statement is evaluated first. If the outer condition is true, then the inner, nested statement is evaluated.

Let’s create a program that helps us decide what to wear based on the weather:

int temp = 45;
boolean raining = true;

if (temp < 60) {
  System.out.println("Wear a jacket!");
  if (raining == true) {
    System.out.println("Bring your umbrella.");
  } else {
    System.out.println("Leave your umbrella home.");
  }
}
```


In the code snippet above, our compiler will check the condition in the first if-then statement: temp < 60. Since temp has a value of 45, this condition is true; therefore, our program will print Wear a jacket!.

Then, we’ll evaluate the condition of the nested if-then statement: raining == true. This condition is also true, so Bring your umbrella is also printed to the screen.

Note that, if the first condition was false, the nested condition would not be evaluated.




<h3>Switch Statement</h3>

An alternative to chaining if-then-else conditions together is to use the switch statement. This conditional will check a given value against any number of conditions and run the code block where there is a match.

Here’s an example of our course selection conditional as a switch statement instead:

```
String course = "History";

switch (course) {
  case "Algebra": 
    // Enroll in Algebra
    break; 
  case "Biology": 
    // Enroll in Biology
    break;
  case "History": 
    // Enroll in History
    break;
  case "Theatre":
    // Enroll in Theatre
    break;
  default:
    System.out.println("Course not found");
}
```

This example enrolls the student in History class by checking the value contained in the parentheses, course, against each of the case labels. If the value after the case label matches the value within the parentheses, the switch block is run.

In the above example, course references the string "History", which matches case "History":.

When no value matches, the default block runs. Think of this as the else equivalent.

Switch blocks are different than other code blocks because they are not marked by curly braces and we use the break keyword to exit the switch statement.

Without break, code below the matching case label is run, including code under other case labels, which is rarely the desired behavior.

```
String course = "Biology";

switch (course) {
  case "Algebra": 
    // Enroll in Algebra
  case "Biology": 
    // Enroll in Biology
  case "History": 
    // Enroll in History
  case "Theatre":
    // Enroll in Theatre
  default:
    System.out.println("Course not found");
}

// enrolls student in Biology... AND History and Theatre!
```


<h3>Review</h3>

Before this lesson, our code executed from top to bottom, line by line.

Conditional statements add branching paths to our programs. We use conditionals to make decisions in the program so that different inputs will produce different results.

Conditionals have the general structure:

```
if (condition) {
    // consequent path
} else {
    // alternative path
}
```

Specific conditional statements have the following behavior:

if-then:
code block runs if condition is true
if-then-else:
one block runs if conditions is true
another block runs if condition is false
if-then-else chained:
same as if-then but an arbitrary number of conditions
switch:
switch block runs if condition value matches case value




<br>
<br>


<h2>CONDITIONAL OPERATORS</h2>

Introduction to Conditional Operators

Java includes operators that only use boolean values. These conditional operators help simplify expressions containing complex boolean relationships by reducing multiple boolean values to a single value: true or false.

For example, what if we want to run a code block only if multiple conditions are true. We could use the AND operator: &&.

Or, we want to run a code block if at least one of two conditions are true. We could use the OR operator: ||.

Finally, we can produce the opposite value, where true becomes false and false becomes true, with the NOT operator: !.

Understanding these complex relationships can feel overwhelming at first. Luckily, truth tables, like the ones seen to the right, can assist us in determining the relationship between two boolean-based conditions.

In this lesson, we’ll explore each of these conditional operators to see how they can be implemented into our conditional statements.





<h3>Combining Conditional Operators</h3>

We have the ability to expand our boolean expressions by using multiple conditional operators in a single expression.

For example:

boolean foo = true && !(false || !true)

How does an expression like this get evaluated by the compiler? The order of evaluation when it comes to conditional operators is as follows:

Conditions placed in parentheses - ()
NOT - !
AND - &&
OR - ||
Using this information, let’s dissect the expression above to find the value of foo:

true && !(false || !true)

First, we’ll evaluate (false || !true) because it is enclosed within parentheses. Following the order of evaluation, we will evaluate !true, which equals false:

true && !(false || false)

Then, we’ll evaluate (false || false) which equals false. Now our expression looks like this:

true && !false

Next, we’ll evaluate !false because it uses the NOT operator. This expression equals true making our expression the following:

true && true

true && true evaluates to true; therefore, the value of foo is true.



<h3>Review</h3>

Conditional operators work on boolean values to simplify our code. They’re often combined with conditional statements to consolidate the branching logic.

Conditional-AND, &&, evaluates to true if the booleans on both sides are true.

```
if (true && false) {
  System.out.println("You won't see me print!");
} else if (true && true) {
  System.out.println("You will see me print!");
}
```

Conditional-OR, ||, evaluates to true if one or both of the booleans on either side is true.

```
if (false || false) {
  System.out.println("You won't see me print!");
} else if (false || true) {
  System.out.println("You will see me print!");
}
```

Logical-NOT, !, evaluates to the opposite boolean value to which it is applied.

```
if (!false) {
  System.out.println("You will see me print!");
}
```











</body>
