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


<br>
<br>
<br>

<h2>Introduction to Arrays</h2>

We have seen how to store single pieces of data in variables. What happens when we need to store a group of data? What if we have a list of students in a classroom? Or a ranking of the top 10 horses finishing a horse race?

If we were storing 5 lottery ticket numbers, for example, we could create a different variable for each value:

```
int firstNumber = 4;
int secondNumber = 8;
int thirdNumber = 15;
int fourthNumber = 16;
int fifthNumber = 23;
```

That is a lot of ungainly repeated code. What if we had a hundred lottery numbers? It is more clean and convenient to use a Java array to store the data as a list.

An array holds a fixed number of values of one type. Arrays hold doubles, ints, booleans, or any other primitives. Arrays can also contain Strings as well as object references!

Each index of an array corresponds with a different value. Here is a diagram of an array filled with integer values:

<img src="https://content.codecademy.com/courses/learn-java/revised-2019/array-introduction.png">;

Notice that the indexes start at 0! The element at index 0 is 4, while the element at index 1 is 8. This array has a length of 5, since it holds five elements, but the highest index of the array is 4.

Let’s explore how to create and use arrays in Java, so that we can store all of our Java data types.

<br>
<br>






<h3>Creating an Array Explicitly</h3>

Imagine that we’re using a program to keep track of the prices of different clothing items we want to buy. We would want a list of the prices and a list of the items they correspond to. To create an array, we provide a name and declare the type of data it holds:

```
double[] prices;
```

Just like with variables, we can declare and initialize in the same line. This allows us to explicitly initialize the array to contain the data we want to store :

```
double[] prices = {13.15, 15.87, 14.22, 16.66};
```

We can use arrays to hold Strings and other objects as well as primitives:

```
String[] clothingItems = {"Tank Top", "Beanie", "Funny Socks", "Corduroys"};
```



<br>
<br>



<h3>Importing Arrays</h3>

When we printed out the array we created in the last exercise, we saw a memory address that did not help us understand what was contained in the array.

If we want to have a more descriptive printout of the array itself, we need a toString() method that is provided by the Arrays package in Java.

```
import java.util.Arrays;
```

We put this at the top of the file, before we even define the class!

When we import a package in Java, we are making all of the methods of that package available in our code.

The Arrays package has many useful methods, including Arrays.toString(). When we pass an array into Arrays.toString(), we can see the contents of the array printed out:

```
import java.util.Arrays;

public class Lottery(){
  
  public static void main(String[] args){
    int[] lotteryNumbers = {4, 8, 15, 16, 23, 42};
    String betterPrintout = Arrays.toString(lotteryNumbers);
    System.out.println(betterPrintout);
  }

}
```

This code will print:

[4, 8, 15, 16, 23, 42]

Instructions

1. In order to make our printout of the topics array more helpful, we are going to want to use the toString() method from the Arrays package.

To use it, we first must import the Arrays package from java.util. Import the package at the top of the Newsfeed.java file.

2. Now that you have the Arrays package, use its toString() method to print out the topics array in the main() method.


```
// import the Arrays package here:
import java.util.Arrays;

public class Newsfeed {
  
  
  public Newsfeed(){
    
  }
    
  public String[] getTopics(){
    String[] topics = {"Opinion", "Tech", "Science", "Health"};
    return topics;
  }
  

  public static void main(String[] args){
    Newsfeed sampleFeed = new Newsfeed();
    String[] topics = sampleFeed.getTopics();
    System.out.println(topics);
    System.out.println(Arrays.toString(topics));  // Arrays.toString example
  }
}

```






<br>
<br>

<h3>Get Element By Index</h3>

Now that we have an array declared and initialized, we want to be able to get values out of it.

We use square brackets, [ and ], to access data at a certain index:

```
double[] prices = {13.1, 15.87, 14.22, 16.66};

System.out.println(prices[1]);
```

This command would print:

15.87

This happens because 15.87 is the item at the 1 index of the array. Remember, the index of an array starts at 0 and ends at an index of one less than the number of elements in the array.

If we try to access an element outside of its appropriate index range, we will receive an ArrayIndexOutOfBoundsException error.

For example, if we were to run the command System.out.println(prices[5]), we’d get the following output:

```
java.lang.ArrayIndexOutOfBoundsException: 5
```
<br>
<br>




```

import java.util.Arrays;

public class Newsfeed {
  
  String[] topics = {"Opinion", "Tech", "Science", "Health"};
  int[] views = {0, 0, 0, 0};
  
  public Newsfeed(){

  }
    
  public String[] getTopics(){
    return topics;
  }
  
  public String getTopTopic(){
    return topics[0];
  }
  
  public void viewTopic(int topicIndex){
    views[topicIndex] = views[topicIndex] + 1;
  }

  public static void main(String[] args){
    Newsfeed sampleFeed = new Newsfeed();
    
    System.out.println("The top topic is "+ sampleFeed.getTopTopic());
    
    sampleFeed.viewTopic(1);
    sampleFeed.viewTopic(1);
    sampleFeed.viewTopic(3);
    sampleFeed.viewTopic(2);
    sampleFeed.viewTopic(2);
    sampleFeed.viewTopic(1);
    
    System.out.println("The " + sampleFeed.topics[1] + " topic has been viewed " + sampleFeed.views[1] + " times!"); 
  }
}
```

<br>
<br>

<h3>Creating an Empty Array</h3>


We can also create empty arrays and then fill the items one by one. Empty arrays have to be initialized with a fixed size:

```
String[] menuItems = new String[5];
```

Once you declare this size, it cannot be changed! This array will always be of size 5.

After declaring and initializing, we can set each index of the array to be a different item:

```
menuItems[0] = "Veggie hot dog";
menuItems[1] = "Potato salad";
menuItems[2] = "Cornbread";
menuItems[3] = "Roasted broccoli";
menuItems[4] = "Coffee ice cream";
```

This group of commands has the same effect as assigning the entire array at once:

```
String[] menuItems = {"Veggie hot dog", "Potato salad", "Cornbread", "Roasted broccoli", "Coffee ice cream"};
```

We can also change an item after it has been assigned! Let’s say this restaurant is changing its broccoli dish to a cauliflower one:

```
menuItems[3] = "Baked cauliflower";
```

Now, the array looks like:

["Veggie hot dog", "Potato salad", "Cornbread", "Baked cauliflower", "Coffee ice cream"]

Keep Reading: AP Computer Science A Students

When we use new to create an empty array, each element of the array is initialized with a specific value depending on what type the element is:

Data Type	Initialized Value
int	0
double	0.0
boolean	false
Reference	null
For example, consider the following arrays:

```
String[] my_names = new String[5];
int[] my_ages = new int[5];
```

Because a String is a reference to an Object, my_names will contain five nulls. my_ages will contain five 0s to begin with.

1. We now want a Newsfeed to be able to keep track of a user’s top 10 articles.

We’ve declared a String array called favoriteArticles, but we haven’t initialized it yet.

In the constructor for Newsfeed, set favoriteArticles to be a new empty String array of size 10.


2. Inside the method setFavoriteArticle(), set the value of the favoriteArticles array at index favoriteIndex to be the value of newArticle.

For example, if I called setFavoriteArticle(2, "Celebrity Hands Throughout the Decades"), the value of favoriteArticles at index 2 would be set to "Celebrity Hands Throughout the Decades".

```
import java.util.Arrays;

public class Newsfeed {
  
  String[] topics = {"Opinion", "Tech", "Science", "Health"};
  int[] views = {0, 0, 0, 0};
  String[] favoriteArticles;
  
  public Newsfeed(){
    // Initialize favoriteArticles here:
    favoriteArticles  = new String[10];
  }
  
  public void setFavoriteArticle(int favoriteIndex, String newArticle){
    // Add newArticle to favoriteArticles:
    favoriteArticles[favoriteIndex] = newArticle;
    
  }
    
  public static void main(String[] args){
    Newsfeed sampleFeed = new Newsfeed();
    
    sampleFeed.setFavoriteArticle(2, "Humans: Exterminate Or Not?");
    sampleFeed.setFavoriteArticle(3, "Organic Eye Implants");
    sampleFeed.setFavoriteArticle(0, "Oil News");
    
    System.out.println(Arrays.toString(sampleFeed.favoriteArticles));
  }
}

```
<br>
<br>


<h3>Length</h3>

What if we have an array storing all the usernames for our program, and we want to quickly see how many users we have? To get the length of an array, we can access the length field of the array object:

```
String[] menuItems = new String[5];
System.out.println(menuItems.length);
```

This command would print 5, since the menuItems array has 5 slots, even though they are all empty.

If we print out the length of the prices array:

```
double[] prices = {13.1, 15.87, 14.22, 16.66};

System.out.println(prices.length);
```

We would see 4, since there are four items in the prices array!

In the method getNumTopics(), return the length of the topics array.

```
import java.util.Arrays;

public class Newsfeed {
  
  String[] topics = {"Opinion", "Tech", "Science", "Health"};
  int[] views = {0, 0, 0, 0};
  
  public Newsfeed(){

  }
    
  public String[] getTopics(){
    return topics;
  }
  
  public int getNumTopics(){
    return topics.length;
    
  }
  
  public static void main(String[] args){
    Newsfeed sampleFeed = new Newsfeed();
    
    System.out.println("The number of topics is "+ sampleFeed.getNumTopics());
   
  }
}
```



<h3>String[] args</h3>

When we write main() methods for our programs, we use the parameter String[] args. Now that we know about array syntax, we can start to parse what this means.

A String[] is an array made up of Strings. Examples of String arrays:

```
String[] humans = {"Talesha", "Gareth", "Cassie", "Alex"};
String[] robots = {"R2D2", "Marvin", "Bender", "Ava"};
```

The args parameter is another example of a String array. In this case, the array args contains the arguments that we pass in from the terminal when we run the class file. (So far, args has been empty.)

So how can you pass arguments to main()? Let’s say we have this class HelloYou:

```
public class HelloYou {
  public static void main(String[] args) {
    System.out.println("Hello " + args[0]);  
  }
}
```

When we run the file HelloYou in the terminal with an argument of "Laura":

```
java HelloYou Laura
```
We get the output:

```
Hello Laura
```

The String[] args would be interpreted as an array with one element, "Laura".

When we use args[0] in the main method, we can access that element like we did in HelloYou.


Instructions
<br>
1. We want to give the user an option to make a Newsfeed object for robots or for humans. We will take either "Robot" or "Human" as an argument to the main() method when the Newsfeed.java file is run.

