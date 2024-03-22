+++
title = "Map in Dart"
weight = 3
description = "Learn map in dart with its properties, methods and examples."
keywords = "dart map, map in dart, learn dart programming, dart maps, learn dart map"
+++

### Map In Dart
In a Map, data is stored as keys and values. In Map, each key must be unique. They are similar to HashMaps and Dictionaries in other languages.

### How To Create Map In Dart
Here we are creating a Map for **String** and **String**. It means keys and values must be the type of String. You can create a Map of any kind as you like.

```dart
void main(){
Map<String, String> countryCapital = {
  'USA': 'Washington, D.C.',
  'India': 'New Delhi',
  'China': 'Beijing'
};
  print(countryCapital);
}
```
{{% expand "Show Output" "false" %}}
````plaintext
{USA: Washington, D.C., India: New Delhi, China: Beijing}
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=091ea93bdb9bbff4028d43f078d42e63" style="blue" %}}Run Online{{% /button %}}

{{% notice info %}}
**Note**: Here **Usa**, **India**, and **China** are keys, and it must be **unique**.
{{% /notice %}}

### Access Value From Key
You can find the value of Map from its key. Here we are printing **Washington, D.C.** by its key, i.e., **USA**.

```dart
void main(){
Map<String, String> countryCapital = {
  'USA': 'Washington, D.C.',
  'India': 'New Delhi',
  'China': 'Beijing'
};
  print(countryCapital["USA"]);
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Washington, D.C.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=fbff727f69e5908ce144cf15bd2c8311" style="blue" %}}Run Online{{% /button %}}

### Map Properties In Dart
|  Properties |  Work |
| ----------- | --------- |
|  **keys**  |    To get all keys.  |
|  **values**  |    To get all values.  |
|  **isEmpty**  |    Return true or false.  |
|  **isNotEmpty**  |    Return true or false.  |
|  **length**  |    It returns the length of the Map.  |


### Example Of Map Properties In Dart
This example finds all keys/values of Map, the first and last element, checks whether it is empty or not, and finds its length.

```dart
void main() {
 
  Map<String, double> expenses = {
    'sun': 3000.0,
    'mon': 3000.0,
    'tue': 3234.0,
  };
  
  print("All keys of Map: ${expenses.keys}");
  print("All values of Map: ${expenses.values}");
  print("Is Map empty: ${expenses.isEmpty}");
  print("Is Map not empty: ${expenses.isNotEmpty}");
  print("Length of map is: ${expenses.length}");
}

