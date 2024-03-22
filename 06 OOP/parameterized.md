+++
title = "Parameterized Constructor in Dart"
weight = 7
description = "A parameterized constructor is a constructor that has parameters. A parameterized constructor is declared using the class name followed by parentheses ()."
keywords = ["parameterized constructor", "parameterized constructor in dart", "parameterized constructor in dart programming", "parameterized constructor in dart programming language"]
+++

### Parameterized Constructor
Parameterized constructor is used to initialize the instance variables of the class. 
Parameterized constructor is the constructor that takes parameters. It is used to pass the values to the constructor at the time of object creation.

### Syntax
```dart
class ClassName {
  // Instance Variables
  int? number;
  String? name;
  // Parameterized Constructor
  ClassName(this.number, this.name);
}
```

### Example 1: Parameterized Constructor In Dart
In this example below, there is a class **Student** with three properties: **name**, **age**, and **rollNumber**. The class has one constructor. The constructor is used to initialize the values of the three properties. We also have an object of the class **Student** called **student**.

```dart
    class Student {
      String? name;
      int? age;
      int? rollNumber;
      // Constructor
      Student(this.name, this.age, this.rollNumber);
    }
    
    void main(){
        // Here student is object of class Student. 
        Student student = Student("John", 20, 1);
        print("Name: ${student.name}");
        print("Age: ${student.age}");
        print("Roll Number: ${student.rollNumber}");
    }
```
{{% expand "Show Output" "false" %}}
````plaintext
Name: John
Age: 20
Roll Number: 1
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=3de8917963386b458cd064701df460e1" style="blue" %}}Run Online{{% /button %}}


### Example 2: Parameterized Constructor With Named Parameters In Dart
In this example below, there is a class **Student** with three properties: **name**, **age**, and **rollNumber**. The class has one constructor. The constructor is used to initialize the values of the three properties. We also have an object of the class **Student** called **student**.

```dart
    class Student {
      String? name;
      int? age;
      int? rollNumber;
    
      // Constructor
      Student({String? name, int? age, int? rollNumber}) {
        this.name = name;
        this.age = age;
        this.rollNumber = rollNumber;
      }
    }
    
    void main(){
        // Here student is object of class Student. 
        Student student = Student(name: "John", age: 20, rollNumber: 1);
        print("Name: ${student.name}");
        print("Age: ${student.age}");
        print("Roll Number: ${student.rollNumber}");
    }
```
{{% expand "Show Output" "false" %}}
````plaintext
Name: John
Age: 20
Roll Number: 1
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=4a031dfc798c36f8d4ee50fafda701e4" style="blue" %}}Run Online{{% /button %}}


### Example 3: Parameterized Constructor With Default Values In Dart
In this example below, there is class **Student** with two properties: **name**, and **age**. The class has parameterized constructor with default values. The constructor is used to initialize the values of the two properties. We also have an object of the class **Student** called **student**.

```dart
    class Student {
      String? name;
      int? age;
    
      // Constructor
      Student({String? name = "John", int? age = 0}) {
        this.name = name;
        this.age = age;
      }
    }
    
    void main(){
        // Here student is object of class Student. 
        Student student = Student();
        print("Name: ${student.name}");
        print("Age: ${student.age}");
    }
```
{{% expand "Show Output" "false" %}}
````plaintext
Name: John
Age: 0
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=99270dddae3eaefb960fd401a0fc5833" style="blue" %}}Run Online{{% /button %}}


{{% notice info %}}
**Note**: In parameterized constructor, at the time of object creation, you must pass the parameters through the constructor which initialize the variables value, avoiding the null values.
{{% /notice %}}

### Video
Watch our video on parameterized constructor in Dart.
{{< youtube -iK2e5A5zBs >}}
