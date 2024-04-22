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



String[] args
8 min
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

1.We want to give the user an option to make a Newsfeed object for robots or for humans. We will take either "Robot" or "Human" as an argument to the main() method when the Newsfeed.java file is run.

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

Store object references as elements
Store elements of the same type (just like arrays)
Access elements by index (just like arrays)
Add elements
Remove elements
Remember how we had to import java.util.Arrays in order to use additional array methods? To use an ArrayList at all, we need to import them from Java’s util package as well:

import java.util.ArrayList;

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
ArrayList<String> babyNames = new ArrayList<String>();
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







</body>











