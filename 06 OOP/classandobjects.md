+++
title = "Class and Objects in Dart"
weight = 4
+++
## What is Class


A class is a blueprint for creating objects. A class defines the properties and methods that an object will have. If you want to learn more about class in Dart, you can read [class in dart](/object-oriented-programming/class-in-dart/).


## What is Object
An object is an instance of a class. You can create multiple objects of the same class. If you want to learn more about an object in Dart, you can read [object in dart](/object-oriented-programming/object-in-dart/).


## Example Of A Class & Object In Dart
In this example below there is class **Animal** with three properties: **name**, **numberOfLegs**, and **lifeSpan**. The class also has a method called **display**, which prints out the values of the three properties.

```dart
class Animal {
  String? name;
  int? numberOfLegs;
  int? lifeSpan;

  void display() {
    print("Animal name: $name.");
    print("Number of Legs: $numberOfLegs.");
    print("Life Span: $lifeSpan.");
  }
}

void main(){
  // Here animal is object of class Animal. 
  Animal animal = Animal();
  animal.name = "Lion";
  animal.numberOfLegs = 4;
  animal.lifeSpan = 10;
  animal.display();
}
```


{{% expand "Show Output" "false" %}}
````plaintext
Animal name: Lion.
Number of Legs: 4.
Life Span: 10.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=6790148500eb3c6c8004609c5904dd9d" style="blue" %}}{{% /button %}}


## Example 2: Find Area Of Ractangle Using Class and Objects
In this example below there is class **Rectangle** with two properties: **length** and **breadth**. The class also has a method called **area**, which calculates the area of the rectangle.

```dart
class Rectangle{
  //properties of rectangle
  double? length;
  double? breadth;
  
  //functions of rectangle
  double area(){
    return length! * breadth!;
  }
}

void main(){
  //object of rectangle created
  Rectangle rectangle = Rectangle();
  
  //setting properties for rectangle
  rectangle.length=10;
  rectangle.breadth=5;
  
  //functions of rectangle called
  print("Area of rectangle is ${rectangle.area()}.");
}
```



{{% expand "Show Output" "false" %}}
````plaintext
Area of rectangle is 50.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=8617b7c594d4a18fdb658a89b896d820" style="blue" %}}{{% /button %}}



{{% notice info %}}
**Note**:  Here **!** is used to tell the compiler that the variable is not null. If you don't use **!**, then you will get an error. You will learn more about it in [null safety](/null-safety/) later.
{{% /notice %}}


## Example 3: Find Simple Interest Using Class and Objects
In this example below there is class **SimpleInterest** with three properties: **principal**, **rate**, and **time**. The class also has a method called **interest**, which calculates the simple interest.

```dart
class SimpleInterest{
  //properties of simple interest
  double? principal;
  double? rate;
  double? time;
  
  //functions of simple interest
  double interest(){
    return (principal! * rate! * time!)/100;
  }
}
void main(){
  //object of simple interest created
  SimpleInterest simpleInterest = SimpleInterest();
  
  //setting properties for simple interest
  simpleInterest.principal=1000;
  simpleInterest.rate=10;
  simpleInterest.time=2;
  
  //functions of simple interest called
  print("Simple Interest is ${simpleInterest.interest()}.");
}
```



{{% expand "Show Output" "false" %}}
````plaintext
Simple Interest is 200.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=f83769f0cc599b7364318f00fc66dea9" style="blue" %}}{{% /button %}}


## Challenge
Create class Home with properties **name**, **address**, **numberOfRooms**. Create a method called **display** which prints out the values of the properties. Create an object of the class **Home** and set the values of the properties. Call the method **display** to print out the values of the properties.
