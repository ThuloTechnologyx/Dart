+++
title = "Function Parameter in Dart"
weight = 3
keywords = "dart positional parameter, dart named parameter, dart optional parameter, dart function parameter"
description = "In this tutorial you will learn everything about function parameters. You will learn positional parameter, named parameter, optional parameter in dart."
+++

## Parameter In Dart
The parameter is the process of passing values to the function. The values passed to the function must match the number of parameters defined. A function can have any number of parameters.

```dart
// here a and b are parameters
void add(int a, int b) { 
} 
```

## Positional Parameter In Dart
In positional parameters, you must supply the arguments in the same order as you defined on parameters when you wrote the function. If you call the function with the parameter in the wrong order, you will get the wrong result.

## Example 1: Use Of Positional Parameter
In the example below, the function **printInfo**  takes two parameters. You must pass the person's name and gender in the same order. If you pass values in the wrong order, you will get the **wrong result**.

```dart
void printInfo(String name, String gender) {
  print("Hello $name your gender is $gender.");
}

void main() {
  // passing values in wrong order
  printInfo("Male", "John");

  // passing values in correct order
  printInfo("John", "Male");

}
```
{{% expand "Show Output" "false" %}}
````plaintext
Hello Male your gender is John.
Hello John your gender is Male.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=c50e88acd2eceaf0a2881db5ce885537" style="blue" %}}{{% /button %}}

## Example 2: Providing Default Value On Positional Parameter
In the example below, function  **printInfo** takes two positional parameters and one optional parameter. The title parameter is optional here. If the user doesn't pass the title, it will automatically set the title value to **sir/ma'am**.
```dart
void printInfo(String name, String gender, [String title = "sir/ma'am"]) {
  print("Hello $title $name your gender is $gender.");
}

void main() {
  printInfo("John", "Male");
  printInfo("John", "Male", "Mr.");
  printInfo("Kavya", "Female", "Ms.");
}

```
{{% expand "Show Output" "false" %}}
````plaintext
Hello sir/ma'am John your gender is Male.
Hello Mr. John your gender is Male.
Hello Ms. Kavya your gender is Female.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=653300bb46e3d64ddcdc4f7ef6b562ed" style="blue" %}}{{% /button %}}

## Example 3: Providing Default Value On Positional Parameter
In the example below, function **add** takes two positional parameters and one optional parameter. The **num3** parameter is **optional** here with default value **0**. 

```dart
  void add(int num1, int num2, [int num3=0]){
   int sum;
  sum = num1 + num2 + num3;
   
   print("The sum is $sum");
}

void main(){
  add(10, 20);
  add(10, 20, 30);
}

```
{{% expand "Show Output" "false" %}}
````plaintext
The sum is 30
The sum is 60
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=ac8d5785455e8b199a416a2fca2f8870" style="blue" %}}{{% /button %}}

## Named Parameter In Dart
Dart allows you to use named parameters to clarify the parameter's meaning in function calls. **Curly braces {}** are used to specify named parameters.

## Example 1: Use Of Named Parameter
In the example below, function **printInfo** takes two named parameters. You can pass value in any order. You will learn about **?** in **[null safety](/null-safety)** section.  

```dart
void printInfo({String? name, String? gender}) {
  print("Hello $name your gender is $gender.");
}

void main() {
  // you can pass values in any order in named parameters.
  printInfo(gender: "Male", name: "John");
  printInfo(name: "Sita", gender: "Female");
  printInfo(name: "Reecha", gender: "Female");
  printInfo(name: "Reecha", gender: "Female");
  printInfo(name: "Harry", gender: "Male");
  printInfo(gender: "Male", name: "Santa");
}

```
{{% expand "Show Output" "false" %}}
````plaintext
Hello John your gender is Male.
Hello Sita your gender is Female.  
Hello Reecha your gender is Female.
Hello Reecha your gender is Female.
Hello Harry your gender is Male.   
Hello Santa your gender is Male.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=a182fb55543a14b269e470f3dd85780c" style="blue" %}}{{% /button %}}

## Example 2: Use Of Required In Named Parameter
In the example below, function **printInfo** takes two named parameters. You can see a **required** keyword, which means you must pass the person's name and gender. If you don't pass it, it won't work.

```dart
void printInfo({required String name, required String gender}) {
  print("Hello $name your gender is $gender.");
}

void main() {
  // you can pass values in any order in named parameters.
  printInfo(gender: "Male", name: "John");
  printInfo(gender: "Female", name: "Suju");
}

```
{{% expand "Show Output" "false" %}}
````plaintext
Hello John your gender is Male.
Hello Suju your gender is Female.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=1537acc3dbcecb6c9185479bff7ae5c1" style="blue" %}}{{% /button %}}

{{% notice info %}}

**Note**: You can pass the value in any order in the named parameter. **?** is used to remove null safety, which we will discuss in the coming chapter.
{{% /notice %}}


## Optional Parameter In Dart
Dart allows you to use optional parameters to make the parameter optional in function calls. **Square braces []** are used to specify optional parameters.

## Example: Use Of Optional Parameter
In the example below, function **printInfo** takes two **positional parameters** and one **optional parameter**. First, you must pass the person's name and gender. The title parameter is optional here. Writing **[String? title]** makes **title** optional.

```dart
void printInfo(String name, String gender, [String? title]) {
  print("Hello $title $name your gender is $gender.");
}

void main() {
  printInfo("John", "Male");
  printInfo("John", "Male", "Mr.");
  printInfo("Kavya", "Female", "Ms.");
}

```
{{% expand "Show Output" "false" %}}
````plaintext
Hello  John your gender is Male.
Hello Mr. John your gender is Male.
Hello Ms. Kavya your gender is Female.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=f0ddca7f46b3d642394eb0d5e96e8606" style="blue" %}}{{% /button %}}
