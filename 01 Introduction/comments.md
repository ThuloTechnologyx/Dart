+++
title = "Comments in Dart"
weight = 6
description = "Learn about dart comments and how to comment in dart with a single line, multi-line, and documentation comments."
keywords = "dart comments, comments in dart, how to comment in dart, single line dart comments, multi line dart comments."
+++
## Comments
**Comments** are the set of statements that are ignored by the dart compiler during program execution. They are used to explain the code so that you or other people can understand it easily.

## Advantages Of Comments
- You can describe your code. 
- Other people will understand your code more clearly.

## Types Of Comments

*   **Single-Line Comment**: For commenting on a single line of code. E.g. // This is a single-line comment.
*   **Multi-Line Comment**: For commenting on multiple lines of code. E.g. /\* This is a multi-line comment. \*/
*   **Documentation Comment**: For generating documentation or reference for a project/software package. E.g. /// This is a documentation comment

## Single-Line Comment In Dart
Single line comments start with `//` in dart. You can write `//` and your text. 

```dart
void main() {
// This is single-line comment.
print("Welcome to Technology Channel.");
}
```

{{% expand "Show Output" "false" %}}
````plaintext
Welcome to Technology Channel.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=f8153241044e41577862f9188f267919" style="blue" %}}Run Online{{% /button %}}

## Multi-Line Comment In Dart
Multi-line comments start with `/*` and end with `*/` . You can write your comment inside `/*` and `*/`. 

```dart
void main(){  
/*
This is a multi-line comment.
*/
    print("Welcome to Technology Channel.");  
}  
```
{{% expand "Show Output" "false" %}}
````plaintext
Welcome to Technology Channel.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=94d21f0d4b06b35c8c9c66154641a1c1" style="blue" %}}Run Online{{% /button %}}

## Documentation Comment In Dart
Documentation comments are helpful when you are writing documentation for your code. Documentation comments start with `///` in dart.

```dart
void main(){  
/// This is documentation comment
    print("Welcome to Technology Channel.");  
}  
```
{{% expand "Show Output" "false" %}}
````plaintext
Welcome to Technology Channel.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=5b319f342606afa2ccff957cb2b4ee0d" style="blue" %}}Run Online{{% /button %}}

