+++
title = "Named Constructor in Dart"
weight = 8
description = "In this section, you will learn about named constructor in dart programming language. You will learn how to create a named constructor in dart programming language."
keywords = ["named constructor", "named constructor in dart", "named constructor in dart programming", "named constructor in dart programming language"]
+++
## Named Constructor In Dart
[![targets](/images/pieces/note-banner.png)](https://pieces.app/?utm_source=dart-tutorial&utm_medium=banner&utm_campaign=dart-tutorial-website&utm_content=note)
In most programming languages like java, c++, c#, etc., we can create multiple constructors with the same name. But in Dart, this is not possible. Well, there is a way. We can create multiple constructors with the same name using **named constructors**.

{{% notice info %}}
**Note**: Named constructors improves code readability. It is useful when you want to create multiple constructors with the same name.
{{% /notice %}}


## Example 1: Named Constructor In Dart
In this example below, there is a class **Student** with three properties: **name**, **age**, and **rollNumber**. The class has two constructors. The first constructor is a default constructor. The second constructor is a named constructor. The named constructor is used to initialize the values of the three properties. We also have an object of the class **Student** called **student**.

```dart
class Student {
  String? name;
  int? age;
  int? rollNumber;

  // Default Constructor
  Student() {
    print("This is a default constructor");
  }

  // Named Constructor
  Student.namedConstructor(String name, int age, int rollNumber) {
    this.name = name;
    this.age = age;
    this.rollNumber = rollNumber;
  }
}

void main() {
  // Here student is object of class Student.
  Student student = Student.namedConstructor("John", 20, 1);
  print("Name: ${student.name}");
  print("Age: ${student.age}");
  print("Roll Number: ${student.rollNumber}");
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=f9544bb84b)

{{% expand "Show Output" "false" %}}
````plaintext
This is a default constructor
Name: John
Age: 20
Roll Number: 1
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=d5e6a6ed2ed16d607c3f13adab3a6f6b" style="blue" %}}{{% /button %}}

## Example 2: Named Constructor In Dart
In this example below, there is class **Mobile** with three properties **name**, **color**, and **prize**. The class has one method **display** which prints out the values of the three properties. We also have an object of the class **Mobile** called **mobile**. There is also constructor **Mobile** which takes all the three properties as parameters. Named constructor **Mobile.namedConstructor** is used to create an object of the class **Mobile** with name, color and optional prize. The default value of the prize is 0. If the prize is not passed, then the default value is used.
  
```dart
class Mobile {
  String? name;
  String? color;
  int? prize;

  Mobile(this.name, this.color, this.prize);
  // here Mobile() is a named constructor
  Mobile.namedConstructor(this.name, this.color, [this.prize = 0]);

  void displayMobileDetails() {
    print("Mobile name: $name.");
    print("Mobile color: $color.");
    print("Mobile prize: $prize");
  }
}

void main() {
  var mobile1 = Mobile("Samsung", "Black", 20000);
  mobile1.displayMobileDetails();
  var mobile2 = Mobile.namedConstructor("Apple", "White");
  mobile2.displayMobileDetails();
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=359a4d82c2)

{{% expand "Show Output" "false" %}}
````plaintext
Mobile name: Samsung.
Mobile color: Black.
Mobile prize: 20000
Mobile name: Apple.
Mobile color: White.
Mobile prize: 0
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=47430bb53f4123a0f1aeea87a8123a6a" style="blue" %}}{{% /button %}}
## Example 3: Named Constructor In Dart
In this example below, there is a class **Animal** with two properties **name** and **age**. The class has three constructors. The first constructor is a default constructor. The second and third constructors are named constructors. The second constructor is used to initialize the values of name and age, and the third constructor is used to initialize the value of name only. We also have an object of the class **Animal** called **animal**.

```dart
class Animal {
  String? name;
  int? age;

  // Default Constructor
  Animal() {
    print("This is a default constructor");
  }

  // Named Constructor
  Animal.namedConstructor(String name, int age) {
    this.name = name;
    this.age = age;
  }

  // Named Constructor
  Animal.namedConstructor2(String name) {
    this.name = name;
  }
}
void main(){
  // Here animal is object of class Animal.
  Animal animal = Animal.namedConstructor("Dog", 5);
  print("Name: ${animal.name}");
  print("Age: ${animal.age}");

  Animal animal2 = Animal.namedConstructor2("Cat");
  print("Name: ${animal2.name}");
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=1b6f459385)

{{% expand "Show Output" "false" %}}
````plaintext
Name: Dog
Age: 5
Name: Cat
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=bdba691a58ae10feecda2ca6288d598a" style="blue" %}}{{% /button %}}

## Example 4: Real Life Example Of Named Constructor In Dart
In this example below, there is a class **Person** with two properties **name** and **age**. The class has three constructors. The first is a parameterized constructor which takes two parameters **name** and **age**. The second and third constructors are named constructors. Second constructor fromJson is used to create an object of the class **Person** from a JSON. The third fromJsonString is used to create an object of the class **Person** from a JSON string. We also have an object of the class **Person** called **person**.

```dart
import 'dart:convert';

class Person {
  String? name;
  int? age;

  Person(this.name, this.age);

  Person.fromJson(Map<String, dynamic> json) {
    name = json['name'];
    age = json['age'];
  }

  Person.fromJsonString(String jsonString) {
    Map<String, dynamic> json = jsonDecode(jsonString);
    name = json['name'];
    age = json['age'];
  }
}

void main() {
// Here person is object of class Person.
  String jsonString1 = '{"name": "Bishworaj", "age": 25}';
  String jsonString2 = '{"name": "John", "age": 30}';

  Person p1 = Person.fromJsonString(jsonString1);
  print("Person 1 name: ${p1.name}");
  print("Person 1 age: ${p1.age}");

  Person p2 = Person.fromJsonString(jsonString2);
  print("Person 2 name: ${p2.name}");
  print("Person 2 age: ${p2.age}");
}

```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=115948a934)

{{% expand "Show Output" "false" %}}
````plaintext
Person 1 name: Bishworaj
Person 1 age: 25
Person 2 name: John
Person 2 age: 30
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=6ecf2c4cb154ab86ece31be27bff4f33" style="blue" %}}{{% /button %}}

## Challenge
Try to create a class **Car** with three properties **name**, **color**, and **prize** and one method **display** which prints out the values of the three properties. Create a constructor, which takes all 3 parameters.  Create a named constructor which takes two parameters **name** and **color**. Create an object of the class from both the constructors and call the method **display**.

## Video
Watch our video on default constructor in Dart.
{{< youtube 3-096Ixpa50 >}}