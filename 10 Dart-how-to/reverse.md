+++
title = "Reverse a List in Dart"
weight = 6
keywords = ["reverse a list in dart", "reverse a list in dart programming", "reverse a list in dart programming language"]
description = "In this tutorial, you will learn how to reverse a list in Dart programming language."
+++

### Reverse a List In Dart
There are several ways to reverse a list in dart. Here are some of the most common approaches:

### Using reversed Method:
The reversed method returns an iterable that provides the reversed view of the list. You can convert this iterable to a list using the toList method. Here's an example:

```dart
List<int> numbers = [1, 2, 3, 4, 5];
List<int> reversedNumbers = numbers.reversed.toList();
print(reversedNumbers); // [5, 4, 3, 2, 1]
```

{{% expand "Show Output" "false" %}}
````plaintext
[5, 4, 3, 2, 1]
````
{{% /expand %}}

### Using List.from Constructor:
You can use the List.from constructor to create a new list from the original list and then call the reversed method on it. Here's an example:

```dart
List<int> numbers = [1, 2, 3, 4, 5];
List<int> reversedNumbers = List.from(numbers.reversed);
print(reversedNumbers); // [5, 4, 3, 2, 1]
```

{{% expand "Show Output" "false" %}}
````plaintext
[5, 4, 3, 2, 1]
````
{{% /expand %}}


### Using a Loop:
You can use a loop to iterate through the original list and add its elements to a new list in reverse order. Here's an example:

```dart
List<int> numbers = [1, 2, 3, 4, 5];
List<int> reversedNumbers = [];
for (int i = numbers.length - 1; i >= 0; i--) {
  reversedNumbers.add(numbers[i]);
}

print(reversedNumbers); // [5, 4, 3, 2, 1]
```

{{% expand "Show Output" "false" %}}
````plaintext
[5, 4, 3, 2, 1]
````
{{% /expand %}}

All of these approaches produce the same result, which is a new list that contains the elements of the original list in reverse order. You can choose the one that suits your needs and preferences best.