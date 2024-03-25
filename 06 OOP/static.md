+++
title = "Static in Dart"
weight = 18
description = "In this section, you will learn about static in Dart programming language."
keywords = ["static", "dart static keyword", "static in dart", "static method in dart", "static in dart programming", "static in dart programming language"]
+++

## Introduction
In this section, you will learn about **dart static** to share the same variable or method across all instances of a class.

## Static In Dart
If you want to define a variable or method that is shared by all instances of a class, you can use the **static** keyword. Static members are accessed using the class name. It is used for **memory management**.

## Dart Static Variable
A static variable is a variable that is shared by all instances of a class. It is declared using the static keyword. It is initialized only once when the class is loaded. It is used to store the **class-level data**.

## How To Declare A Static Variable In Dart
To declare a static variable in Dart, you must use the static keyword before the variable name.
```dart
class ClassName {
  static dataType variableName;
}
```

## How To Initialize A Static Variable In Dart
To initialize a static variable simply assign a value to it.
```dart
class ClassName {
  static dataType variableName = value;
  // for e.g 
  // static int num = 10;
  // static String name = "Dart";
}
```

## How To Access A Static Variable In Dart
You need to use the **ClassName.variableName** to access a static variable in Dart.
```dart
class ClassName {
  static dataType variableName = value;
  // Accessing the static variable inside same class
  void display() {
    print(variableName);
  }
}

void main() {
  // Accessing static variable outside the class
  dataType value =ClassName.variableName;
}
```

## Example 1: Static Variable In Dart
In this example below, there is a class named **Employee**. The class has a static variable **count** to count the number of employees.

```dart
class Employee {
  // Static variable
  static int count = 0;
  // Constructor
  Employee() {
    count++;
  }
  // Method to display the value of count
  void totalEmployee() {
    print("Total Employee: $count");
  }
}

void main() {
  // Creating objects of Employee class
  Employee e1 = new Employee();
  e1.totalEmployee();
  Employee e2 = new Employee();
  e2.totalEmployee();
  Employee e3 = new Employee();
  e3.totalEmployee();
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Total Employee: 1
Total Employee: 2
Total Employee: 3
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=" style="blue" %}}{{% /button %}} 

{{% notice info %}}
**Note:** While creating the objects of the class, the static variable **count** is incremented by 1. The **totalEmployee()** method displays the value of the static variable **count**.
{{% /notice %}}

## Example 2: Static Variable In Dart
In this example below, there is a class named **Student**. The class has a static variable **schoolName** to store the name of the school. If every student belongs to the same school, then it is better to use a static variable.

```dart
class Student {
  int id;
  String name;
  static String schoolName = "ABC School";
  Student(this.id, this.name);
  void display() {
    print("Id: ${this.id}");
    print("Name: ${this.name}");
    print("School Name: ${Student.schoolName}");
  }
}

void main() {
  Student s1 = new Student(1, "John");
  s1.display();
  Student s2 = new Student(2, "Smith");
  s2.display();
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Id: 1
Name: John
School Name: ABC School
Id: 2
Name: Smith
School Name: ABC School
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=" style="blue" %}}{{% /button %}}

## Dart Static Method
A static method is shared by all instances of a class. It is declared using the static keyword. You can access a static method without creating an object of the class.

## Syntax
```dart
class ClassName{
static returnType methodName(){
  //statements
}
}
```

## Example 3: Static Method In Dart
In this example, we will create a static method **calculateInterest()** which calculates the simple interest. You can call **SimpleInterest.calculateInterest()** anytime without creating an instance of the class.

```dart
class SimpleInterest {
  static double calculateInterest(double principal, double rate, double time) {
    return (principal * rate * time) / 100;
  }
}

void main() {
  print(
      "The simple interest is ${SimpleInterest.calculateInterest(1000, 2, 2)}");
}
```
{{% expand "Show Output" "false" %}}
````plaintext
The simple interest is 40.0
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=" style="blue" %}}{{% /button %}}


## Example 4: Static Method In Dart
In this example below, there is static method **generateRandomPassword()** which generates a random password. You can call **PasswordGenerator.generateRandomPassword()** anytime without creating an instance of the class.

```dart
import 'dart:math';

class PasswordGenerator {
  static String generateRandomPassword() {
    List<String> allalphabets = 'abcdefghijklmnopqrstuvwxyz'.split('');
    List<int> numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9];
    List<String> specialCharacters = ["@", "#", "%", "&", "*"];
    List<String> password = [];
    for (int i = 0; i < 5; i++) {
      password.add(allalphabets[Random().nextInt(allalphabets.length)]);
      password.add(numbers[Random().nextInt(numbers.length)].toString());
      password
          .add(specialCharacters[Random().nextInt(specialCharacters.length)]);
    }
    return password.join();
  }
}

void main() {
  print(PasswordGenerator.generateRandomPassword());
}
```
{{% expand "Show Output" "false" %}}
````plaintext
v5*p4*o2&c7%k1@
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=" style="blue" %}}{{% /button %}}


{{% notice info %}}
**Note**: You don't need to create an instance of a class to call a static method.
{{% /notice %}}

## Key Points To Remember
- Static members are accessed using the class name.
- All instances of a class share static members.
