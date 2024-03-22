+++
title = "Ternary Operator in Dart"
weight = 4
description = "Learn what is ternary operator and how to use ternary operator in dart."
keywords = "ternary operator, dart ternary operator"
+++

### Ternary Operator
The ternary operator is like if-else statement. This is a one-liner replacement for the if-else statement. It is used to write a conditional expression, where based on the result of a boolean condition, one of the two values is selected.

### Syntax:
```dart
condition ? exprIfTrue : exprIfFalse
``` 

{{% notice info %}}
**Note**:  The ternary operator takes a condition and returns one of two values, depending upon the condition's boolean value, i.e., true or false.
{{% /notice %}}


### Ternary Operator Vs If Else 
We already learned if-else in dart. Let us see the same example using the if-else and ternary operator.

### Example Using If Else
This program finds greatest number between two numbers using if else.
```dart
void main() {
  int num1 = 10;
  int num2 = 15;
  int max = 0;
  if(num1> num2){
    max = num1;
  }else {
    max = num2;
  }
  print("The greatest number is $max");
}
``` 
{{% expand "Show Output" "false" %}}
````plaintext
The greatest number is 15
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=fbe3c811120bafa1326505d7c413154d" style="blue" %}}Run Online{{% /button %}}

### Example Using Ternary Operator
This program finds greatest number between two numbers using ternary operator.
```dart
void main() {
  int num1 = 10;
  int num2 = 15;
  int max = (num1 > num2) ? num1 : num2;
  print("The greatest number is $max");
}
``` 
{{% expand "Show Output" "false" %}}
````plaintext
The greatest number is 15
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=6b4a8e6c272e2ea21de84313f0769e0b" style="blue" %}}Run Online{{% /button %}}

{{% notice info %}}
**Note**:  Ternary operator makes if-else code much shorter and readable. If you have problems with ternary, you can always use if-else.
{{% /notice %}}

### Example 2 Ternary Operator Dart
If the selection value is 2 then it will set output as Apple otherwise, Banana.
```dart
void main() {
  var selection = 2;
  var output = (selection == 2) ? 'Apple' : 'Banana';
  print(output);
}

``` 
{{% expand "Show Output" "false" %}}
````plaintext
Apple
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=3a69fe146aab9f19add94697e4015ac0" style="blue" %}}Run Online{{% /button %}}

### Example 3 Ternary Operator Dart
This is a dart program to print whether the person is a voter or not using a ternary operator.
```dart
 void main() {
  var age = 18;
  var check = (age >= 18) ? 'You ara a voter.' : 'You are not a voter.';
  print(check);
}
``` 
{{% expand "Show Output" "false" %}}
````plaintext
You ara a voter.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=cfef5f09eb25920a746cc2c62613d71b" style="blue" %}}Run Online{{% /button %}}

### Challenge
Create an int variable age and initialize it with your age. Write **ternary statement** to print "Teenager" if age is between 13 and 19 and "Not Teenager" if age is not between 13 and 19. 
