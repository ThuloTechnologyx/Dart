+++
title = "Where in Dart"
weight = 4
description = "This guide will teach you how to use where in dart programming language with examples."
keywords = "dart where, where in list dart, dart where in list"
+++

### Where Dart
You can use where in list, set, map to **filter specific items**. It returns a new list containing all the elements that satisfy the condition. This is also called **Where Filter** in dart. Let's see the syntax below:

### Syntax
```dart
Iterable<E> where(
bool test(
E element
)
)
```
### Example 1: Filter Only Odd Number From List
In this example, you will get only odd numbers from a list.

```dart
void main() {
  List<int> numbers = [2, 4, 6, 8, 10, 11, 12, 13, 14];

  List<int> oddNumbers = numbers.where((number) => number.isOdd).toList();
  print(oddNumbers);
}
```
{{% expand "Show Output" "false" %}}
````plaintext
[11, 13]
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=01e3d6f236867c5ce07ef02662c95faa" style="blue" %}}Run Online{{% /button %}}

### Example 2: Filter Days Start With S
In this example, you will get only days that start with alphabet s.
```dart
void main() {
  List<String> days = [
    "Sunday",
    "Monday",
    "Tuesday",
    "Wednesday",
    "Thursday",
    "Friday",
    "Saturday"
  ];

  List<String> startWithS =
      days.where((element) => element.startsWith("S")).toList();

  print(startWithS);
}

```
{{% expand "Show Output" "false" %}}
````plaintext
[Sunday, Saturday]
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=70a93a34519688c4ab4b46cc6aeb5561" style="blue" %}}Run Online{{% /button %}}

### Example 3: Where Filter In Map
In this example, you will get students whose marks are greater or equal to 32. 

```dart
void main() {
  Map<String, double> mathMarks = {
    "ram": 30,
    "mark": 32,
    "harry": 88,
    "raj": 69,
    "john": 15,
  };

  mathMarks.removeWhere((key, value) => value < 32);

  print(mathMarks);
}

```
{{% expand "Show Output" "false" %}}
````plaintext
{mark: 32.0, harry: 88.0, raj: 69.0}
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=36aca6332932402e7581f125cdb1e669" style="blue" %}}Run Online{{% /button %}}

