+++
title = "Set in Dart"
weight = 2
description = "Learn Set in dart with its properties, methods, and examples."
keywords = "dart Set, learn dart Set, Set in the dart, learn dart programming, dart tutorial."
+++

### Set In Dart
Set is a unique collection of items. You cannot store duplicate values in the Set. It is unordered, so it can be faster than lists while working with a large amount of data. Set is useful when you need to store unique values without considering the order of the input. E.g., fruits name, months name, days name, etc. It is represented by **Curley Braces{}.**

{{% notice info %}}
**Note**: The list allows you to add **duplicate items**, but the Set doesn't allow it. 
{{% /notice %}}

### Syntax
```dart
Set <variable_type> variable_name = {};
```

### How To Create A Set In Dart
You can create a Set in Dart using the **Set** type annotation. Here **Set\<String>** means only text is allowed in the Set. 

```dart
void main(){
  Set<String> fruits = {"Apple", "Orange", "Mango"};
  print(fruits);
}
```
{{% expand "Show Output" "false" %}}
````plaintext
{Apple, Orange, Mango}
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=a81291eb0617b7bd9db9d5f82d94838e" style="blue" %}}Run Online{{% /button %}}

### Set Properties In Dart
|  Properties |  Work |
| ----------- | --------- |
|  **first**  |    To get first value of Set.  |
|  **last**  |    To get last value of Set.  |
|  **isEmpty**  |    Return true or false.  |
|  **isNotEmpty**  |    Return true or false.  |
|  **length**  |    It returns the length of the Set.  |

### Example of Set Properties Dart
This example finds the first and last element of the Set, checks whether it is empty or not, and finds its length.

```dart
void main() {
  // declaring fruits as Set
  Set<String> fruits = {"Apple", "Orange", "Mango", "Banana"};

  // using different properties of Set
  print("First Value is ${fruits.first}");
  print("Last Value is ${fruits.last}");
  print("Is fruits empty? ${fruits.isEmpty}");
  print("Is fruits not empty? ${fruits.isNotEmpty}");
  print("The length of fruits is ${fruits.length}");
}
```
{{% expand "Show Output" "false" %}}
````plaintext
First Value is Apple
Last Value is Banana
Is fruits empty? false
Is fruits not empty? true
The length of fruits is 4
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=302d88156a2c7b4d5e92cc5012ebd45d" style="blue" %}}Run Online{{% /button %}}

### Check The Available Value
If you want to see whether the Set contains specific items or not, you can use the **contains** method, which returns true or false.

```dart
void main(){
  Set<String> fruits = {"Apple", "Orange", "Mango"};
  print(fruits.contains("Mango"));
  print(fruits.contains("Lemon"));
}
```
{{% expand "Show Output" "false" %}}
````plaintext
true
false
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=f4f4cc1854067bebf1d3af8adef0d71d" style="blue" %}}Run Online{{% /button %}}

### Add & Remove Items In Set
Like lists, you can add or remove items in a Set. To add items use **add()** method and to remove use **remove()** method.

|  Method |  Description 
| ----------- | --------- |
|  **add()** |    Add one element to Set.  |
|  **remove()** |    Removes one element from Set.  |

```dart
void main(){
 Set<String> fruits = {"Apple", "Orange", "Mango"};
  
  fruits.add("Lemon");
  fruits.add("Grape");
  
  print("After Adding Lemon and Grape: $fruits");
  
  fruits.remove("Apple");
  print("After Removing Apple: $fruits");
}
```
{{% expand "Show Output" "false" %}}
````plaintext
After Adding Lemon and Grape: {Apple, Orange, Mango, Lemon, Grape}
After Removing Apple: {Orange, Mango, Lemon, Grape}
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=06d83448873eb77c024265ca9cf12a90" style="blue" %}}Run Online{{% /button %}}

### Adding Multiple Elements
You can use **addAll()** method to add multiple elements from the list to Set.
|  Method |  Description 
| ----------- | --------- |
|  **addAll()**  |   Insert the multiple values to the given Set. |  

```dart
void main(){
 Set<int> numbers = {10, 20, 30};
  numbers.addAll([40,50]);
 print("After adding 40 and 50: $numbers");
}    
```
{{% expand "Show Output" "false" %}}
````plaintext
After adding 40 and 50: {10, 20, 30, 40, 50}
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=cf03cabf46a6d1b1f4a9c1dc97ec65fd" style="blue" %}}Run Online{{% /button %}}

### Printing All Values In Set
You can print all Set items by using loops. [Click here](/conditions-and-loops/loops-in-dart/) if you want to learn loop in dart.

```dart
void main(){
 Set<String> fruits = {"Apple", "Orange", "Mango"};
  
 for(String fruit in fruits){
   print(fruit);
 }
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Apple
Orange
Mango
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=b33cb6f3f3d163891024fe7c57a32cd7" style="blue" %}}Run Online{{% /button %}}

### Set Methods In Dart
Some other helpful Set methods in dart.
|  Method |  Description 
| ----------- | --------- |
|  **clear()** |    Removes all elements from the Set.  |
|  **difference()** |    Creates a new Set with the elements of this that are not in other.  |
|  **elementAt()** |    Returns the index value of element. |
|  **intersection()** |    Find common elements in two sets. |


### Clear Set In Dart
In this example, you can see how to remove all items from the Set in dart. 

```dart
void main() {
  Set<String> fruits = {"Apple", "Orange", "Mango"};
  // to clear all items
  fruits.clear();

  print(fruits);
}
```
{{% expand "Show Output" "false" %}}
````plaintext
{}
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=dd47d41f89714f10d5eb6e365645787c" style="blue" %}}Run Online{{% /button %}}

### Difference In Set 
In Dart, the difference method creates a new Set with the elements that are not in the other.
```dart
void main() {
  Set<String> fruits1 = {"Apple", "Orange", "Mango"};
  Set<String> fruits2 = {"Apple", "Grapes", "Banana"};

  final differenceSet = fruits1.difference(fruits2);

  print(differenceSet);
}
```
{{% expand "Show Output" "false" %}}
````plaintext
{Orange, Mango}
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=c5689e106ed901f586b04a1b4b2be666" style="blue" %}}Run Online{{% /button %}}

### Element At Method In Dart
In Dart you can find the Set value by its index number. The index number starts with 0.
```dart
void main() {
  Set<String> days = {"Sunday", "Monday", "Tuesday"};
  // index starts from 0 so 2 means Tuesday
  print(days.elementAt(2));
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Tuesday
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=12d2de173ce43b54e309fe5e946d78be" style="blue" %}}Run Online{{% /button %}}

### Intersection Method In Dart
In Dart, the intersection method creates a new Set with the common elements in 2 Sets. Here Apple is available in both Sets.
```dart
void main() {
  Set<String> fruits1 = {"Apple", "Orange", "Mango"};
  Set<String> fruits2 = {"Apple", "Grapes", "Banana"};

  final intersectionSet = fruits1.intersection(fruits2);

  print(intersectionSet);
}
```
{{% expand "Show Output" "false" %}}
````plaintext
{Apple}
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=944e1124eb240d663f8a81b6aa50ad6b" style="blue" %}}Run Online{{% /button %}}

### Video
Watch our video on the set in Dart.
{{< youtube s9BwdIaUnnM >}}