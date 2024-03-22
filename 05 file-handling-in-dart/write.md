+++
title = "Write File in Dart"
weight = 2
description = "In this section, you will learn how to write file in dart programming language. You will learn how to write file in dart using File class and writeAsStringSync() method."
keywords = "write file in dart, write file in dart programming, write file in dart programming language"
+++

### Introduction
In this section, you will learn how to write file in dart programming language by using **File** class and **writeAsStringSync()** method.

### Write File In Dart
Let's create a file named **test.txt** in the same directory of your dart program and write some text in it.

```dart
// dart program to write to file
import 'dart:io';

void main() {
  // open file
  File file = File('test.txt');
  // write to file
  file.writeAsStringSync('Welcome to test.txt file.');
  print('File written.');
}
```

{{% expand "Show Output" "false" %}}
````plaintext
File written.
````
{{% /expand %}}

{{% notice info %}}
**Note**: If you have already some content in **test.txt** file, then it will be removed and replaced with new content.
{{% /notice %}}

### Add New Content To Previous Content 
You can use **FileMode.append** to add new content to previous content. Assume that **test.txt** file already contains some text.
```text
Welcome to test.txt file.
```

Now, let's add new content to it.

```dart
// dart program to write to existing file
import 'dart:io';

void main() {
  // open file
  File file =  File('test.txt');
  // write to file
  file.writeAsStringSync('\nThis is a new content.', mode: FileMode.append);
  print('Congratulations!! New content is added on top of previous content.');
}
```

{{% expand "Show Output" "false" %}}
````plaintext
Congratulations!! New content is added on top of previous content.
````
{{% /expand %}}


### Write CSV File In Dart
In the example below, we will ask user to enter **name** and **phone** of 3 students and write it to a csv file named **students.csv**.

```dart
// dart program to write to csv file
import 'dart:io';

void main() {
  // open file
  File file = File("students.csv");
  // write to file
  file.writeAsStringSync('Name,Phone\n');
  for (int i = 0; i < 3; i++) {
    // user input name
    stdout.write("Enter name of student ${i + 1}: ");
    String? name = stdin.readLineSync();
    stdout.write("Enter phone of student ${i + 1}: ");
    // user input phone
    String? phone = stdin.readLineSync();
    file.writeAsStringSync('$name,$phone\n', mode: FileMode.append);
  }
  print("Congratulations!! CSV file written successfully.");
}
```

{{% expand "Show Output" "false" %}}
````plaintext
Enter name of student 1: John 
Enter phone of student 1: 1234567890
Enter name of student 2: Mark
Enter phone of student 2: 0123456789
Enter name of student 3: Elon
Enter phone of student 3: 0122112322
Congratulations!! CSV file written successfully.
````
{{% /expand %}}

**students.csv** file will look like this:

```text
Name,Phone
John,1234567890
Mark,0123456789
Elon,0122112322
```

{{% notice info %}}
**Note**: You can create any type of file using **writeAsStringSync()** method. For example, **.html**, **.json**, **.xml**, etc.
{{% /notice %}}

### Video
Watch our video on file write in Dart.
{{< youtube MQkJ4_2If0U >}}