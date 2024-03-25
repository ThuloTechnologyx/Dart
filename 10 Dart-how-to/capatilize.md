+++
title = "Capitalize First Character"
weight = 3
keywords = ["convert string to int in dart", "dart string to int", "dart string to int parse", "dart string to int parse example", "dart string to int parse example"]
description = "In this tutorial, you will learn to capatilize first character of string in dart programming. You will learn to capitalize first character of string in dart."
+++


## How To Capitalize First Letter Of String In Dart
If you want to capitalize the first letter of a String in Dart, you can use the following code. 

```dart
//Example of capitalize first letter of String
void main() { 
  String text = "hello world"; 
  print("Capitalized first letter of String: ${text[0].toUpperCase()}${text.substring(1)}"); 
} 
``` 
{{% expand "Show Output" "false" %}}
```plaintext
Capitalized first letter of String: Hello world
```
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=b35aec750e198f194c863c1ddf76de2e" style="blue" %}}{{% /button %}}


## Example 2: To Capitalize First Letter Of String Using Extension Method
In this example, we will use the extension method to capitalize the first letter of a String. You can learn more about extension method [here](/useful-information/extension-in-dart/).

```dart
//Example of capitalize first letter of String using extension method
extension StringExtension on String {
  String capitalize() {
    return "${this[0].toUpperCase()}${this.substring(1)}";
  }
}

void main() {
  String text = "hello world";
  print("Capitalized first letter of String: ${text.capitalize()}");
}
```
{{% expand "Show Output" "false" %}}
```plaintext
Capitalized first letter of String: Hello world
```
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=2f875354ca442561d549a8f1c40ac17f" style="blue" %}}{{% /button %}}
