+++
title = "Default Constructor in Dart"
weight = 6
description = "A default constructor is a constructor that is automatically created by the compiler if you don't create a constructor. A default constructor has no parameters. A default constructor is declared using the class name followed by parentheses ()."
keywords = ["default constructor", "default constructor in dart", "default constructor in dart programming", "default constructor in dart programming language"]
+++

## Default Constructor
The constructor which is automatically created by the dart compiler if you don't create a constructor is called a default constructor. A default constructor has no parameters. A default constructor is declared using the class name followed by parentheses (). 

## Example 1: Default Constructor In Dart
In this example below, there is a class **Laptop** with two properties: **brand**, and **prize**. Lets create constructor with no parameter and print something from the constructor. We also have an object of the class **Laptop** called **laptop**.

```dart
class Laptop {
  String? brand;
  int? prize;

  // Constructor
  Laptop() {
    print("This is a default constructor");
  }
}

void main() {
  // Here laptop is object of class Laptop.
  Laptop laptop = Laptop();
}
```
{{% expand "Show Output" "false" %}}
````plaintext
This is a default constructor
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=149eac8a84c228173b72a0710ae4c9f3" style="blue" %}}{{% /button %}}


{{% notice info %}}
**Note**: The default constructor is called automatically when you create an object of the class. It is used to initialize the instance variables of the class.
{{% /notice %}}

## Example 2: Default Constructor In Dart
In this example below, there is a class **Student** with four properties: **name**, **age**, **schoolname** and **grade**. The default constructor is used to initialize the values of the school name. The reason for this is that the school name is the same for all the students. We also have an object of the class **Student** called **student**. The default constructor is called automatically when you create an object of the class.

```dart
class Student {
  String? name;
  int? age;
  String? schoolname;
  String? grade;

  // Default Constructor
  Student() {
    print(
        "Constructor called"); // this is for checking the constructor is called or not.
    schoolname = "ABC School";
  }
}

void main() {
  // Here student is object of class Student.
  Student student = Student();
  student.name = "John";
  student.age = 10;
  student.grade = "A";
  print("Name: ${student.name}");
  print("Age: ${student.age}");
  print("School Name: ${student.schoolname}");
  print("Grade: ${student.grade}");
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Constructor called
Name: John
Age: 10
School Name: ABC School
Grade: A
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=eab58b8724f1e4ad233a4cb15fdccbd8" style="blue" %}}{{% /button %}}


## Challenge
Try to create a class **Person** with two properties: **name**, and **planet**. Create a default constructor to initialize the values of the **planet** to earth. Create an object of the class **Person**, set the name to "Your Name" and print the name and planet.
