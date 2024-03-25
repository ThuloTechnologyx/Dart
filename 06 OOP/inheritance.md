+++
title = "Inheritance in Dart"
weight = 14
description = "In dart, Inheritance allows you to define a class that extend functionality of another class. Inheritance in Dart is used to define a class that inherits the properties and methods of another class."
keywords = ["inheritance", "inheritance in dart", "inheritance in dart programming", "inheritance in dart programming language"]
+++

## Introduction
In this section, you will learn inheritance in Dart programming and how to define a class that reuses the properties and methods of another class.

## Inheritance In Dart
Inheritance is a sharing of behaviour between two classes. It allows you to define a class that extends the functionality of another class. The **extend** keyword is used for inheriting from parent class.

{{% notice info %}}
**Note**: Whenever you use inheritance, it always create a **is-a** relation  between the parent and child class like **Student is a Person**, **Truck is a Vehicle**, **Cow is a Animal** etc.
{{% /notice %}}

Dart supports single inheritance, which means that a class can only inherit from a single class. Dart does not support multiple inheritance which means that a class cannot inherit from multiple classes.

## Syntax
```dart
class ParentClass {
  // Parent class code
}

class ChildClass extends ParentClass {
  // Child class code
}
```
In this syntax, **ParentClass** is the super class and **ChildClass** is the sub class. The **ChildClass** inherits the properties and methods of the **ParentClass**.

## Terminology
**Parent Class:** The class whose properties and methods are inherited by another class is called parent class. It is also known as base class or super class.

**Child Class:** The class that inherits the properties and methods of another class is called child class. It is also known as derived class or sub class.

## Example 1: Inheritance In Dart
In this example, we will create a class **Person** and then create a class **Student** that inherits the properties and methods of the **Person** class.

```dart
class Person {
  // Properties
  String? name;
  int? age;

  // Method
  void display() {
    print("Name: $name");
    print("Age: $age");
  }
}
// Here In student class, we are extending the
// properties and methods of the Person class
class Student extends Person {
  // Fields
  String? schoolName;
  String? schoolAddress;

  // Method
  void displaySchoolInfo() {
    print("School Name: $schoolName");
    print("School Address: $schoolAddress");
  }
}

void main() {
  // Creating an object of the Student class
  var student = Student();
  student.name = "John";
  student.age = 20;
  student.schoolName = "ABC School";
  student.schoolAddress = "New York";
  student.display();
  student.displaySchoolInfo();
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Name: John
Age: 20
School Name: ABC School
School Address: New York
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=7937ca7a2a516afebb151311d1cc0dfd" style="blue" %}}{{% /button %}}

## Advantages Of Inheritance In Dart
- It promotes reusability of the code and reduces redundant code.
- It helps to design a program in a better way. 
- It makes code simpler, cleaner and saves time and money on maintenance.
- It facilitates the creation of class libraries.
- It can be used to enforce standard interface to all children classes.

## Example 2: Inheritance In Dart
In this example, here is parent class **Car** and child class **Toyota**. The **Toyota** class inherits the properties and methods of the **Car** class. 
```dart
class Car{
  String color;
  int year;

  void start(){
    print("Car started");
  }  
}

class Toyota extends Car{
  String model;
  int prize;

  void showDetails(){
    print("Model: $model");
    print("Prize: $prize");
  }
}

void main(){
  var toyota = Toyota();
  toyota.color = "Red";
  toyota.year = 2020;
  toyota.model = "Camry";
  toyota.prize = 20000;
  toyota.start();
  toyota.showDetails();
}
```

{{% expand "Show Output" "false" %}}
```plaintext
Car started
Model: Camry
Prize: 20000
```
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=750fe96f17f40b95a72fe951f60e028d" style="blue" %}}{{% /button %}}

## Types Of Inheritance In Dart

1. **Single Inheritance** - In this type of inheritance, a class can inherit from only one class. In Dart, we can only extend one class at a time.

2. **Multilevel Inheritance** - In this type of inheritance, a class can inherit from another class and that class can also inherit from another class. In Dart, we can extend a class from another class which is already extended from another class.

3. **Hierarchical Inheritance** - In this type of inheritance, parent class is inherited by multiple subclasses. For example, the **Car** class can be inherited by the **Toyota** class and **Honda** class.

4. **Multiple Inheritance** - In this type of inheritance, a class can inherit from multiple classes. **Dart does not support multiple inheritance.** For e.g. **Class Toyota extends Car, Vehicle {}** is not allowed in Dart.

## Example 3: Single Inheritance In Dart
In this example below, there is super class named **Car** with two properties **name** and **prize**. There is sub class named **Tesla** which inherits the properties of the super class. The sub class has a method **display** to display the values of the properties.
  
  ```dart
  class Car {
    // Properties
    String? name;
    double? prize;
  }

  class Tesla extends Car {
    // Method to display the values of the properties
    void display() {
      print("Name: ${name}");
      print("Prize: ${prize}");
    }
  }

  void main() {
    // Create an object of Tesla class
    Tesla t = new Tesla();
    // setting values to the object
    t.name = "Tesla Model 3";
    t.prize = 50000.00;
    // Display the values of the object
    t.display();
  }
  ```
      
{{% expand "Show Output" "false" %}}
````plaintext
Name: Tesla Model 3
Prize: 50000.0
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=e2badfaf79554c14d550c0039c1e892c" style="blue" %}}{{% /button %}}

## Example 4: Multilevel Inheritance In Dart
In this example below, there is super class named **Car** with two properties **name** and **prize**. There is sub class named **Tesla** which inherits the properties of the super class. The sub class has a method **display** to display the values of the properties. There is another sub class named **Model3** which inherits the properties of the sub class **Tesla**. The sub class has a property **color** and a method **display** to display the values of the properties.
  ```dart
 class Car {
  // Properties
  String? name;
  double? prize;
}

