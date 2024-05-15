# Learn-Java
<body>

<a href= "https://github.com/agentjimlam/Learn-Java/blob/main/README.md#for-each-loops">Link to For Each Loop, aka enhanced loops eg. for (String inventoryItem : inventoryItems) </a> <br>
<a href="https://github.com/agentjimlam/Learn-Java/blob/main/README.md#break-and-continue">Link to break and continue, FizzBuzz, eg. check if divisible by 3, print something</a><br>
<a href="https://github.com/agentjimlam/Learn-Java/blob/main/README.md#switch-statement">Link to Switch statement. If-Else-If</a><br>
<a href="https://github.com/agentjimlam/Learn-Java/blob/main/README.md#combining-conditional-operators">Link to Order of Conditional Operators. bracket -> ! -> && -> ||</a><br>
<br>
<a href="https://github.com/agentjimlam/Learn-Java/blob/main/README.md#calling-static-methods">Link to Static Methods</a> <br>
<a href="https://github.com/agentjimlam/Learn-Java/blob/main/README.md#writing-your-own-static-methods">Link to .this and static methods. AKA non-static variable .this cannot be referenced from a static context</a><br>
<a href="https://github.com/agentjimlam/Learn-Java/blob/main/README.md#method-overriding">How to child class method override parent class method</a> <br>
<a href ="https://github.com/agentjimlam/Learn-Java/blob/main/README.md#length">Link to Length property</a><br>
<a href ="https://github.com/agentjimlam/Learn-Java/blob/main/README.md#classes-constructors">Link to Constructors: rmb, an object/instance is a reference data type</a><br> 
<a href ="https://github.com/agentjimlam/Learn-Java/blob/main/README.md#scope">Link to method scope: rmb, variables within methods only exist within the scope of those methods</a><br>
<a href ="https://github.com/agentjimlam/Learn-Java/blob/main/README.md#returns">Link to Return</a><br>
<br>
<a href ="https://github.com/agentjimlam/Learn-Java/blob/main/README.md#creating-an-array-explicitly">Link to Array. import java.util.Arrays</a><br>
<a href ="https://github.com/agentjimlam/Learn-Java/blob/main/README.md#the-tostring-method">Link to ToString method</a><br>
<a href="https://github.com/agentjimlam/Learn-Java/blob/main/README.md#string-args">Link to String[] args - java terminal</a><br>
<br>
<a href="https://github.com/agentjimlam/Learn-Java/blob/main/README.md#intro-to-arraylist">Link to ArrayList- you need to "import java.util.ArrayList" to use ArrayList</a><br>
// Unlike arrays, ArrayList can add and remove elements, whereas arrays cannot add or remove elements, fixed size once created
<br>
// For ArrayList, import java.util.ArrayList. For arrays, import java.util.Arrays
<br> 
// Static Variables belong to the class itself, instead of an object of the class. Like fixed variable shared by ALL objects eg. animal species
// Unlike static methods, you can still access static variables from a specific object of the class. However, no matter what object you use to access the variable, the value will always be the same. You can think of it as all objects of the class sharing the same variable. 
// If eg. class ATM and the object myATM both use "public static int totalMoney" as their money variable, every object is gonna have/shares same value of totalMoney, because it is static variable, shared by across all instances/objects of the ATM class.

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



<h3>Classes: Syntax</h3>

Let’s explore how to define a class in Java. We will use a class called Car that represents a real-world car.

The Car class in Java is defined like so:
```
public class Car { 
  // Empty Java Class 
} 
```

In this example, a class named Car is defined with the public keyword. We’ll discuss what the keyword public means in a later exercise. Inside the body of the class, we can add fields to represent relevant information and functions to represent how this class can interact with other objects. We will fill out this class in later exercises.

Let’s practice creating classes by creating a class to represent a store.

<br>
<br>

<h3>Classes: Constructors</h3>


In Java, the constructor is a special type of method defined within the class, used to initialize fields when an instance of the class is created. The name of the constructor method must be the same as the class itself. Generally, the constructor is defined as public. Again, don’t worry about the meaning of the public keyword for now. We will discuss this in a later exercise.

Let’s look at an updated Car class, which includes a constructor.

```
public class Car { 

 // Constructor
 public Car() { 

   // instructions for creating a Car instance 
 }   
} 
```

In the following example, the Car instance is assigned to the variable ferrari:
```
Car ferrari = new Car(); 
```

In this example, we have created an instance of a Car class called ferrari.

After the assignment operator, (=), we call the constructor method, Car(), using the keyword new to indicate that we’re creating a new instance of the Car class. Omitting the new keyword causes an error.

Keep Reading: AP Computer Science A Students

If we print the value of the variable ferrari we would see its memory address: Car@76ed5528 

<strong>In the above example, our variable ferrari is declared as a reference data type rather than with a primitive data type like int or boolean. This means that the variable holds a reference to the memory address of an instance. During its declaration, we specify the class name as the variable’s type, which in this case is Car. </strong>

If we use a special value, null, we can initialize a reference-type variable without giving it a reference. If we were to assign null to an object, it would have a void reference because null has no value.

For example, consider the following code snippet where we create an instance of a Car, assign it a reference, and then set its value to null:
```
Car thunderBird = new Car(); 

System.out.println(thunderBird); // Prints: Car@76ed5528 

thunderBird = null; // change value to null 

System.out.println(thunderBird); // Prints: null 
```

It’s important to understand that using a null reference to call a method or access an instance variable will result in a NullPointerException error.

<br>
<br>


<h3>Classes: Instance Fields</h3>


A real car has characteristics such as brand, model, year, color, etc. In a Java object representing a car, these characteristics are represented by instance fields or instance variables.

In the last exercise, we created an object, but our object has no characteristics! We’ll add characteristics to our class by including instance fields or instance variables.

Let’s revisit the Car class example.

We want our Car objects to have different colors, so we declare an instance field called color. Instance variables are often characterized by their “has-a” relationship with the object. For example, a Car “has-a” color, “has-a” make, “has-a” model name, and “has-a” model year.

Think about what qualities other than color a car might have.

```
public class Car { 

 /* 
 declare fields inside the class 
 by specifying the type and name 
 */ 

 public String color; 
 public int year; 
 public String modelName; 
 public String make; 

 public Car() { 
   /*  
   instance fields available in 
   scope of the constructor method 
   */ 
 } 
} 
```

Instance variables are specific to each instance of the class which means that each object created from the class will have its own copy of these variables. These fields can be set in the following three ways:

If they are public, they can be set like this ```instanceName.fieldName = someValue;```

They can be set by class methods.

They can be set by the constructor method (shown in the next exercise).

Let’s practice this concept by adding characteristics to a class that represents a dog.


<br>
<br>

<h3>Classes: Constructor Parameters</h3>

In Java, parameters are placeholders that we can use to pass information to a method.

Since the constructor is a method, we can include parameters to assign values to instance fields.

Here the Car constructor has a parameter: ```String carColor```:
```
public class Car { 
  public String color; 

  // constructor method with a parameter 
  public Car(String carColor) { 
    // parameter value assigned to the field 
    color = carColor; 
  } 
} 
```
Now, when we create a new instance of the Car class and pass in a string value to the constructor, it will be stored in the parameter carColor. Inside the constructor, we can use this passed value however we want. In our example, we assign the value stored in carColor to the instance field color.

A method can be characterized by its signature, which is the name, number of, and parameters of the method. In the above example, the signature is ```Car(String carColor)```.

Later, we’ll learn how to pass values into a method!

There are two types of parameters: formal and actual. The parameter we defined in the above example, ```String carColor```, is a formal parameter. We can think of them as variables that will store the data that is passed into a method. It specifies the type and name of the data.

We’ll learn about actual parameters in the next exercise.

For now, let’s practice working with constructor parameters.

Keep Reading: AP Computer Science A Students

A class can have multiple constructors. We can differentiate them based on their parameters. The signature helps the compiler to differentiate between different methods.

For example, here we have defined two constructors:
```
public class Car { 
  public String color; 
  public int mpg; 
  public boolean isElectric; 

  // constructor 1 
  public Car(String carColor, int milesPerGallon) { 
    color = carColor; 
    mpg = milesPerGallon; 
  } 

  // constructor 2 
  public Car(boolean electricCar, int milesPerGallon) { 
    isElectric = electricCar; 
    mpg = milesPerGallon; 
  } 
} 
```

The first constructor has two parameters: ```String carColor``` and ```int milesPerGallon```.

While the second one has these: ```boolean electricCar``` and ```int milesPerGallon```.

The values will help the compiler to decide which constructor to use. For example, ```Car myCar = new Car(true, 40)``` will be created by the second constructor because the arguments match the type and order of the second constructor’s signature.

When we don’t define the constructor, the Java compiler creates a default constructor that assigns default values to an instance. Default values can be created by assigning values to the instance fields during their declaration:
```
public class Car { 
 public String color = "red"; 
 public boolean isElectric = false; 
 public int cupHolders = 4; 

 public static void main(String[] args) { 
   Car myCar = new Car(); 
   System.out.println(myCar.color); // Prints: red 
 } 
} 
```

Notice that the color instance field of the myCar object will have a red value because we’ve already defined the default value during the declaration.


<br>
<br>

<h3>Classes: Assigning Values to Instance Fields</h3>

Since the constructor now accepts a parameter, let’s see how we can use this constructor to create an instance of an object with initial values for its fields.

To use the constructor, we call it just as we would an ordinary method and pass in values for the parameters. These values, known as arguments, will be used to initialize the instance fields of the created object.

Let’s revisit our previous example of the Car class.
```
public class Car { 
  public String color; 

  public Car(String carColor) { 
    // assign parameter value to instance field 
    color = carColor; 
  } 
} 
```

In this case, when creating a specific instance of Car called ferrari, we pass the string “red” as the value for the carColor parameter.
```
class Main{ 
  public static void main(String[] args){ 
  Car ferrari = new Car("red"); 
  } 
}  
```
When passing in values to a constructor, just like an ordinary method, the type of the value must match the type of the parameter.

In the code, we pass the String value “red” to the constructor method call: ```new Car("red")```. The parameter ```carColor``` of type String now refers to the value passed in during the method call, which is “red”.

The field color of the object ferrari now has a value of “red”.

Remember, that we can access the fields of an object by using the dot operator like so:
```
ferrari.color; // "red" 
```

Keep Reading: AP Computer Science A Students

An argument refers to the actual values passed during the method call while a parameter refers to the variables declared in the method signature.

When we pass an argument, a copy of the argument value is passed to the parameter rather than the actual variables. This process of calling a method with an argument value is called a call-by-value.

For example, we passed the String value “red” as an argument, but a copy of this value is assigned to the parameter carColor.


<br>
<br>

<h3>Classes: Multiple Fields</h3>

Objects are not limited to a single instance field. We can declare as many fields as necessary for our program’s requirements. To illustrate this, let’s add two more instance fields to our Car instances.

We’ll add a boolean isRunning, which represents whether the car engine is on or not, and an int velocity, which indicates the speed at which the car is traveling.

```
public class Car { 
  String color; 

  // new fields! 
  boolean isRunning; 
  int velocity; 

  // new parameters that correspond to the new fields 
  public Car(String carColor, boolean carRunning, int milesPerHour) { 
    color = carColor; 

    // assign new parameters to the new fields 
    isRunning = carRunning; 
    velocity = milesPerHour; 
  } 
} 

Public class Main(){ 

  public static void main(String[] args) { 
    // new values passed into the method call 
    Car ferrari = new Car("red", true, 27); 
    Car renault = new Car("blue", false, 70); 

    System.out.println(renault.isRunning); // false 
    System.out.println(ferrari.velocity); // 27 
  } 
} 
```
Now, the constructor has two new parameters: boolean carRunning and int speed`.

Remember, it’s important to pass the arguments in the same order as they are listed in the parameters.
```
// values match types, no error 
Car honda = new Car("green", false, 0); 

