+++
title = "Inheritance Of Constructor in Dart"
weight = 15
description = "In this section, you will learn about inheritance of constructor in Dart programming language with the help of examples."
keywords = ["dart inheritance of constructor", "inheritance of constructor in dart", "inheritance of constructor in dart programming", "inheritance of constructor in dart programming language"]
+++

### Introduction
In this section, you will learn about inheritance of constructor in Dart programming language with the help of examples. Before learning about  inheritance of constructor in Dart, you should have a basic understanding of the [constructor](/object-oriented-programming/constructor-in-dart/) and [inheritance](/object-oriented-programming/inheritance-in-dart/) in Dart.


### What Is Inheritance Of Constructor In Dart?
Inheritance of constructor in Dart is a process of inheriting the constructor of the parent class to the child class. It is a way of reusing the code of the parent class. 

### Example 1: Inheritance Of Constructor In Dart
In this example below, there is class named **Laptop** with a constructor. There is another class named **MacBook** which extends the **Laptop** class. The **MacBook** class has its own constructor. 

```dart
class Laptop {
  // Constructor
  Laptop() {
    print("Laptop constructor");
  }
}

class MacBook extends Laptop {
  // Constructor
  MacBook() {
    print("MacBook constructor");
  }
}

void main() {
  var macbook = MacBook();
}
```

{{% expand "Show Output" "false" %}}
```plaintext
Laptop constructor
MacBook constructor
```
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=df0a9d21ff6110772957e2231c4ea1fa" style="blue" %}}Run Online{{% /button %}}

{{% notice info %}}
**Note**:  The constructor of the parent class is called first and then the constructor of the child class is called.
{{% /notice %}}


### Example 2: Inheritance Of Constructor With Parameters In Dart
In this example below, there is class named **Laptop** with a constructor with parameters. There is another class named **MacBook** which extends the **Laptop** class. The **MacBook** class has its own constructor with parameters. 

```dart
class Laptop {
  // Constructor
  Laptop(String name, String color) {
    print("Laptop constructor");
    print("Name: $name");
    print("Color: $color");
  }
}

class MacBook extends Laptop {
  // Constructor
  MacBook(String name, String color) : super(name, color) {
    print("MacBook constructor");
  }
}

void main() {
  var macbook = MacBook("MacBook Pro", "Silver");
}
```

{{% expand "Show Output" "false" %}}
```plaintext
Laptop constructor
Name: MacBook Pro
Color: Silver
MacBook constructor
```
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=8c31d256bbd5e4be3b9d6b15d103c2f0" style="blue" %}}Run Online{{% /button %}}

### Example 3: Inheritance Of Constructor 
In this example below, there is class named **Person** with properties **name** and **age**. There is another class named **Student** which extends the **Person** class. The **Student** class has additional property **rollNumber**. Lets see how to create a constructor for the **Student** class.
```dart
class Person {
  String name;
  int age;

  // Constructor
  Person(this.name, this.age);
}

class Student extends Person {
  int rollNumber;

  // Constructor
  Student(String name, int age, this.rollNumber) : super(name, age);
}

void main() {
  var student = Student("John", 20, 1);
  print("Student name: ${student.name}");
  print("Student age: ${student.age}");
  print("Student roll number: ${student.rollNumber}");

}
```
{{% expand "Show Output" "false" %}}
```plaintext    
Student name: John
Student age: 20
Student roll number: 1
```
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=fc8150b7266abffd600d331858c3f832" style="blue" %}}Run Online{{% /button %}}


### Example 4: Inheritance Of Constructor With Named Parameters In Dart
In this example below, there is class named **Laptop** with a constructor with named parameters. There is another class named **MacBook** which extends the **Laptop** class. The **MacBook** class has its own constructor with named parameters. 

```dart
class Laptop {
  // Constructor
  Laptop({String name, String color}) {
    print("Laptop constructor");
    print("Name: $name");
    print("Color: $color");
  }
}

class MacBook extends Laptop {
  // Constructor
  MacBook({String name, String color}) : super(name: name, color: color) {
    print("MacBook constructor");
  }
}

void main() {
  var macbook = MacBook(name: "MacBook Pro", color: "Silver");
}
```

{{% expand "Show Output" "false" %}}
```plaintext
Laptop constructor
Name: MacBook Pro
Color: Silver
MacBook constructor
```
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=8cf330e2e7d3d23a3b01cd0b9318e8c2" style="blue" %}}Run Online{{% /button %}}

### Example 5: Calling Named Constructor Of Parent Class In Dart
In this example below, there is class named **Laptop** with one default constructor and one named constructor. There is another class named **MacBook** which extends the **Laptop** class. The **MacBook** class has its own constructor with named parameters. You can call the named constructor of the parent class using the **super** keyword.

```dart
class Laptop {
  // Default Constructor
  Laptop() {
    print("Laptop constructor");
  }

  // Named Constructor
  Laptop.named() {
    print("Laptop named constructor");
  }
}

class MacBook extends Laptop {
  // Constructor
  MacBook() : super.named() {
    print("MacBook constructor");
  }
}

void main() {
  var macbook = MacBook();
}
```

{{% expand "Show Output" "false" %}}
```plaintext
Laptop named constructor
MacBook constructor
```
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=be8b62849068c4ae5e24cca8dee0bd3b" style="blue" %}}Run Online{{% /button %}}

### Video
Watch our video on inheritance of constructor in Dart.
{{< youtube 7vwpgQ04k8o >}}