
+++
title = "While Loop in Dart"
weight = 8
description = "Looping is repeating a specific set of commands until conditions are not completed. We have different types of loop in dart."
keywords = "Loops in dart, for loop in dart, for loop in dart, while loop in dart, do while loop in dart"
+++


### While Loop
In **while loop**, the loop's body will run until and unless the condition is true. You must write conditions first before statements. This loop checks conditions on every iteration. If the condition is true, the code inside {} is executed, if the condition is false, then the loop stops. 

### Syntax
```dart
while(condition){  
       //statement(s);  
      // Increment (++) or Decrement (--) Operation;  
}  
``` 

- A while loop evaluates the condition inside the parenthesis ().
- If the condition is true, the code inside {} is executed.
- The condition is re-checked until the condition is false.
- When the condition is false, the loop stops.

### Example 1: To Print 1 To 10 Using While Loop 
This program prints 1 to 10 using while loop.
```dart
void main() {
  int i = 1;
  while (i <= 10) {
    print(i);
    i++;
  }
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
{{% button href="https://dartpad.dev/?id=bb416850916a0cbb9583db9df249f724" style="blue" %}}Run Online{{% /button %}}    
{{% notice info %}}
**Note**: Do not forget to increase the variable used in the condition. Otherwise, the loop will never end and becomes an infinite loop.
{{% /notice %}}

### Example 2: To Print 10 To 1 Using While Loop 
This program prints 10 to 1 using while loop.

```dart
void main() {
  int i = 10;
  while (i >= 1) {
    print(i);
    i--;
  }
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
{{% button href="https://dartpad.dev/?id=e4746918a3950ee10e718224f044d0bd" style="blue" %}}Run Online{{% /button %}}    


### Example 3: Display Sum of n Natural Numbers Using While Loop
Here, the value of the total is 0 initially. Then, the while loop is iterated from **i = 1 to 100**. In each iteration,  **i** is added to the total, and the value of **i** is increased by 1. Result is **1+2+3+....+99+100**.
```dart
void main(){

  int total = 0;
  int n = 100; // change as per required
  int i =1;

  while(i<=n){
    total = total + i;
    i++;
  }
  
  print("Total is $total");
  
}
``` 
{{% expand "Show Output" "false" %}}
````plaintext
Total is 5050
````
{{% /expand %}} 
{{% button href="https://dartpad.dev/?id=f266b4ae5649fc7ba8f94ef0405de86d" style="blue" %}}Run Online{{% /button %}}    

### Example 4: Display Even Numbers Between 50 to 100 Using While Loop
This program will print even numbers between 50 to 100 using while loop.
```dart
void main(){
  int i = 50;
  while(i<=100){
  if(i%2 == 0){
      print(i);
    }
    i++;
  }
}
``` 
{{% expand "Show Output" "false" %}}
````plaintext
50
52
54
56
58
60
62
64
66
68
70
72
74
76
78
80
82
84
86
88
90
92
94
96
98
100
````
{{% /expand %}} 
{{% button href="https://dartpad.dev/?id=053f6df18f066714f0f1d993e0b35e01" style="blue" %}}Run Online{{% /button %}}    
