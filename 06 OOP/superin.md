+++
title = "Super in Dart"
weight = 16
description = "In this section, you will learn about Super in Dart programming language, with the help of examples."
keywords = ["dart super", "super in dart", "super in dart programming", "super in dart programming language"]
+++

## Introduction 
In this section, you will learn about Super in Dart programming language with the help of examples. Before learning about Super in Dart, you should have a basic understanding of the [constructor](/object-oriented-programming/constructor-in-dart/) and [inheritance](/object-oriented-programming/inheritance-in-dart/) in Dart.

## What Is Super In Dart?
Super is used to refer to the parent class. It is used to call the parent class's properties and methods.

## Example 1: Super In Dart
In this example below, the **show()** method of the **MacBook** class calls the **show()** method of the parent class using the **super** keyword.
```dart
class Laptop {
  // Method
    void show() {
        print("Laptop show method");
    }
}

class MacBook extends Laptop {
    void show() {
        super.show(); // Calling the show method of the parent class
        print("MacBook show method");
    }
}

void main() {
  // Creating an object of the MacBook class
  MacBook macbook = MacBook();
  macbook.show();
}
```
{{% expand "Show Output" "false" %}}
```plaintext
Laptop show method
MacBook show method
```
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=089ad3670be0ee5bfd0723445959f3e7" style="blue" %}}{{% /button %}}


## Example 2: Accessing Super Properties In Dart
In this example below, the **display()** method of the **Tesla** class calls the **noOfSeats** property of the parent class using the **super** keyword.

```dart
class Car {
  int noOfSeats = 4;
}

class Tesla extends Car {
  int noOfSeats = 6;

  void display() {
    print("No of seats in Tesla: $noOfSeats");
    print("No of seats in Car: ${super.noOfSeats}");
  }
}

void main() {
  var tesla = Tesla();
  tesla.display();
}
```
{{% expand "Show Output" "false" %}}
```plaintext
No of seats in Tesla: 6
No of seats in Car: 4
```
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=e742138b7262d0dfbe443d56ff7d76b7" style="blue" %}}{{% /button %}}


## Example 3: Super With Constructor In Dart
In this example below, the **Manager** class constructor calls the **Employee** class constructor using the **super** keyword.

```dart
class Employee {
  // Constructor
  Employee(String name, double salary) {
    print("Employee constructor");
    print("Name: $name");
    print("Salary: $salary");
  }
}

class Manager extends Employee {
  // Constructor
  Manager(String name, double salary) : super(name, salary) {
    print("Manager constructor");
  }
}

void main() {
  Manager manager = Manager("John", 25000.0);
}
```
{{% expand "Show Output" "false" %}}
```plaintext
Employee constructor
Name: John
Salary: 25000.0
Manager constructor
```
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=01fc4d4ec548f1a867cee6ad25c923e8" style="blue" %}}{{% /button %}}

## Example 4: Super With Named Constructor In Dart
In this example below, the **Manager** class named constructor calls the **Employee** class named constructor using the **super** keyword.

```dart
class Employee {
  // Named constructor
  Employee.manager() {
    print("Employee named constructor");
  }
}

class Manager extends Employee {
  // Named constructor
  Manager.manager() : super.manager() {
    print("Manager named constructor");
  }
}

void main() {
  Manager manager = Manager.manager();
}
```




{{% expand "Show Output" "false" %}}
```plaintext
Employee named constructor
Manager named constructor
```
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=1bbe00ebed80ee7464cd87221b77d364" style="blue" %}}{{% /button %}}


## Example 5: Super With Multilevel Inheritance In Dart
In this example below, the **MacBookPro** class method **display** calls the **display** method of the parent class **MacBook** using the **super** keyword. The **MacBook** class method **display** calls the **display** method of the parent class **Laptop** using the **super** keyword.

```dart
class Laptop {
  // Method
  void display() {
    print("Laptop display");
  }
}

class MacBook extends Laptop {
  // Method
  void display() {
    print("MacBook display");
    super.display();
  }
}

class MacBookPro extends MacBook {
  // Method
  void display() {
    print("MacBookPro display");
    super.display();
  }
}

void main() {
  var macbookpro = MacBookPro();
  macbookpro.display();
}
```



{{% expand "Show Output" "false" %}}
```plaintext
MacBookPro display
MacBook display
Laptop display
```
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=a3628ad408cab1ff1e2c8578aeb8ff14" style="blue" %}}{{% /button %}}

## Key Points To Remember
- The **super** keyword is used to access the parent class members.
- The **super** keyword is used to call the method of the parent class.

## Video
Watch our video on super in Dart.
{{< youtube dMC1B1ljZV4 >}}