// values do not match types, error! 
Car junker = new Car(true, 42, "brown"); 
```
Let’s practice this concept!


<br>
<br>


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

<br>
<br>


<h2>LEARN JAVA: METHODS</h2>

<h3>Introduction</h3>

In the last lesson, we learned that objects have state and behavior. We have seen how to give objects state through instance fields. Now, we’re going to learn how to create object behavior using methods. Remember our example of a Savings Account.

<img src = "https://content.codecademy.com/courses/learn-java/revised-2019/diagram%20of%20an%20object-02.png">
<br>

The state tells us what a savings account should know:

The balance of money available
The behavior tells us what tasks a savings account should be able to perform:

Depositing - increasing the amount available
Withdrawing - decreasing the amount available
Checking the balance - displaying the amount available.
Methods are repeatable, modular blocks of code used to accomplish specific tasks. We have the ability to define our own methods that will take input, do something with it, and return the kind of output we want.

Looking at the example above, recreating a savings account is no easy task. How can one program tackle such a large problem? This is where methods with their ability to accomplish smaller, specific tasks come in handy. Through method decomposition, we can use methods to break down a large problem into smaller, more manageable problems.

Methods are also reusable. Imagine we wrote a sandwich-making program that used 20 lines of code to make a single sandwich. Our program would become very long very quickly if we were making multiple sandwiches. By creating a ```makeSandwich()``` method, we can make a sandwich anytime simply by calling it.

```makeSandwich()``` adds ingredients together to make a sandwich

<img src = "https://content.codecademy.com/courses/learn-java/revised-2019/methods-conceptual.gif">
<br>

In this lesson, we’ll learn how to create and call our very own methods inside of our programs.

Keep Reading: AP Computer Science A Students

If we were to share this sandwich-making program with another person, they wouldn’t have to understand how makeSandwich() worked. If we wrote our program well, all they would need to know is that if they called ```makeSandwich()```, they would receive a sandwich. This concept is known as procedural abstraction: knowing what a method does, but not how it accomplishes it.


<h3>Defining Methods</h3>

If we were to define a ```checkBalance()``` method for the Savings Account example we talked about earlier, it would look like the following:
```
public void checkBalance(){
  System.out.println("Hello!");
  System.out.println("Your balance is " + balance);
}
```

The first line, ```public void checkBalance()```, is the method declaration. It gives the program some information about the method:

```public``` means that other classes can access this method. We will learn more about that later in the course.
The ```void``` keyword means that there is no specific output from the method. We will see methods that are not void later in this lesson, but for now, all of our methods will be void.
```checkBalance()``` is the name of the method.

Every method has its own unique <strong>method signature</strong> which is composed of the method’s name and its parameter type. In this example, the method signature is ```checkBalance()```.

The two print statements are inside the body of the method, which is defined by the curly braces: ```{``` and ```}```.

Anything we can do in our ```main()``` method, we can do in other methods! All of the Java tools you know, like the math and comparison operators, can be used to make interesting and useful methods.

Keep Reading: AP Computer Science A Students

```checkBalance()``` is considered a non-static method because its signature does not include the keyword ```static``` like the ```main()``` method does. We’ll learn more about non-static methods later in this course.

<br>
<br>

<h3>Calling Methods</h3>

When we add a non-static method to a class, it becomes available to use on an object of that class. In order to have our methods get executed, we must call the method on the object we created.

Let’s add a non-static ```startEngine()``` method to our Car class from the previous lesson. Inside the ```main()``` method, we’ll call ```startEngine()``` on the ```myFastCar``` object:

```
class Car {

  String color;

  public Car(String carColor) {
    color = carColor;
  }

  public void startEngine() {
    System.out.println("Starting the car!");
    System.out.println("Vroom!");
  }

  public static void main(String[] args){
    Car myFastCar = new Car("red");
    // Call a method on an object 
    myFastCar.startEngine();
    System.out.println("That was one fast car!");
  }
}
```

Let’s take a closer look at the method call:
```
myFastCar.startEngine();
```
First, we reference our object myFastCar. Then, we use the dot operator (.) to call the method startEngine(). Note that we must include parentheses () after our method name in order to call it.

If we run the above program, we will get the following output.
```
Starting the car!
Vroom!
That was one fast car!
```
Code generally runs in a top-down order where code execution starts at the top of a program and ends at the bottom of a program; however, methods are ignored by the compiler unless they are being called.

When a method is called, the compiler executes every statement contained within the method. Once all method instructions are executed, the top-down order of execution continues. This is why Starting the car! and Vroom! are outputted before That was one fast car!.


<br>
<br>

<h3>Scope</h3>

A method is a task that an object of a class performs.

We mark the domain of this task using curly braces: ```{```, and ```}```. Everything inside the curly braces is part of the task. This domain is called the scope of a method.

We can’t access variables that are declared inside a method in code that is outside the scope of that method.

Looking at the Car class again:
```
class Car {
  String color;
  int milesDriven;

  public Car(String carColor) {
    color = carColor;
    milesDriven = 0;         
  }

  public void drive() {
     String message = "Miles driven: " + milesDriven;
     System.out.println(message);
  }

  public static void main(String[] args){
     Car myFastCar = new Car("red");
     myFastCar.drive();
  }
}
```
<strong>The variable message, which is declared and initialized inside of drive, cannot be used inside of ```main()```! It only exists within the scope of the ```drive()``` method.</strong>

However, milesDriven, which is declared at the top of the class, can be used inside all methods in the class, since it is in the scope of the whole class.


<br>

<h3>Adding Parameters</h3>

We saw how a method’s scope prevents us from using variables declared in one method in another method. What if we had some information in one method that we needed to pass into another method?

Similar to how we added parameters to constructors, we can customize all other methods to accept parameters. For example, in the following code, we create a ```startRadio()``` method that accepts a double parameter, ```stationNum```, and a String parameter called ```stationName```:
```
class Car {

  String color;

  public Car(String carColor) {
    color = carColor;        
  }

  public void startRadio(double stationNum, String stationName) {
    System.out.println("Turning on the radio to " + stationNum + ", " + stationName + "!");
    System.out.println("Enjoy!");
  }

  public static void main(String[] args){
    Car myCar = new Car("red");
    myCar.startRadio(103.7, "Meditation Station");
  }
}
```

Adding parameter values impacts our method’s signature. Like constructor signatures, the method signature includes the method name as well as the parameter types of the method. The signature of the above method is ```startRadio(double, String)```.

In the ```main()``` method, we call the ```startRadio()``` method on the myCar object and provide a double argument of 103.7 and String argument of "Meditation Station", resulting in the following output:
```
Turning on the radio to 103.7, Meditation Station!
Enjoy!
```

Note that when we call on a method with multiple parameters, the arguments given in the call must be placed in the same order as the parameters appear in the signature. If the argument types do not match the parameter types, we’ll receive an error.

Keep Reading: AP Computer Science A Students

Through method overloading, our Java programs can contain multiple methods with the same name as long as each method’s parameter list is unique. For example, we can recreate our above program to contain two startRadio() methods:
```
// Method 1
public void startRadio(double stationNum, String stationName) {
  System.out.println("Turning on the radio to " + stationNum + ", " + stationName + "!");
  System.out.println("Enjoy!");
}
  
// Method 2
public void startRadio(double stationNum) {
  System.out.println("Turning on the radio to " + stationNum + "!");
}

public static void main(String[] args){
  Car myCar = new Car("red");
  // Calls the first startRadio() method
  myCar.startRadio(103.7, "Meditation Station");

  // Calls the second startRadio() method
  myCar.startRadio(98.2);
}
```


<br>

<h3>Reassigning Instance Fields</h3>

Earlier, we thought about a Savings Account as a type of object we could represent in Java.

Two of the methods we need are depositing and withdrawing:
```
public class SavingsAccount{
  double balance;
  public SavingsAccount(double startingBalance){
    balance = startingBalance;
  }

  public void deposit(double amountToDeposit){
     //Add amountToDeposit to the balance
  }

  public void withdraw(double amountToWithdraw){
     //Subtract amountToWithdraw from the balance
  }

  public static void main(String[] args){

  }
}
```

These methods would change the value of the variable balance. We can reassign balance to be a new value by using our assignment operator, ```=```, again.
```
public void deposit(double amountToDeposit){
  double updatedBalance = balance + amountToDeposit;
  balance = updatedBalance;
}
```

Now, when we call ```deposit()```, it should change the value of the instance field balance:
```
public static void main(String[] args){
  SavingsAccount myAccount = new SavingsAccount(2000);
  System.out.println(myAccount.balance);
  myAccount.deposit(100);
  System.out.println(myAccount.balance);
}
```
This code first prints 2000, the initial value of ```myAccount.balance```, and then prints 2100, which is the value of myAccount.balance after the ```deposit()``` method has run.

Changing instance fields is how we change the state of an object and make our objects more flexible and realistic.

<br>


<h3>Returns</h3>

Remember, variables can only exist in the scope that they were declared in. We can use a value outside of the method it was created in if we return it from the method.

We return a value by using the keyword return:
```
public int numberOfTires() {
   int tires = 4;
   // return statement
   return tires;
}
```

This method, called ```numberOfTires()```, returns 4. Once the return statement is executed, the compiler exits the function. Any code that exists after the return statement in a function is ignored.

In past exercises, when creating new methods, we used the keyword void. Here, we are replacing void with int, to signify that the return type is an int.

The ```void``` keyword (which means “completely empty”) indicates that no value is returned after calling that method.

A non-void method, like ```numberOfTires()``` returns a value when it is called. We can use datatype keywords (such as int, char, etc.) to specify the type of value the method should return. The return value’s type must match the return type of the method. If the return expression is compatible with the return type, a copy of that value gets returned in a process known as return by value.

Unlike void methods, non-void methods can be used as either a variable value or as part of an expression like so:
```
public static void main(String[] args){
    Car myCar = new Car("red");
    int numTires = myCar.numberOfTires();
}
```

Within ```main()```, we called the ```numberOfTires()``` method on myCar. Since the method returns an int value of 4, we store the value in an integer variable called numTires. If we printed numTires, we would see 4.

Keep Reading: AP Computer Science A Students

We learned how to return primitive values from a method, but what if we wanted our method to return an object? Returning an object works a little differently than returning a primitive value. When we return a primitive value, a copy of the value is returned; however, when we return an object, we return a reference to the object instead of a copy of it.

Let’s create a second class, carLot, that takes in a Car as a parameter and contains a method which returns a Car object.
```
class CarLot {
    Car carInLot;
    public CarLot(Car givenCar) {
        carInLot = givenCar;
    }

    public Car returnACar() {
        // return Car object
        return carInLot;
    }

    public static void main(String[] args) {
        Car myCar = new Car("red", 70);
        System.out.println(myCar); 
        CarLot myCarLot = new CarLot(myCar);
        System.out.println(myCarLot.returnACar());
    }
}
```


This code outputs the same memory address because myCar and carInLot have the same reference value:
```
Car@2f333739
Car@2f333739
```

<br>

<h3>The toString() Method</h3>

When we print out Objects, we often see a String that is not very helpful in determining what the Object represents. In the last lesson, we saw that when we printed our Store objects, we would see output like:
```
Store@6bc7c054
```
where Store is the name of the object and ```6bc7c054``` is its position in memory.

This doesn’t tell us anything about what the Store sells, the price, or the other instance fields we’ve defined. We can add a method to our classes that makes this printout more descriptive.

When we define a ```toString()``` method for a class, we can return a String that will print when we print the object:
```
class Car {

    String color;

    public Car(String carColor) {
        color = carColor;
    }

    public static void main(String[] args){
        Car myCar = new Car("red");
        System.out.println(myCar);
    }

   public String toString(){
       return "This is a " + color + " car!";
   }
}
```

When this runs, the command ```System.out.println(myCar)``` will print ```This is a red car!```, which tells us about the Object myCar.

<br>

<h3>Review</h3>

Great work! Methods are a powerful way to abstract tasks away and make them repeatable. They allow us to define behavior for classes, so that the Objects we create can do the things we expect them to. Let’s review everything we have learned about methods so far.

<ul>
	<li>Defining a method : Method declarations will declare a method’s return type, name, and parameters</li>
	<li>Calling a method : Methods are invoked with a . and ()</li>
	<li>Parameters : Inputs to the method and their types are declared in parentheses in the method signature</li>
	<li>Changing Instance Fields : Methods can be used to change the value of an instance field</li>
	<li>Scope : Variables only exist within the domain that they are created in</li>
	<li>Return : The type of the variables that will be output are declared in the method declaration</li>
</ul>

As you move through more Java material, it will be helpful to frame the tasks you create in terms of methods. This will help you think about what inputs you might need and what output you expect.


<br>
<br>








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

<br>
<br>


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

```
if-then:
code block runs if condition is true

