
+++
title = "List in Dart"
weight = 1
description = "Learn list in dart with its properties, methods and examples."
keywords = "dart list, list in dart, learn dart programming, dart lists, learn dart lists"
+++

##  List In Dart
If you want to store multiple values in the same variable, you can use **List**. List in dart is similar to **Arrays** in other programming languages. E.g. to store the names of multiple students, you can use a List. The List is represented by **Square Braces[].**

## How To Create List
You can create a List by specifying the initial elements in a square bracket. Square bracket **[]** is used to represent a List.
```dart
// Integer List
List<int> ages = [10, 30, 23];

// String List
List<String> names = ["Raj", "John", "Rocky"];

// Mixed List
var mixed = [10, "John", 18.8];
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=32b640a36f)


     
## Types Of Lists
- Fixed Length List
- Growable List [**Mostly Used**]

## Fixed Length List
The fixed-length Lists are defined with the specified length. You cannot change the size at runtime. This will create List of 5 integers with the value 0.
```dart
void main() {  
   var list = List<int>.filled(5,0);  
   print(list);  
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=e7a44a85c8)

{{% expand "Show Output" "false" %}}
````plaintext
[0, 0, 0, 0, 0]
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=7016656046c22a627ffaf0650191ba72" style="blue" %}}{{% /button %}}



{{% notice info %}}
Note: You cannot add a new item to **Fixed Length List**, but you can change the values of List.
{{% /notice %}}

## Growable List
A List defined without a specified length is called Growable List. The length of the growable List can be changed in runtime.

```dart
void main() {  
   var list1 = [210,21,22,33,44,55];  
   print(list1);  
}  
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=d8fb4ca664)

{{% expand "Show Output" "false" %}}
````plaintext
[210, 21, 22, 33, 44, 55]
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=a6736588815f80ac929e019af6bb9e91" style="blue" %}}{{% /button %}}


## Access Item Of List
You can access the List item by **index**. Remember that the List index always starts with **0**.
```dart
void main() {
  var list = [210, 21, 22, 33, 44, 55];

  print(list[0]);
  print(list[1]);
  print(list[2]);
  print(list[3]);
  print(list[4]);
  print(list[5]);
}

```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=fc5842bc4a)

{{% expand "Show Output" "false" %}}
````plaintext
210
21
22
33
44
55
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=b0abb5c0358fc180f0f42608b2a8b189" style="blue" %}}{{% /button %}}

## Get Index By Value
You can also get the index by value. 

```dart
void main() {
  var list = [210, 21, 22, 33, 44, 55];

  print(list.indexOf(22));
  print(list.indexOf(33));
}

```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=1ca640a8bc)

{{% expand "Show Output" "false" %}}
````plaintext
2
3
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=b9bd6e4759a6b2ca7a86461445252ca6" style="blue" %}}{{% /button %}}

## Find The Length Of The List
You can find the length of List by using **.length** property.
```dart
void main(){  
   List<String> names = ["Raj", "John", "Rocky"];
   print(names.length);
 }
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=bf6549aed2)

{{% expand "Show Output" "false" %}}
````plaintext
3
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=8d305a54eb6d3ff2f33c5f36d2aedf67" style="blue" %}}{{% /button %}}


{{% notice info %}}
Note: Remember that List **index** starts with **0** and length always starts with **1**. 
{{% /notice %}}

## Changing Values Of List
You can also change the value of List. You can do it by **listName[index]=value;**. For more, see the example below. 
```dart
void main(){  
   List<String> names = ["Raj", "John", "Rocky"];
   names[1] = "Bill";
   names[2] = "Elon";
   print(names);
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=01c444b564)

{{% expand "Show Output" "false" %}}
````plaintext
[Raj, Bill, Elon]
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=3027d2e23c6734c5dbe8117522473b0e" style="blue" %}}{{% /button %}}


## Mutable And Immutable List
A mutable List means they can change after the declaration, and an immutable List means they can't change after the declaration.
```dart

List<String> names = ["Raj", "John", "Rocky"]; // Mutable List
names[1] = "Bill"; // possible
names[2] = "Elon"; // possible
    
const List<String> names = ["Raj", "John", "Rocky"]; // Immutable List
names[1] = "Bill"; // not possible
names[2] = "Elon"; // not possible
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=d7a54da0da)

## List Properties In Dart
*   **first**: It returns the first element in the List.
*   **last**: It returns the last element in the List.
*   **isEmpty**: It returns **true** if the List is empty and **false** if the List is not empty.
*   **isNotEmpty**: It returns **true** if the List is not empty and **false** if the List is empty.
*   **length**: It returns the length of the List.
*   **reversed**: It returns a List in reverse order.
*   **single**: It is used to check if the List has only one element and returns it.

