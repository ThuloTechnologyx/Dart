+++
title = "Constructor in Dart"
weight = 5
description = "In this section, you will learn about  constructor in Dart programming language and how to use constructors with the help of examples."
keywords = "dart constructor, constructor in dart, oop constructor in dart, object oriented programming constructor in dart, dart oops"
+++

## Introduction


In this section, you will learn about  constructor in Dart programming language and how to use constructors with the help of examples. Before learning about the constructor, you should have a basic understanding of the [class](/object-oriented-programming/class-in-dart/) and [object](/object-oriented-programming/object-in-dart/) in dart.

## Constructor In Dart
**A constructor** is a special method used to initialize an object. It is called automatically when an object is created, and it can be used to set the initial values for the object's properties. For example, the following code creates a **Person** class object and sets the initial values for the **name** and **age** properties.

```dart
Person person = Person("John", 30);
```


## Without Constructor
If you don't define a constructor for class, then you need to set the values of the properties manually. For example, the following code creates a **Person** class object and sets the values for the **name** and **age** properties.

```dart
Person person = Person();
person.name = "John";
person.age = 30;
```


## Things To Remember
- The constructor's name should be the same as the class name. 
- Constructor doesn't have any return type.

## Syntax
```dart
class ClassName {
  // Constructor declaration: Same as class name
  ClassName() {
    // body of the constructor
  }
}
```



{{% notice info %}}
**Note**: When you create a object of a class, the constructor is called automatically. It is used to initialize the values when an object is created.
{{% /notice %}}


## Example 1: How To Declare Constructor In Dart
In this example below, there is a class **Student** with three properties: **name**, **age**, and **rollNumber**. The class has one constructor. The constructor is used to initialize the values of the three properties. We also created an object of the class **Student** called **student**.

```dart
class Student {
  String? name;
  int? age;
  int? rollNumber;

  // Constructor
  Student(String name, int age, int rollNumber) {
    print(
        "Constructor called"); // this is for checking the constructor is called or not.
    this.name = name;
    this.age = age;
    this.rollNumber = rollNumber;
  }
}

void main() {
  // Here student is object of class Student.
  Student student = Student("John", 20, 1);
  print("Name: ${student.name}");
  print("Age: ${student.age}");
  print("Roll Number: ${student.rollNumber}");
}
```


{{% expand "Show Output" "false" %}}
````plaintext
Constructor called
Name: John
Age: 20
Roll Number: 1
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=eeb5fc02bac35e9d4d6869096682d72f" style="blue" %}}{{% /button %}}

{{% notice info %}}
**Note**: The **this** keyword is used to refer to the current instance of the class. It is used to access the current class properties. In the example above, parameter names and class properties of constructor **Student** are the same. Hence to avoid confusion, we use the **this** keyword.
{{% /notice %}}

## Example 2: Constructor In Dart
In this example below, there is a class **Teacher** with four properties: **name**, **age**, **subject**, and **salary**. Class has one constructor for initializing the values of the properties. Class also contain method **display()** which is used to display the values of the properties. We also created 2 objects of the class **Teacher** called **teacher1** and **teacher2**.

```dart
class Teacher {
  String? name;
  int? age;
  String? subject;
  double? salary;

  // Constructor
  Teacher(String name, int age, String subject, double salary) {
    this.name = name;
    this.age = age;
    this.subject = subject;
    this.salary = salary;
  }
  // Method
  void display() {
    print("Name: ${this.name}");
    print("Age: ${this.age}");
    print("Subject: ${this.subject}");
    print("Salary: ${this.salary}\n"); // \n is used for new line
  }
}

void main() {
  // Creating teacher1 object of class Teacher
  Teacher teacher1 = Teacher("John", 30, "Maths", 50000.0);
  teacher1.display();

  // Creating teacher2 object of class Teacher
  Teacher teacher2 = Teacher("Smith", 35, "Science", 60000.0);
  teacher2.display();
}
```


{{% expand "Show Output" "false" %}}
````plaintext
Name: John
Age: 30
Subject: Maths
Salary: 50000

Name: Smith
Age: 35
Subject: Science
Salary: 60000
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=a2d165f7939a1fb53e31ff9f5b7c834b" style="blue" %}}{{% /button %}}

{{% notice info %}}
**Note**: You can create many objects of a class. Each object will have its own copy of the properties.
{{% /notice %}}

## Example 3: Constructor In Dart
In this example below, there is a class **Car** with two properties: **name** and **prize**. The class has one constructor for initializing the values of the properties. The class also contains method **display()**, which is used to display the values of the properties. We also created an object of the class **Car** called **car**.

```dart
 class Car {
  String? name;
  double? prize;

  // Constructor
  Car(String name, double prize) {
    this.name = name;
    this.prize = prize;
  }

  // Method
  void display() {
    print("Name: ${this.name}");
    print("Prize: ${this.prize}");
  }
}

void main() {
  // Here car is object of class Car.
  Car car = Car("BMW", 500000.0);
  car.display();
}
```


{{% expand "Show Output" "false" %}}
````plaintext
Name: BMW
Prize: 500000
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=c325ec378196e7e09564a5291991f063" style="blue" %}}{{% /button %}}