If the args array holds "Human", we will initialize the feed with human topics.
If the args array holds "Robot", we will initialize the feed with robot topics.
Replace the blank in the conditional statement to reflect this expected control flow.


<br>

```
import java.util.Arrays;

public class Newsfeed {
  
  String[] topics;
  
  public Newsfeed(String[] initialTopics) {
		topics = initialTopics;
  }
  
  public static void main(String[] args) {
		Newsfeed feed;
    if (args[0].equals("Human")) {
      
      //topics for a Human feed:
      String[] humanTopics = {"Politics", "Science", "Sports", "Love"};
			feed = new Newsfeed(humanTopics);
      
    } else if(args[0].equals("Robot")) {
      
      //topics for a Robot feed:
      String[] robotTopics = {"Oil", "Parts", "Algorithms", "Love"};
      feed = new Newsfeed(robotTopics);
      
    } else {
      String[] genericTopics = {"Opinion", "Tech", "Science", "Health"};
      feed = new Newsfeed(genericTopics);
    }
        
    System.out.println("The topics in this feed are:");
    System.out.println(Arrays.toString(feed.topics));
  }
}

```




<br>
<br>




<h3>Review</h3>

We have now seen how to store a list of values in arrays. We can use this knowledge to make organized programs with more complex variables.

Throughout the lesson, we have learned about:

Creating arrays explicitly, using { and }.
Accessing an index of an array using [ and ].
Creating empty arrays of a certain size, and filling the indices one by one.
Getting the length of an array using length.
Using the argument array args that is passed into the main() method of a class.



```
import java.util.Arrays;

public class Classroom {
  
  public static void main(String[] args){
  String[] students = {"Sade", "Alexus", "Sam", "Koma"};
  double[] mathScores = new double[4];

  mathScores[0] = 94.5;
  mathScores[2] = 76.8;
  System.out.println("The number of students in the class is " + students.length + ".");
  }
}

```


<br>
<br>


<h2>Intro to Arraylist</h2>

Introduction

When we work with arrays in Java, we’ve been limited by the fact that once an array is created, it has a fixed size. We can’t add or remove elements.

But what if we needed to add to the book lists, newsfeeds, and other structures we were using arrays to represent?

To create mutable and dynamic lists, we can use Java’s ArrayList class. ArrayList allows us to:

<ul>
<li>Store object references as elements</li>
<li>Store elements of the same type (just like arrays)</li>
<li>Access elements by index (just like arrays)</li>
<li>Add elements</li>
<li>Remove elements</li>
</ul>


Remember how we had to import java.util.Arrays in order to use additional array methods? To use an ArrayList at all, we need to import them from Java’s util package as well:

```
import java.util.ArrayList;
```

Let’s learn how to make use of this powerful object…








<h3>Creating ArrayLists</h3>

To create an ArrayList, we need to declare the type of objects it will hold, just as we do with arrays:

```
ArrayList<String> babyNames;
```

We use angle brackets < and > to declare the type of the ArrayList. These symbols are used for generics. Generics are a Java construct that allows us to define classes and objects as parameters of an ArrayList. For this reason, we can’t use primitive types in an ArrayList:

```
// This code won't compile:
ArrayList<int> ages;

// This code will compile:
ArrayList<Integer> ages;
```

The <Integer> generic has to be used in an ArrayList instead. You can also use <Double> and <Character> for types you would normally declare as doubles or chars.

We can initialize to an empty ArrayList using the new keyword:
```
// Declaring:
ArrayList<Integer> ages;
// Initializing:
ages = new ArrayList<Integer>();

// Declaring and initializing in one line:
ArrayList<String> babyNames = new ArrayList<String>();     // empty ArrayList
```

<br>
<br>

Question: Create a new ArrayList that will contain String elements and call it toDoList.

```
import java.util.ArrayList;

class ToDos {
  
  public static void main(String[] args) {
    
    // Create toDoList below:
   

    ArrayList<String> toDoList = new ArrayList<String>();  // the answer, declare and initialize Arraylist in one line
  }
  
}
```

<br>
<br>





<h3>Adding an Item - add() method</h3>

Now we have an empty ArrayList, but how do we get it to store values?

ArrayList comes with an ```add()``` method which inserts an element into the structure. There are two ways we can use add().

If we want to add an element to the end of the ArrayList, we’ll call add() using only one argument that represents the value we are inserting. In this example, we’ll add objects from the Car class to an ArrayList called carShow:

```
ArrayList<Car> carShow = new ArrayList<Car>();

carShow.add(ferrari);
// carShow now holds [ferrari]
carShow.add(thunderbird);
// carShow now holds [ferrari, thunderbird]
carShow.add(volkswagen);
// carShow now holds [ferrari, thunderbird, volkswagen]
```

If we want to add an element at a specific index of our ArrayList, we’ll need two arguments in our method call: the first argument will define the index of the new element while the second argument defines the value of the new element:

```
// Insert object corvette at index 1
carShow.add(1, corvette);
// carShow now holds [ferrari, corvette, thunderbird, volkswagen]

// Insert object porsche at index 2
carShow.add(2, porsche);
// carShow now holds [ferrari, corvette, porsche, thunderbird, volkswagen]
```

By inserting a value at a specified index, any elements that appear after this new element will have their index value shift over by 1.

Also, note that an error will occur if we try to insert a value at an index that does not exist.

Keep Reading: AP Computer Science A Students

When using ArrayList methods (like add()), the reference parameters and return type of a method must match the declared element type of the ArrayList. For example, we cannot add an Integer type value to an ArrayList of String elements.

We’ve discussed how to specify the element type of an ArrayList; however, it is possible to create an ArrayList that holds values of different types.

In the following snippet, assortment is an ArrayList that can store different values because we do not specify its type during initialization.
```
ArrayList assortment = new ArrayList<>();
assortment.add("Hello"); // String
assortment.add(12); // Integer
assortment.add(ferrari); // reference to Car
// assortment holds ["Hello", 12, ferrari]
```

In this case, the items stored in this ArrayList will be considered Objects. As a result, they won’t have access to some of their methods without doing some fancy casting. Although this type of ArrayList is allowed, using an ArrayList that specifies its type is preferred.


1. We’ve created an empty ArrayList called toDoList. Time to add some to-dos!

Below where we’ve initialized toDo1, initialize two new String variables: toDo2 and toDo3.

Set their values to any tasks you like.


2. Use .add() to add toDo1, toDo2, and toDo3 to toDoList.


```
import java.util.ArrayList;

class ToDos {
    
  public static void main(String[] args) {
    
    ArrayList<String> toDoList = new ArrayList<String>();
    String toDo1 = "Water plants";
    // Add more to-dos here:
    String toDo2 = "Do laundry";
    String toDo3 = "Wash the dishes";

    // Add to-dos to toDoList
    toDoList.add(toDo1);
    toDoList.add(toDo2);
    toDoList.add(toDo3);
    
    System.out.println(toDoList);
  }
  
}
```

<br>
<br>


<h3>ArrayList Size - size() method</h3>

Let’s say we have an ArrayList that stores items in a user’s online shopping cart. As the user navigates through the site and adds items, their cart grows bigger and bigger.

If we wanted to display the number of items in the cart, we could find the size of it using the ```size()``` method:

```
ArrayList<String> shoppingCart = new ArrayList<String>();

shoppingCart.add("Trench Coat");
System.out.println(shoppingCart.size());
// 1 is printed
shoppingCart.add("Tweed Houndstooth Hat");
System.out.println(shoppingCart.size());
// 2 is printed
shoppingCart.add("Magnifying Glass");
System.out.println(shoppingCart.size());
// 3 is printed
```

In dynamic objects like ArrayLists, it’s important to know how to access the amount of objects we have stored.

1. Detectives do a lot to solve a case. But who has more to do?

Print out the size of each detective’s to-do ArrayList:

sherlocksToDos for Sherlock Holmes
poirotsToDos for Hercule Poirot

2. So who has more to do? Print the name of the detective whose to-do list is longer. Was it Sherlock or Poirot?

<br>

```
import java.util.ArrayList;

class ToDos {
    
  public static void main(String[] args) {
    
    // Sherlock
    ArrayList<String> sherlocksToDos = new ArrayList<String>();
    
    sherlocksToDos.add("visit the crime scene");
    sherlocksToDos.add("play violin");
    sherlocksToDos.add("interview suspects");
    sherlocksToDos.add("solve the case");
    sherlocksToDos.add("apprehend the criminal");
    
    // Poirot
    ArrayList<String> poirotsToDos = new ArrayList<String>();
    
    poirotsToDos.add("visit the crime scene");
    poirotsToDos.add("interview suspects");
    poirotsToDos.add("let the little grey cells do their work");
    poirotsToDos.add("trim mustache");
    poirotsToDos.add("call all suspects together");
    poirotsToDos.add("reveal the truth of the crime");
    
    // Print the size of each ArrayList below:
    System.out.println(sherlocksToDos.size());
    System.out.println(poirotsToDos.size());
      
    // Print the name of the detective with the larger to-do list:
    System.out.println("Poirot");
  }
}
```


<br>
<br>



<h3>Accessing an Index - get() method</h3>

With arrays, we can use bracket notation to access a value at a particular index:

```
double[] ratings = {3.2, 2.5, 1.7};

System.out.println(ratings[1]);
```

This code prints 2.5, the value at index 1 of the array.

For ArrayLists, bracket notation won’t work. Instead, we use the method get() to access an index:

```
ArrayList<String> shoppingCart = new ArrayList<String>();

shoppingCart.add("Trench Coat");
shoppingCart.add("Tweed Houndstooth Hat");
shoppingCart.add("Magnifying Glass");

System.out.println(shoppingCart.get(2));

This code prints "Magnifying Glass", which is the value at index 2 of the ArrayList.
```


<br>
<br>



<h3>Changing a Value - set() method </h3>

When we were using arrays, we could rewrite entries by using bracket notation to reassign values:

```
String[] shoppingCart = {"Trench Coat", "Tweed Houndstooth Hat", "Magnifying Glass"};

shoppingCart[0] = "Tweed Cape";

// shoppingCart now holds ["Tweed Cape", "Tweed Houndstooth Hat", "Magnifying Glass"]
```

ArrayList has a slightly different way of doing this, using the set() method:

```
ArrayList<String> shoppingCart = new ArrayList<String>();

shoppingCart.add("Trench Coat");
shoppingCart.add("Tweed Houndstooth Hat");
shoppingCart.add("Magnifying Glass");

shoppingCart.set(0, "Tweed Cape");

// shoppingCart now holds ["Tweed Cape", "Tweed Houndstooth Hat", "Magnifying Glass"]
```

<br>
<br>



<h3>Removing an Item - remove() method </h3>

What if we wanted to get rid of an entry altogether? For arrays, we would have to make a completely new array without the value.

Luckily, ArrayLists allow us to remove an item by specifying the index to remove:
```
ArrayList<String> shoppingCart = new ArrayList<String>();

shoppingCart.add("Trench Coat");
shoppingCart.add("Tweed Houndstooth Hat");
shoppingCart.add("Magnifying Glass");

shoppingCart.remove(1);
// shoppingCart now holds ["Trench Coat", "Magnifying Glass"]
```

We can also remove an item by specifying the value to remove:
```
ArrayList<String> shoppingCart = new ArrayList<String>();

shoppingCart.add("Trench Coat");
shoppingCart.add("Tweed Houndstooth Hat");
shoppingCart.add("Magnifying Glass");

shoppingCart.remove("Trench Coat");
// shoppingCart now holds ["Tweed Houndstooth Hat", "Magnifying Glass"]
```

Note: This command removes the FIRST instance of the value "Trench Coat". can have more "Trench Coat" data stored in other array address/ multiple trench coat in shopping cart

Qn: Remove "visit the crime scene" from sherlocksToDos and poirotsToDos using remove().

Moreover, Sherlock Holmes has also gotten some violin playing done.

So you can remove "play violin" from sherlocksToDos as well.
<br>

```
import java.util.ArrayList;

class ToDos {
    
  public static void main(String[] args) {
    
    // Sherlock
    ArrayList<String> sherlocksToDos = new ArrayList<String>();
    
    sherlocksToDos.add("visit the crime scene");
    sherlocksToDos.add("play violin");
    sherlocksToDos.add("interview suspects");
    sherlocksToDos.add("solve the case");
    sherlocksToDos.add("apprehend the criminal");
    
    // Poirot
    ArrayList<String> poirotsToDos = new ArrayList<String>();
    
    poirotsToDos.add("visit the crime scene");
    poirotsToDos.add("interview suspects");
    poirotsToDos.add("let the little grey cells do their work");
    poirotsToDos.add("trim mustache");
    poirotsToDos.add("call all suspects together");
    poirotsToDos.add("reveal the truth of the crime");
    
    // Remove each to-do below:
    sherlocksToDos.remove(0);
    poirotsToDos.remove(0);
    sherlocksToDos.remove("play violin");


    System.out.println(sherlocksToDos.toString() + "\n");
    System.out.println(poirotsToDos.toString());
  }
  
}
```


<h3>Getting an Item's Index - indexOf() method</h3>

What if we had a really large list and wanted to know the position of a certain element in it? For instance, what if we had an ArrayList detectives with the names of fictional detectives in chronological order, and we wanted to know what position "Fletcher" was.

```
// detectives holds ["Holmes", "Poirot", "Marple", "Spade", "Fletcher", "Conan", "Ramotswe"];
System.out.println(detectives.indexOf("Fletcher"));
```

This code would print 4, since "Fletcher" is at index 4 of the detectives ArrayList.


```
import java.util.ArrayList;

class ToDos {
    
  public static void main(String[] args) {
    
    // Sherlock
    ArrayList<String> sherlocksToDos = new ArrayList<String>();
    
    sherlocksToDos.add("visit the crime scene");
    sherlocksToDos.add("play violin");
    sherlocksToDos.add("interview suspects");
    sherlocksToDos.add("listen to Dr. Watson for amusement");
    sherlocksToDos.add("solve the case");
    sherlocksToDos.add("apprehend the criminal");
    
    sherlocksToDos.remove("visit the crime scene");
    
    // Calculate to-dos until case is solved:
    System.out.println(sherlocksToDos.indexOf("solve the case"));  // answer
      
    // Change the value printed:
    System.out.println("PRINT THE ANSWER HERE");

  }
  
}
```

<br>
<br>
<br>

<h2>Introduction to Loops</h2>


In the programming world, we hate repeating ourselves. There are two reasons for this:

Writing the same code over and over is time-consuming.
Having less code means having less to debug.
But we often need to do the same task more than once. Fortunately, computers are really good (and fast) at doing repetitive tasks. And in Java, we can use loops.

A loop is a programming tool that allows developers to repeat the same block of code until some condition is met.

First, a starting condition is evaluated. If the starting condition is true, then the loop body is executed. When the last line of the loop body is executed, the condition is re-evaluated. This process continues until the condition is false (if the condition never becomes false, we can actually end up with an infinite loop!). If the starting condition is false, the loop never gets executed.

We employ loops to easily scale programs - saving time and minimizing mistakes.

We’ll go over three types of loops that we’ll see everywhere:

- while loops
- for loops
- for-each loops


<br>
<br>

<h3>For Loops</h3>

<img src = "https://content.codecademy.com/courses/learn-java/revised-2019/Java-loop-final.gif">

Incrementing with loops is actually so common in programming that Java (like many other programming languages) includes syntax specifically to address this pattern: for loops.

A for loop header is made up of the following three parts, each separated by a semicolon:

<ul>
<li>The initialization of the loop control variable.</li>
<li>A boolean expression.</li>
<li>An increment or decrement statement.</li>
</ul>
<br>

The opening line might look like this:

```
for (int i = 0; i < 5; i++) {

  // code that will run

}
```

In a for loop, an initialization statement is run once in order to initialize the loop control variable. This variable is modified in every iteration, can be referenced in the loop body, and used to test the boolean condition. In the example above, i is the loop control variable.

Let’s breakdown the above example:

i = 0: i is initialized to 0
i < 5: the loop is given a boolean condition that relies on the value of i. The loop will continue to execute until i < 5 is false.
i++: i will increment at the end of each loop and before the condition is re-evaluated.
So the code will run through the loop a total of five times.

We’ll also hear the term “iteration” in reference to loops. When we iterate, it just means that we are repeating the same block of code.


<br>
<br>
<br>

<h3>Using For Loops</h3>

Even though we can write while loops that accomplish the same task, for loops are useful because they help us remember to increment our counter — something that is easy to forget when we increment with a while loop.

Leaving out that line of code would cause an infinite loop — yikes!

Fortunately, equipped with our new understanding of for loops, we can help prevent infinite loops in our own code.

It’s important to be aware that, if we don’t create the correct for loop header, we can cause the iteration to loop one too many or one too few times; this occurrence is known as an “off by one” error.

For example, imagine we wanted to find the sum of the first ten numbers and wrote the following code:

```
int sum = 0;
for (int i = 0; i < 10; i++) {
  sum += i
}
```

This code would produce an incorrect value of 45. We skipped adding 10 to sum because our loop control variable started with a value of 0 and stopped the iteration after it had a value of 9. We were off by one! We could fix this by changing the condition of our loop to be i <= 10; or i < 11;.

These errors can be tricky because, while they do not always produce an error in the terminal, they can cause some miscalculations in our code. These are called logical errors — the code runs fine, but it didn’t do what you expected it to do.


Qn: We’ve provided a while loop that loops from 1 to 100 outputting a string on each iteration. Refactor (rewrite) this code as a for loop.

```
class Coffee {
  
  public static void main(String[] args) {
    
    int cupsOfCoffee = 1;
    
    for (int i = 1; i <= 100; i++) {
      
      System.out.println("Fry drinks cup of coffee #" + cupsOfCoffee);
      cupsOfCoffee++;
      
    }
    
  }
  
}
```

<br>
<br>





<h3>Iterating Over Arrays and ArrayLists</h3>


One common pattern we’ll encounter as a programmer is traversing, or looping, through a list of data and doing something with each item. In Java, that list would be an array or ArrayList and the loop could be a for loop. But wait, how does this work?

In order to traverse an array or ArrayList using a loop, we must find a way to access each element via its index. We may recall that for loops are created with a counter variable. We can use that counter to track the index of the current element as we iterate over the list of data.

Because the first index in an array or ArrayList is 0, the counter would begin with a value of 0 and increment until the end of the list. So we can increment through the array or ArrayList using its indices.

For example, if we wanted to add 1 to every int item in an array secretCode, we could do this:

```
for (int i = 0; i < secretCode.length; i++) {
  // Increase value of element value by 1
  secretCode[i] += 1;
}
```

Notice that our condition in this example is i < secretCode.length. Because array indices start at 0, the length of secretCode is 1 larger than its final index. A loop should stop its traversal before its counter variable is equal to the length of the list.

To give a concrete example, if the length of an array is 5, the last index we want to access is 4. If we were to try to access index 5, we would get an ArrayIndexOutOfBoundsException error! This is a very common mistake when first starting to traverse arrays.


Traversing an ArrayList looks very similar:

```
for (int i = 0; i < secretCode.size(); i++) {
  // Increase value of element value by 1
  int num = secretCode.get(i);
  secretCode.set(i, num + 1);
}
```

We can also use while loops to traverse through arrays and ArrayLists. If we use a while loop, we need to create our own counter variable to access individual elements. We’ll also set our condition to continue looping until our counter variable equals the list length.

For example, let’s use a while loop to traverse through an array:

```
int i = 0; // initialize counter

while (i < secretCode.length) {
  secretCode[i] += 1;
  i++; // increment the while loop
}
```

Traversing through an ArrayList with a while loop would look like this:

```
int i = 0; // initialize counter

while (i < secretCode.size()) {
  int num = secretCode.get(i);
  secretCode.set(i, num + 1);
  i++; // increment the while loop
}
```





<h3>break and continue</h3>

If we ever want to exit a loop before it finishes all its iterations or want to skip one of the iterations, we can use the break and continue keywords.

The break keyword is used to exit, or break, a loop. Once break is executed, the loop will stop iterating. For example:

```
for (int i = 0; i < 10; i++) {
  System.out.println(i);
  if (i == 4) {
    break;
  }
}
```

Even though the loop was set to iterate until the condition i < 10 is false, the above code will output the following because we used break:

```
0
1
2
3
4
```

The continue keyword can be placed inside of a loop if we want to skip an iteration. If continue is executed, the current loop iteration will immediately end, and the next iteration will begin. We can use the continue keyword to skip any even valued iteration:

