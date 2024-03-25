+++
title = "String in Dart"
weight = 9
description = "String data types help you to store text data. In String, you can represent your name, address, or complete book. Here you will learn the properties and methods of strings in dart with examples."
keywords = "dart string, string in dart, string methods dart, string properties dart"
+++

## String In Dart
**String** helps you to store text based data. In String, you can represent your name, address, or complete book. It holds a series or sequence of characters – letters, numbers, and special characters. You can use single or double, or triple quotes to represent String. 

## Example: String In Dart
Single line String is written in single or double quotes, whereas multi-line strings are written in triple quotes. Here is an example of it:
```dart
void main() {   
   String text1 = 'This is an example of a single-line string.';   
   String text2 = "This is an example of a single line string using double quotes.";   
   String text3 = """This is a multiline line   
string using the triple-quotes.
This is tutorial on dart strings.
""";   
   print(text1);  
   print(text2);   
   print(text3);   
}
```
{{% expand "Show Output" "false" %}}
```plaintext
This is an example of a single-line string.
This is an example of a single line string using double quotes.
This is a multiline line   
string using the triple-quotes.
This is tutorial on dart strings.
```
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=98343eaef6355c68aca7e4974822d071" style="blue" %}}{{% /button %}}

## String Concatenation
You can combine one String with another string. This is called concatenation. In Dart, you can use the `+` operator or use **interpolation** to concatenate the String. Interpolation makes it easy to read and understand the code.

## String Concatenation In Dart
```dart
void main() {   
String firstName = "John";
String lastName = "Doe";
print("Using +, Full Name is "+firstName + " " + lastName+".");
print("Using interpolation, full name is $firstName $lastName.");  
  
}
```
{{% expand "Show Output" "false" %}}
```plaintext
Using +, Full Name is John Doe.
Using interpolation, full name is John Doe.
```
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=86778de0ea749b74bac9ef6a09976373" style="blue" %}}{{% /button %}}
## Properties Of String
*   **codeUnits**: Returns an unmodifiable list of the UTF-16 code units of this string.
*   **isEmpty**: Returns true if this string is empty.
*   **isNotEmpty**: Returns false if this string is empty.
*   **length**: Returns the length of the string including space, tab, and newline characters.

## String Properties Example In Dart

```dart
void main() {
   String str = "Hi";
   print(str.codeUnits);   //Example of code units
   print(str.isEmpty);     //Example of isEmpty
   print(str.isNotEmpty);  //Example of isNotEmpty
   print("The length of the string is: ${str.length}");   //Example of Length
}
``` 
{{% expand "Show Output" "false" %}}
```plaintext
[72, 105]
false
true
The length of the String is: 2
```
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=4429e532e9d48e34dadc990a8fcd8432" style="blue" %}}{{% /button %}}

## Methods Of String
*   **toLowerCase()**: Converts all characters in this string to lowercase.
*   **toUpperCase()**: Converts all characters in this string to uppercase.
*   **trim()**: Returns the string without any leading and trailing whitespace.
*   **compareTo()**: Compares this object to another.
*   **replaceAll()**: Replaces all substrings that match the specified pattern with a given 
                      value.
*   **split()**: Splits the string at matches of the specified delimiter and returns a list of 
                 substrings.
*   **toString()**: Returns a string representation of this object.
*   **substring()**:    Returns the text from any position you want.
*   **codeUnitAt()**: Returns the 16-bit UTF-16 code unit at the given index.                    

<!-- Is Empty and iS Not Empty -->

## String Methods Example In Dart
Here you will see various string methods that can help your work a lot better and faster.


## Converting String To Uppercase and Lowercase
You can convert your text to lower case using .toLowerCase() and convert to uppercase using .toUpperCase() method.
```dart
//Example of toUpperCase() and toLowerCase()
void main() { 
   String address1 = "Florida"; // Here F is capital
   String address2 = "TexAs"; // Here T and A are capital
   print("Address 1 in uppercase: ${address1.toUpperCase()}"); 
   print("Address 1 in lowercase: ${address1.toLowerCase()}"); 
   print("Address 2 in uppercase: ${address2.toUpperCase()}"); 
   print("Address 2 in lowercase: ${address2.toLowerCase()}"); 
}
```
{{% expand "Show Output" "false" %}}
```plaintext
Address 1 in uppercase: FLORIDA
Address 1 in lowercase: florida
Address 2 in uppercase: TEXAS
Address 2 in lowercase: texas
```
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=e3d44f31ed56d0eaf18f05474a603b3f" style="blue" %}}{{% /button %}}

## Trim String In Dart
Trim is helpful when removing leading and trailing spaces from the text. This trim method will remove all the starting and ending spaces from the text. You can also use **trimLeft()** and **trimRight()** methods to remove space from left and right, respectively. 