if-then-else:
one block runs if conditions is true
another block runs if condition is false

if-then-else chained:
same as if-then but an arbitrary number of conditions

switch:
switch block runs if condition value matches case value
```


```
public class Order {
  boolean isFilled;
  double billAmount;
  String shipping;
  
  public Order(boolean filled, double cost, String shippingMethod) {
		if (cost > 24.00) {
      System.out.println("High value item!");
    } else {
      System.out.println("Low value item!");
    }
    isFilled = filled;
    billAmount = cost;
    shipping = shippingMethod;
  }
  
  public void ship() {
    if (isFilled) {
      System.out.println("Shipping");
    } else {
      System.out.println("Order not ready");
    }
    
    double shippingCost = calculateShipping();
    
    System.out.println("Shipping cost: ");
    System.out.println(shippingCost);
  }
  
  public double calculateShipping() {
    double shippingCost;
    switch (shipping) {
      case "Regular":
        shippingCost = 0;
        break;
      case "Express":    
        shippingCost = 1.75;
        break;
      default:
        shippingCost = .50; 
    }
    return shippingCost;
 	}
  
  public static void main(String[] args) {
    // create instances and call methods here!
    Order book = new Order(true, 50.00, "Regular");

    book.ship();

    Order gigaToy = new Order(false, 50.00, "nil");

    gigaToy.ship();
  }
}

```

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

<ul>
	<li>Conditions placed in parentheses - ()</li>
	<li>NOT - !</li>
	<li>AND - &&</li>
	<li>OR - ||</li>
</ul>

	
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

public class Main {

  public static void main(String[] args){
    
    String[] students = {"Sade", "Alexus", "Sam", "Koma"};
    int[] mathScores = new int[4];

    System.out.println(students);
    System.out.println(Arrays.toString(students));
    

    mathScores[0] = 64;
    mathScores[1] = 57;
    mathScores[2] = 76;
    mathScores[3] = 98;
    System.out.println(mathScores);
    System.out.println("The number of students in the class is " + students.length + ".");
    System.out.println(Arrays.toString(mathScores));

    System.out.println(students[0] + "... math score: " + mathScores[0]);
    System.out.println(students[1] + "... math score: " + mathScores[1]);
// etc
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

<br>
<br>
<br>
<br>


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
<strong>Dude in forums felt the Qn too easy so he made 3 examples for break and continue.</strong>


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

<strong>We can read the ```:``` as ```“in”``` like this: ```for each inventoryItem (which should be a String) in inventoryItems, print inventoryItem.```</strong>

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
  public static void main(String[] args){
    CheckingAccount accountOne = new CheckingAccount("Zeus", 100, "1");
    
    accountOne.getAccountInformation();
  }
}
```
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

Qn: Here are some ideas that you can experiment with:

- Create a method to close an account.
- Method to apply fees or charges.
- Introduce different currencies into the code.

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
  public CheckingAccount accountOne; 		// have to change from private to public for Main.java to access, else error
  public CheckingAccount accountTwo;		// have to change from private to public for Main.java to access, else error

  public Bank(){
    this.accountOne = new CheckingAccount("Zeus", 100, "1");
    this.accountTwo = new CheckingAccount("Hades", 200, "2");
  }


Main.java
  public static void main(String[] args){
    Bank bankOfGods = new Bank();
    bankOfGods.accountOne.getAccountInformation();	// I changed access modifier to public, else have to write a lot of code in Bank.java
    bankOfGods.accountOne.calculateNextMonthInterest();		
  }

}

```



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

In this situation, Java secretly calls the parent class’ no-argument constructor ```(super())```. So in this specific example, the ```Triangle()``` constructor first calls the ```Shape()``` constructor. That Shape() takes care of whatever business it needs to take care of. And then after that is complete, we go in and set this.numSides to 3.

If you’re writing a constructor of a child class, and don’t explicitly make a call to a constructor from a parent class using super, it’s important to remember that Java will automatically (and secretly) call ```super()``` as the first line of your child class constructor.





<br>
<br>







<h3>Parent Class Aspect Modifiers</h3>

You may recall that Java class members use private and public access modifiers to determine whether they can be accessed from outside the class. So does a child class inherit its parent’s private members?

Well, no. But there is another access modifier we can use to keep a parent class member accessible to its child classes and to files in the package it’s contained in — and otherwise private: protected.


<img src = "https://content.codecademy.com/courses/learn-java/revised-2019/access-modifiers-chart.png">


Here’s what ```protected``` looks like in use:


```
class Shape {

  protected double perimeter;

}

// any child class of Shape can access perimeter
```

In addition to access modifiers, there’s another way to establish how child classes can interact with inherited parent class members: using the ```final``` keyword. If we add ```final``` after a parent class method’s access modifier, we disallow any child classes from changing that method. This is helpful in limiting bugs that might occur from modifying a particular method.

Though it is not required, there is an established order when two or more field modifiers are used (eg. ```public final```). To learn more about this read the documentation.



<br>
<br>
<br>



<h4>On final</h4>
A method can be declared final to prevent subclasses from overriding or hiding it.

It is a compile-time error to attempt to override or hide a final method.

A private method and all methods declared immediately within a final class (§8.1.1.2) behave as if they are final, since it is impossible to override them.

<br>
<br>
<br>



<h3>Introducing Polymorphism</h3>

In Java, if Orange is a Fruit through inheritance, you can then use Orange in the same contexts as Fruit like this:

```
String makeJuice(Fruit fruit) {    // looking for a fruit...

  return "Apple juice and " + fruit.squeeze();

}

// inside main()
Orange orange = new Orange();
System.out.println(juicer.makeJuice(orange));  // and i put in orange
```

Wait, how does that work?

This is because Java incorporates the object-oriented programming principle of polymorphism. Polymorphism, which derives from Greek meaning “many forms”, allows a child class to share the information and behavior of its parent class while also incorporating its own functionality.

The main advantages of polymorphic programming:

<ul>
<li>Simplifying syntax</li>
<li>Reducing cognitive overload for developers</li>
<li>These benefits are particularly helpful when we want to develop our own Java packages for other developers to import and use.</li>
</ul>

For example, the built-in operator ```+``` can be used for both doubles and ints. To the computer, the + means something like addDouble() for one and addInt() for the other, but the creators of Java (and of other languages) didn’t want to burden us as developers with recalling each individual method.

Note that the reverse situation is not true; you cannot use a generic parent class instance where a child class instance is required. So an Orange can be used as a Fruit, but a Fruit cannot be used as an Orange.

<img src ="https://content.codecademy.com/courses/learn-java/revised-2019/polymorphism.gif">

<br>
<br>
<br>






<h3>Method Overriding</h3> // How to child class method override parent class method

One common use of polymorphism with Java classes is something we mentioned earlier — overriding parent class methods in a child class. Like the + operator, we can give a single method slightly different meanings for different classes. This is useful when we want our child class method to have the same name as a parent class method but behave a bit differently in some way.

Let’s say we have a ```BankAccount class``` that allows us to print the current balance. We want to build a ```CheckingAccount``` class that inherits the functionality of a ```BankAccount``` but with a modified ```printBalance()``` method. We can do the following:

```
class BankAccount {
  protected double balance;

  public BankAccount(double balanceIn){
    balance = balanceIn;
  }

  public void printBalance() {
    System.out.println("Your account balance is $" + balance);
  }
}

class CheckingAccount extends BankAccount {
  
  public CheckingAccount(double balance) {
    super(balance);
  }

  @Override
  public void printBalance() {
    System.out.println("Your checking account balance is $" + balance);
  }
}
```

Notice that in order to properly override ```printBalance()```, in ```CheckingAccount``` the method has the following in common with the corresponding method in ```BankAccount```:

<li>Method name</li>
<li>Return type</li>
<li>Number and type of parameters</li>


You may have also noticed the ```@Override``` keyword above ```printBalance()``` in ```CheckingAccount```. This annotation informs the compiler that we want to override a method in the parent class. If the method doesn’t exist in the parent class, we’ll get a helpful error when we compile the program.

Keep Reading: AP Computer Science A Students

In a previous exercise, we learned that the super keyword can be used to call the constructor of a superclass. That’s not the only use of super; we can also use this keyword to call the methods of a parent class. While we now have the ability to override methods from a superclass, we may find ourselves in a unique situation where we want to use the superclass method instead of the subclass’ overridden method.

If that’s the case, we can call the parent class method by prepending super followed by the dot operator (.) to the method call. Note that this only works if we pass in the proper method parameters. Let’s see this in action by adding a ```checkBalances()``` method to CheckingAccount that calls both versions of printBalance():

```
class CheckingAccount extends BankAccount {
  public CheckingAccount(double balance) {
    super(balance);
  }

  @Override
  public void printBalance() {
    System.out.println("Your checking account balance is $" + balance);
  }

  public void checkBalances() {
    // calls method from CheckingAccount
    printBalance();
    // calls method from BankAccount
    super.printBalance();
  }

  public static void main(String[] args) {
    CheckingAccount myCheckings = new CheckingAccount(5000);
    myCheckings.checkBalances();
  }
}
```
This program will output:
```
Your checking account balance is $5000
Your account balance is $5000
```

<br>
<br>
<br>



<h3>Using a Child Class as its Parent Class</h3>  
**KEY Takeaway = override happens at runtime. before that is compiler, compiler sees code, sees child class object instantiated as parent class object, so it sees child class object created to be adult class object 


An important facet of polymorphism is the ability to use a child class object where an object of its parent class is expected.

One way to do this explicitly is to instantiate a child class object as a member of the parent class. We can instantiate a CheckingAccount object as a BankAccount like this:
```
BankAccount kaylasAccount = new CheckingAccount(600.00);
```

We can use ```kaylasAccount``` as if it were an instance of ```BankAccount```, in any situation where a ```BankAccount``` object would be expected. (This would be true even if ```kaylasAccount``` were instantiated as a ```CheckingAccount```, but using the explicit child as parent syntax is most helpful when we want to declare objects in bulk.)

It is important to note here that the compiler just considers ```kaylasAccount``` to be any old ```BankAccount```. But because method overriding is handled at runtime, if we call ```printBalance()```, we’ll see something ```CheckingAccount``` specific:

```
Your checking account balance is $600.00
```

This is because at runtime, ```kaylasAccount``` is recognized as the ```CheckingAccount``` it is. So, what if ```CheckingAccount``` has a method ```transferToSavings()``` that ```BankAccount``` does not have? Can ```kaylasAccount``` still use that method?

Well, no. The compiler believes that ```kaylasAccount``` is just a ```BankAccount``` that doesn’t have some fancy child class ```transferToSavings()``` method, so it would throw an error.


<br>
<br>




<h3>Child Classes in Arrays and ArrayLists</h3>

Usually, when we create an array or an ArrayList, the list items all need to be the same type. But polymorphism puts a new spin on what is considered the same type…

In fact, we can put instances of different classes that share a parent class together in an array or ArrayList! For example, let’s say we have a Monster parent class with a few child classes: Vampire, Werewolf, and Zombie. We can set up an array with instances of each:

```
Monster dracula, wolfman, zombie1;

dracula = new Vampire();
wolfman = new Werewolf();
zombie1 = new Zombie();

