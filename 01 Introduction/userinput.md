+++
title = "User Input in Dart"
weight = 8
description = "Instead of writing hard-coded values, you can use user input in dart. It will make your program more dynamic. Learn to take a string, integer, or double user input."
keywords = "user input dart, how to take user input in dart, dart user input"
+++


## User Input In Dart
Instead of writing hard-coded values, you can give input to the computer. It will make your program more dynamic. You must import the package `import 'dart:io';` for user input.

{{% notice info %}}
**Note**: You won't be able to take input from users using dartpad. You need to run a program from your computer.
{{% /notice %}}

## String User Input
They are used for storing textual user input. If you want to keep values like somebody's name, address, description, etc., you can take string input from the user.
```dart
import 'dart:io';

void main() {
  print("Enter name:");
  String? name  = stdin.readLineSync();
  print("The entered name is ${name}");
}
``` 
{{% expand "Show Output" "false" %}}
````plaintext
Enter name:
Raj Sharma
The entered name is Raj Sharma
````
{{% /expand %}}

## Integer User Input
You can take integer input to get a numeric value from the user without the decimal point. E.g. 10, 100, -800 etc.
```dart
import 'dart:io';

void main() {
  print("Enter number:");
  int? number = int.parse(stdin.readLineSync()!);
  print("The entered number is ${number}");
}
``` 
{{% expand "Show Output" "false" %}}
````plaintext
Enter number:
50
The entered number is 50
````
{{% /expand %}}


## Floating Point User Input
You can use float input if you want to get a numeric value from the user with the decimal point. E.g. 10.5, 100.5, -800.9 etc.
```dart
import 'dart:io';

void main() {
  print("Enter a floating number:");
  double number = double.parse(stdin.readLineSync()!);
  print("The entered num is $number");
}
``` 
{{% expand "Show Output" "false" %}}
````plaintext
Enter a floating number:
55.5
The entered num is 55.5
````
{{% /expand %}}