## Access First And Last Elements Of List
You can access the first and last elements in the List by:
```dart
void main() {
   List<String> drinks = ["water", "juice", "milk", "coke"];
   print("First element of the List is: ${drinks.first}");
   print("Last element of the List is: ${drinks.last}");
}  
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=229748b290)

{{% expand "Show Output" "false" %}}
````plaintext
First element of the List is: water
Last element of the List is: coke
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=685872c01807ccc82672c6dcb5fb01b3" style="blue" %}}{{% /button %}}


## Check The List Is Empty Or Not
You can also check List contain any elements inside it or not. It will give result either in **true** or in **false**. 
```dart
void main() {
   List<String> drinks = ["water", "juice", "milk", "coke"];
   List<int>  ages = [];
   print("Is drinks Empty: "+drinks.isEmpty.toString());
   print("Is drinks not Empty: "+drinks.isNotEmpty.toString());
   print("Is ages Empty: "+ages.isEmpty.toString());
   print("Is ages not Empty: "+ages.isNotEmpty.toString());
   
}  
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=9be14281db)

{{% expand "Show Output" "false" %}}
````plaintext
Is drinks Empty: false
Is drinks not Empty: true
Is ages Empty: true
Is ages not Empty: false
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=49303a10bc78c8174157ecaf29393bec" style="blue" %}}{{% /button %}}


## Reverse List In Dart
You can easily reverse List by using **.reversed** properties. Here is an example below:
```dart
void main() {
   List<String> drinks = ["water", "juice", "milk", "coke"];
   print("List in reverse: ${drinks.reversed}");
}  
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=40494ab0bd)

{{% expand "Show Output" "false" %}}
````plaintext
List in reverse: (coke, milk, juice, water)
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=1a62b6626ba5f38ed629b860c115af49" style="blue" %}}{{% /button %}}


## Adding Item To List
Dart provides four methods to insert the elements into the Lists. These methods are given below.

|  Method |  Description 
| ----------- | --------- |
|  **add()** |    Add one element at a time and returns the modified List object.  |
|  **addAll()**  |   Insert the multiple values to the given List, and each value is separated by the commas and enclosed with a square bracket ([]).  |  
|  **insert()** |    Provides the facility to insert an element at a specified index position.  |
|  **insertAll()** |    Insert the multiple value at the specified index position.  |

## Example 1: Add Item To List 
In this example below, we are adding an item to evenList using **add()** method.
```dart
void main() {  
    var evenList = [2,4,6,8,10];  
    print(evenList);  
    evenList.add(12);  
    print(evenList);  
}  
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=116547b186)

{{% expand "Show Output" "false" %}}
````plaintext
[2, 4, 6, 8, 10]
[2, 4, 6, 8, 10, 12]
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=edefed76627a2cf9cd6c6172994dad71" style="blue" %}}{{% /button %}}


## Example 2: Add Items To List 
In this example below, we are adding items to evenList using **addAll()** method.
```dart
void main() {
  var evenList = [2, 4, 6, 8, 10];
  print(evenList);
  evenList.addAll([12, 14, 16, 18]);
  print(evenList);
}

```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=e8e6459393)

{{% expand "Show Output" "false" %}}
````plaintext
[2, 4, 6, 8, 10]
[2, 4, 6, 8, 10, 12, 14, 16, 18]
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=b19b30e4937cf7ce8d62539361973fa6" style="blue" %}}{{% /button %}}


## Example 3: Insert Item To List 
In this example below, we are adding an item to myList using **insert()** method.
```dart
void main() {
  List myList = [3, 4, 2, 5];
  print(myList);
  myList.insert(2, 15);
  print(myList);
}

```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=8e6f4b80ac)

{{% expand "Show Output" "false" %}}
````plaintext
[3, 4, 2, 5]
[3, 4, 15, 2, 5]
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=6dd64a58623bb3146d39f5b8d9d42db5" style="blue" %}}{{% /button %}}


## Example 4: Insert Items To List 
In this example below, we are adding items to myList using **insertAll()** method.
```dart
void main() {
  var myList = [3, 4, 2, 5];
  print(myList);
  myList.insertAll(1, [6, 7, 10, 9]);
  print(myList);
}
  
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=f9bc4c9894)

{{% expand "Show Output" "false" %}}
````plaintext
[3, 4, 2, 5]
[3, 6, 7, 10, 9, 4, 2, 5]
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=76f2422b26cbf0706d66323a5b824539" style="blue" %}}{{% /button %}}


## Replace Range Of List
You can also replace the range of the List. For more, see the example below.
```dart
void main() {
  var list = [10, 15, 20, 25, 30];
  print("List before updation: ${list}");
  list.replaceRange(0, 4, [5, 6, 7, 8]);
  print("List after updation using replaceAll() function : ${list}");
}

```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=f429409f39)

{{% expand "Show Output" "false" %}}
````plaintext
List before updation: [10, 15, 20, 25, 30]
List after updation using replaceAll() function : [5, 6, 7, 8, 30]
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=430308ef7add291bcd4ca683f8a5feec" style="blue" %}}{{% /button %}}


## Removing List Elements
|  Method |  Description 
| ----------- | --------- |
|  **remove()** |    Removes one element at a time from the given List.  |
|  **removeAt()**  |   Removes an element from the specified index position and returns it.  |  
|  **removeLast()** |   Remove the last element from the given List. |
|  **removeRange()** |    Removes the item within the specified range. |

## Example 1: Removing List Item From List
In this example below, we are removing item of List using **remove()** method.
```dart
void main() {
  var list = [10, 20, 30, 40, 50];
  print("List before removing element : ${list}");
  list.remove(30);
  print("List after removing element : ${list}");
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=4edf408fce)