```
int[] numbers = {1, 2, 3, 4, 5};
    
for (int i = 0; i < numbers.length; i++) {
  if (numbers[i] % 2 == 0) {
    continue;
  }
  System.out.println(numbers[i]);
}
```

This program would output the following:

```
1
3
5
```

In this case, if a number is even, we hit a continue statement, which skips the rest of that iteration, so the print statement is skipped. As a result, we only see odd numbers print.

Keep Reading: AP Computer Science A Students

Loops can exist all throughout our code - including inside a method. If the return keyword was executed inside a loop contained in a method, then the loop iteration would be stopped and the method/constructor would be exited.

For example, we have a method called checkForJacket() that takes in an array of Strings. If any of the elements are equivalent to the String value "jacket", the method will return true:

```
public static boolean checkForJacket(String[] lst) {
  for (int i = 0; i < lst.length; i++) {
    System.out.println(lst[i]);
    if (lst[i] == "jacket") {
      return true;
    }
  }
  return false;
} 

public static void main(String[] args) {
  String[] suitcase = {"shirt", "jacket", "pants", "socks"};   
  System.out.println(checkForJacket(suitcase));
}
```

As soon as an element equals "jacket", return true; is executed. This causes the loop to stop and the compiler to exit checkForJacket(). Running this code would output the following:

```
shirt
jacket
true
```

<br>
<br>

Qn: Take a look at the for loop in the code editor. It starts its iteration at 0 and continues to iterate until i < 100 is false.

Inside the loop, create a condition that checks if i is not divisible by 5. If the condition is true, skip the iteration. Outside the condition statement, print i. The final solution should not contain an else statement.

The only numbers that should be printed are those that are divisible by 5!

<br>
Dude in forums felt the Qn too easy so he made 3 examples for break and continue.


```
import java.util.ArrayList;

class Numbers {

  // Method for 3rd exercise
  public static boolean divisibleByThirteen(ArrayList<Integer> lst) {
    for (int i = 0; i < lst.size(); i++) {
      System.out.println(lst.get(i));
      if (lst.get(i) % 13 == 0) {
        return true;
      }
    }
    return false;
  } 

  public static void main(String[] args) {

    // 1st exercise - Continue
    for (int i = 0; i < 100; i++) {
      if (i % 5 != 0) {
        continue;
      }
      System.out.println(i);
    }

    System.out.println("\n");

    // 2nd exercise - Break
    for (int i = 100; i > 0; i--) {
      System.out.println(i);
      if (i % 12 == 0) {
        break;
      }
    }

    System.out.println("\n");

    // 3rd exercise - Return
    ArrayList<Integer> numbers = new ArrayList<Integer>();
    
    for (int i = 100; i > 0; i--) {
      numbers.add(i);
    }

    System.out.println(divisibleByThirteen(numbers));

  }
}   
```


<br>
<br>


<h3>For-Each Loops</h3>

Sometimes we need access to the elements’ indices or we only want to iterate through a portion of a list. If that’s the case, a regular for loop or while loop is a great choice.

For example, we can use a for loop to print out each element in an array called inventoryItems:

```
for (int inventoryItem = 0; inventoryItem < inventoryItems.length; inventoryItem++) {
  // Print element at current index
  System.out.println(inventoryItems[inventoryItem]);
}
```

But sometimes we couldn’t care less about the indices; we only care about the element itself.

At times like this, for-each loops come in handy.

For-each loops, which are also referred to as enhanced loops, allow us to directly loop through each item in a list of items (like an array or ArrayList) and perform some action with each item.

If we want to use a for-each loop to rewrite our program above, the syntax looks like this:

```
for (String inventoryItem : inventoryItems) {
  // Print element value
  System.out.println(inventoryItem);

}
```

Our enhanced loop contains two items: an enhanced for loop variable (inventoryItem) and a list to traverse through (inventoryItems).

We can read the : as “in” like this: for each inventoryItem (which should be a String) in inventoryItems, print inventoryItem.

If we try to assign a new value to the enhanced for loop variable, the value stored in the array or ArrayList will not change. This is because, for every iteration in the enhanced loop, the loop variable is assigned a copy of the list element.

Note: We can name the enhanced for loop variable whatever we want; using the singular of a plural is just a convention. We may also encounter conventions like ```String word : sentence```.


1. Let’s use a for-each loop to find the priciest item in expenses.

Build a for-each loop that iterates through each expense in expenses. For now, leave the body of the loop empty.


2. Inside the for-each loop, check if expense is greater than mostExpensive.

If it is, set mostExpensive equal to expense.


```
import java.util.ArrayList;

class MostExpensive {
  
  public static void main(String[] args) {
    
    ArrayList<Double> expenses = new ArrayList<Double>();
    expenses.add(74.46);
    expenses.add(63.99);
    expenses.add(10.57);
    expenses.add(81.37);
    
    double mostExpensive = 0;
    
    // Iterate over expenses
    
    for (double expense : expenses){
      if (expense > mostExpensive){
        mostExpensive = expense;
      }
      System.out.println("Checking expense item " + expense);  // you can't directly print out current index/which index is being checked in a for-each loop because it's abstracts away the index.
 	// To abstract (away), specifically in computer science, refers to intentionally obscuring the details of how something works in order to simplify things conceptually."
	// have to use a regular for loop to print out current index  		
    }
    
    System.out.println(mostExpensive);
    System.out.println(expenses.get(2));
  }
  
}
```


<h3>Removing Elements During Traversal</h3>


If we want to remove elements from an ArrayList while traversing through one, we can easily run into an error if we aren’t careful.

When an element is removed from an ArrayList, all the items that appear after the removed element will have their index value shift by negative one — it’s like all elements shifted to the left! We’ll have to be very careful with how we use our counter variable to avoid skipping elements.

Removing An Element Using ```while```
When using a while loop and removing elements from an ArrayList, we should not increment the while loop’s counter whenever we remove an element. We don’t need to increase the counter because all of the other elements have now shifted to the left.

For example, if we removed the element at index 3, then the element that was at index 4 will be moved to index 3. If we increase our counter to 4, we’ll skip that element!

Take a look at this block of code that will remove all odd numbers from an ArrayList. Think about what the value of i is, when we’re increasing the value of i, and when i < lst.size() becomes False.

```
int i = 0; // initialize counter

while (i < lst.size()) {
  // if value is odd, remove value
  if (lst.get(i) % 2 != 0){
    lst.remove(i);
  } else {
    // if value is even, increment counter
    i++;
  }
}
```
<br>
<br>

Removing An Element Using ```for```
We can use a similar strategy when removing elements using a for loop. When using a while loop, we decided to not increase our loop control variable whenever we removed an element. This ensured that we would not skip an element when all of the other elements shifted to the left.

When using a for loop, we, unfortunately, must increase our loop control variable — the loop control variable will always change when we reach the end of the loop (and it will usually change by 1 because we often use something like i++.) Since we can’t avoid increasing our loop control variable, we can take matters into our own hands and decrease the loop control variable whenever we remove an item.

For example:
```
for (int i = 0; i < lst.size(); i++) {
  if (lst.get(i) == "value to remove"){
    // remove value from ArrayList
    lst.remove(lst.get(i));
    // Decrease loop control variable by 1
    i--;    
  }
}
```
Now whenever we remove an item, we’ll decrease i by 1. Then when we reach the end of the loop, i will increase by 1. It will be like i never changed!

Note: Avoid manipulating the size of an ArrayList when using an enhanced for loop. Actions like adding or removing elements from an ArrayList when using a for each loop can cause a ConcurrentModificationException error.

Qn: Take a look at the code placed in the main() method of the Lunch class.

Inside the method removeAnts(), use a for loop or a while loop to iterate through lunchBox and remove any element that has the value "ant".

Outside the loop, return the value of lunchBox.

The final solution should look similar to the code below if using a for loop:

```
for (int i = 0; i < listName.size(); i++) {   // You forgot to int i = 0; you left as int i; GG man
  if (listName.get(i) == "ant"){
    listName.remove(listName.get(i));
    i--;    
   }
}
return listName;

If using a while loop, the solution may look similar to the following snippet:

int i = 0; 
while (i < listName.size()) {
  if (listName.get(i) == "ant"){
    listName.remove(listName.get(i));
  } else {
    i++;
  }
}
```


<br>
<br>

<br>
<br>



<h3>Review</h3>

Nice work! Let’s iterate over what you’ve just learned about loops:

while loops: These are useful to repeat a code block an unknown number of times until some condition is met. For example:
int wishes = 0;
```
while (wishes < 3) {

  // code that will run
  wishes++;
```
}

for loops: These are ideal for when you are incrementing or decrementing with a counter variable. For example:
```
for (int i = 0; i < 5; i++) {

  // code that will run
```
}

For-each loops: These make it simple to do something with each item in a list. For example:
```
for (String inventoryItem : inventoryItems) {

  // do something with each inventoryItem
```
}

<br>
<br>
<br>
<br>

<h2>Introduction to String Methods</h2>


As you may recall, a String, which is widely used in Java, is an object that represents a sequence of characters. It is a great way to store information.

Because character strings are so vital to programming, Java dedicated an entire class to them. 
This is great news for us because the String class has a lot of useful methods to help us perform operations on Strings and data manipulation. 
We don’t have to import anything to use the String class because it’s part of the java.lang package which is available by default.

In this lesson, we will go over several String methods:

<ul>
<li>length()</li>
<li>concat()</li>
<li>equals()</li>
<li>indexOf()</li>
<li>charAt()</li>
<li>substring()</li>
<li>toUpperCase() / toLowerCase()</li>
</ul>
 
Let’s get started!

<br>
<br>
<br>



<h3>length()</h3>

In Java, the ```length()``` string method returns the length ⁠— total number of characters ⁠— of a String.

Suppose we have a String called str, ```str.length()``` would return its length.

Take a look at this code for example:

```
String str = "Hello World!";  

System.out.println(str.length());
```

12 would be printed because str has 12 characters:

``H e l l o _ W o r l d !``

In theory, the length of a String is the same as the Unicode units of the String. For example, escape sequences such as \n count as only one character.


<br>
<br>
<br>

<h3>concat()</h3>

The ```concat()``` method concatenates one string to the end of another string. Concatenation is the operation of joining two strings together.

Suppose we have a String called str1 and another String called str2, using str1.concat(str2) would return str1 with str2 appended to the end of it.

For example:
```
String name = new String("Code");

name = name.concat("cademy");

System.out.println(name);
```

