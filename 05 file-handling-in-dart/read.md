+++
title = "Read File in Dart"
weight = 1
description = "In this section, you will learn how to read file in dart programming language."
keywords = "read file in dart, read file in dart programming, read file in dart programming language"
+++

### Introduction To File Handling
File handling is an important part of any programming language. In this section, you will learn how to read the file in a dart programming language.

### Read File In Dart
Assume that you have a file named `test.txt` in the same directory of your dart program.

```text
Welcome to test.txt file.
This is a test file.
```

Now, you can read this file using **File** class and **readAsStringSync()** method.
```dart
// dart program to read from file
import 'dart:io';

void main() {
  // creating file object
  File file = File('test.txt');
  // read file
  String contents = file.readAsStringSync();
  // print file
  print(contents);
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Welcome to test.txt file.
This is a test file.
````
{{% /expand %}}

### Get File Information
In this example below, you will learn how to get file information like file location, file size, and last modified time.
```dart
import 'dart:io';

void main() {
  // open file
  File file = File('test.txt');
  // get file location
  print('File path: ${file.path}');
  // get absolute path
  print('File absolute path: ${file.absolute.path}');
  // get file size
  print('File size: ${file.lengthSync()} bytes');
  // get last modified time
  print('Last modified: ${file.lastModifiedSync()}');
}
```
{{% expand "Show Output" "false" %}}
````plaintext
File path: test.txt
File absolute path: /home/iambrp/Desktop/Dart Practice/test.txt
File size: 25 bytes
Last modified: 2023-01-28 11:00:32.000
````
{{% /expand %}}

{{% notice info %}}
**Note**: If you try to get information of a file that does not exist, then it will throw an exception.
{{% /notice %}}

### CSV File
A CSV (**Comma Separated Values**) file is a plain text file that contains data organized in a table format, where columns are separated by commas and rows are separated by line breaks. CSV files are used for:
- Data exchange between different applications.
- Data backup and restore.
- Importing and exporting data from databases.
- Automation of data processing tasks.

### Read CSV File In Dart 
Assume that you have a CSV file named `test.csv` in the same directory of your dart program.

```text
Name,Email,Phone
John, john@gmail.com, 1234567890
Smith, smith@gmail.com, 0987654321
```

Now, you can read this file using **File** class and **readAsStringSync()** method. We will use **split()** method to split the string into a list of strings.

```dart
// dart program to read from csv file
import 'dart:io';

void main() {
  // open file
  File file = File('test.csv');
  // read file
  String contents = file.readAsStringSync();
  // split file using new line
  List<String> lines = contents.split('\n');
  // print file
  print('---------------------');
  for (var line in lines) {
    print(line);
  }
}
```
{{% expand "Show Output" "false" %}}
````plaintext
---------------------
Name,Email,Phone
John, john@gmail.com, 1234567890
Smith, smith@gmail.com, 0987654321
````
{{% /expand %}}

### Read Only Part Of File
You can read only part of file using **substring()** method. Here is an example to read only first 10 characters of file. Make sure that you have a file named **test.txt** in the same directory of your dart program.

```text
Welcome to test.txt file
This is a test file.
```

```dart
// dart program to read from file
import 'dart:io';

void main() {
  // open file
  File file = new File('test.txt');
  // read only first 10 characters
  String contents = file.readAsStringSync().substring(0, 10);
  // print file
  print(contents);
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Welcome to
````
{{% /expand %}}

### Read File From Specific Directory
To read a file from a specific directory, you need to provide the full path of the file. Here is an example to read file from a specific directory. 
```dart
// dart program to read from file
import 'dart:io';

void main() {
  // open file
  File file = File('C:\\Users\\test.txt');
  // read file
  String contents = file.readAsStringSync();
  // print file
  print(contents);
}
```
{{% expand "Show Output" "false" %}}
````plaintext
Welcome to test.txt file.
This is a test file.
````
{{% /expand %}}