{{% expand "Show Output" "false" %}}
````plaintext
List before removing element : [10, 20, 30, 40, 50]
List after removing element : [10, 20, 40, 50]
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=060e5f2850e2336aae317c5313f4f4ac" style="blue" %}}{{% /button %}}


## Example 2: Removing List Item From List
In this example below, we are removing item of List using **removeAt()** method.
```dart
void main() {
  var list = [10, 11, 12, 13, 14];
  print("List before removing element : ${list}");
  list.removeAt(3);
  print("List after removing element : ${list}");
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=899047a705)

{{% expand "Show Output" "false" %}}
````plaintext
List before removing element : [10, 11, 12, 13, 14]
List after removing element : [10, 11, 12, 14]
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=41ffae47403073f125e1a8776b523b5e" style="blue" %}}{{% /button %}}


## Example 3: Removing Last Item From List
In this example below, we are removing last item of List using **removeLast()** method.

```dart
void main() {
  var list = [10, 20, 30, 40, 50];
  print("List before removing element:${list}");
  list.removeLast();
  print("List after removing last element:${list}");
}

```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=040d42a95e)

{{% expand "Show Output" "false" %}}
````plaintext
List before removing element:[10, 20, 30, 40, 50]
List after removing last element:[10, 20, 30, 40]
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=487aa90d121cd50909049903d3af6949" style="blue" %}}{{% /button %}}

## Example 4: Removing List Range From List
In this example below, we are removing the range of items of List using **removeRange()** method.
```dart
void main() {
  var list = [10, 20, 30, 40, 50];
  print("List before removing element:${list}");
  list.removeRange(0, 3);
  print("List after removing range element:${list}");
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=a13a4bbe93)

{{% expand "Show Output" "false" %}}
````plaintext
List before removing element:[10, 20, 30, 40, 50]
List after removing range element:[40, 50]
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=c0b97bcba0100a35275457ef85c5e275" style="blue" %}}{{% /button %}}


## Loops In List 
You can use for loop, for each loop, or any other type of loop.
```dart
void main() {
  List<int> list = [10, 20, 30, 40, 50];
  list.forEach((n) => print(n));
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=c5ca47af9c)

{{% expand "Show Output" "false" %}}
````plaintext
10
20
30
40
50
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=5097a898fee561f95061c938e6be2e7c" style="blue" %}}{{% /button %}}


## Multiply All Value By 2 Of All List
This example below multiply value of List item by 2. 
```dart
void main() {
  List<int> list = [10, 20, 30, 40, 50];
  var douledList = list.map((n) => n * 2);

  print((douledList));
}

```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=49814e9ca8)

{{% expand "Show Output" "false" %}}
````plaintext
(20, 40, 60, 80, 100)
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=47d06805319b63589980ee948cf992fe" style="blue" %}}{{% /button %}}


## Combine Two Or More List In Dart
You can combine two or more Lists in dart by using **spread** syntax.
```dart
void main() {
  List<String> names = ["Raj", "John", "Rocky"];
  List<String> names2 = ["Mike", "Subash", "Mark"];

  List<String> allNames = [...names, ...names2];
  print(allNames);
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=575a438905)

{{% expand "Show Output" "false" %}}
````plaintext
[Raj, John, Rocky, Mike, Subash, Mark]
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=4a47d512aa92f10749e0909cf094126f" style="blue" %}}{{% /button %}}

## Conditions In List
You can also use conditions in List. Here **sad = false** so cart doesn't contain  **Beer** in it. 

```dart
void main() {
  bool sad = false;
  var cart = ['milk', 'ghee', if (sad) 'Beer'];
  print(cart);
}
 
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=13784e9ada)

{{% expand "Show Output" "false" %}}
````plaintext
[milk, ghee]
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=17e13c1037ccff0784165d9ed4a6cf34" style="blue" %}}{{% /button %}}


## Where In List Dart
You can use where with List to filter specific items. Here in this example, even numbers are only filtered.
```dart
void main(){
List<int> numbers = [2,4,6,8,10,11,12,13,14];

List<int> even = numbers.where((number)=> number.isEven).toList(); 
print(even);
}
```
[![targets](/images/pieces/save-this-snippet-button.svg)](https://snippets.pieces.cloud/?p=6258429268)

{{% expand "Show Output" "false" %}}
````plaintext
[2, 4, 6, 8, 10, 12, 14]
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=54cbe77fd2d4c1d75adefbcf393d29b4" style="blue" %}}{{% /button %}}

{{% notice info %}}
**Note**: Choose Lists if order matters. You can easily add items to the end. Searching can be slow when the List size is big.
{{% /notice %}}