Codecademy would be printed.

Strings are immutable objects which means that String methods, like concat() do not actually change a String object.

Our variable, name holds a reference to the String object, "Code". When we use concat() on name, we changed its value so that it references a new object — "Code", combined with the String literal, "cademy".

Suppose we do something slightly different. We’ll use concat() on name without reassigning its value:
```
String name = "Code";

name.concat("cademy");

System.out.println(name);
```

Code would be printed instead. The value of the String can’t change! Instead, we create a new object and need to assign that new object to some variable.

Keep Reading: AP Computer Science A Students

When we first discussed Objects we learned that if we tried printing an Object, we’d get an output of the class name and the Object’s memory address. If we wanted to get a more useful printout, we’d have to call the Object’s ```toString()``` method.

This ```toString()``` method comes into play with concat(). If we concatenate a String with another Object, we’re really adding the result of that Object’s toString() method to our original String. We can even see this when we concatenate two Strings together (remember a String is an Object). When we use concat() on another String, we don’t concatenate its memory address to the original String. Instead, we combine the result of its toString() method to the original String.

You can refresh yourself on the toString() method in this exercise.



Qn: Store your first name in firstName and your last name in lastName. Print out your full name using concat().

```

public class CombineNames {
  
	public static void main(String[] args) {
    
    // Add your first names:
    String firstName = "Ming Jun";  
    String lastName = "Lam";

    // What's the full name?
    System.out.println(firstName.concat(lastName));
  }
  
}
```

<br>
<br>
<br>

<h3>equals()</h3>


With objects, such as Strings, we can’t use the primitive equality operator ```==``` to check for equality between two strings. To test equality with strings, we use a built-in method called ```equals()```.

For example:
```
String flavor1 = "Mango";
String flavor2 = "Peach";

System.out.println(flavor1.equals("Mango"));
// prints true

System.out.println(flavor2.equals("Mango"));
// prints false
```

Side note, there’s also an ```equalsIgnoreCase()``` method that compares two strings without considering upper/lower cases.

Keep Reading: AP Computer Science A Students

We can also compare String values lexicographically (think dictionary order) using the ```.compareTo()``` method. When we call the ```.compareTo()``` method, each character in the String is converted to Unicode; then the Unicode character from each String is compared.

The method will return an int that represents the difference between the two Strings.

For example:
```
String flavor1 = "Mango";
String flavor2 = "Peach";

System.out.println(flavor1.compareTo(flavor2)); 
```
Our program above will output -3.

When we use ```.compareTo()```, we must pay attention to the return value:

If the method returns 0, the two Strings are equal.
If the value is less than 0, then the String object is lexicographically less than the String object argument.
If the value is greater than 0, then the String object is lexicographically greater than the String object argument.
In the example above, "Mango" comes before "Peach", so we get a negative number (we specifically get -3 because the Unicode values of "M" and "P" differ by 3). If we did flavor2.compareTo(flavor1), we would get 3, signifying that "Peach" is greater than "Mango".

Note: Make sure to pay attention to capitalization when using ```.compareTo()```. Upper case and lower case letters have different Unicode values. For example, when comparing "Mango" and "Peach", we got -3, meaning that "Mango" was smaller. But if we compare "mango" and "Peach" we get 29. The Unicode value for lower case "m" is actually larger than upper case "P". Using .compareToIgnoreCase() will perform the same task, but will not consider upper/lower case.

<br>
<br>
<br>


<h3>charAt()</h3>

The ```charAt()``` method returns the character located at a String‘s specified index.

For example:
```
String str = "qwer";

System.out.println(str.charAt(2));
```
It would output e because that’s what’s at index 2. (Once again, indices start with 0.)

Suppose we try to return the character located at index 4. It would produce an IndexOutOfBoundsException error because index 4 is out of str‘s range:

```
java.lang.StringIndexOutOfBoundsException: String index out of range: 4
```


<br>
<br>
<br>

<h3>substring()</h3>

There may be times when we only want a part of a string. In such cases, we may want to extract a substring from a string.

The ```substring()``` method does exactly that. For example:
```
String line = "The Heav'ns and all the Constellations rung";

System.out.println(line.substring(24));
```
It would output Constellations rung because that’s what begins at index 24 and ends at the end of line. The substring begins with the character at the specified index and extends to the end of the string.

Suppose we want a substring from the middle of the string. We can instead include two arguments in this method. For example:
```
String line = "The Heav'ns and all the Constellations rung";

System.out.println(line.substring(27, 33));
```

When ```substring()``` is called with two arguments, the first argument is inclusive and the second is exclusive. This means the resulting substring will begin at index 27 and extend up to, but not including, index 33. Therefore, the example above would output stella because that’s the substring that begins at index 27 and ends at index 32, one index before 33.

We can use this method to return a single-element substring at a specific index. We do this by calling substring() with the desired index value as the first argument and then the index value plus one as the second argument.

For example, we can use this method to output just C:
```
String line = "The Heav'ns and all the Constellations rung";

System.out.println(line.substring(24, 25));
// Prints: C
```

<br>
<br>
<br>



<h3>toUpperCase() / toLowerCase()</h3>

There will be times when we have a word in a case other than what we need it in. Luckily, Java has a couple String methods to help us out:

toUpperCase(): returns the string value converted to uppercase
toLowerCase(): returns the string value converted to lowercase

For example:

```
String input = "Cricket!";

String upper = input.toUpperCase();
// stores "CRICKET!"

String lower = input.toLowerCase();
// stores "cricket!"
```

A good use of this functionality is to ensure consistency of the data you store in a database. Making sure all of the data you get from a user is lowercase before you store it in your database will make your database easier to search through later.

Qn: In Hashtag.java, use toLowerCase() to print out the lower case version of hashtag.

```

public class Hashtag {
  
  public static void main(String[] args) {
    
    String hashtag = "#100DaysOfCode";
    
    // Make the hashtag lowercase:
    System.out.println(hashtag.toLowerCase()); 
    
  }
}
```

<br>
<br>
<br>


<h3>Review</h3>

Congratulations! 🙌

We have learned some of the string methods that come with the String class:

<ul>
	<li>length()</li>
	<li>concat()</li>
	<li>indexOf()</li>
	<li>charAt()</li>
	<li>equals() / equalsIgnoreCase()</li>
	<li>substring()</li>
	<li>toUpperCase() / toLowerCase()</li>
</ul>


<br>
<br>
<br>



<h2>ACCESS, ENCAPSULATION, AND SCOPE</h2>

<h3>What are Access and Scope?</h3>

As our Java programs begin to get bigger and we begin to have multiple Objects and Classes that interact with each other, the concepts of access and scope come into play. To oversimplify things, the concepts of access and scope both center around what parts of your programs can interact with specific variables or methods from other parts of your program. Let’s take a brief look at some of the concepts we’ll cover:

Access
<ul>
<li>The public and private keywords and how they relate to Classes, variables, constructors, and methods</li>
<li>The concept of encapsulation</li>
<li>Accessor methods, sometimes known as “getters”</li>
<li>Mutator methods, sometimes known as “setters”</li>
</ul>


Scope
<ul>
<li>Local variables vs. instance variables</li>
<li>The this keyword</li>
<li>Let’s get started!</li>
</ul>

<br>
<br>
<br>


<h3>The public Keyword</h3>

After running the code in the last exercise, you should be developing an intuition on what the public and private keywords are doing. These keywords are defining what parts of your code have access to other parts of your code.

We can define the access of many different parts of our code including instance variables, methods, constructors, and even a class itself. If we choose to declare these as public this means that any part of our code can interact with them - even if that code is in a different class!

The way we declare something to be public is to use the public keyword in the declaration statement. In the code block below, we have a public class, constructor, instance variables, and method. Notice the five different uses of public.

```
public class Dog{
  public String name;
  public int age;

  public Dog(String input_name, int input_age){
    name = input_name;
    age = input_age;
  }
    
  public void speak() {
    System.out.println("Arf Arf! My name is " + name + " and I am a good dog!");
  }
}
```

Since everything about a Dog is public, any other class can access anything about a Dog. For example, let’s say there was a DogSchool class. Any method of the DogSchool class could make a new Dog using the public Dog constructor, directly access that Dog’s instance variables, and directly use that Dog’s methods:

```
public class DogSchool{
  public void makeADog(){
    Dog cujo = new Dog("Cujo", 7);
    System.out.println(cujo.age);
    cujo.speak();
  }
}
```

Notice that the DogSchool class and the ```makeADog()``` method are also public. This means that if some other class created a DogSchool, they would have access to these methods as well! We have public methods calling public methods!

One final thing to note is that for the purposes of this lesson, we’ll almost always make our classes and constructors public. While you can set them to private, it’s fairly uncommon to do so. Instead, we’ll focus on why you might make your instance variables and methods private. We’ll start looking into the private keyword in the next exercise.


<br>
<br>
<br>

<h3>The private Keyword and Encapsulation</h3>

By now you’re probably catching onto what the private keyword does. When a Class’ instance variable or method is marked as private, that means that you can only access those structures from elsewhere inside that same class. Let’s look back at our DogSchool example:
```
public class DogSchool{

  public void makeADog(){
    Dog cujo = new Dog("Cujo", 7);
    System.out.println(cujo.age);
    cujo.speak();
  }
}
```
makeADog is trying to directly access Dog‘s .age variable. It’s also trying to use the .speak() method. If those are marked as private in the Dog class, the DogSchool class won’t be able to do that. Other methods within the Dog class would be able to use .age or .speak() (for example, we could use cujo.age within the Dog class), but other classes won’t have access.

Keep Reading: AP Computer Science A Students

At this point, you might be thinking to yourself “Why even bother with any of this? In the last exercise, my code was broken until I flipped some variables and methods to public. Why don’t I just make everything public?”

While those are valid points, sometimes restricting our code is actually useful from a design perspective. This is one of the core ideas behind encapsulation. By making our instance variables (and some methods) private, we encapsulate our code into nice little bundles of logic.

For example, a Bank object doesn’t necessarily need to know the inner workings of a CheckingAccount object. It doesn’t need to know that the money is stored in a field named money, or that interest is added to an account by using a method named .addInterest(). In fact, if it had access to those fields or methods, it’s possible that someone using a Bank object could change things in a CheckingAccount without realizing it. By limiting access by using the private keyword, we are able to segment, or encapsulate, our code into individual units.

