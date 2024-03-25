+++
title = "Setter in Dart"
weight = 12
description = "Setter is a method that is used to update the value of a private property. Setter in Dart is used to update the value of a private property. Setter in Dart is also used to restrict the access of data members of a class."
keywords = ["setter", "setter in dart", "setter in dart programming", "setter in dart programming language"]
+++

## Setter In Dart
**Setter** is used to set the value of a property. It is mostly used to update a **private property's** value. Setter provide explicit write access to an object properties.

## Syntax
```dart
set property_name (value) {
  // Setter body
}
```

{{% notice info %}}
**Note:** Instead of writing { } after the property name, you can also write **=>** (fat arrow) after the property name.
{{% /notice %}}

## Example 1: Setter In Dart
In this example below, there is a class named **NoteBook**. The class has two private properties **_name** and **_prize**. There are two setters **name** and **prize** to update the value of the properties. There is also a method **display** to display the value of the properties.

```dart
class NoteBook {
  // Private Properties
  String? _name;
  double? _prize;

  // Setter to update private property _name
  set name(String name) => this._name = name;

  // Setter to update private property _prize
  set prize(double prize) => this._prize = prize;

  // Method to display the values of the properties
  void display() {
    print("Name: ${_name}");
    print("Price: ${_prize}");
  }
}

void main() {
  // Create an object of NoteBook class
  NoteBook nb = new NoteBook();
  // setting values to the object using setter
  nb.name = "Dell";
  nb.prize = 500.00;
  // Display the values of the object
  nb.display();
}
```
    
{{% expand "Show Output" "false" %}}
````plaintext
Name: Dell
Price: 500.0
````
{{% /expand %}}    
{{% button href="https://dartpad.dev/?id=18a42e026ec7d75665059143aabdb47e" style="blue" %}}{{% /button %}}   


{{% notice info %}}
**Note:** In the above example, a setter  **name** and **prize** are used to update the value of the properties **_name** and **_prize**. 
{{% /notice %}}


## Example 2: Setter In Dart With Data Validation
In this example, there is a class named **NoteBook**. The class has two private properties **_name** and **_prize**. If the value of **_prize** is less than 0, we will throw an exception. There are also two setters **name** and **prize** to update the value of the properties. The class also has a method **display()** to display the values of the properties.

```dart
class NoteBook {
  // Private properties
  String? _name;
  double? _prize;

  // Setter to update the value of name property
  set name(String name) => _name = name;

  // Setter to update the value of prize property
  set prize(double prize) {
    if (prize < 0) {
      throw Exception("Price cannot be less than 0");
    }
    this._prize = prize;
  }

  // Method to display the values of the properties
  void display() {
    print("Name: $_name");
    print("Price: $_prize");
  }
}

void main() {
  // Create an object of NoteBook class
  NoteBook nb = new NoteBook();
  // setting values to the object using setter
  nb.name = "Dell";
  nb.prize = 250;

  // Display the values of the object
  nb.display();
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Name: Dell
Price: 500.0
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=142623e9802c21916b61bcd2b1445f62" style="blue" %}}{{% /button %}}   

{{% notice info %}}
**Note**: It is generally best to not allow the user to set the value of a field directly. Instead, you should provide a setter method that can validate the value before setting it. This is very important when working on large and complex programs.
{{% /notice %}}

## Example 3: Setter In Dart 
In this example, there is a class named **Student**. The class has two private properties **_name** and **_classnumber**. We will also create two setters **name** and **classnumber** to update the value of the properties. The **classnumber** setter will only accept a value between 1 and 12. The class also has a method **display()** to display the values of the properties.

```dart
class Student {
  // Private properties
  String? _name;
  int? _classnumber;

  // Setter to update the value of name property
  set name(String name) => this._name = name;

  // Setter to update the value of classnumber property
  set classnumber(int classnumber) {
    if (classnumber <= 0 || classnumber > 12) {
      throw ('Classnumber must be between 1 and 12');
    }
    this._classnumber = classnumber;
  }

  // Method to display the values of the properties
  void display() {
    print("Name: $_name");
    print("Class Number: $_classnumber");
  }
}
void main() {
  // Create an object of Student class
  Student s = new Student();
  // setting values to the object using setter
  s.name = "John Doe";
  s.classnumber = 12;

  // Display the values of the object
  s.display();

  // This will generate error
  //s.setClassNumber(13);
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Name: John
Class Number: 10
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=4a6112fd2bef9da8c7642ae31c19a8f9" style="blue" %}}{{% /button %}}   


## Why Is Setter Important?
- It is used to set the value of a private property.
- It is also used for data validation.
- It gives you better control over the data.

## Video
Watch our video on setters in Dart.
{{< youtube j4PwccC77Y4 >}}

## Challenge
Try to create a class named **University** with two private properties **_name** and **_year**. The class will also have two setters **name** and **year** to update the value of the properties. The **year** setter will only accept a value between 1900 and 2023. Also, create a method **display()** to display the values of the properties.
