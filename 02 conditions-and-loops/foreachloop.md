
+++
title = "For Each Loop in Dart"
weight = 7
description = "Learn what is for each loop and how to use it."
keywords = "dart for each loop, for each loop in the dart, dart for loops explained."
+++

## For Each Loop
The **for each** loop iterates over all list elements or variables. It is useful when you want to loop through **list/collection**. The syntax of for-each loop is:
 ```dart
collection.forEach(void f(value));
``` 


## Example1: Print Each Item Of List Using Foreach
This will print each name of football players.
```dart
void main(){
  List<String> footballplayers=['Ronaldo','Messi','Neymar','Hazard'];
  footballplayers.forEach( (names)=>print(names));
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Ronaldo
Messi
Neymar
Hazard
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=98b00ed40ea3f320ca9293ea8008eb3d" style="blue" %}}{{% /button %}}   

## Example2: Print Each Total and Average Of Lists 
This program will print the total sum of all numbers and also the average value from the total.
```dart
void main(){
  List<int> numbers = [1,2,3,4,5];
  
  int total = 0;
  
   numbers.forEach( (num)=>total= total+ num);
  
  print("Total is $total.");
  
  double avg = total / (numbers.length);
  
  print("Average is $avg.");
  
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Total is 15.
Average is 3.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=2862b491ddf133b378efc286d7abb19f" style="blue" %}}{{% /button %}}   

## For In Loop In Dart
There is also another for loop, i.e., **for in loop**. It also makes looping over the list very easily.
```dart
void main(){
    List<String> footballplayers=['Ronaldo','Messi','Neymar','Hazard'];

  for(String player in footballplayers){
    print(player);
  }
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Ronaldo
Messi
Neymar
Hazard
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=40945de9addd2ff387f9e27b9e25c843" style="blue" %}}{{% /button %}}   


## How to Find Index Value Of List
In dart, asMap method converts the list to a map where the keys are the index and values are the element at the index.
```dart
void main(){

List<String> footballplayers=['Ronaldo','Messi','Neymar','Hazard'];

footballplayers.asMap().forEach((index, value) => print("$value index is $index"));

}
```
{{% expand "Show Output" "false" %}}
````plaintext
Ronaldo index is 0
Messi index is 1
Neymar index is 2
Hazard index is 3
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=29748f257fd8df51a075558e936311f4" style="blue" %}}{{% /button %}}   


## Example: Print Unicode Value of Each Character of String 
This will split the name into Unicode values and then find characters from the Unicode value. 

```dart
void main(){
  
  String name = "John";
     
for(var codePoint in name.runes){
  print("Unicode of ${String.fromCharCode(codePoint)} is $codePoint.");
}
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Unicode of J is 74.
Unicode of o is 111.
Unicode of h is 104.
Unicode of n is 110.
````
{{% /expand %}} 
{{% button href="https://dartpad.dev/?id=1995b53502871e59bb7538fc7a4f6399" style="blue" %}}{{% /button %}} 