Note that we don’t necessarily want to completely block everything from other classes. In the next exercise, we’ll get into when you might want to make methods public — we’ll take a look at getter and setter methods.


<br>
<br>
<br>


<h3>Accessor and Mutator Methods</h3>

When writing classes, we often make all of our instance variables private. However, we still might want some other classes to have access to them, we just don’t want those classes to know the exact variable name. To give other classes access to a private instance variable, we would write an accessor method (sometimes also known as a “getter” method).
```
public class Dog{
  private String name;
    
  //Other methods and constructors

  public String getName() {
    return name;
  }
}
```

Even though the instance variable name is private, other classes could call the public method getName() which returns the value of that instance variable. Accessor methods will always be public, and will have a return type that matches the type of the instance variable they’re accessing.

Similarly, private instance variables often have mutator methods (sometimes known as “setters”). These methods allow other classes to reset the value stored in private instance variables.
```
public class Dog{
  private String name;
    
  //Other methods and constructors

  public void setName(String newName) {
    name = newName;
  }

  public static void main(String[] args){
    Dog myDog = new Dog("Cujo");
    myDog.setName("Lassie");
  }
}
```

Mutator methods, or “setters”, often are void methods — they don’t return anything, they just reset the value of an existing variable. Similarly, they often have one parameter that is the same type as the variable they’re trying to change.



<h3>Scope: Local Variables</h3>

In addition to access modifiers like public and private, the scope of the variable also determines what parts of your code can access that variable.

The scope of a variable is determined by where the variable is declared. For example, because instance variables are declared inside a class but outside any methods or constructors, all methods and constructors are within the scope of that variable. For example, in the code block below, constructors and methods of the Dog class are using the Dog instance variables like name and age:

```
class Dog{
  public String name;
  public int age;
  public int weight;

  public Dog(){
    name = "Winston";
    age = 8;
    weight = 30;
  }

  public void speak(){
    System.out.println("My name is " + name);
  }
}
```

However, if we have a variable declared inside a method, that variable can only be used inside that method. The same is true for parameters. The scope of those parameters is only the method they’re associated with. If you try to use a parameter outside the function it’s defined in, you’ll get an error. These variables are often called local variables. Note that we don’t use public or private when declaring local variables.

This idea of scope extends to conditionals and loops as well. If you declare a variable inside the body of a conditional or in a loop, that variable can only be used inside that structure. This also includes the variable you’re using as your looping variable. For example, consider the following block of code:

```
for(int i = 0; i < 10; i++){
  // You can use i here
}
// i is out of scope here
```

You can only use i between the curly braces of the for loop. In general, whenever you see curly braces, be aware of scope. If a variable is defined inside curly braces, and you try to use that variable outside of those curly braces, you will likely see an error!



<br>
<br>
<br>

<h3>Scope: The this Keyword</h3>

// ```this.``` simply means refers to instance variable. it's to make your coding super clear which variable you aiming 

Often times when creating classes, programmers will create local variables with the same name as instance variables. For example, consider the code block below:

```
public class Dog{
  public String name;

  public Dog(String inputName){
    name = inputName;
  }

  public void speakNewName(String name){
    System.out.println("Hello, my new name is" + name);
  }

  public static void main(String[] args){
    Dog myDog = new Dog("Winston");
    myDog.speakNewName("Darla"); // Prints "Darla" - "Winston" ignored

  }
}
```

We have an instance variable named name, but the method speakNewName has a parameter named name. So when the method tries to print name, which variable will be printed? By default, Java refers to the local variable name. So in this case, the value passed to the parameter will be printed and not the instance variable.

If we wanted to access the instance variable and not the local variable, we could use the this keyword.

```
public class Dog{
  public String name;

  public Dog(String inputName){
    name = inputName;
  }

  public void speakNewName(String name){
    System.out.println("Hello, my new name is" + this.name);
  }
    
  public static void main(String[] args){
    Dog a = new Dog("Fido");
    Dog b = new Dog("Odie");

    a.speakNewName("Winston");
    // "Fido", the instance variable of Dog a is printed. "Winston" is ignored

    b.speakNewName("Darla");
    // "Odie", the instance variable of Dog b is printed. "Darla" is ignored.
  }
}
```

The this keyword is a reference to the current object. We used this.name in our speakNewName() method. This caused the method to print out the value stored in the instance variable name of whatever Dog Object called speakNewName(). (Note that in this somewhat contrived example, the local variable name used as a parameter gets completely ignored).

Oftentimes, you’ll see constructors have parameters with the same name as the instance variable. For example, you might see something like:
```
public Dog(String name){
  this.name = name;
}
```

You can read this as “set this Dog‘s instance variable name equal to the variable passed into the constructor”. While this naming is a common convention, it can also be confusing. There’s nothing wrong with naming your parameters something else to be more clear. Sometimes you will see something like:
```
public Dog(String inputName){
  this.name = inputName;
}

This is now a little clearer — we’re setting the Dog‘s instance variable name equal to the name we give the constructor.

Finally, mutator methods also usually follow this pattern:

public void setName(String name){
  this.name = name;
}
```

We reset the instance variable to the value passed into the parameter.

Throughout the rest of this lesson, we’ll use ```this.``` when referring to an instance variable. This isn’t always explicitly necessary — if there’s no local variable with the same name, Java will know to use the instance variable with that name. That being said, it is a good habit to use this. when working with your instance variables to avoid potential confusion.

<br>
<br>
<br>






<h3>Using this With Methods</h3>

We’ve seen how the this works with variables, but we can also use the this with methods.

Recall how we’ve been calling methods up to this point:

```
public static void main(String[] args){
  Dog myDog = new Dog("Odie");
  myDog.speak();
}
```

Here we’re creating an instance of a Dog and using that Dog to call the ```speak()``` method. However, when defining methods, we can also use the this keyword to call other methods. Consider the code block below:
```
public class Computer{
  public int brightness;
  public int volume;
  
  public void setBrightness(int inputBrightness){
    this.brightness = inputBrightness;
  }

  public void setVolume(int inputVolume){
    this.volume = inputVolume;
  }

  public void resetSettings(){
    this.setBrightness(0);
    this.setVolume(0);
  }
}
```

Take a look at the ```resetSettings()``` method in particular. This method calls other methods from the class. But it needs an object to call those methods! Rather than create a new object (like we did with the Dog named myDog earlier), we use this as the object. What this means is that the object that calls resetSettings() will be used to call setBrightness(0) and setVolume(0).
```
public static void main(String[] args){
  Computer myComputer = new Computer();
  myComputer.resetSettings();
}
```

In this example, calling ```myComputer.resetSettings()``` is as if we called myComputer.setBrightness(0) and myComputer.setVolume(0). this serves as a placeholder for whatever object was used to call the original method.

Keep Reading: AP Computer Science A Students

Finally, this can be used as a value for a parameter. Let’s say a method exists that takes a Computer as a parameter (that method’s signature might be something like public void pairWithOtherComputer(Computer other)). If you’re writing another method in Computer, and want to call the pairWithOtherComputer() method, you could use this as the parameter. That call might look something like this.pairWithOtherComputer(this). You’re using the current object to call the method and are passing that object as that method’s parameter.

```
public void pairWithOtherComputer(Computer other){
  // Code for method that uses the parameter other
}

public void setUpConnection(){
  // We use "this" to call the method and also pass "this" to the method so it can be used in that method
  this.pairWithOtherComputer(this);
}
```

Qn: Complete the ```hasBirthday()``` method. This method should call the mutator methods to increase age by 1, increase wisdom by 5, and decrease fitness by 3.

When you’re done writing ```hasBirthday()``` look at the ```main()``` method to see how we’re calling it.


```
public class Person{
  public int age;
  public int wisdom;
  public int fitness;

  public Person(int inputAge){
    this.age = inputAge;
    this.wisdom = inputAge * 5;
    this.fitness = 100 - inputAge;
  }

  public void setAge(int newAge){
    this.age = newAge;
  }

  public void setWisdom(int newWisdom){
    this.wisdom = newWisdom;
  }

  public void setFitness(int newFitness){
    this.fitness = newFitness;
  }

  public void hasBirthday(){
    //Complete this method
    this.setAge(this.age + 1);
    this.setWisdom(this.wisdom + 5);
    this.setFitness(this.fitness - 3);

  }

  public static void main(String[] args){
    Person emily = new Person(20);
    emily.hasBirthday();
    System.out.println("New age is: " + emily.age);
    System.out.println("New wisdom is: " + emily.wisdom);
    System.out.println("New fitness is: " + emily.fitness);

  }
}
```
<br>
<br>
<br>



<h3>Other Private Methods</h3>

Now that we’ve seen how methods can call other methods using this., let’s look at a situation where you might want to use private methods. Oftentimes, private methods are helper methods — that is to say that they’re methods that other, bigger methods use.

For example, for our CheckingAccount example, we might want a public method like ```getAccountInformation()``` that prints information like the name of the account owner, the amount of money in the account, and the amount of interest the account will make in a month. That way, another class, like a Bank, could call that public method to get all of that information quickly.

Well, in order to get that information, we might want to break that larger method into several helper methods. For example, inside ```getAccountInformation()```, we might want to call a function called calculateNextMonthInterest(). That helper method should probably be private. There’s no need for a Bank to call these smaller helper methods — instead, a Bank can call the one public method, and rely on that method to do all of the complicated work by calling smaller private methods.


Qn: Let’s implement what we described in the narrative. We’ve written our ```getAccountInformation()``` method in the CheckingAccount.java class. But we haven’t yet implemented the ```calculateNextMonthInterest()``` method. This should be a private method and return a double — the balance of the account multiplied by the interestRate. Write that function.

Then flip back to Bank.java and take a look at the ```main()``` method. We’re calling ```bankOfGods.accountOne.getAccountInformation();```. Will a Bank be able to do this? Run your code to find out.


```
CheckingAccount.java


public class CheckingAccount{
  private String name;
  private int balance;
  private String id;
  private double interestRate;

  public CheckingAccount(String inputName, int inputBalance, String inputId){
    this.name = inputName;
    this.balance = inputBalance;
    this.id = inputId;
    this.interestRate = 0.02;
  }

  public void getAccountInformation(){
    System.out.println("Money in account: " + this.getBalance());
    System.out.println("Next Month's Interest: " + this.calculateNextMonthInterest());

  }

  private int getBalance(){
    return this.balance;
  }

  // Write the calculateNextMonthInterest() here
  private double calculateNextMonthInterest(){
    return this.interestRate * this.balance; 
  }
}



Bank.java

public class Bank{
  private CheckingAccount accountOne;
  private CheckingAccount accountTwo;

  public Bank(){
    this.accountOne = new CheckingAccount("Zeus", 100, "1");
    this.accountTwo = new CheckingAccount("Hades", 200, "2");
  }

  public static void main(String[] args){
    Bank bankOfGods = new Bank();
    bankOfGods.accountOne.getAccountInformation();
    bankOfGods.accountOne.calculateNextMonthInterest();
  }

}

```
<br>
<br>
<br>

