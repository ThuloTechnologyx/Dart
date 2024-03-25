+++
title = "Delete File in Dart"
weight = 3
description = "In this section, you will learn how to delete file in dart programming language. You will learn how to delete file in dart using File class and deleteSync() method."
keywords = "delete file in dart, delete file in dart programming, delete file in dart programming language"
+++

## Introduction
In this section, you will learn how to delete file in dart programming language using **File** class and **deleteSync()** method.

## Delete File In Dart
Assume that you have a file named **test.txt** in the same directory of your dart program. Now, let's delete it.

```dart
// dart program to delete file
import 'dart:io';

void main() {
  // open file
  File file = File('test.txt');
  // delete file
  file.deleteSync();
  print('File deleted.');
}
```

{{% expand "Show Output" "false" %}}
````plaintext
File deleted.
````
{{% /expand %}}

{{% notice info %}}
**Note**: If you try to delete a file that does not exist, then it will throw an exception.
{{% /notice %}}

## Delete File If Exists
You can use **File.existsSync()** method to check if a file exists or not. If it exists, then you can delete it.

```dart
// dart program to delete file if exists
import 'dart:io';

void main() {
  // open file
  File file = File('test.txt');
  // check if file exists
  if (file.existsSync()) {
    // delete file
    file.deleteSync();
    print('File deleted.');
  } else {
    print('File does not exist.');
  }
}
```

{{% expand "Show Output" "false" %}}
````plaintext
File does not exist.
````
{{% /expand %}}
