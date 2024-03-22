+++
title = "Break and Continue in Dart"
weight = 10
description = "Learn how to use break and continue in dart."
keywords = "break in dart, continue in dart, break and continue in dart."
+++

### Dart Break and Continue
In this tutorial, you will learn about the **break and continue** in dart. While working on loops, we need to skip some elements or terminate the loop immediately without checking the condition. In such a situation, you can use the break and continue statement.

### Break Statement
Sometimes you will need to break out of the loop immediately without checking the condition. You can do this using break statement.

The break statement is used to exit a loop. It stops the loop immediately, and the program's control moves outside the loop. Here is syntax of break:

```dart
break;
``` 

### Example 1: Break In Dart For Loop
Here, the loop condition is true until the value of i is less than or equal to 10. However, the break says to go outside the loop when the value of i becomes 5.
```dart
void main() {
  for (int i = 1; i <= 10; i++) {
    if (i == 5) {
      break;
    }
    print(i);
  }
}

``` 
{{% expand "Show Output" "false" %}}
````plaintext
1
2
3
4
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=78e5717d41d98bf2d991b1a2312aa97c" style="blue" %}}Run Online{{% /button %}}

### Example 2: Break In Dart Negative For Loop
Here, the loop condition is true until the value of i is more than or equal to 1. However, the break says to go outside the loop when the value of i becomes 7.
```dart
void main() {
  for (int i = 10; i >= 1; i--) {
    if (i == 7) {
      break;
    }
    print(i);
  }
}
```
{{% expand "Show Output" "false" %}}
````plaintext
10
9
8
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=f3d1f98a372e3dd7df2cf4fa2c240026" style="blue" %}}Run Online{{% /button %}}


### Example 3: Break In Dart While Loop
Here, this while loop condition is true until the value of i is less than or equal to 10. However, the break says to go outside the loop when the value of i becomes 5.
```dart
void main() {
 int i =1;
 while(i<=10){
  print(i);
   if (i == 5) {
      break;
    }
    i++;
 }
}
```
{{% expand "Show Output" "false" %}}
````plaintext
1
2
3
4
5
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=cf611e7dc2ab2bc3064c7cac318d1a25" style="blue" %}}Run Online{{% /button %}}

### Example 4: Break In Switch Case
As we already learn in [dart switch case](/conditions-and-loops/switch-case-in-dart/), it is important to add **break** keyword in switch statement. This example prints the month name based on the number of the month using a switch case.

```dart
void main() {
  var noOfMoneth = 5;
  switch (noOfMoneth) {
    case 1:
      print("Selected month is January.");
      break;
    case 2:
      print("Selected month is February.");
      break;
    case 3:
      print("Selected month is march.");
      break;
    case 4:
      print("Selected month is April.");
      break;
    case 5:
      print("Selected month is May.");
      break;
    case 6:
      print("Selected month is June.");
      break;
    case 7:
      print("Selected month is July.");
      break;
    case 8:
      print("Selected month is August.");
      break;
    case 9:
      print("Selected month is September.");
      break;
    case 10:
      print("Selected month is October.");
      break;
    case 11:
      print("Selected month is November.");
      break;
    case 12:
      print("Selected month is December.");
      break;
    default:
      print("Invalid month.");
      break;
  }
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Selected month is May.
````
{{% /expand %}} 
{{% button href="https://dartpad.dev/?id=f5f2fe64072f8fbaac7a90cff64b64bb" style="blue" %}}Run Online{{% /button %}}
### Continue Statement
Sometimes you will need to skip an iteration for a specific condition. You can do this utilizing continue statement.

The continue statement skips the current iteration of a loop. It will bypass the statement of the loop. It does not terminate the loop but rather continues with the next iteration. Here is the syntax of continue statement:

```dart
continue;
``` 

### Example 1: Continue In Dart
Here, the loop condition is true until the value of i is less than or equal to 10. However, the continue says to go to the next iteration of the loop when the value of i becomes 5.
```dart
void main() {
  for (int i = 1; i <= 10; i++) {
    if (i == 5) {
      continue;
    }
    print(i);
  }
}
``` 
{{% expand "Show Output" "false" %}}
````plaintext
1
2
3
4
6
7
8
9
10
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=9addce33e98b6c048dc7b4e6ca36dd39" style="blue" %}}Run Online{{% /button %}}

### Example 2: Continue In For Loop Dart
Here, the loop condition is true until the value of i is more than or equal to 1. However, the continue says to go to the next iteration of the loop when the value of i becomes 4.
```dart
void main() {
  for (int i = 10; i >= 1; i--) {
    if (i == 4) {
      continue;
    }
    print(i);
  }
}
``` 
{{% expand "Show Output" "false" %}}
````plaintext
10
9
8
7
6
5
3
2
1
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=ac3889e41518f16988808f1b330faed2" style="blue" %}}Run Online{{% /button %}}

### Example 3: Continue In Dart While Loop
Here, this while loop condition is true until the value of i is less than or equal to 10. However, the continue says to go to the next iteration of the loop when the value of i becomes 5.
```dart
void main() {
  int i = 1;
  while (i <= 10) {
    if (i == 5) {
      i++;
      continue;
    }
    print(i);
    i++;
  }
}

```
{{% expand "Show Output" "false" %}}
````plaintext
1
2
3
4
6
7
8
9
10
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=754c4200cc5de0c0c046776cef22e563" style="blue" %}}Run Online{{% /button %}}
