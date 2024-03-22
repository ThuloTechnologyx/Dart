
+++
title = "Do While Loop in Dart"
weight = 9
description = "Looping is repeating a specific set of commands until conditions are not completed. Learn to use do while loop in dart"
keywords = "dart do while loop, do while loop in dart."
+++

### Do While Loop
Do while loop is used to run a block of code multiple times. The loop's body will be executed first, and then the condition is tested. The syntax of do while loop is:
```dart
do{
    statement1;
    statement2;
    .
    .
    .
    statementN;
}while(condition);
``` 

- First, it runs statements, and finally, the condition is checked.
- If the condition is true, the code inside {} is executed.
- The condition is re-checked until the condition is false.
- When the condition is false, the loop stops.

{{% notice info %}}
**Note**: In a do-while loop, the statements will be executed at least once time, even if the condition is false. It is because the statement is executed before checking the condition.
{{% /notice %}}

### Example 1: To Print 1 To 10 Using Do While Loop

```dart
void main() {
  int i = 1;
  do {
    print(i);
    i++;
  } while (i <= 10);
}

``` 
{{% expand "Show Output" "false" %}}
````plaintext
1
2
3
4
5
6
7
8
9
10
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=e0b267d2ae5f1c3112b4b416742b3aef" style="blue" %}}Run Online{{% /button %}} 
### Example 2: To Print 10 To 1 Using Do While Loop
```dart
void main() {
  int i = 10;
  do {
    print(i);
    i--;
  } while (i >= 1);
}

``` 
{{% expand "Show Output" "false" %}}
````plaintext
10
9
8
7
6
5
4
3
2
1
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=74f04a1a9a92579854d55c40b2e88875" style="blue" %}}Run Online{{% /button %}} 

### Example 3: Display Sum of n Natural Numbers Using Do While Loop
Here, the value of the **total** is 0 initially. Then, the do-while loop is iterated from **i = 1 to 100**. In each iteration,  **i** is added to the total, and the value of **i** is increased by 1. Result is **1+2+3+....+99+100**.
```dart
void main(){

  int total = 0;
  int n = 100; // change as per required
  int i =1;
  
  do{
  total = total + i;
    i++;
  }while(i<=n);
  
  print("Total is $total");
  
}
``` 
{{% expand "Show Output" "false" %}}
````plaintext
Total is 5050
````
{{% /expand %}} 
{{% button href="https://dartpad.dev/?id=0eed00a17e46465d02cbdadf71ff287a" style="blue" %}}Run Online{{% /button %}} 



### When The Condition Is False
Let's make one condition false and see the demo below. **Hello** got printed if the condition is false.

```dart
void main(){

  int number = 0;
  
  do{
  print("Hello");
  number--;
  }while(number >1);
  
}
``` 
{{% expand "Show Output" "false" %}}
````plaintext
Hello
````
{{% /expand %}} 
{{% button href="https://dartpad.dev/?id=25463e567eb5d7b465befd97eb2ebe25" style="blue" %}}Run Online{{% /button %}} 
