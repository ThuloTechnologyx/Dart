+++
title = "Data Types in Dart"
weight = 5
description = "Here you will learn different data types in dart with examples. You will also learn to convert dart double to int, int to double, a string to int, and so on. This page will also help you in flutter data-types conversion."
keywords = "dart datatypes, numbers in dart, dart strings, dart booleans, dart lists, dart maps, dart sets, dart runes, dart null, dart programming data types, how to convert int to double, convert string to int dart"
+++

### Data Types
**Data types** help you to categorize all the different types of data you use in your code. **For e.g. numbers, texts, symbols, etc**. The data type specifies what type of value will be stored by the variable. Each variable has its data type. Dart supports the following built-in data types :
1. Numbers
2. Strings
3. Booleans
4. Lists
5. Maps
6. Sets
7. Runes 
8. Null 

### Built-In Types
In Dart language, there is the type of values that can be represented and manipulated. The data type classification is as given below: 

|  Data Type  |  Keyword  |  Description  |
| ----------- | --------- | ------------- |
|  Numbers  |    int, double, num    | It represents numeric values  |
|  Strings  |    String  |  It represents a sequence of characters  |
|  Booleans  |  bool  | It represents Boolean values true and false  |
|  Lists  |  List  |    It is an ordered group of items  |
|  Maps  |  Map  |  It represents a set of values as key-value pairs  |
|  Sets  |  Set  |  It is an unordered list of unique values of same types |
|  Runes  |  runes  |  It represents Unicode values of String |
|  Null  |  null  |  It represents null value |

### Numbers
When you need to store numeric value on dart, you can use either int or double. Both int and double are subtypes of **num**. You can use num to store both int or double value.

```dart
 void main() {
 // Declaring Variables  
int num1 = 100; // without decimal point.
double num2 = 130.2; // with decimal point.
num num3 = 50;
num  num4 = 50.4;  

// For Sum   
num sum = num1 + num2 + num3 + num4;
   
// Printing Info   
print("Num 1 is $num1");
print("Num 2 is $num2");  
print("Num 3 is $num3");  
print("Num 4 is $num4");  
print("Sum is $sum");  
   
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=ac404e915a)

{{% expand "Show Output" "false" %}}
````plaintext
Num 1 is 100
Num 2 is 130.2
Num 3 is 50
Num 4 is 50.4
Sum is 330.59999999999997
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=a9919677147fb1cd2b887846b93a3034" style="blue" %}}Run Online{{% /button %}}

### Round Double Value To 2 Decimal Places
The `.toStringAsFixed(2)` is used to round the double value upto 2 decimal places in dart. You can round to any decimal places by entering numbers like 2, 3, 4, etc.

```dart
void main() {
// Declaring Variables
double prize = 1130.2232323233233; // valid.
print(prize.toStringAsFixed(2));
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=2cd249946e)

{{% expand "Show Output" "false" %}}
````plaintext
1130.22
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=75519f1fd124093402be8f7b75c36148" style="blue" %}}Run Online{{% /button %}}

### String
String helps you to store text data. You can store values like **I love dart**, **New York 2140** in String. You can use single or double quotes to store string in dart. 

```dart
void main() {
// Declaring Values     
String schoolName = "Diamond School";
String address = "New York 2140";   

// Printing Values
print("School name is $schoolName and address is $address");   
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=7c7c4dba14)

{{% expand "Show Output" "false" %}}
````plaintext
School name is Diamond School and address is New York 2140
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=3499e05553d3b7171528e91c01b834ed" style="blue" %}}Run Online{{% /button %}}

### Create A Multi-Line String In Dart
If you want to create a multi-line String in dart, then you can use triple quotes with either single or double quotation marks.

```dart
 void main() {
// Multi Line Using Single Quotes   
String multiLineText = '''
This is Multi Line Text
with 3 single quote
I am also writing here.
''';
   
// Multi Line Using Double Quotes   
String otherMultiLineText = """
This is Multi Line Text
with 3 double quote
I am also writing here.
""";
   
// Printing Information   
print("Multiline text is $multiLineText");
print("Other multiline text is $otherMultiLineText");
}

```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=94f84180fb)

{{% expand "Show Output" "false" %}}
````plaintext
Multiline text is This is Multi Line Text
with 3 single quote
I am also writing here.

Other multiline text is This is Multi Line Text
with 3 double quote
I am also writing here.

````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=b92d5489dbe64d42c2227e855ea116b3" style="blue" %}}Run Online{{% /button %}}

### Special Character In String
|  Special Character |  Work 
| ----------- | --------- |
|  \n  |    New Line    |
|  \t  |    Tab  |  

```dart
 void main() {
   
// Using \n and \t   
print("I am from \nUS.");
print("I am from \tUS.");
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=fa814fbb04)

