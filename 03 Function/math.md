+++
title = "Math in Dart"
weight = 7
keywords = "dart math, math in dart, generate random number in dart, dart math with example"
description = "In this tutorial, you will learn about math in dart with examples. Math helps you to perform the mathematical task easily."
+++

## Math In Dart
Math helps you to perform mathematical calculations efficiently. With dart math, you can **generate random number**, **find square root**, **find power of number**, or **round specific numbers**. To use math in dart, you must `import 'dart:math';`.

## How To Generate Random Numbers In Dart
This example shows how to generate random numbers from **0 - 9** and also **1 to 10**. After watching this example, you can generate a random number between your choices.

```dart
import 'dart:math';
void main()
{
Random random = new Random();
int randomNumber = random.nextInt(10); // from 0 to 9 included
print("Generated Random Number Between 0 to 9: $randomNumber");
  
int randomNumber2 = random.nextInt(10)+1; // from 1 to 10 included  
print("Generated Random Number Between 1 to 10: $randomNumber2"); 
}
```

{{% expand "Show Output" "false" %}}
````plaintext
Generated Random Number Between 0 to 9: 8
Generated Random Number Between 1 to 10: 4
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=3f21a2bd9f0ddfff1f3052d7f797bf68" style="blue" %}}{{% /button %}}

- In this program, **random.nextInt(10)** function is used to generate a random number between  **0 and 9** in which the value is stored in a variable **randomNumber**. 

- The **random.nextInt(10)+1** function is used to generate random number between
**1 to 10** in which the value is stored in a variable **randomNumber2**.

## Generate Random Number Between Any Number
Use this formula to generate a random number between any numbers in the dart. 
```dart
 min + Random().nextInt((max + 1) - min);
```
## Example: Random Number In Dart Between 10 - 20.
This program generates random numbers between 10 to 20.
```dart
import 'dart:math';
void main()
{

int min = 10;
int max = 20; 

int randomnum = min + Random().nextInt((max + 1) - min);
  
print("Generated Random number between $min and $max is: $randomnum");  
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Generated Random number between 10 and 20 is 19
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=62cffa7daf9ee4948f1b7893705874a8" style="blue" %}}{{% /button %}}

## Random Boolean And Double Value
Here you will learn how to generate random boolean and double values in dart.

```dart
  Random().nextBool(); // return true or false
  Random().nextDouble(); // return 0.0 to 1.0
```

## Example 1: Generate Random Boolean And Double Values
This example below generate random and boolean value.
```dart
import 'dart:math';
void main()
{
double randomDouble = Random().nextDouble();
bool randomBool = Random().nextBool();
  
print("Generated Random double value is: $randomDouble");  
print("Generated Random bool value is: $randomBool");  
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Generated Random double value is: 0.6120530538023836
Generated Random bool value is: false
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=246a9a6edf29f379b795f1e84ca8b503" style="blue" %}}{{% /button %}}

## Example 2:  Generate a List Of Random Numbers In Dart
This example will generate a list of 10 random numbers between 1 to 100.
```dart
import 'dart:math';
void main()
{
List<int> randomList = List.generate(10, (_) => Random().nextInt(100)+1); 
print(randomList);  
}

```
{{% expand "Show Output" "false" %}}
````plaintext
[94, 68, 21, 66, 86, 82, 70, 46, 66, 69]
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=3e70116ed445d4f034bef9c1c1158ce8" style="blue" %}}{{% /button %}}

## Useful Math Function In Dart
You can use some useful math functions to perform your daily task with dart programming. 
|  Function Name |  Output  |  Description  |
| ----------- | --------- | ------------- |
|  pow(10,2)  |  100  |    10 to the power 2 is 10*10  |
|  max(10,2)  |  10  | Maximum number is 10  |
|  min(10,2)  |  2  | Minimum number is 2  |
|  sqrt(25)  |  5  | Square root of 25 is 5  |

## Example: Math In Dart
This example below finds the power of a number, a minimum and maximum value between two numbers, and the square root of a number.

```dart
import 'dart:math';
void main()
{
  int num1 = 10;
  int num2 = 2;

  num powernum = pow(num1,num2);
  num maxnum = max(num1,num2);
  num minnum = min(num1,num2);
  num squareroot = sqrt(25); // Square root of 25
  
  print("Power is $powernum"); 
  print("Maximum is $maxnum"); 
  print("Minimum is $minnum"); 
  print("Square root is $squareroot"); 
  
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Power is 100
Maximum is 10
Minimum is 2
Square root is 5.0
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=5ee1443f8b24df0914c9df0c2e362e25" style="blue" %}}{{% /button %}}

- In this program, **pow(num1, num2)** is a function where num1 is a digit and num2 is a power.
- **max(num1,num2)** is a function which give the maximum number between num1 and num2.
- **min(num1,num2)** is a function which give the mininum number between num1 and num2.
- **sqrt(25)** is a function that gives the square root of 25.