Monster[] monsters = {dracula, wolfman, zombie1};
```

We can even iterate through the list of items — regardless of subclass — and perform the same action with each item:
```
for (Monster monster : monsters) {

  monster.attack();

}
```

In the code above, we were able to call ```attack()``` on each monster in monsters despite the fact that, in the ```for-each``` loop, monster is declared as the parent class type ```Monster```.

<br>
<br>
<br>

<a href= "https://github.com/agentjimlam/Learn-Java/blob/main/README.md#for-each-loops">Link to For Each Loop</a> <br>
<a href="https://github.com/agentjimlam/Learn-Java/blob/main/README.md#calling-static-methods">Link to Static Methods</a> <br>
<a href="https://github.com/agentjimlam/Learn-Java/blob/main/README.md#method-overriding">How to child class method override parent class method</a> <br>
<a href ="https://github.com/agentjimlam/Learn-Java/blob/main/README.md#length">Link to Length property</a><br>

<h3>Child Classes in Method Parameters</h3>
**Superclass = parent class 

When we call a method that contains parameters, the arguments we place in our method call must match the parameter type. Similar to the previous exercise, polymorphism gives us a little more flexibility with the arguments we can use.

If we use a superclass reference as a method parameter, we can call the method using subclass reference arguments!

For example, imagine the class ScaryStory, whose constructor takes in a reference to the Monster class:
```
class ScaryStory {
  Monster monster;
  String setting;

  public ScaryStory(Monster antagonist, String place) {
    monster = antagonist;
    setting = place;
  }

  public void tellStory(){
    System.out.println("Once upon a time, " + monster.name + " was at " + setting + " looking to scare some mortals.");
  }

  public static void main(String[] args) {
    Monster dracula;
    dracula = new Vampire("Dracula");
    ScaryStory countDracula = new ScaryStory(dracula, "Dracula Castle");
    countDracula.tellStory();
  }
}
```

In the ```main()``` method, we used a reference of the class ```Vampire``` as our argument even though the constructor requested an object of class Monster. This is allowed because ```Vampire``` is a subclass of the ```Monster``` class.

<br>
<br>

<h3>Review of Inheritance and Polymorphism</h3>

Excellent work! You’ve learned quite a bundle about inheritance and polymorphism in Java:

<ul>
	<li>A Java class can inherit fields and methods from another class.</li>
	<li>Each Java class requires its own file, but only one class in a Java package needs a ```main()``` method.</li>
	<li>Child classes inherit the parent constructor by default, but it’s possible to modify the constructor using ```super()``` or override it completely.</li>
	<li>You can use protected and final to control child class access to parent class members.</li>
	<li>Java’s OOP principle of polymorphism means you can use a child class object like a member of its parent class, but also give it its own traits.</li>
	<li>You can override parent class methods in the child class, ideally using the ```@Override``` keyword.</li>
	<li>It’s possible to use objects of different classes that share a parent class together in an array or ```ArrayList```.</li>
</ul>



<br>
<br>

<h2>Debugging</h2>

<br>

<h3>Introduction to Bugs</h3>

“First actual case of bug being found.”

The story goes that on September 9th, 1947, computer scientist Grace Hopper found a moth in the Harvard Mark II computer’s log book and reported the world’s first literal computer bug. However, the term “bug”, in the sense of technical error, dates back at least to 1878 and with Thomas Edison.

On your programming journey, you are destined to encounter innumerable red errors. Some even say that debugging is over 75% of the development time. But what makes a programmer successful isn’t avoiding errors; it’s knowing how to find the solution.

In Java, there are many different ways of classifying errors, but they can be boiled down to three categories:

<li>Syntax errors: Errors found by the compiler.</li>
<li>Run-time errors: Errors that occur when the program is running.</li>
<li>Logic errors: Errors found by the programmer looking for the causes of erroneous results.</li>

Generally speaking, the errors become more difficult to find and fix as you move down the above list.

In this lesson, we will be looking at different errors and different error messages, and we’ll teach you how to think about errors in your code a little differently.

<br>
<br>


<h3>Syntax Errors / Compile-time errors</h3> 

When we are writing Java programs, the compiler is our first line of defense against errors. It can catch syntax errors.

Syntax errors represent grammar errors in the use of the programming language. They are the easiest to find and correct. The compiler will tell you where it got into trouble, and its best guess as to what you did wrong.

Some common syntax errors are:


<li>Misspelled variable and method names</li>
<li>Omitting semicolons ;</li>
<li>Omitting closing parenthesis ), square bracket ], or curly brace }</li>

Here’s an example of a syntax error message:
```
Debug.java:5: error: ';' expected
  int year = 2019
                  ^
1 error
```

Usually the error is on the exact line indicated by the compiler, or the line just before it; however, if the problem is incorrectly nested braces, the actual error may be at the beginning of the nested block.

<br>
<br>


<h3>Run-time Errors</h3>

If our program has no compile-time errors, it’ll run. This is where the fun really starts.

Errors which happen during program execution (run-time) after successful compilation are called run-time errors. Run-time errors occur when a program with no compile-time errors asks the computer to do something that the computer is unable to reliably do.

Some common run-time errors:

<li>Division by zero also known as division error</li>
<li>Trying to open a file that doesn’t exist</li>
<li>There is no way for the compiler to know about these kinds of errors when the program is compiled.</li>

<br>
<br>


<h3>Exceptions</h3>

In the last exercise when we were dealing with run-time errors, you might’ve noticed a new word in the error message: “Exception”.

Java uses exceptions to handle errors and other exceptional events. <strong>Exceptions are the conditions that occur at runtime and may cause the termination of the program.</strong>

When an exception occurs, Java displays a message that includes the name of the exception, the line of the program where the exception occurred, and a stack trace. The stack trace includes:

<ul>
	<li>The method that was running</li>
	<li>The method that invoked it</li>
	<li>The method that invoked that one</li>
	<li>and so on…</li>
</ul>


Make sure to examine it.

Some common exceptions that you will see in the wild:

<ul>
	<li>ArithmeticException: Something went wrong during an arithmetic operation; for example, division by zero.</li>
	<li>NullPointerException: You tried to access an instance variable or invoke a method on an object that is currently null.</li>
	<li>ArrayIndexOutOfBoundsException: The index you are using is either negative or greater than the last index of the array (i.e., array.length-1).</li>
	<li>FileNotFoundException: Java didn’t find the file it was looking for.</li>
</ul>



<br>
<br>





<h3>Exception Handling</h3>

Exception handling is an essential feature of Java programming that allows us to use run-time error exceptions to make our debugging process a little easier.

One way to handle exceptions is using the try/catch:

The try statement allows you to define a block of code to be tested for errors while it is being executed.

The catch statement allows you to define a block of code to be executed if an error occurs in the try block.

The try and catch keywords come in pairs, though you can also catch several types of exceptions in a single block:

```
try {

  //  Block of code to try

} catch (NullPointerException e) {

  // Print the error message like this:
  System.err.println("NullPointerException: " + e.getMessage());
  
  // Or handle the error another way here

}
```

Notice how we used System.err.println() here instead of System.out.println(). System.err.println() will print to the standard error and the text will be in red.

You can also chain exceptions together:

```
try {

  //  Block of code to try

} catch (NullPointerException e) {

  //  Code to handle a NullPointerException

} catch (ArithmeticException e) {

  //  Code to handle an ArithmeticException

}
```

You can learn more about exceptions and handling them here.

Qn: Put the code that you think will cause an ArithmeticException into a try block. Create a catch block that catches the ArithmeticException and prints the error message to the terminal.

```
public class Debug {

  public static void main(String[] args) {
    
    int width = 0;
    int length = 40;
    
    

    try {
     //  Block of code to try
      int ratio = length / width;

    } catch (NullPointerException e) {

      //  Code to handle a NullPointerException
     System.err.println("NullPointerException: " + e.getMessage());

    } catch (ArithmeticException e) {

     //  Code to handle an ArithmeticException
       System.err.println("ArithmeticException: " + e.getMessage());
    }


  }
  
}
```

<br>
<br>




<h3>Logic Errors</h3>

Once we have removed the syntax errors and run-time errors, the program runs successfully. But sometimes, the program still doesn’t do what we want it to do or no output is produced. Hmmm…

These types of errors, which provide incorrect output, but appear to be error-free, are called logic errors. Logic errors occur when there is a design flaw in your program. These are some of the most common errors that happen to beginners and also usually the most difficult to find and eliminate.

Because logical errors solely depend on the logical thinking of the programmer, your job now is to figure out why the program didn’t do what you wanted it to do.

Some common logic errors:

<li>Program logic is flawed</li>
<li>Some “silly” mistake in an if statement or a for/while loop</li>

Note: Logic errors don’t have error messages. Sometimes, programmers use a process called test-driven development (TDD), a way to give logic errors error messages and save yourself a lot of headaches!

<br>
<br>


<h3>Debugging Techniques</h3>

If you have examined the code thoroughly, and you are sure the compiler is compiling the right source file, it is time for desperate measures:

1. Divide and conquer: Comment out or temporarily delete half the code to isolate an issue.

If the program compiles now, you know the error is in the code you deleted. Bring back about half of what you removed and repeat.
If the program still doesn’t compile, the error must be in the code that remains. Delete about half of the remaining code and repeat.
Tip: In most code editors, one can highlight a block of code and use the keyboard shortcut command + / to comment it out.

2. Print statements for the rescue: Use System.out.println() to check variable/return values at various points throughout the program.

A lot of the time with logic errors, there was a flawed piece of logic, a miscalculation, a missing step, etc. By printing out the values at different stages of the execution flow, you can then hopefully pinpoint where you made a mistake.


<h3>Review</h3>


Finding bugs is a huge part of a programmer’s life. Don’t be intimidated by them… embrace them. Errors in your code mean you’re trying to do something cool!

In this lesson, we have learned about the three types of Java errors:
<ul>
	<li>Syntax errors: Errors found by the compiler.</li>
	<li>Run-time errors: Errors found by checks in a running program.</li>
	<li>Logic errors: Errors found by the programmer looking for the causes of erroneous results.</li>
</ul>

	
Remember, Google and Stack Overflow are a programmer’s best friends. For some more motivation, check out this blog post: Thinking About Errors in Your Code Differently.

Sometimes once you’ve tracked down a bug, you might still be confused on how to fix it! Whenever you want to know more about how Java works and what it can do, the best place to go is documentation. You can find the Java documentation at Oracle.


<br>
<br>
<br>



<h2>2D ARRAYS: JAVA</h2>

<h3>Introduction to 2D Arrays</h3>

As we have learned previously, an array is a group of data consisting of the same type. This means that we can have an array of primitive data types (such as integers):
```
[1, 2, 3, 4, 5]
```
We can even have an array of Objects. For example, the following example shows an array of String Objects:
```
["hello", "world", "how", "are", "you"]
```
In Java, arrays are considered Objects; therefore, we can also have an array of arrays:
```
[[1, 2, 3], [4, 5, 6], [7, 8, 9]]
```

These are called 2D arrays since we can logically view them as a two-dimensional matrix of values containing both rows and columns.


Additionally, we can have 2D arrays which are not rectangular in shape. These are called jagged arrays:
```
[['a', 'b', 'c', 'd'], ['e', 'f'], ['g', 'h', 'i', 'j'], ['k']]
```

<img src="https://static-assets.codecademy.com/Paths/ap-computer-science/TwoDArrays/jagged.png">

We won’t be covering jagged arrays in this lesson, but be aware that 2D arrays don’t always have to have the same number of subarrays in each array. This would cause the shape of the 2D array to not be rectangular.

Why use 2D arrays?

<ul>
	<li>It is useful to use 2D arrays for situations where you need to store and organize data by rows and columns. For example, exporting data to be used in a spreadsheet.</li>
	<li>You can condense multiple arrays down to a single variable using 2D arrays. For example, if you have 10 students who each have 10 different quiz grades, you can represent the overall class quiz grades as a 	10x10 2D array by having each row represent a student and each column represent one of the quizzes they have taken.</li>
	<li>2D arrays can be used to map out data. For example, if you want to create a game of tic-tac-toe, you can represent the game state by using a 3x3 2D array.</li>
</ul>



There are many other ways to use 2D arrays depending on the application. The only downside is that once initialized, no new rows or columns can be added or removed without copying the data to a newly initialized 2D array. This is because the length of arrays in Java are immutable (unable to be changed after creation).


<img src="https://static-assets.codecademy.com/Paths/ap-computer-science/TwoDArrays/two_d_arrays.png">


<br>
<br>
<br>


<h3>Accessing Elements in a 2D Array</h3>

Let’s first review how to access elements in regular arrays.

For a normal array, all we need to provide is an index (starting at 0) which represents the position of the element we want to access. Let’s look at an example!

Given an array of five Strings:

```
String[] words = {"cat", "dog", "apple", "bear", "eagle"};
```

We can access the first element using index 0, the last element using the length of the array minus one (in this case, 4), and any of the elements in between. We provide the index of the element we want to access inside a set of brackets. Let’s see those examples in code:
```
// Store the first element from the String array
String firstWord = words[0]; 

