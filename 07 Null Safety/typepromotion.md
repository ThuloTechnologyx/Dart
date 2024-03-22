+++
title = "Type Promotion in Dart"
weight = 3
description = "Type promotion in Dart is the process by which a value of one type is automatically converted to a value of another type."
keywords = "type promotion in dart, type promotion in dart example, type promotion in dart usecase, type promotion in dart flutter, type promotion in dart null safety, type promotion in dart flutter example, type promotion in dart flutter usecase, type promotion in dart flutter null safety"
+++

### Type Promotion In Dart
**Type promotion in dart** means that dart automatically converts a value of one type to another type. Dart does this when it knows that the value is of a specific type. 

### How Type Promotion Works In Dart?
Types Promotion in Dart works in the following ways:
- Promoting from **general types** to **specific subtypes**.
- Promoting from **nullable types** to **non-nullable types**.

### Example 1: Promoting From General Types To Specific Subtypes
In this example, the variable **name** is declared as an **Object**. The **Object** class doesn't have a **.length** property. Variable **name** gets promoted from **Object** to **String** so that you can access the **.length** property of the String class.

```dart
void main(){
Object name = "Pratik";
// print(name.length) will not work because Dart doesn't know that name is a String

if(name is String) {
// name promoted from Object to String
  print("The length of name is ${name.length}");
}
}
```
{{% expand "Show Output" "false" %}}
````plaintext
The length of name is 6
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=7a6d740ee6ae02f6884d45d0953bbe0d" style="blue" %}}Run Online{{% /button %}}


### Example 2: Type Promotion In Dart
In this example, the variable **result** is declared as a **String**. In both **if** and **else** blocks, the variable **result** is assigned a value of type **String**. Therefore, the variable **result** is automatically promoted to a non-nullable type **String**.
```dart
void main(){
// result is a String
String result;
// result is promoted to a non-nullable type String
if(DateTime.now().hour < 12) {
  result = "Good Morning";
} else {
  result = "Good Afternoon";
}
// display the result
print("Result is $result");
print("Length of result is ${result.length}");
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Result is Good Afternoon
Length of result is 15
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=709573f1c60bf14cbabfb256f26be782" style="blue" %}}Run Online{{% /button %}}

### Example 3: Type Promotion With Nullable To Non-Nullable Type
In Dart, you can also throw an exception if the variable is null. In this example, method **printLength**, takes a **String** type parameter. If the parameter is null, then it will throw an exception.
```dart
// method to print the length of the text
void printLength(String? text){
    if(text == null) {
        throw Exception("The text is null");
    }
    print("Length of text is ${text.length}");
}
// main method
void main() {
    printLength("Hello");
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Length of text is 5
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=3acebdaf31a83036db811f7e2a123d40" style="blue" %}}Run Online{{% /button %}}

### Example 4: Type Promotion With Nullable Type To Non-Nullable Type
In this example, the variable **value** contains a value of type **String** or **null**. The variable **value** is promoted to a non-nullable type **String** in the **if** block. If the variable **value** is null, then the **else** block is executed.

```dart
// importing dart:math library
import 'dart:math';
// creating a class DataProvider
class DataProvider{
    // creating a method stringorNull
    String? get stringorNull => Random().nextBool() ? "Hello" : null;

    // creating a method myMethod
    void myMethod(){
        String? value = stringorNull;
        // checking if value String or not
        if(value is String){
            print("The length of value is ${value.length}");
        }else{
            print("The value is not string.");
        }

    }
}
// main method
void main() {
    DataProvider().myMethod();
}
```
{{% expand "Show Output" "false" %}}
````plaintext
The length of value is 5
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=0c7841acafbb586a4da7ebc39f6f7d96" style="blue" %}}Run Online{{% /button %}}

{{% notice info %}}
**Note:** The output of the above example is random. It can be either **The length of value is 5** or **The value is not string.**
{{% /notice %}}



### Video
Watch our video on the type promotion in Dart.
{{< youtube WI-PCBewEBo >}}
