
+++
title = "For Loop in Dart"
weight = 6
description = "Learn about for loop and how to use for loop in dart"
keywords = "for loop in dart, dart for loop, infinite loop in dart"
+++
### For Loop
This is the most common type of loop. You can use **for loop** to run a code block multiple times according to the condition. The syntax of for loop is: 

```dart
for(initialization; condition; increment/decrement){
            statements;
}
``` 
- Initialization is executed (one time) before the execution of the code block.
- Condition defines the condition for executing the code block.
- Increment/Decrement is executed (every time) after the code block has been executed.

### Example 1: To Print 1 To 10 Using For Loop
This example prints 1 to 10 using for loop. Here **int i = 1;** is initialization, **i<=10** is condition and **i++** is increment/decrement.
```dart
void main() {
  for (int i = 1; i <= 10; i++) {
    print(i);
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
{{% button href="https://dartpad.dev/?id=3bd07e68c0e6283b662899c545030113" style="blue" %}}Run Online{{% /button %}}    
     
### Example 2: To Print 10 To 1 Using For Loop
This example prints 10 to 1 using for loop. Here **int i = 10;** is initialization, **i>=1** is condition and **`i--`** is increment/decrement.
```dart
void main() {
  for (int i = 10; i >= 1; i--) {
    print(i);
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
{{% button href="https://dartpad.dev/?id=13f464d876a73c3884fe56aa04f74740" style="blue" %}}Run Online{{% /button %}}  

### Example 3: Print Name 10 Times Using For Loop
This example prints the name 10 times using for loop. Based on the condition, the body of the loop executes 10 times.

```dart
void main() {
  for (int i = 0; i < 10; i++) {
    print("John Doe");
  }
}
``` 
{{% expand "Show Output" "false" %}}
````plaintext
John Doe
John Doe
John Doe
John Doe
John Doe
John Doe
John Doe
John Doe
John Doe
John Doe
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=882e5e4b652726fb346b38d5f328144b" style="blue" %}}Run Online{{% /button %}} 

### Example 4: Display Sum of n Natural Numbers Using For Loop
Here, the value of the **total** is **0** initially. Then, the for loop is iterated from **i = 1 to 100**. In each iteration,  **i** is added to the **total**, and the value of **i** is increased by 1. Result is **1+2+3+....+99+100**.
```dart
void main(){

  int total = 0;
  int n = 100; // change as per required
  
  for(int i=1; i<=n; i++){
    total = total + i;
  }
  
  print("Total is $total");
  
}
``` 
{{% expand "Show Output" "false" %}}
````plaintext
Total is 5050
````
{{% /expand %}} 
{{% button href="https://dartpad.dev/?id=4c35ca27d7c8746ab9278b2f08c537ec" style="blue" %}}Run Online{{% /button %}}


### Example 5: Display Even Numbers Between 50 to 100 Using For Loop
This program will print even numbers between 50 to 100 using for loop.
```dart
void main(){
  for(int i=50; i<=100; i++){
    if(i%2 == 0){
      print(i);
    }
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
{{% button href="https://dartpad.dev/?id=5bc8b63388a9ca1d693759475c360d93" style="blue" %}}Run Online{{% /button %}}


### Infinite Loop In Dart
If the condition never becomes false in looping, it is called an infinite loop. It uses more resources on your computer. The task is done repeatedly until the memory runs out.

This program prints 1 to infinite because the condition is **i>=1**, which is always true with i++.
```dart
void main() {
  for (int i = 1; i >= 1; i++) {
    print(i);
  }
}
``` 

{{% notice info %}}
**Note**: Infinite loops take your computer resources continuously, use more power, and slow your computer. So always check your loop before use.
{{% /notice %}}
