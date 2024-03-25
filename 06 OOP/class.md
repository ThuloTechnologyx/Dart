+++
title = "Class in Dart"
weight = 2
description = "In this section, you will learn about the class in Dart programming language. You will learn about the class, its properties, and its methods."
keywords = "dart class, class in dart, oop class in dart, object oriented programming class in dart, dart oops"
+++

## Class In Dart 
In object-oriented programming, a class is a blueprint for creating objects. A class defines the properties and methods that an object will have. For example, a class called **Dog** might have properties like **breed**, **color** and methods like **bark**, **run**.

## Declaring Class In Dart
You can declare a class in dart using the **class** keyword followed by class name and braces {}. It's a good habit to write class name in **PascalCase**. For example, **Employee**, **Student**, **QuizBrain**, etc.


## Syntax
```dart
class ClassName {
// properties or fields
// methods or functions
}
```

In the above syntax:
- The **class** keyword is used for defining the class.
- **ClassName** is the name of the class and must start with capital letter.
- Body of the class consists of **properties** and **functions**.
- **Properties** are used to store the data. It is also known as **fields** or **attributes**.
- **Functions** are used to perform the operations. It is also known as **methods**.

## Example 1: Declaring A Class In Dart
In this example below, there is class **Animal** with three properties: **name**, **numberOfLegs**, and **lifeSpan**. The class also has a method called **display**, which prints out the values of the three properties. 

```dart
class Animal {
  String? name;
  int? numberOfLegs;
  int? lifeSpan;

  void display() {
    print("Animal name: $name.");
    print("Number of Legs: $numberOfLegs.");
    print("Life Span: $lifeSpan.");
  }
}
```
{{% notice info %}}
**Note: This program will not print anything** because we have not created any object of the class. You will learn about the  [object](/object-oriented-programming/object-in-dart/) later. The **?** is used for null safety. You will also learn about [null safety](/null-safety/) later.
{{% /notice %}}

## Example 2: Declaring A Person Class In Dart
In this example below, there is class **Person** with four properties: **name**, **phone**, **isMarried**, and **age**. The class also has a method called **displayInfo**, which prints out the values of the four properties.

```dart
class Person {
  String? name;
  String? phone;
  bool? isMarried;
  int? age;

  void displayInfo() {
    print("Person name: $name.");
    print("Phone number: $phone.");
    print("Married: $isMarried.");
    print("Age: $age.");
  }
}
```

## Example 3: Declaring Area Class In Dart
In this example below, there is class **Area** with two properties: **length** and **breadth**. The class also has a method called **calculateArea**, which calculates the area of the rectangle.

```dart
class Area {
  double? length;
  double? breadth;

  double calculateArea() {
    return length! * breadth!;
  }
}
```

## Example 4: Declaring A Student Class In Dart
In this example below, there is class **Student** with three properties: **name**, **age**, and **grade**. The class also has a method called **displayInfo**, which prints out the values of the three properties. 

```dart
class Student {
  String? name;
  int? age;
  int? grade;

  void displayInfo() {
    print("Student name: $name.");
    print("Student age: $age.");
    print("Student grade: $grade.");
  }
}
```
## Key Points
- The class is declared using the **class** keyword.
- The class is a blueprint for creating objects.
- The class body consists of properties and methods.
- The properties are also known as fields, attributes, or data members.
- The methods are also known as behaviors, or member functions.


## Challenge
Create a class **Book** with three properties: **name**, **author**, and **prize**. Also, create a method called **display**, which prints out the values of the three properties.

{{% notice info %}}
**Note**: In the next section, you will learn how to create an object from a class.
{{% /notice %}}
