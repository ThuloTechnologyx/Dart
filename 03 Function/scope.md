+++
title = "Scope in Dart"
weight = 6
keywords = "dart tutorial scope, dart function scope, scope in dart, dart scope, learn scope in dart"
description = "In this tutorial, you will learn about scope in dart. The scope is a concept that refers to where values can be accessed or referenced. "
+++

## Scope In Dart
The scope is a concept that refers to where values can be accessed or referenced. Dart uses curly braces **{}** to determine the scope of variables. If you define a variable inside curly braces, you can't use it outside the curly braces.

## Method Scope
If you created variables inside the method, you can use them inside the method block but not outside the method block.

## Example 1: Method Scope

```dart
void main() {
  String text = "I am text inside main. Anyone can't access me.";
  print(text);
}
```
{{% expand "Show Output" "false" %}}
````plaintext
I am text inside main. Anyone can't access me.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=6b3e28b49091f667dcec3eea55f2166f" style="blue" %}}{{% /button %}}

In this program, **text** is a String type where you can access and print method only inside the main function but not outside the main function. 

## Global Scope

You can define a variable in the global scope to use the variable anywhere in your program.

## Example 1: Global Scope
```dart
String global = "I am Global. Anyone can access me.";
void main() {
  print(global);
}
```
{{% expand "Show Output" "false" %}}
````plaintext
I am Global. Anyone can access me.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=4103d7d0db2cb45132a40c83e815185c" style="blue" %}}{{% /button %}}

In this program, the variable named **global** is a top-level variable; you can access it anywhere in the program.

{{% notice info %}}
**Note**: Define your variable as much as close **Local** as you can. It makes your code clean and prevents you from using or changing them where you shouldn't.
{{% /notice %}}

## Lexical Scope
Dart is lexically scoped language, which means you can find the scope of variables with the help of **braces {}**.

