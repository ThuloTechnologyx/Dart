+++
title = "Loops in Dart"
weight = 5
description = "Looping is repeating a specific set of commands until conditions are not completed. We have different types of loop in dart."
keywords = "Loops in dart, for loop in dart, for loop in dart, while loop in dart, do while loop in dart"
+++

## Dart Loops
In Programming, loops are used to repeat a block of code until certain conditions are not completed. For, e.g., if you want to print your name 100 times, then rather than typing print("your name"); 100 times, you can use a loop.  

There are different types of loop in Dart. They are:
*   **[For Loop](/conditions-and-loops/for-loop-in-dart/)**
*   **[For Each Loop](/conditions-and-loops/for-each-loop-in-dart/)**
*   **[While Loop](/conditions-and-loops/while-loop-in-dart/)**
*   **[Do While Loop](/conditions-and-loops/do-while-loop-in-dart/)**

{{% notice info %}}
**Note**: The primary purpose of all loops is to repeat a block of code.
{{% /notice %}}

## Print Your Name 10 Times Without Using Loop
Let's first print the name 10 times without using a loop.

```dart
void main() {
    print("John Doe");
    print("John Doe");
    print("John Doe");
    print("John Doe");
    print("John Doe");
    print("John Doe");
    print("John Doe");
    print("John Doe");
    print("John Doe");
    print("John Doe");
}
``` 
{{% expand "Show Output" "false" %}}
````plaintext
John Doe
John Doe
John Doe
John Doe
John Doe
John Doe
John Doe
John Doe
John Doe
John Doe
````
{{% /expand %}} 
{{% button href="https://dartpad.dev/?id=21f7f965f37d6f79787d5b455742db9c" style="blue" %}}{{% /button %}}

## Print Your Name 10 Times Using Loop
We will learn for loop in the next section, paste the code and see the output. It will print your name 10 times.

```dart
void main() {
  for (int i = 0; i < 10; i++) {
    print("John Doe");
  }
}
``` 
{{% expand "Show Output" "false" %}}
````plaintext
John Doe
John Doe
John Doe
John Doe
John Doe
John Doe
John Doe
John Doe
John Doe
John Doe
````
{{% /expand %}} 
{{% button href="https://dartpad.dev/?id=24cc41317ae68ba7f2510eec1395027e" style="blue" %}}{{% /button %}}

What if you want to print your name 1000 times? Without using a loop, it will be difficult for you.

{{% notice info %}}
**Note**: Loops are helpful because they reduce errors, save time, and make code more readable.
{{% /notice %}}
## What After Now?
Move to a new section to understand each loop clearly.