<h3>Review</h3>

Nice work! In this lesson, we dove into some of the more subtle features of classes with a focus on access, encapsulation, and scope. Here are some of the main takeaways from this lesson:

<ul>
<li>The public and private keywords are used to define what parts of code have access to other classes, methods, constructors, and instance variables.</li>
<li>Encapsulation is a technique used to keep implementation details hidden from other classes. Its aim is to create small bundles of logic.</li>
<li>The this keyword can be used to designate the difference between instance variables and local variables.</li>
<li>Local variables can only be used within the scope that they were defined in.</li>
<li>The this keyword can be used to call methods when writing classes.</li>
</ul>

<br>
<br>
<br>

<h3>The Math Class</h3>

Math can play a major role in our programs. It can become tedious to write out every equation we need in our code. Luckily, a lot of this work can be truncated using the Math class. The Java Math class is part of the java.lang package; it contains a variety of methods that can be used to perform numerical calculations in our programs. In this article, we’ll discuss the different types of Math methods available to us and how to implement them in our Java programs.

The Math class also offers a good opportunity for us to learn about Static methods. We’ll take a look at what static methods are and how they’re different from non-static methods.

<br>
<br>

<h3>Calling Static Methods</h3>

Every method in the Math class is static. This means that we can call and use these methods without creating an object of the class. There are two main options for calling a static method.
// Static methods are methods that belong to an entire class, not a specific object of the class.

<br>

Our first option is to append the dot operator to the class name followed by the method we want to execute. If we wanted to reference a method of the Math class, we would use Math.NameOfMethodHere. Let’s see this in action with the Math class method min() which returns the smaller value of two given numbers:
```
class Numbers {
  public static void main(String[] args) {
    // Call method using the Class name, the dot operator, the method name, and arguments
    int smallerNumber = Math.min(3, 10);
    System.out.println(smallerNumber); // Prints: 3
  }
}
```
How is this any different from calling a non-static method? We don’t need to create an object of the class in order to use the methods it contains. Let’s see an example of a non-static method:
```
class Numbers {
  int firstNumber;
  int secondNumber;

  public Numbers (int num1, int num2) {
    firstNumber = num1;
    secondNumber = num2;
  }
  
  // non-static method
  public int returnSum() {
    return firstNumber + secondNumber;
  }
  
  public static void main(String[] args) {
    // Create an object
    Numbers myNumbers = new Numbers(2, 5);
    // Call a non-static method on object
    int sum = myNumbers.returnSum();
    System.out.println(sum); // Prints: 7
  }
}
```

In our code above, we had to create an object of type Numbers in order to use the non-static method returnSum(). With non-static methods, if we don’t create an object of this class (or one of its subclasses), we do not have access to its methods. This isn’t the case for static methods.

Our second option for calling a static method from the Math class is to import the class by adding import static java.lang.Math.*; to the top of our program. If we import the Math class, we can reference the method using only the method name like so:

```
import static java.lang.Math.*; // import Math class

class Numbers {
  public static void main(String[] args) {
    // Call method by using method name and arguments
    int smallerNumber = min(3, 10);
    System.out.println(smallerNumber); // Prints: 3
  }
}
```

<h4>Useful Methods</h4>

There are many useful methods from the Math class that can be implemented in our programs. For those of us taking the AP Computer Science A exam, the following methods and their descriptions will be available in the Java Quick Reference Guide:

<h4>int abs(int x)</h4>
Purpose: Returns the absolute value of an int value

The absolute value states how many numbers a value is away from 0. The absolute value is always a positive number. For example, the absolute value of -5 is 5 because it is 5 away from 0. In Java, we can get the absolute value of a number like this:
```
System.out.println(Math.abs(5)); // Prints: 5
System.out.println(Math.abs(-5)); // Prints: 5
```
<h4>double abs(double x)</h4>
Purpose: Returns the absolute value of a double value

This is similar to the previous method, but this method takes in and returns a double type value:
```
System.out.println(Math.abs(5.0)); // Prints: 5.0
System.out.println(Math.abs(-5.0)); // Prints: 5.0
```

<h4>double pow(double base, double exponent)</h4>
Purpose: Returns the value of the first parameter raised to the power of the second parameter.

The power, or exponent, describes how many times a number should be multiplied by itself. For example, 5 to the power of 3 is equivalent to 5 * 5 * 5, or 125. If we wanted to see this in Java, we could use Math.pow() like this:
```
double x = Math.pow(5, 3);
System.out.println(x); // Prints: 125.0
```


<h4>double sqrt(double x)</h4>
Purpose: Returns the positive square root of a double value

The square root of a number represents what value can be multiplied by itself in order to equal a specified value. For example, the square root of 49 is 7 because 7 * 7 is 49. In java, getting the square root of a value looks like this:

```
double x = Math.sqrt(49); 
System.out.println(x); // Prints: 7.0
double y = Math.sqrt(52); 
System.out.println(y); // Prints: 7.211102550927978
```



<h4>double random()</h4>

Purpose: Returns a double value greater than or equal to 0.0 and less than 1.0

Randomization is a great way to add probability to our programs. There are many ways to implement Math.random() in Java. Its default use case is to produce a random double value between 0.0 and 1.0. For example:
```
System.out.println(Math.random());
System.out.println(Math.random());
System.out.println(Math.random());
```

The random values can change every time we run our program. An example output of the above program is the following:

```
0.8592007008856128
0.6120058754881421
0.48259656765819403
```

With some manipulation, we can use Math.random() to create a random int or double value within a predefined range.

For example, if we wanted a random double value between 0 and 10, not including 10, we would multiply Math.random() by 10

```
// Random double value between 0 and 10, not including 10
double a = Math.random() * 10;

If we wanted a random int value between 0 and 9, we would need to implement the (int) casting operator in our expression like so:

// Random int value between 0 and 9
int b = (int)(Math.random() * 10);

If we wanted our range to start at 1 and end at 10, we would have to add 1 to the end of our previous expression:

// Random int value between 1 and 10
int c = (int)(Math.random() * 10) + 1;
```

Using addition also gives us the ability to start the range at any number. What if we wanted an int value in the range of 10 up to and including 20? We would have to implement the algorithm (Math.random() * (maxValue - minValue + 1)) + minValue.

For example:
```
// Random int value between 10 and 20
int d = (int)(Math.random() * 11 ) + 10;
```

We multiply Math.random() by 11 because 20 (our max value) minus 10 (our minimum value) plus 1 is 11. We add + 10 outside the parentheses so that our smallest value is guaranteed to be 10.

Here’s another way to think about this algorithm — the value that you multiply by defines the number of possible values you can get. The number that you add defines the starting value. So, for example, (int)(Math.random() * 3 ) + 5; will give you one of three random values starting at 5. So this could give you 5, 6, or 7.

Finally, be careful of off-by-one errors when using Math.random(). For example, you might write some code that you think generates a number between 1 and 10, but it actually generates a number between 1 and 9. Be sure to test your code frequently to spot logical errors like these!


<br>
<br>
<br>



<h3>Static Methods Refresher</h3>


In this lesson, we’re going to dive into how to create classes with your own static methods and static variables. To begin, let’s take a quick refresher on static methods.

Static methods are methods that belong to an entire class, not a specific object of the class. Static methods are called using the class name and the . operator. We’ve seen a couple of static methods already!
```
double randomNumber = Math.random();
// Stores a random decimal between 0.0 and 1.0 in randomNumber

double number = Double.valueOf("2.5");
// Transforms the String "2.5" into a double
```


In the first example, ```random()``` is a static method that belongs to the Math class. We didn’t need to create a Math object (like Math myMathObject = new Math()) in order to use that method. We could just call it using the class name.

Similarly, valueOf() is a static method of the Double class. Given a String as an input, this method will turn that String into a double. Again, we don’t need to create a Double object in order to call this method — we use the class itself to call it.

Finally, notice that our main() methods have been static this whole time. When Java runs your program, it calls that the main method of your class — YourClassName.main().



```
public class ExerciseOne{
  public static void main(String[] args){

    int randomNum = (int)(Math.random() * 10) + 1;
    System.out.println("Your random number between one and ten is " + randomNum);
    
    int negativeNum = -2;
    int absNum = Math.abs(negativeNum);
    System.out.println("The absolute value of "+ negativeNum + " is " + absNum);

    String myNewString = Integer.toString(1);
    System.out.println(myNewString);

  }
}
```

<br>
<br>

<h3>Static Variables</h3>
// Static Variables belong to the class itself, instead of an object of the class. Like fixed variable eg. animal species


We’ll begin writing our own static methods soon, but before we do, let’s take a look at static variables. Much like static methods, you can think of static variables as belonging to the class itself instead of belonging to a particular object of the class.

Just like with static methods, we can access static variables by using the name of the class and the . operator. Finally, we declare static variables by using the static keyword during declaration. This keyword usually comes after the variable’s access modifier (public or private).

When we put this all together, we might end up with a class that looks something like this:
```
public class Dog{

  // Static variables
  public static String genus = "Canis";

  //Instance variables
  public int age;
  public String name;

  public Dog(int inputAge, String inputName){
    this.age = inputAge;
    this.name = inputName;
  }
}
```
Since all dogs share the same genus, we could use a static variable to store that information for the entire class. However, we want each dog to have its own unique name and age, so those aren’t static. We could now access this static variable in a main() function like so:
```
public class Dog{
  //Variables, constructors and methods defined here

  public static void main(String[] args){
    System.out.println(Dog.genus); // Prints Canis
  }
}
```

Unlike static methods, you can still access static variables from a specific object of the class. However, no matter what object you use to access the variable, the value will always be the same. You can think of it as all objects of the class sharing the same variable
```
public static void main(String[] args){
  Dog snoopy = new Dog(3, "Snoopy");
  Dog ringo = new Dog(5, "Ringo");

  System.out.println(Dog.genus); // Prints Canis
  System.out.println(snoopy.genus); // Prints Canis
  System.out.println(ringo.genus); // Prints Canis
}
```

