+++
title = "Extension In Dart"
weight = 3
description = "In this tutorial, you will learn about extension in Dart programming language. You will learn how to use extension in Dart programming language."
keywords = "dart extension, extension in dart, learn dart programming, dart extension, learn dart extension"
+++

### Dart Extension Method
In Dart, you can extend the functionality of a class by using extension. It is a new feature in Dart 2.7.0. It is similar to extension methods in C# and Kotlin. It is also similar to the concept of mixins in Dart.

### How To Use Extension In Dart
Here we are extending the functionality of **String** class. We are adding a new method **capitalize** to the **String** class. We are using **extension** keyword to extend the functionality of **String** class.

```dart
void main(){
  String name = "john";
  print(name.capitalize());
}

extension StringExtension on String{
  String capitalize(){
    return "${this[0].toUpperCase()}${this.substring(1)}";
  }
}
```
{{% expand "Show Output" "false" %}}
````plaintext
John
````
{{% /expand %}}

### Watch Video
Watch this video to learn more about extension in Dart programming language.
{{< youtube D3j0OSfT9ZI >}}
