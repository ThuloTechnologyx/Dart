+++
title = "Factory Constructor in Dart"
weight = 23
keywords = ["dart factory constructor", "factory constructor in dart", "factory constructor in dart programming", "factory constructor in dart programming language"]
description = "In this section, you will learn about factory constructors in Dart programming language. You will learn about the factory constructor, its properties, and its methods."
+++
## Introduction
In this section, you will learn about factory constructors with examples. Before learning about factory constructors, you should have a basic understanding of [class and objects](/object-oriented-programming/class-and-objects-in-dart/), [constructor](/object-oriented-programming/constructor-in-dart/), [abstract class](/object-oriented-programming/abstract-class-in-dart/), [interface](/object-oriented-programming/interface-in-dart/) and [inheritance](/object-oriented-programming/inheritance-in-dart/) in Dart.

## Factory Constructor In Dart
[![targets](/images/pieces/note-banner.png)](https://pieces.app/?utm_source=dart-tutorial&utm_medium=banner&utm_campaign=dart-tutorial-website&utm_content=note)
All of the constructors that you have learned until now are **generative constructors**. Dart also provides a special type of constructor called a **factory constructor**. 

A **factory constructor** gives more flexibility to create an object. Generative constructors only create an instance of the class. But, the factory constructor can return an instance of the **class or even subclass**. It is also used to return the **cached instance** of the class.

## Syntax
```dart
class ClassName {
  factory ClassName() {
    // TODO: return ClassName instance
  }

  factory ClassName.namedConstructor() {
    // TODO: return ClassName instance
  }
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=d70b4b9737)

## Rules For Factory Constructors
- Factory constructor must return an instance of the **class** or **sub-class**.
- You can't use **this** keyword inside factory constructor.
- It can be **named** or **unnamed** and called like normal constructor.
- It can't access **instance members** of the class. 

## Example 1: Without Factory Constructor 
In this example below, there is a class named **Area** with final properties **length** and **breadth**, and **area**. When you pass the **length** and **breadth** to the constructor, it calculates the **area** and stores it in the **area** property.

{{% notice info %}}
**Note**: An initializer list allows you to assign properties to a new instance variable before the constructor body runs, but after creation. 
{{% /notice %}}

```dart
class Area {
  final int length;
  final int breadth;
  final int area;

  // Initializer list 
 const Area(this.length, this.breadth) : area = length * breadth;
}

void main() {
  Area area = Area(10, 20);
  print("Area is: ${area.area}");

  // notice that here is a negative value
  Area area2 = Area(-10, 20);
  print("Area is: ${area2.area}");
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=ebdc40bcd4)

{{% expand "Show Output" "false" %}}
````plaintext
Area is: 200
Area is: -200
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=585680686a8077f88a4cccae5b4f8fa1" style="blue" %}}{{% /button %}}

Here **area2** object has a negative value. This is because we are not validating the input. Let's create a factory constructor to validate the input.

## Example 2: With Factory Constructor
In this example below, **factory constructor** is used to validate the input. If the input is valid, it will return a new class instance. If the input is invalid, then it will throw an exception. 

```dart
class Area {
  final int length;
  final int breadth;
  final int area;

  // private constructor
  const Area._internal(this.length, this.breadth) : area = length * breadth;

  // Factory constructor
  factory Area(int length, int breadth) {
    if (length < 0 || breadth < 0) {
      throw Exception("Length and breadth must be positive");
    }
    // redirect to private constructor
    return Area._internal(length, breadth);
  }
}

void main() {
  // This works
  Area area = Area(10, 20);
  print("Area is: ${area.area}");

  // notice that here is negative value
  Area area2 = Area(-10, 20);
  print("Area is: ${area2.area}");
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=72864dbd82)

{{% expand "Show Output" "false" %}}
````plaintext
Area is: 200
Unhandled exception:
Exception: Length and breadth must be positive
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=873d3da7cde74b237d63f39b2c54d63f" style="blue" %}}{{% /button %}}

{{% notice info %}}
**Note**: With a factory constructor, you can initialize a final variable using logic that can't be handled in the initializer list.
{{% /notice %}}

## Example 3: Factory Constructor In Dart
In this example below, there is a class named **Person** with two properties, **firstName** and **lastName**, and two constructors, a **normal constructor** and a **factory constructor**. The factory constructor creates a Person object from a [**Map**](/collections/map-in-dart/).
```dart
class Person {
  String firstName;
  String lastName;

  // constructor
  Person(this.firstName, this.lastName);

  // factory constructor Person.fromMap
  factory Person.fromMap(Map<String, Object> map) {
    final firstName = map['firstName'] as String;
    final lastName = map['lastName'] as String;
    return Person(firstName, lastName);
  }
}

void main() {
  // create a person object
  final person = Person('John', 'Doe');

  // create a person object from map
  final person2 = Person.fromMap({'firstName': 'Harry', 'lastName': 'Potter'});

  // print first and last name
  print("From normal constructor: ${person.firstName} ${person.lastName}");
  print("From factory constructor: ${person2.firstName} ${person2.lastName}");
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=94bc4e924e)

In the main method, two objects are created, one using the **generative/normal constructor** and the other using the **factory constructor**. 

{{% expand "Show Output" "false" %}}
````plaintext
From normal constructor: John Doe
From factory constructor: Harry Potter
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=aa31b7d6b3ba89641c72e2d61c9ec0a8" style="blue" %}}{{% /button %}}

## Example 4: Factory Constructor In Dart
In this example below, there is [**enum**](/object-oriented-programming/enum-in-dart/) **ShapeType** with two values: **circle** and **rectangle**. There is an [**interface**](/object-oriented-programming/interface-in-dart/) **Shape** with a factory constructor that creates objects of type Shape, either Circle or Rectangle. The **main** method instantiates two objects, one of each type, and calls the **draw()** method on each.

```dart
// enum ShapeType
enum ShapeType { circle, rectangle }

// abstract class Shape
abstract class Shape {
  // factory constructor
  factory Shape(ShapeType type) {
    switch (type) {
      case ShapeType.circle:
        return Circle();
      case ShapeType.rectangle:
        return Rectangle();
      default:
        throw 'Invalid shape type';
    }
  }
  // method
  void draw();
}

class Circle implements Shape {
  // implement draw method
  @override
  void draw() {
    print('Drawing circle');
  }
}

class Rectangle implements Shape {
  // implement draw method
  @override
  void draw() {
    print('Drawing rectangle');
  }
}

void main() {
  // create Shape object
  Shape shape = Shape(ShapeType.circle);
  Shape shape2 = Shape(ShapeType.rectangle);
  shape.draw();
  shape2.draw();
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=7e3f46b82c)

{{% expand "Show Output" "false" %}}
````plaintext
Drawing circle
Drawing rectangle
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=2c9e5109815d6810af34dbc0e82fc2a5" style="blue" %}}{{% /button %}}

{{% notice info %}}
**Note**: Here it is possible to make **List<Shape>** which contains both **Circle** and **Rectangle** objects in it.
{{% /notice %}}

## Example 5: Factory Constructor In Dart
In this example below, there is class **Person** with a final field **name**. It also has a private constructor and a static **_cache** field. The class also has a **factory constructor** that checks if the **_cache** field contains a key that matches the name parameter. If it does, it returns the Person object associated with that key. Otherwise, it creates a new **Person** object, adds it to the **_cache**, and returns it.

```dart
class Person {
  // final fields
  final String name;

  // private constructor
  Person._internal(this.name);

  // static _cache field
  static final Map<String, Person> _cache = <String, Person>{};

  // factory constructor
  factory Person(String name) {
    if (_cache.containsKey(name)) {
      return _cache[name]!;
    } else {
      final person = Person._internal(name);
      _cache[name] = person;
      return person;
    }
  }
}

void main() {
  final person1 = Person('John');
  final person2 = Person('Harry');
  final person3 = Person('John');

  // hashcode of person1 and person3 are same
  print("Person1 name is : ${person1.name} with hashcode ${person1.hashCode}");
  print("Person2 name is : ${person2.name} with hashcode ${person2.hashCode}");
  print("Person3 name is : ${person3.name} with hashcode ${person3.hashCode}");
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=2ce4409163)

{{% expand "Show Output" "false" %}}
````plaintext
Person1 name is : John with hashcode 117
Person2 name is : Harry with hashcode 118
Person3 name is : John with hashcode 117
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=d8922d8720f238a5346c6c1b61d9e27f" style="blue" %}}{{% /button %}}

## Singleton In Dart
Singletons are a common design pattern in object-oriented programming. A singleton class can have only one instance and provides a global point of access to it. You can create a singleton in Dart by defining a **factory constructor** that always returns the same instance. It is mostly useful when you want to create a single instance of a class and use it throughout the application like **database connection app**.
 
## Example 6: Singleton Using Factory Constructor
This code creates a **Singleton** class that can only be instantiated once, and provides a factory constructor to get the instance of the class. The main method creates two objects of the Singleton class, and prints the hashcode of the objects to verify that **they are same**.
```dart
// Singleton using dart factory
class Singleton {
 // static variable
 static final Singleton _instance = Singleton._internal();
 
// factory constructor
 factory Singleton() {
   return _instance;
 }
 // private constructor 
 Singleton._internal();
}
 
void main() {
 Singleton obj1 = Singleton();
 Singleton obj2 = Singleton();
 print(obj1.hashCode);
 print(obj2.hashCode);
}
 
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=babd45ae7c)

{{% expand "Show Output" "false" %}}
````plaintext
2147483648
2147483648
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=c62b923bfe3f42cc1b92c7c2d42752b4" style="blue" %}}{{% /button %}}

You can see that both objects have the same hashcode. This is because both objects are pointing to the same instance.

{{% notice info %}}
**Note**: Here Singleton._internal() is a private constructor so that it can not be called from outside the library. The factory constructor is used to return the same instance of the class.
{{% /notice %}}

## Key Points
Here **It** means **factory constructor**
- It uses the **factory** keyword to define a factory constructor.
- It returns an instance of the same class or sub-class. 
- It is used to implement factory design patterns. [Return sub-class instance based on input parameter as shown in example 4]
- It is used to implement singleton design patterns. [Return the same instance every time]
- It is used to initialize a final variable using logic that can't be handled in the initializer list.

## Question For Practice
Create an interface called **Bottle** and add a method to it called **open()**. Create a class called **CokeBottle** and implement the Bottle and print the message **"Coke bottle is opened"**. Add a factory constructor to **Bottle** and return the object of **CokeBottle**. Instantiate **CokeBottle** using the factory constructor and call the **open()** on the object.
