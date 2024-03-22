+++
title = "Convert String to Int"
weight = 1
keywords = ["convert string to int in dart", "dart string to int", "dart string to int parse", "dart string to int parse example", "dart string to int parse example"]
description = "In this tutorial, you will learn to convert string to int in dart programming. You will learn to convert string to int in dart."
+++

### Convert String To Int In Dart
[![targets](/images/pieces/note-banner.png)](https://pieces.app/?utm_source=dart-tutorial&utm_medium=banner&utm_campaign=dart-tutorial-website&utm_content=note)

The String is the textual representation of data, whereas int is a numeric representation without a decimal point. While coding in must of the case, you need to convert data from one type to another type. In dart, you can convert String to int by using the **int.parse() method**.

```dart
int.parse("String");
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=af004aa592)

You can replace **String** with any numeric value and convert String to int. Make sure you  have numeric value there. To know more see the example below.


### Example To Convert String to Int
This program converts String to int. You can view type of variable with **.runtimeType**.
```dart
void main(){
String value = "10";
int numericValue = int.parse(value);
print("Type of value is ${value.runtimeType}");
print("Type of numeric value is ${numericValue.runtimeType}");
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=c7f34e9a03)

{{% expand "Show Output" "false" %}}
````plaintext
Type of value is String
Type of numeric value is int
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=2f875354ca442561d549a8f1c40ac17f" style="blue" %}}Run Online{{% /button %}}

### Example 2 To Convert String to Int
This program first converts String to int and finds the sum of two numbers.
```dart
void main(){
String value = "10";

int num2 = 20;
int num1 = int.parse(value);

int sum = num1 + num2;

print("Type sum is $sum");
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=161d42981d)

{{% expand "Show Output" "false" %}}
````plaintext
Sum is 110
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=15f9c24418653dc0c6c070fd0763db15" style="blue" %}}Run Online{{% /button %}}


### Things To Remember While Casting String To Int
You must be sure that String could convert the to int. If it doesn't convert to int, it will throw an exception. You can use the try-catch statement to show your custom message. If you don't know exception handling in dart [learn from here](/conditions-and-loops/exception_handeling-in-dart/).


### Example With Try Catch
This program throws an exception because you can't convert "hello" to int. In this situation, you can use the try-catch exception to display your custom message.
```dart
void main(){
try {
String value = "hello";
int numericValue = int.parse(value);
print("Type of numeric value is ${numericValue.runtimeType}");

  }
catch(ex){
print("Something went wrong.");
}

}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=111d45b730)

{{% expand "Show Output" "false" %}}
````plaintext
Something went wrong.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=bc0e369d9dc9556834319284e1bd2bc4" style="blue" %}}Run Online{{% /button %}}