{{% expand "Show Output" "false" %}}
````plaintext
I am from 
US.
I am from 	US.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=6cdd60d155830f25642f2da6263f070b" style="blue" %}}Run Online{{% /button %}}

### Create A Raw String In Dart
You can also create raw string in dart.  Special characters won't work here. You must write **r** after equal sign.

```dart
 void main() {
// Set prize value
num prize = 10;
String withoutRawString = "The value of prize is \t $prize"; // regular String
String withRawString =r"The value of prize is \t $prize"; // raw String

print("Without Raw: $withoutRawString"); // regular result
print("With Raw: $withRawString"); // with raw result

}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=c0de48987f)

{{% expand "Show Output" "false" %}}
````plaintext
Without Raw: The value of prize is 	 10
With Raw: The value of prize is \t $prize
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=6b31b681217f80ba0208c07e8c9d11d8" style="blue" %}}Run Online{{% /button %}}

### Type Conversion In Dart
In dart, type conversion allows you to convert one data type to another type. For e.g. to convert String to int, int to String or String to bool, etc.

### Convert String To Int In dart
You can convert String to int using int.parse() method. The method takes String as an argument and converts it into an integer.

```dart
void main() {
String strvalue = "1";
print("Type of strvalue is ${strvalue.runtimeType}");   
int intvalue = int.parse(strvalue);
print("Value of intvalue is $intvalue");
// this will print data type
print("Type of intvalue is ${intvalue.runtimeType}");
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=b0134591ee)

{{% expand "Show Output" "false" %}}
````plaintext
Type of strvalue is String
Value of intvalue is 1
Type of intvalue is int
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=a6822a6bce6f84b4d28dbdebe8541a2e" style="blue" %}}Run Online{{% /button %}}

### Convert String To Double In Dart
You can convert String to double using double.parse() method. The method takes String as an argument and converts it into a double.
```dart
void main() {
String strvalue = "1.1";
print("Type of strvalue is ${strvalue.runtimeType}");
double doublevalue = double.parse(strvalue);
print("Value of doublevalue is $doublevalue");
// this will print data type
print("Type of doublevalue is ${doublevalue.runtimeType}");
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=78214698b1)

{{% expand "Show Output" "false" %}}
````plaintext
Type of strvalue is String
Value of doublevalue is 1.1
Type of doublevalue is double
````
{{% /expand %}}
### Convert Int To String In Dart
You can convert int to String using the toString() method. Here is example:

```dart
void main() {
int one = 1;
print("Type of one is ${one.runtimeType}");
String oneInString = one.toString(); 
print("Value of oneInString is $oneInString");
// this will print data type
print("Type of oneInString is ${oneInString.runtimeType}");
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=6d8f44b9a6)

{{% expand "Show Output" "false" %}}
````plaintext
Type of one is int
Value of oneInString is 1
Type of oneInString is String
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=931a151d6dc316a48a2b20a8a820e0fe" style="blue" %}}Run Online{{% /button %}}

### Convert Double To Int In Dart
You can convert double to int using the toInt() method.

```dart
void main() { 
   double num1 = 10.01;
   int num2 = num1.toInt(); // converting double to int

  print("The value of num1 is $num1. Its type is ${num1.runtimeType}");
  print("The value of num2 is $num2. Its type is ${num2.runtimeType}");
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=c3d54aaa93)

{{% expand "Show Output" "false" %}}
````plaintext
The value of num1 is 10.01. Its type is double
The value of num2 is 10. Its type is int
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=3edee3c0689b8cf96254ec49264102b6" style="blue" %}}Run Online{{% /button %}}

### Booleans
In Dart, boolean holds either true or false value. You can write the **bool** keyword to define the boolean data type. You can use boolean if the answer is true or false. Consider the answer to the following questions:
- Are you married?
- Is the door open?
- Does a cat fly?
- Is the traffic light green?
- Are you older than your father?

**These all are yes/no questions. Its a good idea to store them in boolean.**

```dart
void main() {
bool isMarried = true;
print("Married Status: $isMarried");
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=bbb1408261)

{{% expand "Show Output" "false" %}}
````plaintext
Married Status: true
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=33c42a2ac8bfa78f8c9cb01fb599527c" style="blue" %}}Run Online{{% /button %}}

### Lists
The list holds multiple values in a single variable. It is also called arrays. If you want to store multiple values without creating multiple variables, you can use a list.