Finally, you might have seen a few static variables before. If you want easy access to the largest possible integer, you can get it by using Integer.MAX_VALUE. If you look at the official documentation you’ll see that this variable is public, static, and ```final```. 

(final means that you can’t change the variable’s value after creating it.) We’re starting to know a lot of Java keywords!

<br>
<br>

<h3>Modifying Static Variables</h3>

Now that we’ve created a couple of static variables, let’s start to edit them. The good news is that editing static variables is similar to editing any other variable. Whether you’re writing code in a constructor, a non-static method, or a static method, you have access to static variables.

Before we jump into the checkpoints, let’s think about times when you might want to edit static variables. Often times, you’ll see static variables used to keep track of information about all objects of a class. For example, our variable numATMs is keeping track of the total number of ATMs in the system. Therefore, every time an ATM is created (using the constructor), we should increase that variable by 1. If we could somehow destroy an ATM, the method that destroys it should decrease numATMs static variable by 1.

Similarly, we have a variable named totalMoney. This variable is keeping track of all money across all ATMs. Whenever we remove money from an ATM using the non-static withdrawMoney() method, we should modify the money instance variable for that particular ATM as well as the totalMoney variable. In doing so, all ATMs will know how much money is in the system.


```
public class ATM{
  // Static variables
  public static int totalMoney = 0;
  public static int numATMs = 0;

  // Instance variables
  public int money;

  public ATM(int inputMoney){
    this.money = inputMoney;

    // Steps 1 and 2: Edit numATMs and total money here
    numATMs += 1;
    totalMoney += inputMoney;
  }

  public void withdrawMoney(int amountToWithdraw){
    if(amountToWithdraw <= this.money){
      this.money -= amountToWithdraw;

      // Step 3: Edit totalMoney here
      totalMoney -= amountToWithdraw;
    }
  }

  public static void main(String[] args){

    System.out.println("Total number of ATMs: " + ATM.numATMs); 
    ATM firstATM = new ATM(1000);
    ATM secondATM = new ATM(500);
    System.out.println("Total number of ATMs: " + ATM.numATMs); 

    System.out.println("Total amount of money in all ATMs: " + ATM.totalMoney);  
    firstATM.withdrawMoney(500);
    secondATM.withdrawMoney(200);
    System.out.println("Total amount of money in all ATMs: " + ATM.totalMoney);

  }
}
```

<br>
<br>
<br>


<h3>Writing Your Own Static Methods</h3>

Nice work! Now that we’ve seen how static variables work, let’s look into how to write our own static methods.

Let’s get the syntax out of the way first — just like with variables, to create a static method, use the static keyword in the method’s definition. Just like with variables, this keyword usually comes after public or private.

```
public static void myFirstStaticMethod(){
  // Some code here
}
```
Often times, you’ll see static methods that are accessors or mutators for static variables.
```
public static int getMyStaticVariable(){
  return myStaticVariable;
}

public static void setMyStaticVariable(int newValue){
  myStaticVariable = newValue;
}
```

One important rule to note is that static methods can’t interact with non-static instance variables.

To wrap your mind around this, consider why we use this when working with non-static instance variables. Let’s say we have a Dog class with a non-static instance variable named age. If we have a line of code like this.age = 5;, that means we’re setting the age of a specific Dog equal to 5. However, if age were static, that would mean that the variable belongs to the entire class, not a specific object.


<strong>The ```this``` keyword can’t be used by a static method since static methods are associated with an entire class, not a specific object of that class. If you try to mix this with a static method, you’ll see the error message non-static variable this cannot be referenced from a static context. ***</strong>


```
public class ATM{
  // Static variables
  public static int totalMoney = 0;
  public static int numATMs = 0;

  // Instance variables
  public int money;

  public ATM(int inputMoney){
    this.money = inputMoney;
    numATMs += 1;
    totalMoney += inputMoney;
  }

  public void withdrawMoney(int amountToWithdraw){
    if(amountToWithdraw <= this.money){
      this.money -= amountToWithdraw;
      totalMoney -= amountToWithdraw;
    }
  }

  // Write your averageMoney() method here
  public static void averageMoney(){
    System.out.println(totalMoney / numATMs);
    System.out.println(this.money); // produces error to show there's single object for reference, as static method belongs and refers to whole class. Computer tells you this. is for single object reference, and it don't make sense for static context'
  }

  public static void main(String[] args){

    System.out.println("Total number of ATMs: " + ATM.numATMs); 
    ATM firstATM = new ATM(1000);
    ATM secondATM = new ATM(500);
    System.out.println("Total number of ATMs: " + ATM.numATMs); 

    System.out.println("Total amount of money in all ATMs: " + ATM.totalMoney);  
    firstATM.withdrawMoney(500);
    secondATM.withdrawMoney(200);
    System.out.println("Total amount of money in all ATMs: " + ATM.totalMoney);    

    // Call averageMoney() here
    ATM.averageMoney();
  }

}
```


<h3>Review</h3>

Great work! You now have an understanding of what the static keyword does. In fact, if you’ve made it this far in your Java lessons, you probably have a pretty good sense of what all the keywords and jargon are doing in public static void main(String[] args). Take a moment to celebrate — that line of code can be incredibly intimidating for new learners and it’s a real accomplishment to learn about all of those different pieces.

To review, here are some of the main takeaways about static methods and variables:

<ul>
<li>Static methods and variables are associated with the class as a whole, not objects of the class.</li>
<li>Static methods and variables are declared as static by using the static keyword upon declaration.</li>
<li>Static methods cannot interact with non-static instance variables. This is due to static methods not having a this reference.</li>
<li>Both static methods and non-static methods can interact with static variables.</li>
</ul>


```
public class ATM{
  // Static variables
  public static int totalMoney = 0;
  public static int numATMs = 0;

  // Instance variables
  public int money;

  public ATM(int inputMoney){
    this.money = inputMoney;
    numATMs += 1;
    totalMoney += inputMoney;
  }

  public void withdrawMoney(int amountToWithdraw){
    if(amountToWithdraw <= this.money){
      this.money -= amountToWithdraw;
      totalMoney -= amountToWithdraw;
    }
  }

  public void depositMoney(int amountToDeposit){
      this.money += amountToDeposit;
      totalMoney += amountToDeposit;
    
  }

  public static void averageMoney(){
    System.out.println(totalMoney / numATMs);
  }

  public static void main(String[] args){

    System.out.println("Total number of ATMs: " + ATM.numATMs); 
    ATM firstATM = new ATM(1000);
    ATM secondATM = new ATM(500);
    System.out.println("Total number of ATMs: " + ATM.numATMs); 

    System.out.println("Total amount of money in all ATMs: " + ATM.totalMoney);  
    firstATM.withdrawMoney(500);
    secondATM.withdrawMoney(200);
    System.out.println("Total amount of money in all ATMs: " + ATM.totalMoney);    

    firstATM.depositMoney(5000);
    System.out.println("Total amount of money in all ATMs: " + ATM.totalMoney); 
    System.out.println("Total amount of money in all first ATM: " + firstATM.money); 

    // Call averageMoney() here
    ATM.averageMoney();
  }

}
```

<br>
<br>
<br>


<h2>INHERITANCE AND POLYMORPHISM</h2>

<h3>Introducing Inheritance</h3>

Our Triangle class will inherit all the traits of Shape, but Triangle can also contain its own unique methods and variables. For example, we could have an instance variable called hypotenuse and a method called findHypotenuse() that can only be accessed by Triangle class references. Objects of Triangle can call any method contained in Triangle or Shape. This gives us a bunch of possibilities!

There are several terms you’ll encounter frequently:

<li>Parent class, superclass, and base class refer to the class that another class inherits from (like Shape).</li>
<li>Child class, subclass, and derived class refer to a class that inherits from another class (like Triangle).</li>

<img src = "https://content.codecademy.com/courses/learn-java/revised-2019/inheritance.gif">


<br>
<br>
<br>

<h3>Inheritance in Practice</h3>

So how do we define a child class so that it inherits from a parent class? We use the keyword extends like this:

```
class Shape {

  // Shape class members

}

class Triangle extends Shape {

  // additional Triangle class members

}
```

Now Triangle has inherited traits from Shape, meaning it copied over class members from Shape. When we use inheritance to extend a subclass from a superclass, we create an “is-a” relationship from the subclass to the superclass. For example, an object of Triangle is a member of the Shape class; however, an object of Shape is not necessarily an object of Triangle.

Until now, we’ve only been working with one class and one file. However, most Java programs utilize multiple classes, each of which requires its own file. Only one file needs a ```main() method``` — this is the file we will run.

Note: the various classes in our Java package — even though they are in different files — will have access to each other, so we can instantiate one class inside of another.


<br>
<br>


<h3>Inheriting the Constructor</h3>

Hang on, you might be thinking, if the child class inherits its parent’s fields and methods, does it also inherit the constructor? Let’s take a look at how the super() constructor works!

Let’s say Shape has a numSides field that is set by passing an integer into the constructor. If we’re instantiating a Triangle, we would want that number to always be 3, so we’d want to modify the constructor to automatically assign numSides with a value of 3.

Can we do that?

As it happens, Java has a trick up its sleeve for just this occasion: using the super() method which acts like the parent constructor inside the child class constructor:

```
class Triangle extends Shape {

  Triangle() {
    super(3);
  }

  // additional Triangle class members

}
```
By passing 3 to super(), we are making it possible to instantiate a Triangle without passing in a value for numSides.

Meanwhile, super(3) (behaving as Shape(3)) will shoulder the responsibility of setting numSides to 3 for our Triangle object. It’s like we called Shape(3).

It is also possible to write a constructor without making a call to any ```super()``` constructor:

```
class Triangle extends Shape {

  Triangle() {
    this.numSides = 3;
  }

  // additional Triangle class methods

}
```

In this situation, Java secretly calls the parent class’ no-argument constructor (super()). So in this specific example, the Triangle() constructor first calls the Shape() constructor. That Shape() takes care of whatever business it needs to take care of. And then after that is complete, we go in and set this.numSides to 3.

If you’re writing a constructor of a child class, and don’t explicitly make a call to a constructor from a parent class using super, it’s important to remember that Java will automatically (and secretly) call super() as the first line of your child class constructor.


<br>
<br>
















</body>


