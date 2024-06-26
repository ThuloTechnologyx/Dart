+++
title = "Variables in Dart"
weight = 4
description = "Variables are containers used to store value in the program. Learn variables in the dart, var keyword var types, etc."
keywords = "variables in dart, how to use variables in dart, var in dart, types of variables"
+++

## Variables
Variables are containers used to store value in the program. There are different types of variables where you can keep different kinds of values.
Here is an example of creating a variable and initializing it.
```dart
// here variable name contains value John.
var name = "John";
```          

## Variable Types
They are called data types. We will learn more about data types later in this dart tutorial.

- **String**: For storing text value. E.g. "John" \[Must be in quotes\]
- **int**: For storing integer value. E.g. 10, -10, 8555 \[Decimal is not included\] 
- **double**: For storing floating point values. E.g. 10.0, -10.2, 85.698 \[Decimal is included\] 
- **num**: For storing any type of number. E.g. 10, 20.2, -20 \[both int and double\] 
- **bool**: For storing true or false. E.g. true, false \[Only stores true or false values\]
- **var**: For storing any value. E.g. 'Bimal', 12, 'z', true

## Syntax
```dart
type variableName = value;

```  
## Example
```dart
 void main() {
//Declaring Variables
String name = "John";
String address = "USA";  
num age = 20; // used to store any types of numbers 
num height = 5.9;
bool isMarried = false;
   
// printing variables value   
print("Name is $name");
print("Address is $address");
print("Age is $age");
print("Height is $height");
print("Married Status is $isMarried");
}
``` 
{{% expand "Show Output" "false" %}}
````plaintext
Name is John
Address is USA
Age is 20
Height is 5.9
Married Status is false
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=1112525ad54f10c89a1f768460928e9e" style="blue" %}}{{% /button %}}

{{% notice info %}}
**Note**: Always use the descriptive variable name. Don’t use a variable name like a, b, c because this will make your code more complex.
{{% /notice %}}

## Rules For Creating Variables In Dart

* Variable names are case sensitive, i.e., a and A are different.
* A variable name can consist of letters and alphabets.
* A variable name cannot start with a number. 
* Keywords are not allowed to be used as a variable name.
* Blank spaces are not allowed in a variable name.
* Special characters are not allowed except for the underscore (_) and the dollar ($) sign.


## Dart Constant
Constant is the type of variable whose value never changes. In programming, changeable values are **mutable** and unchangeable values are **immutable**. Sometimes, you don’t need to change the value once declared. Like the value of PI=3.14, it never changes. To create a constant in Dart, you can use the const keyword.

```dart
void main(){
const pi = 3.14;
pi = 4.23; // not possible  
print("Value of PI is $pi");
}
```

{{% expand "Show Output" "false" %}}
````plaintext
Constant variables can't be assigned a value.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=1e3d4c1b325e6f22ad17747a54b452b7" style="blue" %}}{{% /button %}}

## Naming Convention For Variables In Dart
It is a good habit to follow the naming convention. In Dart Variables, the variable name should start with lower-case, and every second word’s first letter will be upper-case like num1, fullName, isMarried, etc. Technically, this naming convention is called **lowerCamelCase**. 

## Example
```dart
// Not standard way
var fullname = "John Doe";
// Standard way
var fullName = "John Doe";
const pi = 3.14;
```
