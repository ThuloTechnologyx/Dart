+++
title = "Arrow Function in Dart"
weight = 5
keywords = "dart arrow function, dart functions, how to use arrow function in dart."
description = "In this tutorial, you will learn the arrow function in dart with examples and how to use the arrow function."
+++

## Arrow Function In Dart
Dart has a special syntax for the function body, which is only one line. The arrow function is represented by **=>** symbol. It is a shorthand syntax for any function that has only one expression.

## Syntax 
The syntax for the dart arrow function.

```dart
returnType functionName(parameters...) => expression;

```
{{% notice info %}}
**Note**: The arrow function is used to make your code short.**=> expr** syntax is a shorthand for **{ return expr; }**. 
{{% /notice %}}


## Example 1: Simple Interest Without Arrow Function
This program finds simple interest without using the arrow function.
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
Simple interest is 450.0
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=b56428cb81ead44765f9f7ca17109b78" style="blue" %}}{{% /button %}}


## Example 2: Simple Interest With Arrow Function
This program finds simple interest using the arrow function.
```dart
// arrow function that calculate interest
double calculateInterest(double principal, double rate, double time) =>
    principal * rate * time / 100;

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
Simple interest is 450.0
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=5a2af3ecadc0d798d9e04026d9cb0245" style="blue" %}}{{% /button %}}

## Example 3: Simple Calculation Using Arrow Function
This program finds the sum, difference, multiplication, and division of two numbers using the arrow function.
```dart
int add(int n1, int n2) => n1 + n2;
int sub(int n1, int n2) => n1 - n2;
int mul(int n1, int n2) => n1 * n2;
double div(int n1, int n2) => n1 / n2;

void main() {
  int num1 = 100;
  int num2 = 30;

  print("The sum is ${add(num1, num2)}");
  print("The diff is ${sub(num1, num2)}");
  print("The mul is ${mul(num1, num2)}");
  print("The div is ${div(num1, num2)}");
}
```
{{% expand "Show Output" "false" %}}
````plaintext
The sum is 130
The diff is 70
The mul is 3000
The div is 3.3333333333333335
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=7330e7ec5cce424afe8f89ad921c4469" style="blue" %}}{{% /button %}}

