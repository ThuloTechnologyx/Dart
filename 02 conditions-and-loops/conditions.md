
+++
title = "Conditions in Dart"
weight = 1
description = "Use conditions to control the flow of the dart program. Learn if condition, else condition, if else if condition, etc."
keywords = "control flow in dart, conditions in dart, if condition in dart, if else in dart, decision making in dart"
+++

## Conditions In Dart
When you write a computer program, you need to be able to tell the computer what to do in different situations. With conditions, you can control the flow of the dart program. Suppose you need to execute a specific code when a particular situation is true. In that case, you can use conditions in Dart. E.g., a calculator app must perform subtraction if the user presses the subtract button and addition if the user taps the add button.

## Types Of Condition
You can use following conditions to control the flow of your program.
*   **If Condition**
*   **If-Else Condition**
*   **If-Else-If Condition**
*   **Switch case**

## If Condition 
The easy and most common way of controlling the flow of a program is through the use of an *if statement*. If statement allow us to execute a code block when the given condition is true. Conditions evaluate boolean values. 

## Syntax
```dart
if(condition) {
    Statement 1;
    Statement 2;
       .
       .
    Statement n;
}
``` 
## Example Of If Condition
It prints whether the person is a voter. If the person's age is greater and equal to 18, it will print, You are a voter.
```dart
void main()
{
    var age = 20;
    
    if(age >= 18){
      print("You are voter.");
    }
}
```
{{% expand "Show Output" "false" %}}
````plaintext
You are voter.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=21c3bb5301c9ba8c578adc301fdd5356" style="blue" %}}{{% /button %}}

## If-Else Condition
If the result of the condition is true, then the body of the if-condition is executed. Otherwise, the body of the else-condition is executed.

## Syntax
```dart
if(condition){
statements;
}else{
statements;
}
```
## Example Of If-Else Condition
Dart program prints whether the person is a voter or not based on age.

```dart
  void main()
  {
        int age = 12;
        if(age >= 18){
            print("You are voter.");
        }else{
            print("You are not voter.");
        }
  }
```
{{% expand "Show Output" "false" %}}
````plaintext
You are not voter.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=8120148f16a6c6ccfd832a5477ab6508" style="blue" %}}{{% /button %}}

## Condition Based On Boolean Value
If the married status is false, it prints you are single; otherwise, it will print you are married.
```dart
  void main()
  {
        bool isMarried = false;
        if(isMarried){
            print("You are married.");
        }else{
            print("You are single.");
        }
  }
```
{{% expand "Show Output" "false" %}}
````plaintext
You are single.
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=6af373c2e52a629f99bd5aeba9455c2b" style="blue" %}}{{% /button %}}

## If-Else-If Condition 
When you have multiple if conditions, then you can use if-else-if. You can learn more in the example below. When you have more than two conditions, you can use if, else if, else in dart. 

## Syntax
```dart
if(condition1){
statements1;
}else if(condition2){
statements2;
}else if(condition3){
statements3;
}
.
.
.
else(conditionN){
statementsN;
}
```

## Example Of If-Else-If Condition
This program prints the month name based on the numeric value of that month. You will get a different result if you change the number of month.

```dart
void main() {
  int noOfMonth = 5;

  // Check the no of month
  if (noOfMonth == 1) {
    print("The month is jan");
  } else if (noOfMonth == 2) {
    print("The month is feb");
  } else if (noOfMonth == 3) {
    print("The month is march");
  } else if (noOfMonth == 4) {
    print("The month is april");
  } else if (noOfMonth == 5) {
    print("The month is may");
  } else if (noOfMonth == 6) {
    print("The month is june");
  } else if (noOfMonth == 7) {
    print("The month is july");
  } else if (noOfMonth == 8) {
    print("The month is aug");
  } else if (noOfMonth == 9) {
    print("The month is sep");
  } else if (noOfMonth == 10) {
    print("The month is oct");
  } else if (noOfMonth == 11) {
    print("The month is nov");
  } else if (noOfMonth == 12) {
    print("The month is dec");
  } else {
    print("Invalid option given.");
  }
}
``` 
{{% expand "Show Output" "false" %}}
````plaintext
The month is may
````
{{% /expand %}}
{{% button href="https://dartpad.dev/?id=d57d81ebfa776940cd254423c163d45c" style="blue" %}}{{% /button %}}

## Find Greatest Number Among 3 Numbers
Dart program, which finds the greatest number among three numbers.

```dart
void main()
{
        int num1 = 1200;
        int num2 = 1000;
        int num3 = 150;

        if(num1 > num2  && num1 > num3){
            print("Num 1 is greater: i.e $num1");
        }
        if(num2 > num1 && num2 > num3){
           print("Num2 is greater: i.e $num2");
        }
        if(num3 > num1 && num3 > num2){
            print("Num3 is greater: i.e $num3");
        }
    }

``` 
{{% expand "Show Output" "false" %}}
````plaintext
Num 1 is greater: i.e 1200
````

