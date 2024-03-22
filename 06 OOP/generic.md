+++
title = "Generic in Dart"
weight = 24
description = "In this tutorial, you will learn about dart Generics, how to create generics class and methods with examples."
keywords = ["generics", "dart", "dart tutorial", "dart generics"]
+++

### Introduction
This tutorial will teach you about dart Generics, how to create generics classes and methods with examples.

### Generics In Dart
**Generics** is a way to create a class, or function that can work with different types of data **(objects)**. If you look at the internal implementation of [**List**](/collections/list-in-dart/) class, it is a generic class. It can work with different data types like int, String, double, etc. For example, **List\<int\>** is a list of integers, **List\<String\>** is a list of strings, and **List\<double\>**  is a list of double values.

### Syntax
```dart
class ClassName<T> {
  // code
}
```
### Example 1: Without Using Generics
Suppose, you need to create a class that can work with both **int** and **double** data types. You can create two classes, one for **int** and another for **double** like this:

```dart
// Without Generics
// Creating a class for int
class IntData {
  int data;
  IntData(this.data);
}
// Creating a class for double
class DoubleData {
  double data;
  DoubleData(this.data);
}

void main() {
  // Create an object of IntData class
  IntData intData = IntData(10);
  DoubleData doubleData = DoubleData(10.5);
  // Print the data
  print("IntData: ${intData.data}");
  print("DoubleData: ${doubleData.data}");
}
```
{{% expand "Show Output" "false" %}}
````plaintext
IntData: 10
DoubleData: 10.5
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=" style="blue" %}}Run Online{{% /button %}}

This is not a good practice because both class contain same code. You can create one **Generics** class that can work with different data types. See the example below.

### Example 2: Using Generics
In this example below, there is single class that can work with **int**, **double**, and any other data types using **Generics**. 

```dart
// Using Generics
class Data<T> {
  T data;
  Data(this.data);
}

void main() {
  // create an object of type int and double
  Data<int> intData = Data<int>(10);
  Data<double> doubleData = Data<double>(10.5);

  // print the data
  print("IntData: ${intData.data}");
  print("DoubleData: ${doubleData.data}");
}
```
{{% expand "Show Output" "false" %}}
````plaintext
IntData: 10
DoubleData: 10.5
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=" style="blue" %}}Run Online{{% /button %}}

### Generics Type Variable
Generics type variables are used to define the type of data that can be used with the class. In the above example, **T** is a type variable. You can use any name for the type variable. A few typical names are **T**, **E**, **K**, and **V**.

|  Name |  Work 
| ----------- | --------- |
|  T |  Type  |
|  E |  Element  |
|  K |  Key  |
|  V |  Value  |


### Dart Map Class
Like [**List**](/collections/list-in-dart/), internal implementation of [**Map**](/collections/map-in-dart/) work with different types of data like int, String, double, etc. This is because Map is a generic class.

```dart
// Dart implementation of Map class
abstract class Map<K, V> {
  // code
  external factory Map();
}
```
This simply means that the Map class can work with different types of data. 
```dart
void main() {
  final info = {
    "name": "John",
    "age": 20,
    "height": 5.5,
  }
}
```


### Generics Methods
You can also create a generic method. For this, you need to use the **\<T\>** keyword before the method's return type. See the example below.

```dart
// Define generic method
T genericMethod<T>(T value) {
  return value;
}

void main() {
  // call the generic method
  print("Int: ${genericMethod<int>(10)}");
  print("Double: ${genericMethod<double>(10.5)}");
  print("String: ${genericMethod<String>("Hello")}");
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Int: 10
Double: 10.5
String: Hello
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=" style="blue" %}}Run Online{{% /button %}}

### Example 3: Generic Method With Multiple Parameters
In this example below, you will learn to create a generic method with multiple parameters.
```dart
// Define generic method
T genericMethod<T, U>(T value1, U value2) {
  return value1;
}

void main() {
  // call the generic method
  print(genericMethod<int, String>(10, "Hello"));
  print(genericMethod<String, int>("Hello", 10));
}
```
{{% expand "Show Output" "false" %}}
````plaintext
10
Hello
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=" style="blue" %}}Run Online{{% /button %}}


### Restricting the Type of Data
While implementing generics, you can restrict the type of data that can be used with the class or method. This is done by using the **extends** keyword. See the example below.

### Example 4: Generic Class With Restriction
In this example below, there is a **Data** class that works only with **int** and **double** types. It will not work with other types..

```dart
// Define generic class with bounded type
class Data<T extends num> {
  T data;
  Data(this.data);
}

void main() {
  // create an object of type int and double
  Data<int> intData = Data<int>(10);
  Data<double> doubleData = Data<double>(10.5);
  // print the data
  print("IntData: ${intData.data}");
  print("DoubleData: ${doubleData.data}");
  // Not Possible
  // Data<String> stringData = Data<String>("Hello");
}
```
{{% expand "Show Output" "false" %}}
````plaintext
IntData: 10
DoubleData: 10.5
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=" style="blue" %}}Run Online{{% /button %}}


### Example 5: Generic Method With Restriction
In this example below, a generic method **getAverage** takes two parameters of Type **T**, which is considered a **num**. The method returns the average of the two parameters.
```dart
// Define generic method
double getAverage<T extends num>(T value1, T value2) {
  return (value1 + value2) / 2;
}

void main() {
  // call the generic method
  print("Average of int: ${getAverage<int>(10, 20)}");
  print("Average of double: ${getAverage<double>(10.5, 20.5)}");
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Average of int: 15
Average of double: 15.5
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=" style="blue" %}}Run Online{{% /button %}}

### Example 6: Generic Class In Dart
In this example below, there is an abstract class **Shape** with one abstract method called area which returns a double. Also there are two classes that implement Shape, **Circle** and **Rectangle**. There is class **Region** which takes a list of Shape objects and has a method called totalArea which returns the sum of the areas of all the shapes in the list.

```dart
// abstract class Shape
abstract class Shape {
  // abstract method area
  double get area;
}

// class Circle which implements Shape
class Circle implements Shape {
  // field radius
  final double radius;
  // constructor
  Circle(this.radius);

  // implementation of area method
  @override
  double get area => 3.14 * radius * radius;
}
// class Rectangle which implements Shape
class Rectangle implements Shape {
  // fields width and height
  final double width;
  final double height;
  // constructor
  Rectangle(this.width, this.height);

  // implementation of area method
  @override
  double get area => width * height;
}

// Generic class Region
class Region<T extends Shape> {
  // field shapes
  List<T> shapes;
  // constructor
  Region({required this.shapes});

  // method totalArea
  double get totalArea {
    double total = 0;
    shapes.forEach((shape) {
      total += shape.area;
    });
    return total;
  }
}

void main() {
  // create objects of Circle and Rectangle
  var circle = Circle(10);
  var rectangle = Rectangle(10, 20);
  // create a list of Shape objects
  var region = Region(shapes: [circle, rectangle]);
  // print the total area
  print("Total Area of Region: ${region.totalArea}");
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Total Area of Region: 514
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=" style="blue" %}}Run Online{{% /button %}}

### Advantages of Generics
- It solve the problem of type safety.
- It helps to reuse our code.

### Video
Watch our video on generics in Dart.
{{< youtube Te6M8gVqKv4 >}}
