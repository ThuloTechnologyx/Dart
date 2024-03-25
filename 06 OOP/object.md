+++
title = "Object in Dart"
weight = 3
description = "In this section, you will learn about the object in Dart programming language. You will learn about the object, its properties, and its methods."
keywords = "dart object, object in dart, oop object in dart, object oriented programming object in dart, dart oops"
+++
## Object In Dart
**In object-oriented programming**, an object is a self-contained unit of code and data. Objects are created from templates called classes. An object is made up of properties(variables) and methods(functions). An object is an instance of a class.

**For example**, a bicycle object might have attributes like color, size, and current speed. It might have methods like changeGear, pedalFaster, and brake.

{{% notice info %}}
**Note**: To create an object, you must create a class first. It's a good practice to declare the object name in lower case.
{{% /notice %}}


## Instantiation
In object-oriented programming, instantiation is the process of creating an instance of a class. In other words, you can say that instantiation is the process of creating an object of a class. For example, if you have a class called **Bicycle**, then you can create an object of the class called **bicycle**.

## Declaring Object In Dart
Once you have created a class, it's time to declare the object. You can declare an object by the following syntax: 

## Syntax

```dart
ClassName objectName = ClassName();
```

## Example 1: Declaring An Object In Dart
In this example below, there is class **Bycycle** with three properties: **color**, **size**, and **currentSpeed**. The class has two methods. One is **changeGear**, which changes the gear of the bicycle, and **display** method prints out the values of the three properties. We also have an object of the class **Bycycle** called **bicycle**.

```dart
    class Bicycle {
      String? color;
      int? size;
      int? currentSpeed;
    
      void changeGear(int newValue) {
        currentSpeed = newValue;
      }
    
      void display() {
        print("Color: $color");
        print("Size: $size");
        print("Current Speed: $currentSpeed");
      }
    }

    void main(){
        // Here bicycle is object of class Bicycle. 
        Bicycle bicycle = Bicycle();
        bicycle.color = "Red";
        bicycle.size = 26;
        bicycle.currentSpeed = 0;
        bicycle.changeGear(5);
        bicycle.display();
    }
```    
{{% expand "Show Output" "false" %}}
````plaintext
Color: Red
Size: 26
Current Speed: 5
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=ac6ab46115153304cc99e2054c93cc17" style="blue" %}}{{% /button %}}

{{% notice info %}}
**Note**:  Once you create an object, you can access the properties and methods of the object using the dot(.) operator.
{{% /notice %}}

## Example 2: Declaring Animal Class Object In Dart
In this example below there is class **Animal** with three properties: **name**, **numberOfLegs**, and **lifeSpan**. The class also has a method called **display**, which prints out the values of the three properties. We also have an object of the class **Animal** called **animal**.    

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
{{% button href="https://dartpad.dev/?id=98521faeb62ecddd3b85bb7e36ac4893" style="blue" %}}{{% /button %}}


## Example 3: Declaring Car Class Object In Dart
In this example below there is class **Car** with three properties: **name**, **color**, and **numberOfSeats**. The class also has a method called **start**, which prints out the message "Car Started". We also have an object of the class **Car** called **car**.
    
```dart
    class Car {
      String? name;
      String? color;
      int? numberOfSeats;
    
      void start() {
        print("$name Car Started.");
      }
    }

    void main(){
        // Here car is object of class Car. 
        Car car = Car();
        car.name = "BMW";
        car.color = "Red";
        car.numberOfSeats = 4;
        car.start();

        // Here car2 is another object of class Car.
        Car car2 = Car();
        car2.name = "Audi";
        car2.color = "Black";
        car2.numberOfSeats = 4;
        car2.start();
    }
```    
{{% expand "Show Output" "false" %}}
````plaintext
BMW Car Started.
Audi Car Started.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=249f536b52056a86fc82520a97797ad7" style="blue" %}}{{% /button %}}

## Key Points
- The main method is the program's entry point, so it is always needed to see the result.
- The **new** keyword can be used to create a new object, but it is unnecessary.

## Challenge
Create a class Camera with properties: **name**, **color**, **megapixel**. Create a method called **display** which prints out the values of the three properties. Create two objects of the class Camera and call the method display.

## Video
Watch our video on parameterized constructor in Dart.
{{< youtube gFliT0oeddo >}}