{{% notice info %}}
**Note**: The trim() method in Dart doesn’t remove spaces in the middle. 
{{% /notice %}}
```dart
//Example of trim()
void main() { 
  String address1 = " USA"; // Contain space at leading.
  String address2 = "Japan  "; // Contain space at trailing. 
  String address3 = "New Delhi"; // Contains space at middle.
  
  print("Result of address1 trim is ${address1.trim()}");
  print("Result of address2 trim is ${address2.trim()}");
  print("Result of address3 trim is ${address3.trim()}");
  print("Result of address1 trimLeft is ${address1.trimLeft()}");
  print("Result of address2 trimRight is ${address2.trimRight()}");
}

``` 
{{% expand "Show Output" "false" %}}
```plaintext
Result of address1 trim is USA
Result of address2 trim is Japan
Result of address3 trim is New Delhi
Result of address1 trimLeft is USA
Result of address2 trimRight is Japan
```
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=7a187a4b42a82eeb36bea536322a7f91" style="blue" %}}{{% /button %}}

## Compare String In Dart
In Dart, you can compare two strings. It will give the result 0 when two texts are equal, 1 when the first String is greater than the second, and -1 when the first String is smaller than the second.

```dart
//Example of compareTo()
void main() { 
   String item1 = "Apple"; 
   String item2 = "Ant"; 
   String item3 = "Basket"; 
   
   print("Comparing item 1 with item 2: ${item1.compareTo(item2)}"); 
   print("Comparing item 1 with item 3: ${item1.compareTo(item3)}"); 
   print("Comparing item 3 with item 2: ${item3.compareTo(item2)}"); 
} 

``` 
{{% expand "Show Output" "false" %}}
```plaintext
Comparing item 1 with item 2: 1
Comparing item 1 with item 3: -1
Comparing item 3 with item 2: 1
```
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=1f32270ac5f3b3d76081e304146ce852" style="blue" %}}{{% /button %}}

## Replace String In Dart
You can replace one value with another with the replaceAll("old", "new") method in Dart. It will replace all the "old" words with "new". Here in this example, this will replace milk with water.

```dart
//Example of replaceAll()
void main() { 
String text = "I am a good boy I like milk. Doctor says milk is good for health.";
  
String newText = text.replaceAll("milk", "water"); 
 
print("Original Text: $text");
print("Replaced Text: $newText");  
   
} 
``` 
{{% expand "Show Output" "false" %}}
```plaintext
Original Text: I am a good boy I like milk. Doctor says milk is good for health.
Replaced Text: I am a good boy I like water. Doctor says water is good for health.
```
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=3e879e575f5fa52dcda400ada387bed9" style="blue" %}}{{% /button %}}

## Split String In Dart
You can use the dart split method if you want to split String by comma, space, or other text. It will help you to split String to list. 

```dart
//Example of split()
void main() { 
  String allNames = "Ram, Hari, Shyam, Gopal";

  List<String> listNames = allNames.split(",");
  print("Value of listName is $listNames");

  print("List name at 0 index ${listNames[0]}");
  print("List name at 1 index ${listNames[1]}");
  print("List name at 2 index ${listNames[2]}");
  print("List name at 3 index ${listNames[3]}");
   
} 
```
{{% expand "Show Output" "false" %}}
```plaintext
Value of listName is [Ram,  Hari,  Shyam,  Gopal]
List name at 0 index Ram
List name at 1 index  Hari
List name at 2 index  Shyam
List name at 3 index  Gopal
```
{{% /expand %}} 
{{% button href="https://dartpad.dev/?id=7ac857ea9296eab61337d6ef488de4b6" style="blue" %}}{{% /button %}}

## ToString In Dart
In dart, toString() represents String representation of the value/object.
 
```dart
//Example of toString()
void main() { 
int number = 20;     
String result = number.toString(); 
  
print("Type of number is ${number.runtimeType}");  
print("Type of result is ${result.runtimeType}");  
    
}   
``` 
{{% expand "Show Output" "false" %}}
```plaintext
Type of number is int
Type of result is String
```
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=ff6f11ae46f404acff251dcdfa7f0c38" style="blue" %}}{{% /button %}}

## SubString In Dart
You can use substring in Dart when you want to get a text from any position. 
```dart
//Example of substring()
void main() { 
   String text = "I love computer"; 
   print("Print only computer: ${text.substring(7)}"); // from index 6 to the last index 
   print("Print only love: ${text.substring(2,6)}");// from index 2 to the 6th index 
} 
``` 
{{% expand "Show Output" "false" %}}
```plaintext
Print only computer: computer
Print only love: love
```
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=0a0646a66f9918cc35adcc4b2acc44e0" style="blue" %}}{{% /button %}}

## Reverse String In Dart
If you want to reverse a String in Dart, you can reverse it using a different solution. One solution is here. 

```dart
void main() { 
  String input = "Hello"; 
  print("$input Reverse is ${input.split('').reversed.join()}"); 
} 
``` 
{{% expand "Show Output" "false" %}}
```plaintext
Hello Reverse is olleH
```
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=6749681d9189498c78067e5c2ba945b3" style="blue" %}}{{% /button %}}


## How To Capitalize First Letter Of String In Dart
If you want to capitalize the first letter of a String in Dart, you can use the following code. 

```dart
//Example of capitalize first letter of String
void main() { 
  String text = "hello world"; 
  print("Capitalized first letter of String: ${text[0].toUpperCase()}${text.substring(1)}"); 
} 
``` 
{{% expand "Show Output" "false" %}}
```plaintext
Capitalized first letter of String: Hello world
```
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=b35aec750e198f194c863c1ddf76de2e" style="blue" %}}{{% /button %}}