```
{{% expand "Show Output" "false" %}}
````plaintext
All keys of Map: (sun, mon, tue)
All values of Map: (3000, 3000, 3234)
Is Map empty: false
Is Map empty: true
Length of map is: 3
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=b7d0739a2a9636ce2ad3d49ae9b8e31c" style="blue" %}}Run Online{{% /button %}}

### Adding Element To Map
If you want to add an element to the existing Map. Here is the way for you: 
```dart
void main(){
Map<String, String> countryCapital = {
  'USA': 'Washington, D.C.',
  'India': 'New Delhi',
  'China': 'Beijing'
};
  // Adding New Item
  countryCapital['Japan'] = 'Tokio';
  print(countryCapital);
}
```
{{% expand "Show Output" "false" %}}
````plaintext
{USA: Washington, D.C., India: New Delhi, China: Beijing, Japan: Tokio}
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=f80c06b7faeba56ab3ed36c2ee93d02f" style="blue" %}}Run Online{{% /button %}}

### Updating An Element Of Map
If you want to update an element of the existing Map. Here is the way for you: 
```dart
void main(){
Map<String, String> countryCapital = {
  'USA': 'Nothing',
  'India': 'New Delhi',
  'China': 'Beijing'
};
  // Updating Item
  countryCapital['USA'] = 'Washington, D.C.';
  print(countryCapital);
}
```
{{% expand "Show Output" "false" %}}
````plaintext
{USA: Washington, D.C., India: New Delhi, China: Beijing}
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=ff6b20a18e157dd4826f90aa645f59c4" style="blue" %}}Run Online{{% /button %}}


### Map Methods In Dart
Some useful Map methods in dart.
|  Properties |  Work |
| ----------- | --------- |
|  **keys.toList()**  |    Convert all Maps keys to List.  |
|  **values.toList()**  |    Convert all Maps values to List.  |
|  **containsKey('key')**  |    Return true or false.  |
|  **containsValue('value')**  |    Return true or false.  |
|  **clear()** |    Removes all elements from the Map.  |
|  **removeWhere()** |    Removes all elements from the Map if condition is valid. |


### Convert Maps Keys & Values To List
Let's convert keys and values of Map to List.
```dart
void main() {
 
  Map<String, double> expenses = {
    'sun': 3000.0,
    'mon': 3000.0,
    'tue': 3234.0,
  };
  
  // Without List
  print("All keys of Map: ${expenses.keys}");
  print("All values of Map: ${expenses.values}");
 
  // With List
  print("All keys of Map with List: ${expenses.keys.toList()}");
  print("All values of Map with List: ${expenses.values.toList()}");
  
}
```
{{% expand "Show Output" "false" %}}
````plaintext
All keys of Map: (sun, mon, tue)
All values of Map: (3000, 3000, 3234)
All keys of Map with List: [sun, mon, tue]
All values of Map with List: [3000, 3000, 3234
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=76f6726a5a0b3247f1981714ec37a4cf" style="blue" %}}Run Online{{% /button %}}

### Check Map Contains Specific Key/Value Or Not?
Let's check whether the Map contains a specific key/value in it or not.
```dart
void main() {
 
  Map<String, double> expenses = {
    'sun': 3000.0,
    'mon': 3000.0,
    'tue': 3234.0,
  };
  
  // For Keys
  print("Does Map contain key sun: ${expenses.containsKey("sun")}");
  print("Does Map contain key abc: ${expenses.containsKey("abc")}");
 
  // For Values
  print("Does Map contain value 3000.0: ${expenses.containsValue(3000.0)}");
  print("Does Map contain value 100.0: ${expenses.containsValue(100.0)}");
  
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Does Map contain key sun: true
Does Map contain key abc: false
Does Map contain value 3000.0: true
Does Map contain value 100.0: false
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=a7cc41ca01fd761c41307f270aab38d9" style="blue" %}}Run Online{{% /button %}}


### Removing Items From Map
Suppose you want to remove an element of the existing Map. Here is the way for you: 

```dart
void main(){
Map<String, String> countryCapital = {
  'USA': 'Nothing',
  'India': 'New Delhi',
  'China': 'Beijing'
};
  
  countryCapital.remove("USA");
  print(countryCapital);
}
```
{{% expand "Show Output" "false" %}}
````plaintext
{India: New Delhi, China: Beijing}
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=039f4c562c94e775498e5f6db13beabf" style="blue" %}}Run Online{{% /button %}}


### Looping Over Element Of Map
You can use any loop in Map to print all keys/values or to perform operations in its keys and values.
```dart
void main(){

  Map<String, dynamic> book = {
    'title': 'Misson Mangal',
    'author': 'Kuber Singh',
    'page': 233
  };
  
 // Loop Through Map
  for(MapEntry book in book.entries){
    print('Key is ${book.key}, value ${book.value}');
  }
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Key is title, value Misson Mangal
Key is author, value Kuber Singh
Key is page, value 233
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=d31306e1ff47dcc39fa5ed6bf78a39c7" style="blue" %}}Run Online{{% /button %}}

### Looping In Map Using For Each
In this example, you will see how to use a loop to print all the keys and values in Map.
```dart
void main(){

  Map<String, dynamic> book = {
    'title': 'Misson Mangal',
    'author': 'Kuber Singh',
    'page': 233
  };
  
  
 // Loop Through For Each
  book.forEach((key,value)=> print('Key is $key and value is $value'));
  
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Key is title and value is Misson Mangal
Key is author and value is Kuber Singh
Key is page and value is 233
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=6c033b4fe37e6cb770cc4dab19865fe9" style="blue" %}}Run Online{{% /button %}}

### Remove Where In Dart Map
In this example, you will see how to get students whose marks are greater or equal to 32 using where method.

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
{{% button href="https://dartpad.dev/?id=06e45a111a171f6a746dc5bc3266a2e9" style="blue" %}}Run Online{{% /button %}}
