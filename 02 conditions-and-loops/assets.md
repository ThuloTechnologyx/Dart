
+++
title = "Assert in Dart"
weight = 2
description = "In dart assert takes conditions as an argument. If the condition is true, nothing happens. If a condition is false, it will raise an error."
keywords = "dart assert, assert in dart, how to use assert in dart, dart assert in details"
+++

### Assert
While coding, it is hard to find errors in big projects, so dart provide a **assert** method to check for the error. It takes conditions as an argument. If the condition is true, nothing happens. If a condition is false, it will raise an error.

### Syntax
You can use assert without a custom message or with a custom message.
```dart
assert(condition);
// or 
assert(condition, "Your custom message");
```
### Example How To Use Assert In Dart Program
This example shows how you can use assert without a custom message. 
```dart
void main() { 
   var age = 22;
   assert(age!=22);
}
``` 
{{% expand "Show Output" "false" %}}
````plaintext
Uncaught Error: Assertion failed
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=b70d85fe957e214ceaa16b9410243746" style="blue" %}}Run Online{{% /button %}}

### Example 2 How To Use Assert In Dart Program
This example shows how you can use assert with a custom message. 
```dart
void main() { 
   var age = 22;
   assert(age!=22, "Age must be 22");
}
``` 
{{% expand "Show Output" "false" %}}
````plaintext
Uncaught Error: Assertion failed: "Age must be 22"
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=8be7c091b45258d69cbeeeade76c198f" style="blue" %}}Run Online{{% /button %}}

### How to Run File In Assert Mode
Use this command to run the dart file, which enables assert. If you don't use this, you will not be able to see the issue. You can use this command below if you are running a dart file from the computer.

```dart
dart --enable-asserts file_name.dart
``` 

{{% notice info %}}
**Note**: The **assert(condition)** method only runs in development mode. It will throw an exception only when the condition is false. If the condition is true, nothing happens. Production code ignores it.
{{% /notice %}}