## Example 4: Constructor In Dart
In this example below, there is a class **Staff** with four properties: **name**, **phone1**, **phone2**, and **subject** and one method **display()**. Class has one constructor for initializing the values of only **name**, **phone1** and **subject**. We also created an object of the class **Staff** called **staff**.
```dart
 class Staff {
  String? name;
  int? phone1;
  int? phone2;
  String? subject;

  // Constructor
  Staff(String name, int phone1, String subject) {
    this.name = name;
    this.phone1 = phone1;
    this.subject = subject;
  }

  // Method
  void display() {
    print("Name: ${this.name}");
    print("Phone1: ${this.phone1}");
    print("Phone2: ${this.phone2}");
    print("Subject: ${this.subject}");
  }
}

void main() {
  // Here staff is object of class Staff.
  Staff staff = Staff("John", 1234567890, "Maths");
  staff.display();
}
```


{{% expand "Show Output" "false" %}}
````plaintext
Name: John
Phone1: 1234567890
Phone2: null
Subject: Maths
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=f2b41d81556c49993ebe12a919fd1784" style="blue" %}}{{% /button %}}

## Example 5: Write Constructor Single Line
In the avobe section, you have written the constructor in long form. You can also write the constructor in short form. You can directly assign the values to the properties. For example, the following code is the short form of the constructor in one line.

```dart
class Person{
  String? name;
  int? age;
  String? subject;
  double? salary;

  // Constructor in short form
  Person(this.name, this.age, this.subject, this.salary);

  // display method
  void display(){
    print("Name: ${this.name}");
    print("Age: ${this.age}");
    print("Subject: ${this.subject}");
    print("Salary: ${this.salary}");
  }
}

void main(){
  Person person = Person("John", 30, "Maths", 50000.0);
  person.display();
}
```


{{% expand "Show Output" "false" %}}
````plaintext
Name: John
Age: 30
Subject: Maths
Salary: 50000
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=cb1695cb756eda574060b4818f593ba0" style="blue" %}}{{% /button %}}


## Example 6: Constructor With Optional Parameters
In the example below, we have created a class **Employee** with four properties: **name**, **age**, **subject**, and **salary**. Class has one constructor for initializing the all properties values. For **subject** and **salary**, we have used optional parameters. It means we can pass or not pass the values of **subject** and **salary**. The Class also contain method **display()** which is used to display the values of the properties. We also created an object of the class **Employee** called **employee**.

```dart
class Employee {
  String? name;
  int? age;
  String? subject;
  double? salary;

  // Constructor
  Employee(this.name, this.age, [this.subject = "N/A", this.salary=0]);

  // Method
  void display() {
    print("Name: ${this.name}");
    print("Age: ${this.age}");
    print("Subject: ${this.subject}");
    print("Salary: ${this.salary}");
  }
}

void main(){
  Employee employee = Employee("John", 30);
  employee.display();
}
```


{{% expand "Show Output" "false" %}}
````plaintext
Name: John
Age: 30
Subject: N/A
Salary: 0
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=32a8dce515ee86ddbbf673f1c11506c0" style="blue" %}}{{% /button %}}


## Example 7: Constructor With Named Parameters
In the example below, we have created a class **Chair** with two properties: **name** and **color**. Class has one constructor for initializing the all properties values with named parameters. The Class also contain method **display()** which is used to display the values of the properties. We also created an object of the class **Chair** called **chair**.
  
  ```dart 
class Chair {
  String? name;
  String? color;

  // Constructor
  Chair({this.name, this.color});

  // Method
  void display() {
    print("Name: ${this.name}");
    print("Color: ${this.color}");
  }
}

void main(){
  Chair chair = Chair(name: "Chair1", color: "Red");
  chair.display();
}
```


{{% expand "Show Output" "false" %}}
````plaintext
Name: Chair1
Color: Red
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=e33af11085f5dc397b96edc102517757" style="blue" %}}{{% /button %}}


## Example 8: Constructor With Default Values
In the example below, we have created a class **Table** with two properties: **name** and **color**. Class has one constructor for initializing the all properties values with default values. The Class also contain method **display()** which is used to display the values of the properties. We also created an object of the class **Table** called **table**.

```dart
class Table {
  String? name;
  String? color;

  // Constructor
  Table({this.name = "Table1", this.color = "White"});

  // Method
  void display() {
    print("Name: ${this.name}");
    print("Color: ${this.color}");
  }
}

void main(){
  Table table = Table();
  table.display();
}
```


{{% expand "Show Output" "false" %}}
````plaintext
Name: Table1
Color: White
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=8d00a0f0de26c181e6d56749330172f8" style="blue" %}}{{% /button %}}

## Key Points
- The constructor's name should be the same as the class name. 
- Constructor doesn't have any return type.
- Constructor is only called once at the time of the object creation.
- Constructor is called automatically when an object is created.
- Constructor is used to initialize the values of the properties of the class.

## Challenge
Create a class **Patient** with three properties **name**, **age**, and **disease**. The class has one constructor. The constructor is used to initialize the values of the three properties. Also, create an object of the class **Patient** called **patient**. Print the values of the three properties using the object.
