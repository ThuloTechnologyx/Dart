+++
title = "Mixin in Dart"
weight = 22
description = "A mixin is a class that contains methods for use by other classes without having to be the parent class of those other classes. A mixin is declared using the keyword mixin followed by the mixin name."
keywords = ["mixin", "mixin in dart", "mixin in dart programming", "mixin in dart programming language"]
+++

## Introduction
In this section, you will learn about **dart mixins** to reuse the code in multiple classes. Before learning about mixins you should have a basic understanding of **[class](/object-oriented-programming/class-in-dart/)**, **[object](/object-oriented-programming/object-in-dart/)**, **[constructor](/object-oriented-programming/constructor-in-dart/)**, and **[inheritance](/object-oriented-programming/inheritance-in-dart/)**.

## Mixin In Dart
Mixins are a way of reusing the code in multiple classes. Mixins are declared using the keyword **mixin** followed by the mixin name. Three keywords are used while working with mixins: **mixin**, **with**, and **on**. It is possible to use multiple mixins in a class.


{{% notice info %}}
**Note:** The **with** keyword is used to apply the mixin to the class. It promotes DRY(Don't Repeat Yourself) principle.
{{% /notice %}}

## Rules For Mixin
- **Mixin** can't be instantiated. You can't create object of mixin.
- Use the **mixin** to share the code between multiple classes.
- **Mixin** has no constructor and cannot be extended.
- It is possible to use multiple **mixins** in a class. 


## Syntax
```dart
mixin Mixin1{
  // code
}

mixin Mixin2{
  // code
}

class ClassName with Mixin1, Mixin2{
  // code
}
```

## Example 1: Mixin In Dart
In this example below, there are two mixins named **ElectricVariant** and **PetrolVariant**. The **ElectricVariant** mixin has a method **electricVariant()** and the **PetrolVariant** mixin has a method **petrolVariant()**. The **Car** class uses both the **ElectricVariant** and **PetrolVariant** mixins.

```dart
mixin ElectricVariant {
  void electricVariant() {
    print('This is an electric variant');
  }
}

mixin PetrolVariant {
  void petrolVariant() {
    print('This is a petrol variant');
  }
}
// with is used to apply the mixin to the class
class Car with ElectricVariant, PetrolVariant {
  // here we have access of electricVariant() and petrolVariant() methods
}

void main() {
  var car = Car();
  car.electricVariant();
  car.petrolVariant();
}
```

{{% expand "Show Output" "false" %}}
````plaintext
This is an electric variant
This is a petrol variant
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=04f7a0b34fa4771e486da08c7e536ecd" style="blue" %}}{{% /button %}}

## Example 2: Mixin In Dart
In this example below, there are two mixins named **CanFly** and **CanWalk**. The **CanFly** mixin has a method **fly()** and the **CanWalk** mixin has a method **walk()**. The **Bird** class uses both the **CanFly** and **CanWalk** mixins. The **Human** class uses the **CanWalk** mixin.
    
```dart
mixin CanFly {
  void fly() {
    print('I can fly');
  }
}

mixin CanWalk {
  void walk() {
    print('I can walk');
  }
}

class Bird with CanFly, CanWalk {
 
}

class Human with CanWalk {
 
}

void main() {
  var bird = Bird();
  bird.fly();
  bird.walk();

  var human = Human();
  human.walk();
}
```

{{% expand "Show Output" "false" %}}
````plaintext
I can fly
I can walk
I can walk
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=e3438206f24d8b36216acc71bd2d8b47" style="blue" %}}{{% /button %}}

## On Keyword
Sometimes, you want to use a mixin only with a specific class. In this case, you can use the **on** keyword. 

## Syntax Of On Keyword
```dart
mixin Mixin1 on Class1{
  // code
}
```

## Example 3: On Keyword In Mixin In Dart
In this example below, there is abstract class named **Animal** with properties **name** and **speed**. The **Animal** class has an abstract method **run()**. The **CanRun** mixin is only used by class that extends **Animal**. The **Dog** class extends the **Animal** class and uses the **CanRun** mixin. The **Bird** class cannot use the **CanRun** mixin because it does not extend the **Animal** class.

```dart
abstract class Animal {
  // properties
  String name;
  double speed;

  // constructor
  Animal(this.name, this.speed);

  // abstract method
  void run();
}

// mixin CanRun is only used by class that extends Animal
mixin CanRun on Animal {
  // implementation of abstract method
  @override
  void run() => print('$name is Running at speed $speed');
}

class Dog extends Animal with CanRun {
  // constructor
  Dog(String name, double speed) : super(name, speed);
}

void main() {
  var dog = Dog('My Dog', 25);
  dog.run();
}

// Not Possible
// class Bird with Animal { } 

```
{{% expand "Show Output" "false" %}}
````plaintext
My Dog is Running at speed 25.0
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=3dd05d67ad65aee3486c936c73c3f9ce" style="blue" %}}{{% /button %}}


## What Is Allowed For Mixin
- You can add properties and static variables.
- You can add regular, abstract, and static methods.
- You can use one or more mixins in a class.

## What Is Not Allowed For Mixin
- You can't define a constructor.
- You can't extend a mixin.
- You can't create an object of mixin.

## Video
Watch our video on mixin in Dart.
{{< youtube cM5-oUWeM30 >}}