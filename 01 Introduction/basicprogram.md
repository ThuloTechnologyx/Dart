+++
title = "Basic Dart Program"
weight = 3
description = "Learn dart language basics, create a hello world program in the dart, and learn how to make complete dart projects."
keywords = "dart hello world program, how to create dart program, dart simple program, learn dart programming"
+++

## Basic Dart Program
This is a simple dart program that prints **Hello World** on screen. Most programmers write the Hello World program as their first program.

```dart
void main() { 
   print("Hello World!"); 
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Hello World!
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=0af2b28fb35507498bc37843e948f95e" style="blue" %}}{{% /button %}}

## Basic Dart Program Explained
- void main() is the starting point where the execution of your program begins. 
- Every program starts with a main function.
- The curly braces {} represent the beginning and the ending of a block of code.
- print("Hello World!"); prints Hello World! on screen.
- Each code statement must end with a semicolon.
 
## Basic Dart Program For Printing Name

```dart
void main()
{
    var name = "John";
    print(name);
}
``` 
{{% expand "Show Output" "false" %}}
````plaintext
John
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=469378fc6d2fbc30a446f9cdf84f1c4f" style="blue" %}}{{% /button %}}

## Basic Dart Program To Join One Or More Variables
Here **$variableName** is used to join variables. This joining process in dart is called string interpolation.

```dart
void main(){
  var firstName = "John";
  var lastName = "Doe";
  print("Full name is $firstName $lastName");
}
``` 
{{% expand "Show Output" "false" %}}
````plaintext
Full name is John Doe
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=d9a87dca5ed42563f198ebc9090de893" style="blue" %}}{{% /button %}}

## Dart Program For Basic Calculation
Performing addition, subtraction, multiplication, and division in dart.

```dart
void main() {
int num1 = 10; //declaring number1
int num2 = 3; //declaring number2
  
// Calculation
int sum = num1 + num2;
int diff = num1 - num2;
int mul = num1 * num2;
double div = num1 / num2; // It is double because it outputs number with decimal.
  
// displaying the output
print("The sum is $sum");
print("The diff is $diff");
print("The mul is $mul");
print("The div is $div");
}
```
{{% expand "Show Output" "false" %}}
````plaintext
The sum is 13
The diff is 7
The mul is 30
The div is 3.3333333333333335
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=33d8e11932346850b77cf9057e2268ab" style="blue" %}}{{% /button %}}

## Create Full Dart Project
It's nice to work on a single file, but if your project gets bigger, you need to manage configurations, packages, and assets files. So creating a dart project will help you to manage this all.

```dart
dart create <project_name>
```
This will create a simple dart project with some ready-made code.

## Steps To Create Dart Project
- Open folder location on command prompt/terminal.
- Type `dart create project_name` (For E.g. dart create first_app)
- Type `cd first_app`
- Type `code .` to open project with visual studio code
- To check the main dart file go to **bin/first_app.dart** and edit your code.

## Run Dart Project
First, open the project location on the command/terminal and run the project with this command.
```dart
dart run
```

## Convert Dart Code To Javascript
|  Command  |  Description  |
| ----------- | --------- | 
|  dart compile js filename.dart  |  Compile dart to javascript. You can run this file with Node.js.  |

## Challenge
Create a new dart project with name **stockmanagement** and then run it.