```dart
void main() {
List<String> names = ["Raj", "John", "Max"];
print("Value of names is $names");
print("Value of names[0] is ${names[0]}"); // index 0
print("Value of names[1] is ${names[1]}"); // index 1
print("Value of names[2] is ${names[2]}"); // index 2

  // Finding Length of List 
int length = names.length;  
print("The Length of names is $length");
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=32864e92d4)

{{% expand "Show Output" "false" %}}
````plaintext
Value of names is [Raj, John, Max]
Value of names[0] is Raj
Value of names[1] is John
Value of names[2] is Max
The Length of names is 3
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=72ab5bdd38125a2979610e9882382604" style="blue" %}}Run Online{{% /button %}}

{{% notice info %}}
Note: List index always starts with 0. Here names[0] is Raj, names[1] is John and names[2] is Max.
{{% /notice %}}


### Sets
An unordered collection of unique items is called set in dart. You can store unique data in sets.

{{% notice info %}}
Note: Set doesn't print duplicate items.
{{% /notice %}}

```dart
void main() {
Set<String> weekday = {"Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat"};
print(weekday);
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=afda4e88cf)

{{% expand "Show Output" "false" %}}
````plaintext
{Sun, Mon, Tue, Wed, Thu, Fri, Sat}
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=b5568b9645ae5feba4446f01f6b546db" style="blue" %}}Run Online{{% /button %}}

### Maps
In Dart, a map is an object where you can store data in key-value pairs. Each key occurs only once, but you can use same value multiple times. 
```dart
void main() {
Map<String, String> myDetails = {
   'name': 'John Doe',
   'address': 'USA',
   'fathername': 'Soe Doe'
};

print(myDetails['name']);
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=f2a340ae62)

{{% expand "Show Output" "false" %}}
````plaintext
John Doe
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=308158d4a7f592602b768d17c838813a" style="blue" %}}Run Online{{% /button %}}

### Var Keyword In Dart
In Dart, **var** automatically finds a data type. In simple terms, var says if you don't want to specify a data type, I will find a data type for you. 

 ```dart
void main(){
 var name = "John Doe"; // String
 var age = 20; // int
 
 print(name);
 print(age);
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=8c704b9b78)

{{% expand "Show Output" "false" %}}
````plaintext
John Doe
20
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=213ab2f088e156dd0a8620013bcd1895" style="blue" %}}Run Online{{% /button %}}

### Runes In Dart
With runes, you can find Unicode values of String. The Unicode value of **a** is **97**, so runes give 97 as output.

 ```dart
void main() {

String value = "a";
print(value.runes);
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=54c94fa182)

{{% expand "Show Output" "false" %}}
````plaintext
(97)
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=708b8348adac48a05ae308d37464dd07" style="blue" %}}Run Online{{% /button %}}

### How To Check Runtime Type
You can check runtime type in dart with `.runtimeType` after the variable name.
```dart
void main() { 
   var a = 10;
   print(a.runtimeType); 
   print(a is int); // true
}
``` 
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=fbe74aabf5)

{{% expand "Show Output" "false" %}}
````plaintext
int
true
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=a4ea5418158069933bdce4a7d82ef7ce" style="blue" %}}Run Online{{% /button %}}

### Optionally Typed Language
You may have heard of the **statically-typed** language. It means the data type of variables is known at compile time. Similarly, **dynamically-typed** language means data types of variables are known at run time. Dart supports dynamic and static types, so it is called optionally-typed language. 


### Statically Typed 
A language is statically typed if the data type of variables is known at compile time. Its main advantage is that the compiler can quickly check the issues and detect bugs.
```dart
void main() { 
   var myVariable = 50; // You can also use int instead of var
   myVariable = "Hello"; // this will give error
   print(myVariable);
}
``` 
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=dcb2438603)

{{% expand "Show Output" "false" %}}
````plaintext
Error:
A value of type 'String' can't be assigned to a variable of type 'int'.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=e9966f0fc66d4142233d9f4ba0330446" style="blue" %}}Run Online{{% /button %}}

### Dynamically Typed Example
A language is dynamically typed if the data type of variables is known at run time.
```dart
void main() { 
   dynamic myVariable = 50;
   myVariable = "Hello";
   print(myVariable);
}
``` 
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=a26f4b9ff4)

{{% expand "Show Output" "false" %}}
````plaintext
Hello
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=b56c00badb6eb97738776091504aa019" style="blue" %}}Run Online{{% /button %}}

{{% notice info %}}
Note: Using static type helps you to prevent writing silly mistakes in code. It's a good habit to use static type in dart.
{{% /notice %}}

