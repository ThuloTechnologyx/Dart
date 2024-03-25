+++
title = "Types of Functions in Dart"
weight = 2
keywords = "function types in dart, dart function types, dart functions"
description = "In this tutorial you will learn about function types in dart with examples. You will also learn how to use different function types in dart."
+++

## Types Of Function
**Functions** are the block of code that performs a specific task. Here are different types of functions:

* No Parameter And No Return Type
* Parameter And No Return Type
* No Parameter And Return Type
* Parameter And Return Type

## Function With No Parameter And No Return Type
In this function, you do not pass any parameter and expect no return type. Here is an example of it: 

## Example 1: No Parameter & No Return Type
Here **printName()** is a function which prints name on screen.
```dart
void main() {
  printName();
}

void printName() {
  print("My name is John Doe.");
}
```
{{% expand "Show Output" "false" %}}
````plaintext
My name is John Doe.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=fe3164c766264100f44498144360a85f" style="blue" %}}{{% /button %}} 


In this program, **printName()** is the function which has keyword **void**. It means it has **no return type**, and the empty pair of parentheses implies that there is **no parameter** that is passed to the function.


## Example 2: No Parameter & No Return Type
Here **printPrimeMinisterName()** is a function which prints prime minister name on screen.

```dart
void main() {
  print("Function With No Parameter and No Return Type");
  printPrimeMinisterName();
}

void printPrimeMinisterName() {
  print("John Doe.");
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Function With No Parameter and No Return Type
John Doe.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=1813d19a18dcdc81433e886de2136340" style="blue" %}}{{% /button %}} 


## Function With Parameter And No Return Type
In this function, you do pass the parameter and expect no return type. Here is an example of it: 

## Example 1: Parameter & No Return Type
Here **printName(String name)** is a function which welcome person.
```dart
void main() {
  printName("John");
}

void printName(String name) {
  print("Welcome, ${name}.");
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Welcome, John.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=8c0cbea0f66b4e514022c724653c7224" style="blue" %}}{{% /button %}} 


In this program, **printName(String name)** is the function which has keyword **void**. It means it has **no return type**, and the pair of parentheses is not empty but this time that suggests it to accept an **parameter**.


## Example 2: Parameter & No Return Type
Here **add(int a, int b)** is a function that finds and prints the sum of two numbers.

```dart
// This function add two numbers
void add(int a, int b) {
  int sum = a + b;
  print("The sum is $sum");
}

void main() {
  int num1 = 10;
  int num2 = 20;

  add(num1, num2);
}
```
{{% expand "Show Output" "false" %}}
````plaintext
The sum is 30
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=dff98899bce207d6832db67d2ef9b399" style="blue" %}}{{% /button %}} 


## Function With No Parameter And Return Type
In this function, you do not pass any parameter but expect return type. Here is an example of it: 

## Example 1: No Parameter & Return Type
Here **primeMinisterName()** is a function which returns prime minister name. In the entire program, anyone can use this function to find the name of the prime minister.

```dart
void main() {
// Function With No Parameter & Return Type
  String name = primeMinisterName();
  print("The Name from function is $name.");
}
String primeMinisterName() {
  return "John Doe";
}

```
{{% expand "Show Output" "false" %}}
````plaintext
The name from function is John Doe
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=604a0408721263ff39754ddde84597a2" style="blue" %}}{{% /button %}} 


In this program, **primeMinisterName()** is the function which has **String** keyword before function name, means it **return** String value, and the empty pair of parentheses suggests that there is **no parameter** that is passed to the function. 

## Example 2: No Parameter & Return Type
Here **voterAge()** is a function which returns minimum voter age.

```dart
// Function With No Parameter & Return Type
void main() {
  int personAge = 17;

  if (personAge >= voterAge()) {
    print("You can vote.");
  } else {
    print("Sorry, you can't vote.");
  }
}

int voterAge() {
  return 18;
}

```
{{% expand "Show Output" "false" %}}
````plaintext
Sorry, you can't vote.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=506e558c6657088310310682269a4723" style="blue" %}}{{% /button %}} 


## Function With Parameter And Return Type
In this function, you do pass the parameter and also expect return type. Here is an example of it: 

## Example 1: Parameter & Return Type
Here **add(int a, int b)** is a function that returns its sum in integer. We can display results in our main function.

```dart
// this function add two numbers
int add(int a, int b) {
  int sum = a + b;
  return sum;
}

void main() {
  int num1 = 10;
  int num2 = 20;

  int total = add(num1, num2);
  print("The sum is $total.");
}

```
{{% expand "Show Output" "false" %}}
````plaintext
The sum is 30.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=8c5d49c666430f9953aefc34f3556b99" style="blue" %}}{{% /button %}} 


In this program, **int add(int a, int b)** is the function with **int** as the return type, and the pair of parenthesis has two **parameters**, i.e., a and b.


## Example 2: Parameter & Return Type
Here **calculateInterest(double principal, double rate, double time)** is a function that returns its simple interest in double. We can display results in our main function.

```dart
// function that calculate interest
double calculateInterest(double principal, double rate, double time) {
  double interest = principal * rate * time / 100;
  return interest;
}

void main() {
  double principal = 5000;
  double time = 3;
  double rate = 3;
  double result = calculateInterest(principal, rate, time);
  print("The simple interest is $result.");
}
```
{{% expand "Show Output" "false" %}}
````plaintext
The simple interest is 450.0.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=1c8b74b94e0de80ec42aaf06e8a02ab1" style="blue" %}}{{% /button %}} 


{{% notice info %}}
Note: void is used for no return type as it is a non value-returning function.
{{% /notice %}}

##  Complete Example 
Here is the program, which includes all types of functions we studied earlier.

```dart
// parameter and return type
int add(int a, int b) {
  var total;
  total = a + b;
  return total;
}

// parameter and no return type
void mul(int a, int b) {
  var total;
  total = a * b;
  print("Multiplication is : $total");
}

// no parameter and return type
String greet() {
  String greet = "Welcome";
  return greet;
}

// no parameter and no return type
void greetings() {
  print("Hello World!!!");
}

void main() {
  var total = add(2, 3);
  print("Total sum: $total");
  mul(2, 3);
  var greeting = greet();
  print("Greeting: $greeting");
  greetings();
}

 ```
 {{% expand "Show Output" "false" %}}
````plaintext
Total sum: 5
Multiplication is : 6
Greeting: Welcome
Hello World!!!
````
{{% /expand %}}

{{% button href="https://dartpad.dev/?id=f7fe41debf32283aac6a831326aa2e9e" style="blue" %}}{{% /button %}}  