// Store the last element of the String array
String lastWord = words[words.length-1];

// Store an element from a different position in the array
String middleWord = words[2];
```

Now for 2D arrays, the syntax is slightly different. This is because instead of only providing a single index, we provide two indices. Take a look at this example:

```
// Given a 2D array of integer data
int[][] data = {{2,4,6}, {8,10,12}, {14,16,18}};

// Access and store a desired element 
int stored = data[0][2];
```

There are two ways of thinking when accessing a specific element in a 2D array.

<li>The first way of thinking is that the first value represents a row and the second value represents a column in the matrix</li>
<li>The second way of thinking is that the first value represents which subarray to access from the main array and the second value represents which element of the subarray is accessed</li>


The above example of the 2D array called data can be visualized like so. The indices are labeled outside of the matrix:

<img src ="https://static-assets.codecademy.com/Paths/ap-computer-science/TwoDArrays/indexes.png">


Using this knowledge, we now know that the result of ```int stored = data[0][2];``` would store the integer 6. This is because the value 6 is located on the first row (index 0) and the third column (index 2). Here is a template which can be used for accessing elements in 2D arrays:
```
datatype variableName = existing2DArray[row][column];
```
Here is another way to visualize the indexing system for our example integer array seen above. We can see what row and column values are used to access the element at each position.

<img src="https://static-assets.codecademy.com/Paths/ap-computer-science/TwoDArrays/accessing.png">


When accessing these elements, if either the row or column value is out of bounds, then an ArrayIndexOutOfBoundsException will be thrown by the application.


Qn 1. Access the integer at the first row and fourth column of intMatrix and store it in a variable called retrievedInt.

If you’d like to check your work, print retrievedInt after creating it.

Qn 2. Print the center value of intMatrix multiplied by 3 to the console. Make sure to access the correct element!

```
public class Exercise3 {
	public static void main(String[] args) {
		// Using the provided 2D array
	  int[][] intMatrix = {
				{1, 1, 1, 1, 1},
				{2, 4, 6, 8, 0},
				{9, 8, 7, 6, 5}
		};
    
		// Access the integer at the first row and fourth column of intMatrix and store it in a variable called retrievedInt
	  	int retrievedInt = intMatrix[0][3];
		System.out.println(retrievedInt);

		// Print 3 times the center value of intMatrix to the console. Make sure to access the correct element!
		System.out.println(intMatrix[1][2] * 3);

    }
}
```

<br>
<br>
<br>


<h3>Modifying Elements in a 2D Array</h3>

Now let’s review how to modify elements in a normal array.

For a one dimensional array, you provide the index of the element which you want to modify within a set of brackets next to the variable name and set it equal to an acceptable value:

```
storedArray[5] = 10;
```

For 2D arrays, the format is similar, but we will provide the outer array index in the first set of brackets and the subarray index in the second set of brackets. We can also think of it as providing the row in the first set of brackets and the column index in the second set of brackets if we were to visualize the 2D array as a rectangular matrix:

```
twoDArray[1][3] = 150;
```

To assign a new value to a certain element, make sure that the new value you are using is either of the same type or is castable to the type already in the 2D array.

Let’s say we wanted to replace four values from a new 2D array called intTwoD. Look at this example code to see how to pick individual elements and assign new values to them.

```
int[][] intTwoD = new int[4][3];

intTwoD[3][2] = 16;
intTwoD[0][0] = 4;
intTwoD[2][1] = 12;
intTwoD[1][1] = 8;
```

<img src="https://static-assets.codecademy.com/Paths/ap-computer-science/TwoDArrays/modifying.png">

```
The array now looks like {{4,0,0},{0,8,0},{0,12,0},{0,0,16}}
```


Qn 1. Replace the number 4 in intMatrix with the number 0.

2. Declare and initialize a new empty 2x2 int 2D array called subMatrix.

3. Using 4 lines of code, multiply each of the elements in the 2x2 top left corner of intMatrix by 5 and store the results in the subMatrix you created. Notice how we have to write a similar line of code 4 times. Afterwards, uncomment the provided print statement to see the result. In the next exercise, we’ll start looking into how to use loops to make this process quicker.


```
import java.util.Arrays;
public class Modifying {
	public static void main(String[] args) {
		// Using the provided 2D array
	  int[][] intMatrix = {
				{1, 1, 1, 1, 1},
				{2, 4, 6, 8, 0},
				{9, 8, 7, 6, 5}
		};   
    
		// Replace the number 4 in the 2D array with the number 0
    intMatrix[1][1] = 0;

		// Declare and initialize a new empty 2x2 integer 2D array called subMatrix
		int[][] subMatrix = new int[2][2];

		// Using 4 lines of code, multiply each of the elements in the 2x2 top left corner of intMatrix by 5 and store the results in the subMatrix you created. Afterwards, uncomment the provided print statement below.
		subMatrix[0][0] = intMatrix[0][0] * 5;
   		 subMatrix[0][1] = intMatrix[0][1] * 5;
  		  subMatrix[1][0] = intMatrix[1][0] * 5;
 		   subMatrix[1][1] = intMatrix[1][1] * 5; 
    
   System.out.println(Arrays.deepToString(subMatrix));
    }
}
```

<br>
<br>
<br>

<h3>Review of Nested Loops</h3>

We’re about to look at how we can use loops to make our lives easier when working with 2D arrays. But before we do that, let’s take a moment to refresh ourselves on how nested loops work.

Nested loops consist of two or more loops placed within each other. We will be looking at one loop nested within another for 2D traversal.

The way it works is that, for every iteration of the outer loop, the inner loop finishes all of its iterations.

Here is an example using for loops:
```
for(int outer = 0; outer < 3; outer++){
    System.out.println("The outer index is: " + outer);
    for(int inner = 0; inner < 4; inner++){
        System.out.println("\tThe inner index is: " + inner);
    }
}
```

The output of the above nested loops looks like so:
```
The outer index is: 0
    The inner index is: 0
    The inner index is: 1
    The inner index is: 2
    The inner index is: 3
The outer index is: 1
    The inner index is: 0
    The inner index is: 1
    The inner index is: 2
    The inner index is: 3
The outer index is: 2
    The inner index is: 0
    The inner index is: 1
    The inner index is: 2
    The inner index is: 3
```

From this example we can see how every time the outer loop iterates one time, the inner loop iterates fully.

This is an important concept for 2D array traversal, because for every row in a two dimensional matrix, we want to iterate through every column. We will look more at this in the next exercise.

Nested loops can consist of any type of loop and with any combination of loops. Let’s take a look at a few more interesting examples.

Here is an example of nested while loops:

```
int outerCounter = 0;
int innerCounter = 0; 
while(outerCounter<5){
    outerCounter++;
    innerCounter = 0;
    while(innerCounter<7){
        innerCounter++;
    }
}
```
We can even have some interesting combinations. Here is an enhanced for loop inside of a while loop:

```
int outerCounter = 0;
int[] innerArray = {1,2,3,4,5};

while(outerCounter<7){
    System.out.println();
    for(int number : innerArray){
        System.out.print(number * outerCounter + " ");
    }
    outerCounter++;
}
```

The output of the above example creates a multiplication table:

```
0 0 0 0 0 
1 2 3 4 5 
2 4 6 8 10 
3 6 9 12 15 
4 8 12 16 20 
5 10 15 20 25 
6 12 18 24 30 
```

<img src="https://global.discourse-cdn.com/codecademy/optimized/5X/6/c/d/9/6cd99ac9b7b618f781f3fa355e66a46968ded060_2_681x499.png">

This is an interesting example, because for every iteration of the while loop, we iterate through every element of an array using an enhanced for loop. This is similar to the iteration pattern we use for 2D array traversal. We will be going over that in the next exercise.

Let’s practice using nested loops!

You are in charge of controlling the amount of people who reserve seats for the world famous programming contest. You have two long arrays of integers which represent the contestant’s IDs for two days of the competition. The index of the array represents their seat number. You need to use nested for loops to find if a contestant tried to register for both days. Print out the ID of the contestants who tried to register twice as well as their seat numbers for both days.

Qn: Replace 1==2 with conditional logic to check if an element in the first array matches an element in the second array.

```
public class NestedLoops {
	public static void main(String[] args) {
		int[] seatsDayOne = {850007, 841141, 150017, 622393, 178505, 952093, 492450, 790218, 515994, 926666, 476090, 709827, 908660, 718422, 641067, 624652, 429205, 394328, 802772, 468793, 901979, 504963, 733939, 706557, 724430, 663772, 577480, 886333, 323197, 283056, 378922, 628641, 494605, 606387, 179993, 755472, 253608, 975198, 328457, 885712, 411958, 418586, 254970, 299345, 632115, 915208, 661570, 328375, 538422, 321303};
    
		int[] seatsDayTwo = {740912, 209431, 310346, 316462, 915797, 850440, 803140, 459194, 293277, 302424, 790507, 711980, 639916, 707446, 940339, 613076, 524157, 189604, 595934, 509691, 234133, 787575, 674602, 944308, 710345, 889699, 622393, 151931, 964325, 944568, 357684, 933857, 541190, 935076, 468848, 449446, 278951, 885503, 539124, 278723, 998622, 846182, 394328, 914002, 803795, 851135, 828760, 504936, 504322, 648644};
		
		int matchCounter = 0;
		// Fix the outer loop header to iterate through the first array of seats
		for(int i = 0; i < seatsDayOne.length; i++) {

			// Fix the inner loop header to iterate through the second array of seats
			for(int j = 0; j < seatsDayTwo.length; j++) {

				// Replace 1==2 with conditional logic to check if an element in the first array matches an element in the second array
				if(seatsDayOne[i] == seatsDayTwo[j]) {
					matchCounter++;
					System.out.println("Contestant: " + seatsDayOne[i] + ", Seat Day One: " + i + ", Seat Day Two: " + j);
					break;
				}
			}
		}
		System.out.println("The total number of contestants reserving seats on both days was: " + matchCounter);
	}
}

```

<br>
<br>
<br>



<h3>Traversing 2D Arrays: Introduction</h3>

In the last exercise, we reviewed how to use nested loops as well as how to iterate through regular arrays using loops. In this exercise, we will apply that knowledge in order to learn how to traverse 2D arrays.

Traversing 2D arrays using loops is important because it allows us to access many elements quickly, access elements in very large 2D arrays, and even access elements in 2D arrays of unknown sizes.

Let’s remember the structure of 2D arrays in Java:

```
char[][] letterBlock = {{'a','b','c'},{'d','e','f'},{'g','h','i'},{'j', 'k', 'l'}};
```

In Java, 2D arrays are like normal arrays, but each element is another array. This is shown by the initialized 2D array above. The outer array consists of four elements, where each element consists of a three element subarray.

Let’s see what happens when we access elements of the outer array

```
System.out.println(Arrays.toString(letterBlock[0]) + "\n");
System.out.println(Arrays.toString(letterBlock[1]) + "\n");
System.out.println(Arrays.toString(letterBlock[2]) + "\n");
System.out.println(Arrays.toString(letterBlock[3]) + "\n");
```

Here is the output of the above code:

```
[a, b, c]

[d, e, f]

[g, h, i]

[j, k, l]
```

As you can see, we can retrieve the entire subarray from each of the outer array elements. If you look at how we are accessing these subarrays, we are just increasing the index. This means we can access each sub-array in the 2D array using a loop!

Let’s take a look at an example which produces the same output, but can handle any sized 2D array.

```
for(int index = 0; index < letterBlock.length; index++){
    System.out.println(Arrays.toString(letterBlock[index]) + "\n");
}
```

Here is the result:

```
[a, b, c]

