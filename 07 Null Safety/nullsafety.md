+++
title = "Null Safety in Dart"
weight = 1
description = "Learn about the null safety in dart programming language with examples."
keywords = "dart null safety, null safety in dart, learn dart programming, null in dart, learn dart null safety"
+++

## Null Safety
**Null safety** is a feature in the Dart programming language that helps developers to avoid null errors. This feature is called **Sound Null Safety** in dart. This allows developers to catch null errors at edit time.

## Advantage Of Null Safety
- Write safe code.
- Reduce the chances of application crashes.
- Easy to find and fix bugs in code.

{{% notice info %}}
**Note**: Null safety avoids null errors, runtime bugs, vulnerabilities, and system crashes which are difficult to find and fix.
{{% /notice %}}

## Example 1: Using Null In Variables
In the example below, the variable **age** is a **int** type. If you pass a null value to this variable, it will give an error instantly.
```dart
void main() { 
   int age = null; // give error
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Error: Compilation failed.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=881e97181f24a5aea1444f5f614b1028" style="blue" %}}{{% /button %}}


## Problem With Null
Programmers do have a lot of difficulties while handling null values. They forget that there are **null** values, so the program breaks. In real world **null** mostly acts as **time bomb** for programmers, which is ready to break the program. 

{{% notice info %}}
**Note**: Common cause of errors in programming generally comes from not correctly handling null values.
{{% /notice %}}

## Non-Nullable By Default
In Dart, variables and fields are non-nullable by default, which means that they cannot have a value **null** unless you explicitly allow it. 

```dart
int productid = 20; // non-nullable
int productid = null; // give error
``` 

## How To Declare Null Value
With dart **sound null Safety**, you cannot provide a null value by **default**. If you are 100% sure to use it, then you can use **?** operator after the type declaration.

```dart
// Declaring a nullable variable by using ?
String? name;
``` 
This declares a variable **name**, which can be null or a string.

## How To Assign Values To Nullable Variables
You can assign a value to nullable variables just like any other variable. However, you can also assign null to them.
  
```dart
void main(){
// Declaring a nullable variable by using ?
String? name;
// Assigning John to name
name = "John";
// Assigning null to name
name = null;
}
```
{{% expand "Show Output" "false" %}}
````plaintext
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=538c21384ddad080b760f78c0807e780" style="blue" %}}{{% /button %}}
## How To Use Nullable Variables
You can use nullable variables in many ways. Some of them are shown below:
- You can use **if** statement to check whether the variable is null or not.
- You can use **!** operator, which returns null if the variable is null.
- You can use **??** operator to assign a default value if the variable is null.
  
```dart
void main(){
// Declaring a nullable variable by using ?
String? name;
// Assigning John to name
name = "John";
// Assigning null to name
name = null;
// Checking if name is null using if statement
if(name == null){
print("Name is null");
}
// Using ?? operator to assign a default value
String name1 = name ?? "Stranger";
print(name1);
// Using ! operator to return null if name is null
String name2 = name!;
print(name2);
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Name is null
Stranger
Uncaught TypeError: Cannot read properties of null (reading 'toString')Error: TypeError: Cannot read properties of null (reading 'toString')
````  
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=0b97978a7e5d8a4f830d9bb2648c65a9" style="blue" %}}{{% /button %}}

## Example 2: Define List Of Nullable Items
You can also store null in list values. In this example, the **items** is a list of nullable integers. It can contain null values as well as integers.

```dart
void main() {
  // list of nullable ints
  List<int?> items = [1, 2, null, 4];
  print(items);
}
```
{{% expand "Show Output" "false" %}}
````plaintext
[1, 2, null, 4]
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=6f9d091e5642c9af8e2ee73ad24d05c1" style="blue" %}}{{% /button %}}

## Example 3: Null Safety In Dart Functions
In this example, the function **printAddress** has a parameter **address** which is a **String** type. If you pass a **null** value to this function, it will give a edit-time error.

```dart
void printAddress(String address) {
  print(address);
}

void main() {
  printAddress(null); // give error
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Error: Compilation failed.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=012c547e1a4fec99b817820da3aafcaf" style="blue" %}}{{% /button %}}

## Example 4: Define Function With Nullable Parameter
If you are 100% sure, then you can use **?** for the type declaration. In this example, the function **printAddress** has a parameter **address**, which is a **String?** type. You can pass both null and string values to this function.

```dart
// address is a nullable string
void printAddress(String? address) {
  print(address);
}
void main() {
  // Passing null to printAddress
  printAddress(null); // Works
}
```
{{% expand "Show Output" "false" %}}
````plaintext
null
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=3f81104be1ca39800bc5b87a14883296" style="blue" %}}{{% /button %}}

## Example 5: Null Safety In Dart Classes
In the example, the class **Person** has a parameter **name**, which is a **String** type. If you pass a null value to this class, it will give a compile-time error.

```dart
class Person {
  String name;
  Person(this.name);
}

void main() {
  Person person = Person(null); // give error
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Error: Compilation failed.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=1035bcaf9f4b6e7cc029bddef1f206a7" style="blue" %}}{{% /button %}}

## Example 6: Define Null To Class Property
In this example, the class **Person** has a parameter **name**, which is a **String?** type. You can pass both null and string values to this class. To define a nullable property in a class, you can use the **?** operator after the type.

```dart
class Person {
  String? name;
  Person(this.name);
}

void main() {
  Person person = Person(null); // Works
}
```
{{% expand "Show Output" "false" %}}
````plaintext
null
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=be9d889764e72caa642a03a0e66118c8" style="blue" %}}{{% /button %}}

## Example 7: Working With Nullable Class Properties
In the example below, the **Profile** class has two nullable properties: **name** and **bio**. The **printProfile** method prints the name and bio of the profile. If the name or bio is **null**, it prints a default value instead.
  
```dart
  class Profile {
  String? name;
  String? bio;

  Profile(this.name, this.bio);

  void printProfile() {
    print("Name: ${name ?? "Unknown"}");
    print("Bio: ${bio ?? "None provided"}");
  }
}

void main() {
  // Create a profile with a name and bio
  Profile profile1 = Profile("John", "Software engineer and avid reader");
  profile1.printProfile();

  // Create a profile with only a name
  Profile profile2 = Profile("Jane", null);
  profile2.printProfile();

  // Create a profile with only a bio
  Profile profile3 = Profile(null, "Loves to travel and try new foods");
  profile3.printProfile();

  // Create a profile with no name or bio
  Profile profile4 = Profile(null, null);
  profile4.printProfile();
}

```
{{% expand "Show Output" "false" %}}
````plaintext
Name: John
Bio: Software engineer and avid reader
Name: Jane
Bio: None provided
Name: Unknown
Bio: Loves to travel and try new foods
Name: Unknown
Bio: None provided
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=0d1f63452df10a633be7e83b61980a07" style="blue" %}}{{% /button %}}

## Important Point In Dart Null Safety
- Null means no value.
- Common error in programming is caused due to null.
- Dart 2.12 introduced **sound null Safety** to solve null problems.
- Non-nullable type is confirmed never to be **null**.

{{% notice info %}}
**Note**: Sometimes you heard word like **NNBD**. It is **Non-Nullable By Default**, which means you can't assign null to a variable by default.
{{% /notice %}}
