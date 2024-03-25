+++
title = "Anonymous Function in Dart"
weight = 4
keywords = "dart anonymous function, dart functions, how to use the anonymous function in dart."
description = "In this tutorial, you will learn what is an anonymous function in dart and how to use an anonymous function."
+++

## Anonymous Function In Dart
This tutorial will teach you the anonymous function and how to use it. You already saw function like **main()**, **add()**, etc. These are the **named** functions, which means they have a certain name. 

But not every function needs a name. If you remove the return type and the function name, the function is called **anonymous function**.

## Syntax
Here is the syntax of the anonymous function.
```dart
(parameterList){
// statements
}

```
## Example 1: Anonymous Function In Dart
In this example, you will learn to use an anonymous function to print all list items. This function invokes each fruit without having a function name. 

```dart
void main() {
  const fruits = ["Apple", "Mango", "Banana", "Orange"];

  fruits.forEach((fruit) {
    print(fruit);
  });
}

```
{{% expand "Show Output" "false" %}}
````plaintext
Apple
Mango
Banana
Orange
````
{{% /expand %}}

{{% button href="https://dartpad.dev/?id=7f9135e19160e6ca3dc76e93bff6d3f0" style="blue" %}}{{% /button %}}
## Example 2: Anonymous Function In Dart
In this example, you will learn to find the cube of a number using an anonymous function. 

```dart
void main() {
// Anonymous function
  var cube = (int number) {
    return number * number * number;
  };

  print("The cube of 2 is ${cube(2)}");
  print("The cube of 3 is ${cube(3)}");
}
```
{{% expand "Show Output" "false" %}}
````plaintext
The cube of 2 is 8
The cube of 3 is 27
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=687ef3c989719b79a55638c9dc425712" style="blue" %}}{{% /button %}}