[d, e, f]

[g, h, i]

[j, k, l]
```

Now let’s remember how to access a value from the subarray. Previously, we learned that we can use the double brackets [][], where the first set of brackets contains the index of the element of the outer array and the second set of brackets contains the index of the element in the subarray. If we wanted to retrieve the letter 'f' we would use:

```
char storedLetter = letterBlock[1][2];
```

Since we know we can use a loop to retrieve each of the subarrays stored in the outer array, we can then use a nested loop to access each of the elements from the sub-array.

You might be wondering how we can figure out the number of iterations needed in order to fully traverse the 2D array.

In order to find the number of elements in the outer array, we just need to get the length of the 2D array.

<a href ="https://github.com/agentjimlam/Learn-Java/blob/main/README.md#length">Link to Length property</a><br>
<strong>** length is a property of arrays that returns the number of elements in that array. it does not return you the actual subarray element content at row 0 aka letterBlock[0]. </strong>


```
int lengthOfOuterArray = letterBlock.length;
```

When thinking about the 2D array in matrix form, this is the height of the matrix (the number of rows)
In order to find the number of elements in the subarray, we can get the length of the subarray after it has been retrieved from the outer array.

Remember that we retrieved the sub array earlier using this format:
```
char[] subArray = letterBlock[0];
```
Therefore, we can use this to get the length of the first subarray in the 2D array

```
int lengthOfSubArray = letterBlock[0].length;
```

When thinking about the 2D array in matrix form, this is the width of the matrix (the number of columns)
In most cases, getting the length of the first subarray in the 2D array will apply to the rest of the subarrays (if it is rectangular in shape), but there are rare occasions where the length of the subarrays could be different. This occurs if the 2D array is a jagged array. We won’t be working with any jagged 2D arrays in this lesson, but it’s something to keep in mind.

Let’s look at an example!
```
for(int a = 0; a < letterBlock.length; a++) {
    for(int b = 0; b < letterBlock[a].length; b++) {
        System.out.print("Accessed: " + letterBlock[a][b] + "\t");
    }
    System.out.println();
}
```


You can think of the variable a as being the outer loop index, and the variable b as being the inner loop index.

Here is the output:
```
Accessed: a Accessed: b Accessed: c 
Accessed: d Accessed: e Accessed: f 
Accessed: g Accessed: h Accessed: i 
```

Within the nested for loop, we can see that each of the subarray elements are being accessed by using the outer loop index for the outer array, and the inner loop index for the subarray.

Here is a diagram to help visualize how the 2D array is traversed using nested loops:

<img src="https://static-assets.codecademy.com/Paths/ap-computer-science/TwoDArrays/traversal.png">

We don’t have to only use regular for loops for traversing 2D arrays. We can use enhanced for loops if we do not need to keep track of the indices. Since enhanced for loops only use the element of the arrays, it is a bit more cumbersome to keep track of which index we are at. This same idea applies to while and do-while loops as well. This is why we usually use regular for loops except for when we want to do something simple like printing.

We have gone over how to think about 2D array traversal in terms of arrays of arrays, but there are two main ways of thinking about traversal in terms of rows and columns. These are called row-major order and column-major order.


Qn 1. Store the number of subarrays of intMatrix into an int variable called numSubArrays. If you want to confirm your work, print that number after creating it. You should expect to see the number of rows in the 2D array. <br>

Qn 2. Store the length of the subarrays using the first subarray in intMatrix. Store it in a variable called subArrayLength. This should be an int. <br>

Qn 3. Store the number of columns in intMatrix into a variable called columns and the number of rows in intMatrix into a variable called rows. <br>

Qn 4. Replace the outer and inner for loop headers to iterate through the entire 2D array. Use the iterators i for the outer loop and j for the inner loop. Also, add a line of code which calculates the sum of all of the elements in the 2D array. <br>

```
public class Introduction {
	public static void main(String[] args) {
		//Given the provided 2d array
		int[][] intMatrix = {
				{ 4,  6,  8, 10, 12, 14, 16},
				{18, 20, 22, 24, 26, 28, 30},
				{32, 34, 36, 38, 40, 42, 44},
				{46, 48, 50, 52, 54, 56, 58},
				{60, 62, 64, 66, 68, 70, 79}
		};
		// Store the number of subarrays of intMatrix into a variable called 'numSubArrays'
		int numSubArrays = intMatrix.length;
		System.out.println("Number of rows = " + numSubArrays);
		// Store the length of the subarrays using the first subarray in intMatrix. Store it in a variable called subArrayLength.
		int subArrayLength = intMatrix[0].length;
		System.out.println("Number of columns = " + subArrayLength);

		// Store the number of columns in intMatrix into a variable called 'columns'
		int columns = subArrayLength;

		// Store the number of rows in intMatrix into a variable called 'rows'
		int rows = numSubArrays;

		// Replace the outer and inner for loop headers to iterate through the entire 2D array. Use the iterators `i` for the outer loop and `j` for the inner loop.
		int sum = 0;
		for(int i= 0; i < rows; i++) {
			for(int j = 0; j < columns; j++) {
				// Insert a line of code to increase the variable `sum` by each accessed element
				System.out.println("Accessed: " + intMatrix[i][j] + "\t");
        sum = sum + intMatrix[i][j];
			}
		}
		System.out.println(sum);
	}
}

