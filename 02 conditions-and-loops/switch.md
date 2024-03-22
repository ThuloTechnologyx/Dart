
+++
title = "Switch Case in Dart"
weight = 3
description = "Learn switch case in dart. A Switch case is used to execute the code block based on the condition. The syntax of switch statements is cleaner and much easier to read and write."
keywords = "switch case dart, dart switch case, switch case in dart, string switch case dart, enum switch case dart"
+++

### Switch Case In Dart
[![targets](/images/pieces/note-banner.png)](https://pieces.app/?utm_source=dart-tutorial&utm_medium=banner&utm_campaign=dart-tutorial-website&utm_content=note)
In this tutorial, you will learn to use **dart switch case** to control your program's flow. A Switch case is used to execute the code block based on the condition. 

```dart
switch(expression) {
    case value1:
        // statements
        break;
    case value2:
        // statements
        break;
    case value3:
        // statements
        break;
    default:
       // default statements
}
``` 
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=92f24e8c38)

**How does switch-case statement work in dart**
- The **expression** is evaluated once and compared with each case value.   
- If **expression** matches with case value1, the statements of case value1 are executed. Similarly, case value 2 will be executed if the expression matches case value2. If the expression matches the case value3, the statements of case value3 are executed.
- The **break** keywords tell dart to exit the switch statement because the statements in the case block are finished.
- If there is no match, **default statements** are executed.

{{% notice info %}}
**Note**:  You can use a Switch case as an alternative to the **if-else-if** condition.
{{% /notice %}}


### Replace If Else If With Switch In Dart
Here you can see the same program using **if else if** and **switch** in dart.  

### Example Using If Else If
This example prints the day name based on the numeric day of the week using a if else if.
```dart
void main(){
   var dayOfWeek = 5;
if (dayOfWeek == 1) {
        print("Day is Sunday.");
  }
else if (dayOfWeek == 2) {
       print("Day is Monday.");
     }
else if (dayOfWeek == 3) {
      print("Day is Tuesday.");
     }
else if (dayOfWeek == 4) {
        print("Day is Wednesday.");
     }
else if (dayOfWeek == 5) {
        print("Day is Thursday.");
   }
else if (dayOfWeek == 6) {
        print("Day is Friday.");
    }
else if (dayOfWeek == 7) {
        print("Day is Saturday.");
}else{
        print("Invalid Weekday.");
     }
 }

```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=bdd64ba0a8)

{{% expand "Show Output" "false" %}}
````plaintext
Day is Thursday.
````
{{% /expand %}} 
{{% button href="https://dartpad.dev/?id=47306bb3550def46d9cc25b5b46b8753" style="blue" %}}Run Online{{% /button %}}

### Example Of Switch Statement
This example prints the day name based on the numeric day of the week using a switch case.
```dart
void main() {
  var dayOfWeek = 5;
  switch (dayOfWeek) {
    case 1:
        print("Day is Sunday.");
        break;
    case 2:
        print("Day is Monday.");
      break;
    case 3:
      print("Day is Tuesday.");
      break;
    case 4:
        print("Day is Wednesday.");
      break;
    case 5:
        print("Day is Thursday.");
      break;
    case 6:
        print("Day is Friday.");
      break;
    case 7:
        print("Day is Saturday.");
      break;
    default:
        print("Invalid Weekday.");
      break;
  }
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=13f549adcc)

{{% expand "Show Output" "false" %}}
````plaintext
Day is Thursday.
````
{{% /expand %}} 
{{% button href="https://dartpad.dev/?id=4f69e4fd09f10849546f8b7ef8bafa28" style="blue" %}}Run Online{{% /button %}}
{{% notice info %}}
**Note**:  The syntax of switch statements is cleaner and much easier to read and write.
{{% /notice %}}


### Switch Case On Strings
You can also use a switch case with strings. This program prints information based on weather value.
```dart
void main() {
 const weather = "cloudy";

  switch (weather) {
    case "sunny":
        print("Its a sunny day. Put sunscreen.");
        break;
    case "snowy":
        print("Get your skis.");
      break;
    case "cloudy":
    case "rainy": 
      print("Please bring umbrella.");
      break;
    default:
        print("Sorry I am not familiar with such weather.");
      break;
  }
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=a7f244a276)

{{% expand "Show Output" "false" %}}
````plaintext
Please bring umbrella.
````
{{% /expand %}} 
{{% button href="https://dartpad.dev/?id=c177885042b281c34faddb7eeac6a5b7" style="blue" %}}Run Online{{% /button %}}

### Switch Case On Enum
An **[enum](/object-oriented-programming/enum-in-dart/)** or enumeration is used for defining value according to you. You can define your own type with a finite number of options. Here is the syntax for defining enum.

### Syntax
```dart
enum enum_name { 
  constant_value1, 
  constant_value2, 
  constant_value3 
  }
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=da2844828a)

### Example of Switch Using Enum In Dart
Enum plays well with switch statements. Let's see an example using enum.

```dart
// define enum outside main function
enum Weather{ sunny, snowy, cloudy, rainy}
// main method
void main() {
 const weather = Weather.cloudy;
  
  switch (weather) {
    case Weather.sunny:
        print("Its a sunny day. Put sunscreen.");
        break;
    case Weather.snowy:
        print("Get your skis.");
      break;
    case Weather.rainy:
    case Weather.cloudy:
      print("Please bring umbrella.");
      break;
    default:
        print("Sorry I am not familiar with such weather.");
      break;
  }
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=5ed84ea12d)

{{% expand "Show Output" "false" %}}
````plaintext
Please bring umbrella.
````
{{% /expand %}} 
{{% button href="https://dartpad.dev/?id=c93ad2410bf834284d40de28ca5a72ab" style="blue" %}}Run Online{{% /button %}}
