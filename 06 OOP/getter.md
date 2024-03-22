+++
title = "Getter in Dart"
weight = 11
description = "Getter is a method that is used to access the value of a private property. Getter in Dart is used to access the value of a private property. Getter in Dart is also used to restrict the access of data members of a class."
keywords = ["getter", "getter in dart", "getter in dart programming", "getter in dart programming language"]
+++

### Getter In Dart
**Getter** is used to get the value of a property. It is mostly used to access a **private property's** value. Getter provide explicit read access to an object properties.

### Syntax
```dart
return_type get property_name {
  // Getter body
}
```

{{% notice info %}}
**Note:** Instead of writing { } after the property name, you can also write **=>** (fat arrow) after the property name.
{{% /notice %}}


### Example 1: Getter In Dart
In this example below, there is a class named **Person**. The class has two properties **firstName** and **lastName**. There is getter **fullName** which is responsible to get full name of person.

```dart
class Person {
  // Properties
  String? firstName;
  String? lastName;

  // Constructor
  Person(this.firstName, this.lastName);

  // Getter
  String get fullName => "$firstName $lastName";
}

void main() {
  Person p = Person("John", "Doe");
  print(p.fullName);
}
```
{{% expand "Show Output" "false" %}}
````plaintext
John Doe
````
{{% /expand %}} 
{{% button href="https://dartpad.dev/?id=9fb39aa9ec4074756d26b8399b5e090f" style="blue" %}}Run Online{{% /button %}}  

### Example 2: Getter In Dart
In this example below, there is a class named **NoteBook**. The class has two private properties **_name** and **_prize**. There are two getters  **name** and **prize** to access the value of the properties.

```dart
class NoteBook {
  // Private properties
  String? _name;
  double? _prize;

  // Constructor
  NoteBook(this._name, this._prize);

  // Getter method to access private property _name
  String get name => this._name!;

  // Getter method to access private property _prize
  double get prize => this._prize!;
}

void main() {
  // Create an object of NoteBook class
  NoteBook nb = new NoteBook("Dell", 500);
  // Display the values of the object
  print(nb.name);
  print(nb.prize);
}
```
    
{{% expand "Show Output" "false" %}}
````plaintext
Name: Dell
Price: 500.0
````
{{% /expand %}} 

{{% button href="https://dartpad.dev/?id=49ca28af8b8f24aab21f4919ae5cac5f" style="blue" %}}Run Online{{% /button %}}   

{{% notice info %}}

**Note:** In the above example, a getter **name** and **prize** are used to access the value of the properties **_name** and **_prize**. 
{{% /notice %}}

### Example 3: Getter In Dart With Data Validation
In this example below, there is a class named **NoteBook**. The class has two private properties **_name** and **_prize**. There are two getters **name** and **prize** to access the value of the properties. If you provide a blank name, then it will return **No Name**.

```dart
   class NoteBook {
  // Private properties
  String _name;
  double _prize;

  // Constructor
  NoteBook(this._name, this._prize);

  // Getter to access private property _name
  String get name {
    if (_name == "") {
      return "No Name";
    }
    return this._name;
  }

  // Getter to access private property _prize
  double get prize {
    return this._prize;
  }
}

void main() {
  // Create an object of NoteBook class
  NoteBook nb = new NoteBook("Apple", 1000);
  print("First Notebook name: ${nb.name}");
  print("First Notebook prize: ${nb.prize}");
  NoteBook nb2 = new NoteBook("", 500);
  print("Second Notebook name: ${nb2.name}");
  print("Second Notebook prize: ${nb2.prize}");
}
```
{{% expand "Show Output" "false" %}}
````plaintext
First Notebook name: Apple
First Notebook prize: 1000.0
Second Notebook name: No Name
Second Notebook prize: 500.0
````
{{% /expand %}} 
{{% button href="https://dartpad.dev/?id=7dfcf9e55aa622517e02d4394063808e" style="blue" %}}Run Online{{% /button %}}   


### Example 4: Getter In Dart
In this example below, there is a class named **Doctor**. The class has three private properties **_name**, **_age** and **_gender**. There are three getters **name**, **age**, and **gender** to access the value of the properties. It has **map** getter to get **[Map](/collections/map-in-dart/)** of the object.

```dart
class Doctor {
// Private properties
  String _name;
  int _age;
  String _gender;

// Constructor
  Doctor(this._name, this._age, this._gender);

// Getters
  String get name => _name;
  int get age => _age;
  String get gender => _gender;

// Map Getter
  Map<String, dynamic> get map {
    return {"name": _name, "age": _age, "gender": _gender};
  }
}

void main() {
// Create an object of Doctor class
  Doctor d = Doctor("John", 41, "Male");
  print(d.map);
}

```
{{% expand "Show Output" "false" %}}
````plaintext
{name: John, age: 41, gender: Male}
````
{{% /expand %}}   
{{% button href="https://dartpad.dev/?id=b26194aae0566166f490755b9e550685" style="blue" %}}Run Online{{% /button %}}


### Why Is Getter Important In Dart?
- To access the value of private property.
- To restrict the access of data members of a class.

### Video
Watch our video on getters in Dart.
{{< youtube j4PwccC77Y4 >}}

### Conclusion
In this section, you have learned about **Getter** with the help of examples. In the next section, you will learn about **[Setter In Dart](/object-oriented-programming/setter-in-dart/)**.