```


<br>
<br>
<br>
<br>



<h3>Traversing 2D Arrays: Practice with Loops</h3>

We have seen how to traverse 2D arrays using standard ```for loops```, but in this exercise, we will practice traversing them using some other loop types. For example, you may want to only retrieve elements without keeping track of the indices using enhanced for loops, or you could continuously update the 2D array until a condition is met using ```while``` loops.

In enhanced for loops, each element is iterated through until the end of the array. When we think about the structure of 2D arrays in Java (arrays of array objects) then we know that the outer enhanced for loop elements are going to be arrays.

Let’s take a look at an example:

Given this 2D array of character data:

```
char[][] charData = {{'a', 'b', 'c', 'd', 'e', 'f'},{'g', 'h', 'i', 'j', 'k', 'l'}};
```

Print out every character using enhanced for loops:
```
for(char[] charRow : charData) {
    for(char c : charRow) {
        System.out.print(c + " ");
    }
    System.out.println();
}
```

Remember that the syntax for enhanced for loops looks like so: ```for( datatype elementName : arrayName){```. Since 2D arrays in Java are arrays of arrays, each element in the outer enhanced for loop is an entire row of the 2D array. The nested enhanced for loop is then used to iterate through each element in the extracted row. Here is the output of the above code:
```
a b c d e f 
g h i j k l
```

Here is an example which accomplishes the same thing, but using while loops:
```
int i = 0, j=0;
while(i<charData.length) {
    j = 0;
    while(j<charData[i].length) {
        System.out.print(charData[i][j] + " ");
        j++;
    }
    System.out.println();
    i++;
}
```

Here is the output of the above code:
```
a b c d e f 
g h i j k l
```

Notice how we can use different loop types for traversal, but still receive the same result.

Let’s work some example problems using different loop types!


Qn 1. Use nested enhanced for loops to calculate the total number of characters in the ```wordData``` 2D array and print the result to the console. (Get the string .length() of each element)<br>

Qn 2. Using nested while loops, iterate through all of the elements in the 2D array and print them to the console using the format: word [row][column]. The print statement has been provided (you will need to modify it if you use iterators other than i and j). <br>

```
public class LoopPractice {
	public static void main(String[] args) {
		String[][] wordData = {{"study", "consider", "examine", "learn"}, {"ponder", "read", "think", "cogitate"}};
		
		//Use nested enhanced for loops to calculate the total number of characters in the wordData 2D array and print the result to the console. (Get the string .length() of each element)
		int characterCount = 0;
    for (String[] wordRow : wordData){
        for (String word : wordRow){
          characterCount = characterCount + word.length();
        }
    }

		System.out.println(characterCount);
		
		//Using nested while loops, iterate through all of the elements in the 2D array and print them to the console using the format: word [row][column]. The formatted print statement has been provided.
		int i = 0, j = 0;
    while (i < wordData.length){
      j=0;
      while (j < wordData[i].length){
        System.out.println(wordData[i][j] + ": [" + i + "]" + "[" + j + "]");
        j++;
      }
      i++;
    }

	//System.out.println(wordData[i][j] + ": [" + i + "]" + "[" + j + "]");

	}
	
}
```


<br>
<br>
<br>



<h3>Traversing 2D Arrays: Row-Major Order</h3>

Row-major order for 2D arrays refers to a traversal path which moves horizontally through each row starting at the first row and ending with the last.

Although we have already looked at how 2D array objects are stored in Java, this ordering system conceptualizes the 2D array into a rectangular matrix and starts the traversal at the top left element and ends at the bottom right element.

Here is a diagram which shows the path through the 2D array:

<img src="https://static-assets.codecademy.com/Paths/ap-computer-science/TwoDArrays/row_major.png">


This path is created by the way we set up our nested loops. In the previous exercise, we looked at how we can traverse the 2D array by having nested loops in a variety of formats, but if we want to control the indices, we typically use standard for loops.

Let’s take a closer look at the structure of the nested for loops when traversing a 2D array:

Given this 2D array of strings describing the element positions:
```
String[][] matrix = {{"[0][0]", "[0][1]", "[0][2]"}, 
                     {"[1][0]", "[1][1]", "[1][2]"},
                     {"[2][0]", "[2][1]", "[2][2]"},
                     {"[3][0]", "[3][1]", "[3][2]"}};
```


Lets keep track of the total number of iterations as we traverse the 2D array:

```
int stepCount = 0;
        
for(int a = 0; a < matrix.length; a++) {
    for(int b = 0; b < matrix[a].length; b++) {
        System.out.print("Step: " + stepCount);
        System.out.print(", Element: " + matrix[a][b]);
        System.out.println();
        stepCount++;
    }
}
```

Here is the output of the above code:
```
Step: 0, Element: [0][0]
Step: 1, Element: [0][1]
Step: 2, Element: [0][2]
Step: 3, Element: [1][0]
Step: 4, Element: [1][1]
Step: 5, Element: [1][2]
Step: 6, Element: [2][0]
Step: 7, Element: [2][1]
Step: 8, Element: [2][2]
Step: 9, Element: [3][0]
Step: 10, Element: [3][1]
Step: 11, Element: [3][2]
```


The step value increases with every iteration within the inner for loop. Because of this, we can see the order in which each element is accessed. If we follow the step value in the output shows us that the elements are accessed in the same order as the row-major diagram above. Now why is that?

This is because in our for loop, we are using the number of rows as the termination condition within the outer for loop header ```a < matrix.length;``` Additionally, we are using the number of columns ```b < matrix[a].length``` as the termination condition for our inner loop. Logically we are saying: “For every row in our matrix, iterate through every single column before moving to the next row”. This is why our above example is traversing the 2D array using row-major order.

Here is a diagram showing which loop accesses which part of the 2D array for row-major order:

Starting at the first row, looping through each column in that row. When the end of the row is reached, we move on to the next row

<img src ="https://static-assets.codecademy.com/Paths/ap-computer-science/TwoDArrays/row_major_loop.png">

Why Use Row-Major Order?

Row-major order is important when we need to process data in our 2D array by row. You can be provided data in a variety of formats and you may need to perform calculations of rows of data at a time instead of individual elements. Let’s take one of our previous checkpoint exercises as an example. You were asked to calculate the sum of the entire 2D array of integers by traversing and accessing each element. Now, if we wanted to calculate the sum of each row, or take the average of each row, we can use row-major order to access the data in the order that we need. Let’s look at an example!

Given a 6X3 2D array of doubles:
```
double[][] data = {{0.51,0.99,0.12},
                   {0.28,0.99,0.89},
                   {0.05,0.94,0.05},
                   {0.32,0.22,0.61},
                   {1.00,0.95,0.09},
                   {0.67,0.22,0.17}};
```

Calculate the sum of each row using row-major order:
```
double rowSum = 0.0;
for(int o = 0; o < data.length; o++) {
    rowSum = 0.0;
    for(int i = 0; i < data[o].length; i++) {
        rowSum += data[o][i];
    }
    System.out.println("Row: " + o +", Sum: " + rowSum);
}
```

The output of the above code is:
```
Row: 0, Sum: 1.62
Row: 1, Sum: 2.16
Row: 2, Sum: 1.04
Row: 3, Sum: 1.15
Row: 4, Sum: 2.04
Row: 5, Sum: 1.06
```

An interesting thing to note is that, due to the way 2D arrays are structured in Java, enhanced for loops are always in row-major order. This is because an enhanced for loop iterates through the elements of the outer array which causes the terminating condition to be the length of the 2D array which is the number of rows.


Qn 1. You are provided with some runner lap data. Take a look at the loops we’re using to iterate through this 2D array. Replace the incorrect for loop headers to perform row-major traversal. Use the iterators outer and inner for the outer and inner loops. <br>

Qn 2. Enter the missing line of code within the nested for loop to sum up the values for each row in the runner data. We’ve already created a variable named runnerTime that you can use to sum these values.<br>

Qn 3. We’ve given you a variable named averageVal that currently stores 0. Edit that line of code to find the average time of each runner.

```
public class RowMajor {
	public static void main(String[] args) {
		// Given runner lap data
		double[][] times = {{64.791, 75.972, 68.950, 79.039, 73.006, 74.157}, {67.768, 69.334, 70.450, 67.667, 75.686, 76.298}, {72.653, 77.649, 74.245, 62.121, 63.379, 79.354}};
		
		// Replace the incorrect for loop headers, use the iterators 'outer' and 'inner' for the outer and inner loops
		double runnerTime = 0.0;
		for(int outer = 0; outer < times.length; outer++) { //time.length here summons number of elements, which are subarrays/rows bc it's 2D array
			runnerTime = 0.0;
			for(int inner = 0; inner < times[outer].length; inner++) {
        System.out.println("Runner index: " + outer + ", Time index: " + inner);
				// Enter the missing line of code to sum up the values in each row. Use the variable runnerTime
				runnerTime = runnerTime + times[outer][inner];
        
			}
			// Enter the missing line of code to find the average time of each runner. Use the variable averageVal
      double averageVal = runnerTime / times[outer].length;

			System.out.println("Sum of runner " + outer + " times: " + runnerTime);
			System.out.println("Average of runner " + outer + ": " + averageVal);
		}
	}
}

```

<br>
<br>
<br>



<h3>2D ARRAYS: JAVA</h3>
Traversing 2D Arrays: Column-Major Order

Column-major order for 2D arrays refers to a traversal path which moves vertically down each column starting at the first column and ending with the last.

This ordering system also conceptualizes the 2D array into a rectangular matrix and starts the traversal at the top left element and ends at the bottom right element. Column-major order has the same starting and finishing point as row-major order, but it’s traversal is completely different

Here is a diagram which shows the path through the 2D array:

<img src= "https://static-assets.codecademy.com/Paths/ap-computer-science/TwoDArrays/column_major.png">

In order to perform column-major traversal, we need to set up our nested loops in a different way. We need to change the outer loop from depending on the number of rows, to depending on the number of columns. Likewise we need the inner loop to depend on the number of rows in its termination condition.

Let’s look at our example 2D array from the last exercise and see what needs to be changed.

Given this 2D array of strings describing the element positions:
```
String[][] matrix = {{"[0][0]", "[0][1]", "[0][2]"}, 
                     {"[1][0]", "[1][1]", "[1][2]"},
                     {"[2][0]", "[2][1]", "[2][2]"},
                     {"[3][0]", "[3][1]", "[3][2]"}};
```

Let’s keep track of the total number of iterations as we traverse the 2D array. We also need to change the termination condition (middle section) within the outer and inner for loop.

```
int stepCount = 0;
                
for(int a = 0; a < matrix[0].length; a++) {
    for(int b = 0; b < matrix.length; b++) {
        System.out.print("Step: " + stepCount);
        System.out.print(", Element: " + matrix[b][a]);
        System.out.println();
        stepCount++;
    }
}   
```

Here is the output of the above code:
```
Step: 0, Element: [0][0]
Step: 1, Element: [1][0]
Step: 2, Element: [2][0]
Step: 3, Element: [3][0]
Step: 4, Element: [0][1]
Step: 5, Element: [1][1]
Step: 6, Element: [2][1]
Step: 7, Element: [3][1]
Step: 8, Element: [0][2]
Step: 9, Element: [1][2]
Step: 10, Element: [2][2]
Step: 11, Element: [3][2]
```

As you can see in the code above, the way we accessed the elements from our 2D array of strings called matrix is different from the way we accessed them when using row-major order. Let’s remember that the way we get the number of columns is by using ```matrix[0].length``` and the way we get the number of rows is by using ```matrix.length```. Because of these changes to our for loops, our iterator a now iterates through every column while our iterator b iterates through every row. Since our iterators now represent the opposite values, whenever we access an element from our 2D array, we need to keep in mind what indices we are passing to our accessor. Remember the format we use for accessing the elements ```matrix[row][column]```? Since a now iterates through our column indices, we place it in the right set of brackets, and the b is now placed in the left set of brackets.

Here is a diagram showing which loop accesses which part of the 2D array for column-major order:

The outer loop controls the column while the inner loop controls the row in that column.

Why Use Column-Major Order?

Column major order is important because there are a lot of cases when you need to process data vertically. Let’s say that we have a chart of information which includes temperature data about each day. The top of each column is labeled with a day, and each row represents an hour. In order to find the average temperature per day, we would need to traverse the data vertically since each column represents a day. As mentioned in the last exercise, data can be provided in many different formats and shapes and you will need to know how to traverse it accordingly.

Let’s look at our sum example from the last exercise, but now using column-major order.

Given a 6X3 2D array of doubles:

double[][] data = {{0.51,0.99,0.12},
                   {0.28,0.99,0.89},
                   {0.05,0.94,0.05},
                   {0.32,0.22,0.61},
                   {1.00,0.95,0.09},
                   {0.67,0.22,0.17}};

Calculate the sum of each column using column-major order:
```
double colSum = 0.0;
for(int o = 0; o < data[0].length; o++) {
    colSum = 0.0;
    for(int i = 0; i < data.length; i++) {
        colSum += data[i][o];
    }
    System.out.println("Column: " + o +", Sum: " + colSum);
}
```

The output of the above code is:
```
Column: 0, Sum: 2.83
Column: 1, Sum: 4.31
Column: 2, Sum: 1.93
```

Let’s try an example!

We will be using the same runner data from the last exercise, but this time we are going to take the average times per lap rather than per runner. This requires that we use column-major traversal.


<li>Qn 1. You are provided with some runner lap data. Take a look at the loops we’re using to iterate through this 2D array. Replace the incorrect ```for``` loop headers to perform column-major traversal. Use the iterators outer and inner for the outer and inner loops.</li>

<li>Enter the missing line of code within the nested ```for``` loop to sum up the values for each column in the runner data. We’ve already created a variable named ```lapTime``` that you can use to sum these values.</li>
<li>We’ve given you a variable named ```averageVal``` that currently stores 0. Edit that line of code to find the average time of each lap.</li>


<h4>Why use times[0].length and not times[outer].length in the outer for loop?</h4>
<ul>
	<li><strong>Avoiding Index Out of Bounds:</strong> If we were to use times[outer].length instead of times[0].length for the outer loop condition, we would risk encountering an ArrayIndexOutOfBoundsException if any row in the array has fewer columns than the first row (times[0]). Using times[0].length ensures that we iterate only up to the number of columns in the first row, preventing such errors. Therefore, times[0].length is used in the outer loop to safely iterate over the columns of the two-dimensional array data.</li>
	<li><strong>Using times[0].length:</strong> By using times[0].length, we are assuming that all rows in the data array have the same number of columns as the first row (times[0]). This is a common assumption when dealing with rectangular two-dimensional arrays, where all rows have the same length.</li>
</ul>



```
public class ColumnMajor {
	public static void main(String[] args) {
    // Given runner lap data
		double[][] times = {{64.791, 75.972, 68.950, 79.039, 73.006, 74.157}, {67.768, 69.334, 70.450, 67.667, 75.686, 76.298}, {72.653, 77.649, 74.245, 62.121, 63.379, 79.354}};
		
		// Replace the incorrect for loop headers, use the iterators 'outer' and 'inner' for the outer and inner loops
		double lapTime = 0.0;
		for(int outer = 0; outer < times[0].length; outer++){
			lapTime = 0.0;
			for(int inner = 0; inner < times.length; inner++){
				System.out.println("Lap index: " + outer + ", Time index: " + inner);
				// Enter the missing line of code to sum up the values in each column. Use the variable lapTime
      				lapTime = lapTime + times [inner][outer];

			}
			// Enter the missing line of code to find the average time of each lap. Use the variable averageVal
			double averageVal = lapTime / times.length;

			System.out.println("Sum of lap " + outer + " times: " + lapTime);
			System.out.println("Average time for lap " + outer + ": " + averageVal);


      
		}
	}
}
```

<br>
<br>
<br>
<br>



<h3>Combining Traversal and Conditional Logic</h3>

When working with 2D arrays, it is important to be able to combine traversal logic with conditional logic in order to effectively navigate and process the data. Here are a few ways in how conditional logic can affect 2D array traversal:
<ul>
	<li>Skipping or selecting certain rows and columns</li>
	<li>Modifying elements only if they meet certain conditions</li>
	<li>Complex calculations using the 2D array data</li>
	<li>Formatting the 2D array</li>
	<li>Avoiding exceptions / smart processing</li>
</ul>

Let’s go over a few examples which use these ideas:

First, let’s think about a situation where you have some string data inside a 2D array. We have an application which allows users to input events on a calendar. This is represented by a 5x7 2D array of strings. Due to the fact that the number of days in each month is slightly different and that there are less than 35 days in a month, we know that some of our elements are going to be empty. We want our application to do a few things:

<li>Detect which days of which weeks have something planned and alert us about the event.</li>
<li>Count the number of events for each week</li>
<li>Count the number of events for each day</li>

<img src="https://static-assets.codecademy.com/Paths/ap-computer-science/TwoDArrays/calendar.png">

<br>

Here’s what our calendar data looks like in our application
```
String[][] calendar = {{"volunteer", "delivery", null, null, "doctor", null, "soccer"}, {null, "exam 1", null, "mechanic", null, null, "soccer"}, {"volunteer", "off work", null, "birthday", null, "concert", null}, {null, "exam 2", null, null, "doctor", null, "soccer"}, {"visit family", null, null, null, null, null, null}};
```

Let’s look at some code which accomplishes the requirements above. Carefully look through each line of code and read all of the comments.

There are a few things to note:

<li>Row-major or column-major order can be used to access the individual events</li>
<li>Row-major order must be used to count the number of events per week since each row represents a week</li>


Let’s take care of the first 2 requirements in one set of nested row-major loops
```
for(int i = 0; i < calendar.length; i++) {
    numberOfEventsPerWeek = 0;
    for(int j = 0; j < calendar[i].length; j++) {
        // We need conditional logic to ensure that we do not count the empty days
        String event = calendar[i][j];
        if(event!=null && !event.equals("")) {
            // If the day does not have a null value and an empty string for an event, then we print it and count it
            System.out.println("Week: " + (i+1) + ", Day: " + (j+1) + ", Event: " + event);
            numberOfEventsPerWeek++;
        }
    }
    System.out.println("Total number of events for week "+ (i+1) +": " + numberOfEventsPerWeek + "\n");
}
```

The above code produces this output:
```
Week: 1, Day: 1, Event: volunteer
Week: 1, Day: 2, Event: delivery
Week: 1, Day: 5, Event: doctor
Week: 1, Day: 7, Event: soccer
Total number of events for week 1: 4

Week: 2, Day: 2, Event: exam 1
Week: 2, Day: 4, Event: mechanic
Week: 2, Day: 7, Event: soccer
Total number of events for week 2: 3

Week: 3, Day: 1, Event: volunteer
Week: 3, Day: 2, Event: off work
Week: 3, Day: 4, Event: birthday
Week: 3, Day: 6, Event: concert
Total number of events for week 3: 4

Week: 4, Day: 2, Event: exam 2
Week: 4, Day: 5, Event: doctor
Week: 4, Day: 7, Event: soccer
Total number of events for week 4: 3

Week: 5, Day: 1, Event: visit family
Total number of events for week 5: 1
```

Now let’s complete the third requirement. Since we need to count all of the events for each of the weekdays, we will need to traverse the calendar vertically.
```
int numberOfEventsPerWeekday = 0;
// We will use this array of day strings for our output later on so we don't have (day: 1)
String[] days = {"Sundays", "Mondays", "Tuesdays", "Wednesdays", "Thursdays", "Fridays", "Saturdays"};
for(int i = 0; i < calendar[0].length; i++) {
    numberOfEventsPerWeekday = 0;
    for(int j = 0; j < calendar.length; j++) {
        // Don't forget to flip the iterators in the accessor since we are flipping the direction we are navigating.
        // Remember, i now controls columns and j now controls rows
        String event = calendar[j][i];
        if(event!=null && !event.equals("")) {
            // Make sure we have an event for the day before counting it
            numberOfEventsPerWeekday++;
        }
    }
    // Use the days string array from earlier to convert the day index to a real weekday string
    System.out.println("Number of events on " + days[i] + ": " + numberOfEventsPerWeekday);
}
```

The output is:
```
Number of events on Sundays: 3
Number of events on Mondays: 4
Number of events on Tuesdays: 0
Number of events on Wednesdays: 2
Number of events on Thursdays: 2
Number of events on Fridays: 1
Number of events on Saturdays: 3
```


This example uses many of the concepts we have learned before. We use row-major order, column-major order, as well as including conditional logic to ensure that we have data for the elements we are accessing.

Additionally, we can use conditional logic to skip portions of the 2D array. For example, let’s say we wanted to print the events for weekdays only and skip the weekends.

We could use a conditional statement such as ```if(j!=0 && j!=6)``` in order to skip Sunday (0) and Saturday (6).

These modifications to our 2D array traversal are very common when processing data in applications. We need to know which cells to look at (skipping column titles for example), which cells to ignore (empty data, invalid data, outliers, etc.), and which cells to convert (converting string input from a file to numbers).

Let’s try an example!

We are making a simple grayscale image editor program and we want to apply some modifications to the image. We have a 4x8 pixel image that is stored as a 2D array of integers. The integer value represents the brightness of the pixel, where the acceptable values are between 0 and 255, inclusive.


Qn 1. First, we want to crop the image down to a 4x6 image, removing the right 2 columns. Declare and initialize a new 2D array of integers with 4 rows and 6 columns called ```newImage```.
<br>
Qn 2.Now that you have your empty image, use nested for loops to copy over the data from the original image (stored in imageData) to the new image, make sure not to include the cropped out columns (right 2 columns).
<br>
Qn 3. You want to decrease the brightness of the new image by 50 units. The way this works is that for every integer in the new 2D array, we will subtract the value by 50. Remember that the value range for the pixel is 0-255, so if the result tries to go below 0, just set it equal to 0.
<br>

```
import java.util.Arrays;
public class Combining {
	public static void main(String[] args) {
		int[][] imageData={{100,90,255,80,70,255,60,50}, //8 col
							         {255,10,5,255,10,5,255,255}, // 8 col
							         {255,255,255,0,255,255,255,75}, //8 col
							         {255,60,30,0,30,60,255,255}}; //8 col
		
		//First, we want to crop the image down to a 4x6 image, removing the right 2 columns. Declare and initialize a new 2D array of integers with 4 rows and 6 columns called `newImage`.
		int[][] newImage = new int[4][6];
		
    
		//Now that you have your empty image, use nested **for** loops to copy over the data from the original image to the new image, make sure not to include the cropped out columns.
 for(int i = 0; i < newImage.length; i++){

      for(int j = 0; j < newImage[0].length; j++){
          newImage[i][j] = imageData [i][j];
          System.out.println("Pixel value at " + "[" + i + "]" + "[" + j + "]" + " = " + newImage[i][j]);
          newImage[i][j] = newImage[i][j] - 50;
          if (newImage[i][j] < 0){
            newImage[i][j] = 0;
          }
          System.out.println("Pixel value after decrease value by 50: " + newImage[i][j]);
      }


   }

		System.out.println(Arrays.deepToString(newImage));
	
		//You want to decrease the brightness of the new image by 50 units. The way this works is that for every integer in the new 2D array, we will subtract the value by 50. Remember that the value range for the pixel is 0-255, so if the result tries to go below 0, just set it equal to 0.
		
		
		System.out.println(Arrays.deepToString(newImage));
	}
}
```



<br>
<br>
<br>



<h3>2D Array Review</h3>

Let’s review the concepts we have learned throughout this lesson.

Arrays are objects in Java, we can have arrays of objects, therefore we can also have arrays of arrays. This is the way 2D arrays are structured in Java.

We can declare and initialize 2D arrays in a few different ways depending on the situation:
```
// Declaring without initializing
int[][] intTwoD;

// Initializing an empty 2D array which has already been declared
intTwoD = new int[5][5];

// Declaring and initializing an empty 2D array at once
String[][] stringData = new String[3][6];

// Declaring and initializing a 2D array using initializer lists
double[][] doubleValues = {{1.5, 2.6, 3.7}, {7.5, 6.4, 5.3}, {9.8,  8.7, 7.6}, {3.6, 5.7, 7.8}};

// Initializing a 2D array using initializer lists after it has already been declared, or already contains data;
char[][] letters = new char[100][250];
letters = new char[][]{{'a', 'b', 'c'}, {'d', 'e', 'f'}};
```

We retrieve elements in a 2D array by providing a row and column index ```char c = letters[0][1];```
<ul>
	<li>We can also think of them as the index of the outer array and the index of the subarray</li>
	<li>We can modify elements the same way letters[1][2] = 'z';</li>
</ul>


We traverse 2D arrays using nested loops.

<li>We can use loops of any type, but we typically use nested for loops to keep track of the indices</li>
<li>Row-major order traverses through each row moving horizontally to the right through each row</li>
<li>Column-major order traverses through each column moving vertically down through each column</li>
<li>Row-major order and column-major order start and end on the same elements, but the paths are different.</li>
<li>In order to convert row-major to column-major, we need to make the outer loop terminating condition depend on the number of columns, make the inner loop terminating condition depend on the number of rows, and flip the variables in our accessor within the inner loop to ensure that we don’t try to access outside of the 2D array since we flipped the direction of traversal.</li>


Here are examples of row-major and column-major order:

```
// Row-major order
for(int o = 0; o < letters.length; o++) {
    for(int i = 0; i < letters[o].length; i++) {
        char c = letters[o][i];
    }
}

// Column-major order
for(int o = 0; o < letters[0].length; o++) {
    for(int i = 0; i < letters.length; i++) {
        char c = letters[i][o];
    }
}
```

Conditional logic in our 2D array traversal allows us to use the data in a meaningful way. We can control which rows and columns we look at, ensure that the data we are looking at is what we want, perform calculations on specific elements, avoid throwing exceptions, and more.

Here is an example of traversal with conditional logic.

Given this 2D array of Strings:

```
String[][] words = {{"championship", "QUANTITY", "month"},{"EMPLOYEE", "queen", "understanding"},{"method", "writer", "MOVIE"}};
```
We are going to flip the capitalization of the words:

```
System.out.println("Before...");
System.out.println(Arrays.deepToString(words).replace("],", "],\n") + "\n");

for(int i=0; i<words.length; i++) {
    for(int j = 0; j<words[i].length; j++) {
        if(words[i][j]!=null) {

            // Check the capitalization
            boolean allCaps = true;
            for(char c : words[i][j].toCharArray()) 
                if(!Character.isUpperCase(c)) 
                    allCaps = false;
                
            // Flip the capitalization
            if(allCaps)
                words[i][j] = words[i][j].toLowerCase();
            else
                words[i][j] = words[i][j].toUpperCase();
        }
    }
}

System.out.println("After...");
System.out.println(Arrays.deepToString(words).replace("],", "],\n") + "\n");
```


Here is the output of the above code:

```
Before...
[[championship, QUANTITY, month],
 [EMPLOYEE, queen, understanding],
 [method, writer, MOVIE]]

After...
[[CHAMPIONSHIP, quantity, MONTH],
 [employee, QUEEN, UNDERSTANDING],
 [METHOD, WRITER, movie]]
```

Time to work some review problems!

After learning about 2D arrays, you have decided to become a CS professor and you are now teaching your class about 2D arrays. You are making an application which will keep track of their exam grades and show you statistics about their performance. You will be using 2D arrays to keep track of their exam grades


Qn 1. First, declare and initialize a 4x3 2D array of doubles called scores which will contain the exam data for four students. The rows will represent the student and the columns will represent the exam number. You already know the first exam scores (80.4, 96.2, 100.0, 78.9). Use initializer lists to store the first exam scores in the first column and -1 for the remaining exams. Use the provided print statement to print the result in the console. <br>

Qn 2. The next set of exams have occurred. Using 4 lines of code, manually enter the scores (89.7, 90.5, 93.6, 88.1) for the second exam (column 1). Use the provided print statement to print the updated 2D array as well.
<br>

Qn 3. You have realized that you will only be keeping track of 2 exam grades instead of 3. Declare and initialize an empty 4x2 2D array of double values called ```newScores```. <br>

Qn 4. Using loops, copy all of the scores for exam 1 and 2 into the new 2D array. (Do not include the -1 values) <br>

Qn 5. You have allowed the students to complete an extra credit activity to contribute towards their scores. For all exam grades less than 90, add 2 additional points to the grade in newScores. <br>



```
import java.util.Arrays;
public class Review {
	public static void main(String[] args) {  

		//First, declare and initialize a 4x3 2D array of doubles called `scores` which will contain the exam data for four students. The rows will represent the student and the columns will represent the exam number. You already know the first exam scores (80.4, 96.2, 100.0, 78.9). Use initializer lists to store the first exam scores in the first column and -1 for the remaining exams. Use the provided print statement to print the result in the console.
  double[][] scores = {
            {80.4, -1, -1},
            {96.2, -1, -1},
            {100.0, -1, -1},
            {78.9, -1, -1}
        };

  System.out.println(Arrays.deepToString(scores));

	//The next set of exams have occurred. Using 4 lines of code, manually enter the scores (89.7, 90.5, 93.6, 88.1) for the second exam (column 1). Use the provided print statement to print the updated 2D array as well.
  scores[0][1] = 89.7;
  scores[1][1] = 90.5;
  scores[2][1] = 93.6;
  scores[3][1] = 88.1;

  System.out.println(Arrays.deepToString(scores));
		
  //You have realized that you will only be keeping track of 2 exam grades instead of 3. Declare and initialize an empty 4x2 2D array of double values  called newScores
  double[][] newScores = new double[4][2];
  System.out.println(newScores[0].length);
  System.out.println(newScores.length);


  //Using loops, copy all of the scores for exam 1 and 2 into the new 2D array. (do not include the -1 values)
  for (int i = 0; i < newScores[0].length; i++) {    // Column-major order
    for (int j = 0; j < newScores.length; j++) {
      newScores[j][i] = scores[j][i];
      System.out.println("Student: " + j + " Column/Exam " + i + ": " + newScores[j][i]);
    }
  }

/* for (int i = 0; i < scores.length; i++) {      // Row-major order
            for (int j = 0; j < 2; j++) {
                if (scores[i][j] != -1) {   
                    newScores[i][j] = scores[i][j];
                }
            }
        }
*/


  System.out.println(Arrays.deepToString(newScores));

  //You have allowed the students to complete an extra credit activity to contribute towards their scores. For all exam grades less than 90, add 2 additional points to the grade in `newScores`
   for (int i = 0; i < newScores[0].length; i++) {
    for (int j = 0; j < newScores.length; j++) {
      if(newScores[j][i] < 90){
        newScores[j][i] += 2;
      }
    }
   }
    

  System.out.println(Arrays.deepToString(newScores));
	}
}


```




</body>


















