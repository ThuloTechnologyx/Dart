+++
title = "Late Keyword in Dart"
weight = 4
description = "Late keyword in Dart is used to indicate that a variable or field will be initialized at a later time."
keywords = "late keyword in dart, late keyword in dart example, late keyword in dart usecase, late keyword in flutter, late keyword in dart null safety, late keyword in dart flutter example, late keyword in dart flutter usecase, late keyword in dart flutter null safety"
+++

## Late Keyword In Dart
[![targets](/images/pieces/note-banner.png)](https://pieces.app/?utm_source=dart-tutorial&utm_medium=banner&utm_campaign=dart-tutorial-website&utm_content=note)
In dart, **late** keyword is used to declare a variable or field that will be initialized at a later time. It is used to declare a **non-nullable** variable that is not initialized at the time of declaration. 

## Example 1: Late Keyword In Dart
In this example, **name** variable is declared as a **late** variable. The **name** variable is initialized in the **main** method.
```dart
// late variable
late String name;

void main() {
  // assigning value to late variable
  name = "John";
  print(name);
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=7c524a84ec)

{{% expand "Show Output" "false" %}}
````plaintext
John
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=33508983194cdda4600196be311e61ba" style="blue" %}}{{% /button %}}

When you put **late** infront of a variable declearation, you tell Dart the following:
- Don't assign that variable a value yet.
- You will assign value later.
- You will make sure the variable has a value before you use it.

{{% notice info %}}
**Note**: The **late** keyword is contract between you and Dart. You are telling Dart that you will assign a value to the variable before you use it. If you don't assign a value to the variable before you use it, Dart will throw an error.
{{% /notice %}}

## Example 2: Late Keyword In Dart
In this example, there is **Person** class with a **name** field. The **name** field is declared as a late variable.

```dart
class Person {
  // late variable
  late String name;

  void greet() {
    print("Hello $name");
  }
}

void main() {
  Person person = Person();
  // late variable is initialized here
  person.name = "John";
  person.greet();
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=b0b94db901)

{{% expand "Show Output" "false" %}}
````plaintext
Hello John
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=92a273fac270f25ebf941d33208a9388" style="blue" %}}{{% /button %}}

## Usecase of Late Keyword In Dart
Dart late keyword has two use cases:
- **Declaring a non-nullable variable or field** that is not initialized at the point of declaration.
- **Lazy initialization** of a variable or field.

## What Is Lazy Initialization
**Lazy initialization** is a design pattern that delays the creation of an object, the calculation of a value, or some other expensive process until the **first time you need it**.

{{% notice info %}}
Note: Using  **late** means dart doesn't initialize value right away, it only initializes when you access it for the first time. This is also called **lazy loading**.
{{% /notice %}}

## Example 3: Late Keyword In Dart
In this example, the **provideCountry** function is not called when the **value** variable is declared. The **provideCountry** function is called only when the **value** variable is used. **Lazy initialization** is used to avoid unnecessary computation.
```dart
// function
String provideCountry() {
  print("Function is called");
  return "USA";
}

void main() {
  print("Starting");
  // late variable
  late String value = provideCountry();
  print("End");
  print(value);
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=e134469a05)

Guess the output before clicking on the **Show Output** button. If you remove the **late** keyword from the **value** variable, the **provideCountry** function will be called when the **value** variable is declared.

{{% expand "Show Output" "false" %}}
````plaintext
Starting
End
Function is called
USA
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=47dfd8c5098cfcb4c322f833fed9eb5d" style="blue" %}}{{% /button %}}

## Example 4: Late Keyword In Class
In this example, the **heavyComputation** function is called when the **description** variable is used. If you remove the **late** keyword from the **description** variable, the **heavyComputation** function will be called when the **Person** class is instantiated.

```dart
// Person class
class Person {
  final int age;
  final String name;
  late String description = heavyComputation();

// constructor
  Person(this.age, this.name) {
    print("Constructor is called");
  }
// method
  String heavyComputation() {
    print("heavyComputation is called");
    return "Heavy Computation";
  }
}

void main() {
  // object of Person class
  Person person = Person(10, "John");
  print(person.name);
  print(person.description); 
}

```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=715e49be7a)

{{% expand "Show Output" "false" %}}
````plaintext
Constructor is called
John
heavyComputation is called
Heavy Computation
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=f3a63a2b72718d99642bc22086fe5079" style="blue" %}}{{% /button %}}

## Example 5: Late Keyword In Class
In this example, the **_getFullName** function is called when the **fullName** variable is used. The **firstName** and **lastName** variables are initialized when the **fullName** variable is used.
```dart
class Person {
  // declaring late variables
  late String fullName = _getFullName();
  late String firstName = fullName.split(" ").first;
  late String lastName = fullName.split(" ").last;

// method
  String _getFullName() {
    print("_getFullName is called");
    return "John Doe";
  }
}
// main method
void main() {
  print("Start");
  Person person = Person();
  print("First Name: ${person.firstName}");
  print("Last Name: ${person.lastName}");
  print("Full Name: ${person.fullName}");
  print("End");
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=b5f14bb4cf)


{{% expand "Show Output" "false" %}}
````plaintext
Start
_getFullName is called
First Name: John
Last Name: Doe
Full Name: John Doe
End
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=10279966dbb82109333937e40460cd94" style="blue" %}}{{% /button %}}

{{% notice info %}}
**Note**: If you remove the **late** keyword from the **fullName** variable, the **_getFullName** function will be called when the **Person** class is instantiated.
{{% /notice %}}

## Late Final Keyword In Dart
If you want to assign a value to a variable only once, you can use the **late final** keyword. This is useful when you want to initialize a variable only once. 

## Example 6: Late Final Keyword In Dart
In this example, there is class **Student** with a **name** field. The **name** field is declared as a **late final** variable. The **name** field is initialized in the **Student** constructor. The **name** field is assigned a value only once. If you try to assign a value to the **name** field again, you will get an error.
```dart
// Student class
class Student {
  // late final variable
  late final String name;

  // constructor
  Student(this.name);
}

void main() {
  // object of Student class
  Student student = Student("John");
  print(student.name);
  student.name = "Doe"; // Error
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=4d624486f4)

{{% expand "Show Output" "false" %}}
````plaintext
John
Unhandled exception:
LateInitializationError: Field 'name' has already been initialized.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=f5544cbe648f3ce048e15b40f935606b" style="blue" %}}{{% /button %}}
