+++
title = "Null Safety Exercise"
weight = 5
description = "Practice Exercise for Null Safety in Dart Programming Language. Practice exercise to master the null safety in dart programming language."
keywords = "null safety exercise, null safety exercise dart, null safety exercise dart example, null safety exercise dart usecase, null safety exercise dart flutter, null safety exercise dart null safety, null safety exercise dart flutter example, null safety exercise dart flutter usecase, null safety exercise dart flutter null safety"
+++

### Null Safety Exercise
Practice these exercises to master **dart null safety**. To practice these exercises, click on **Run Online** button and solve the problem.

### Exercise 1: Null Safety In Dart
In variable name **age**, assign a **null** value to it using **?**.
```dart
// Try to assign a null value to age variable using ?
void main() {
  int age;
  age = null;
  print("Age is $age");
}
```
{{% button href="https://dartpad.dev/?id=d5947f463c719ff9667c6af855376536" style="blue" %}}Run Online{{% /button %}}

### Exercise 2: Nullable Type Parameter For Generics
Try using **?** to make the type parameter of **List** nullable.
```dart
// Try to make the type parameter of List nullable
void main() {
  List<int> items = [1, 2, null, 4];
  print(items);
}
```
{{% button href="https://dartpad.dev/?id=3ed4aec39a483738d18cca44944be8e8" style="blue" %}}Run Online{{% /button %}}

### Exercise 3: Null Assertion Operator (!)
Try using null assertion operator **!** to print null if the variable is null.
```dart
// Try to use null assertion operator(!) to print null if the variable is null
void main() {
  String? name;
  name = null;
  String name1 = name;
  print(name1);
}
```
{{% button href="https://dartpad.dev/?id=c244f5fee631d9426d1004a20f7c01c3" style="blue" %}}Run Online{{% /button %}}

### Exercise 4: Null Assertion Operator (!) For Generics
Try using null assertion operator **!** to print null if the variable is null.
```dart
// Try to use null assertion operator(!) to print null if the variable is null
void main() {
  List<int?> items = [1, 2, null, 4];
 
  int firstItem = items.first;
  
  print(firstItem);
}
```
{{% button href="https://dartpad.dev/?id=c1bcc0544dcb955a8d2e69373f88617b" style="blue" %}}Run Online{{% /button %}}

### Exercise 5: Null Assertion Operator (!) For Generics
Try using null assertion operator **!** to print null if the variable is null.
```dart
// Try to use null assertion operator(!) to print null if the variable is null
int? returnNullButSometimesNot() {
  return -5;
}

void main() {
 int result = returnNullButSometimesNot().abs();
 print(result);
}
```
{{% button href="https://dartpad.dev/?id=1b9b4febfbc21b23be8ae5bf146e95c1" style="blue" %}}Run Online{{% /button %}}

### Exercise 6: Null Assertion Operator (!) 
Try using null assertion operator **!** to print the length of the String or return null if the variable is null.
```dart
// Try to use null assertion operator(!) to print the length of the String or return null if the variable is null
int findLength(String? name) {
    // add null assertion operator here
  return name.length;
}

void main() {
  int? length = findLength("Hello");
  print("The length of the string is $length");
}
```
{{% button href="https://dartpad.dev/?id=ae7997a085f35212078c2db830d3b673" style="blue" %}}Run Online{{% /button %}}

### Exercise 7: Null Coalescing Operator (??)
If you want to assign a default value to a variable if it is null, you can use null coalescing operator **??**. 

Try using null coalescing operator **??** to assign a default value to **Stranger** if it is null.
```dart
// Try to use null coalescing operator(??) to assign a default value to Stranger if it is null
void main() {
  String? name;
  name = null;
  String name1 = name;
  print(name1);
}
```
{{% button href="https://dartpad.dev/?id=ebddc5b4f402664e6c0439f2ac2fcce6" style="blue" %}}Run Online{{% /button %}}

### Exercise 8: Type Promotion
Solve the error using type promotion:
```dart
// Try to solve the error using type promotion
Object name = "Mark";
print("The length of name is ${name.length}");
```
{{% button href="https://dartpad.dev/?id=b7fa99e858705bc1cf05a94514a7f95e" style="blue" %}}Run Online{{% /button %}}


### Exercise 9: Type Promotion
Solve the error using type promotion:
```dart
// Try to solve the error using type promotion
import 'dart:math';
class DataProvider{
    String? get stringorNull => Random().nextBool() ? "Hello" : null;

    void myMethod(){
        if(stringorNull is String){
            print("The length of value is ${stringorNull.length}");
        }else{
            print("The value is not string.");
        }

    }
}

void main() {
    DataProvider().myMethod();
}
```
{{% button href="https://dartpad.dev/?id=fe82354a868ce0200cc928387296d52b" style="blue" %}}Run Online{{% /button %}}


### Exercise 10: Late Keyword
Try using **late** keyword to solve the error:
```dart
// Try to solve the error using late keyword
class Person{
    String _name;

    void setName(String name){
        _name = name;
    }

    String get name => _name;
}

void main() {
    Person person = Person();
    person.setName("Mark");
    print(person.name);
}
```
{{% button href="https://dartpad.dev/?id=30f4779d30a8f00cc2178cc9662dc8e3" style="blue" %}}Run Online{{% /button %}}