class Tesla extends Car {
  // Method to display the values of the properties
  void display() {
    print("Name: ${name}");
    print("Prize: ${prize}");
  }
}

class Model3 extends Tesla {
  // Properties
  String? color;

  // Method to display the values of the properties
  void display() {
    super.display();
    print("Color: ${color}");
  }
}

void main() {
  // Create an object of Model3 class
  Model3 m = new Model3();
  // setting values to the object
  m.name = "Tesla Model 3";
  m.prize = 50000.00;
  m.color = "Red";
  // Display the values of the object
  m.display();
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Name: Tesla Model 3
Prize: 50000.0
Color: Red
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=f5a50bac67ef983b7894f88a37bc47f4" style="blue" %}}{{% /button %}}

{{% notice info %}}
**Note:** Here super keyword is used to call the method of the parent class.
{{% /notice %}}

## Example 5: Multilevel Inheritance In Dart
In this example below, there is class named **Person** with two properties **name** and **age**. There is sub class named **Doctor** with properties **listofdegrees** and **hospitalname**. There is another subclass named **Specialist** with property **specialization**. The sub class has a method **display** to display the values of the properties.

```dart
class Person {
  // Properties
  String? name;
  int? age;
}

class Doctor extends Person {
  // Properties
  List<String>? listofdegrees;
  String? hospitalname;

  // Method to display the values of the properties
  void display() {
    print("Name: ${name}");
    print("Age: ${age}");
    print("List of Degrees: ${listofdegrees}");
    print("Hospital Name: ${hospitalname}");
  }
}

class Specialist extends Doctor {
  // Properties
  String? specialization;

  // Method to display the values of the properties
  void display() {
    super.display();
    print("Specialization: ${specialization}");
  }
}

void main() {
  // Create an object of Specialist class
  Specialist s = new Specialist();
  // setting values to the object
  s.name = "John";
  s.age = 30;
  s.listofdegrees = ["MBBS", "MD"];
  s.hospitalname = "ABC Hospital";
  s.specialization = "Cardiologist";
  // Display the values of the object
  s.display();
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Name: John
Age: 30
List of Degrees: [MBBS, MD]
Hospital Name: ABC Hospital
Specialization: Cardiologist
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=88098415597eaf0bc0a5c1b787281cfc" style="blue" %}}{{% /button %}}

## Example 6: Hierarchical Inheritance In Dart
In this example below, there is class named **Shape** with two properties **diameter1** and **diameter2**. There is sub class named **Rectangle** with method **area** to calculate the area of the rectangle. There is another subclass named **Triangle** with method **area** to calculate the area of the triangle.

```dart
class Shape {
  // Properties
  double? diameter1;
  double? diameter2;
}

class Rectangle extends Shape {
  // Method to calculate the area of the rectangle
  double area() {
    return diameter1! * diameter2!;
  }
}

class Triangle extends Shape {
  // Method to calculate the area of the triangle
  double area() {
    return 0.5 * diameter1! * diameter2!;
  }
}

void main() {
  // Create an object of Rectangle class
  Rectangle r = new Rectangle();
  // setting values to the object
  r.diameter1 = 10.0;
  r.diameter2 = 20.0;
  // Display the area of the rectangle
  print("Area of the rectangle: ${r.area()}");

  // Create an object of Triangle class
  Triangle t = new Triangle();
  // setting values to the object
  t.diameter1 = 10.0;
  t.diameter2 = 20.0;
  // Display the area of the triangle
  print("Area of the triangle: ${t.area()}");
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Area of the rectangle: 200.0
Area of the triangle: 100.0
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=5eb99c4fb8e32fdfdafb6f1039a6644d" style="blue" %}}{{% /button %}}


## Key Points
- Inheritance is used to reuse the code.
- Inheritance is a concept which is achieved by using the **extends** keyword.
- Properties and methods of the super class can be accessed by the sub class.
- Class **Dog** extends class **Animal**{} means Dog is sub class and Animal is super class.
- The sub class can have its own properties and methods.

## Why Dart Does Not Support Multiple Inheritance?
Dart does not support multiple inheritance because it can lead to ambiguity. For example, if class **Apple** inherits class **Fruit** and class **Vegetable**, then there may be two methods with the same name **eat**. If the method is called, then which method should be called? This is the reason why Dart does not support multiple inheritance.


## What's problem Of Copy Paste Instead Of Inheritance?
If you copy the code from one class to another class, then you will have to maintain the code in both the classes. If you make any changes in one class, then you will have to make the same changes in the other class. This can lead to errors and bugs in the code.

## Does Inheritance Finished If I Learned Extending Class?
No, there is a lot more to learn about inheritance. You need to learn about **Constructor Inheritance**, **Method Overriding**, **Abstract Class**, **Interface** and **Mixin** etc. You will learn about these concepts in the next chapters.

## Video
Watch our video on inheritance in Dart.
{{< youtube NBdbNBCD4N4 >}}