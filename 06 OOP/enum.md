+++
title = "Enum in Dart"
weight = 19
description = "An enum is a special data type that enables for a variable to be a set of predefined constants. The variable must be equal to one of the values that have been predefined for it. An enum is declared using the keyword enum followed by the name of the enum."
keywords = ["enum", "enum in dart", "enum in dart programming", "enum in dart programming language"]
+++

### Enum In Dart
An enum is a special type that represents a fixed number of constant values. An enum is declared using the keyword **enum** followed by the enum's name. 

### Syntax Of Enum In Dart
```dart
enum enumName {
  constantName1,
  constantName2,
  constantName3,
  ...
  constantNameN
}
```

### Example 1: Enum In Dart
In this example below, there is enum type named **days**. It contains seven constants days. The **days** enum type is used in the **main()** function.

```dart
enum days {
  Sunday,
  Monday,
  Tuesday,
  Wednesday,
  Thrusday,
  Friday,
  Saturday
}

void main() {
  var today = days.Friday;
  switch (today) {
    case days.Sunday:
      print("Today is Sunday.");
      break;
    case days.Monday:
      print("Today is Monday.");
      break;
    case days.Tuesday:
      print("Today is Tuesday.");
      break;
    case days.Wednesday:
      print("Today is Wednesday.");
      break;
    case days.Thursday:
      print("Today is Thursday.");
      break;
    case days.Friday:
      print("Today is Friday.");
      break;
    case days.Saturday:
      print("Today is Saturday.");
      break;
  }
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Today is Friday.
````
{{% /expand %}}

### Example 2: Enum In Dart
In this example, there is an enum type named **Gender**. It contains three constants **Male**, **Female**, and **Other**. The **Gender** enum type is used in the **Person** class.

```dart
enum Gender { Male, Female, Other }

class Person {
  // Properties
  String? firstName;
  String? lastName;
  Gender? gender;

  // Constructor
  Person(this.firstName, this.lastName, this.gender);

  // display() method
  void display() {
    print("First Name: $firstName");
    print("Last Name: $lastName");
    print("Gender: $gender");
  }
}

void main() {
  Person p1 = Person("John", "Doe", Gender.Male);
  p1.display();

  Person p2 = Person("Menuka", "Sharma", Gender.Female);
  p2.display();
}
```
{{% expand "Show Output" "false" %}}
````plaintext
First Name: John
Last Name: Doe
Gender: Gender.Male
First Name: Menuka
Last Name: Sharma
Gender: Gender.Female
````
{{% /expand %}}

### How to Print All Enum Values
In this example, there is enum type named **Days**. It contain 7 days. The for loop iterates through all the enum values.
```dart
enum Days { Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday }

void main() {
 // Days.values: It returns all the values of the enum.
  for (Days day in Days.values) {
    print(day);
  }
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Days.Sunday
Days.Monday
Days.Tuesday
Days.Wednesday
Days.Thursday
Days.Friday
Days.Saturday
````
{{% /expand %}}

### Advantages Of Enum In Dart
- It is used to define a set of named constants.
- Makes your code more readable and maintainable.
- It makes the code more reusable and makes it easier for developers.

### Characteristics Of Enum
- It must contain at least one constant value.
- Enums are declared outside the class.
- Used to store a large number of constant values. 

### Enhanced Enum In Dart
In dart, you can declare enums with members. For example, for your accounting software you can store company types like **Sole Proprietorship**, **Partnership**, **Corporation**, and **Limited Liability Company**. You can declare an enum with members as shown below.

```dart
enum CompanyType {
  soleProprietorship("Sole Proprietorship"),
  partnership("Partnership"),
  corporation("Corporation"),
  limitedLiabilityCompany("Limited Liability Company");

  // Members
  final String text;
  const CompanyType(this.text);
}

void main() {
  CompanyType soleProprietorship = CompanyType.soleProprietorship;
  print(soleProprietorship.text);
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Sole Proprietorship
````
{{% /expand %}}

### Video
Watch our video on enum in Dart.
{{< youtube W9peo3BzK_Y >}}
