+++
title = "Datetime In Dart"
weight = 2
description = "In this section, you will learn about  datetime in Dart programming language and how to use datetime with the help of examples."
keywords = "dart datetime, datetime in dart, date time in dart, date time in dart programming, dart date time"
+++
## DateTime In Dart


Date and time are often used in our day-to-day activities. As a programmer you need to know how to find a date and time? How to format date? and how to perform different calculation in date? 


## How To Get Date And Time
Use the following code to get the current date and time in the dart.

```dart
void main() {
  print(DateTime.now());
}
```



{{% expand "Show Output" "false" %}}
````plaintext
This is just sample output. This will print current date and time 
2022-04-17 08:59:21.508300
````
{{% /expand %}}

## Get Year, Month, Day Of Datetime In Dart
Here is the way to get a year, month, day, hour, minutes, and seconds in Dart. You can convert DateTime to String by using the `toString()` method. 

## Example
```dart
void main() {
  DateTime datetime = DateTime.now();
  print("Year is " + datetime.year.toString());
  print("Month is " + datetime.month.toString());
  print("Day is ${datetime.day}"); // If you don't want to use .toString
  print("Hour is " + datetime.hour.toString());
  print("Minutes is " + datetime.minute.toString());
  print("Second is " + datetime.second.toString());
}
```


{{% expand "Show Output" "false" %}}
````plaintext
This is just sample output. This will print curent year, month and day.
Year is 2022
Month is 4
Day is 17
Hour is 9
Minutes is 13
Second is 25
````
{{% /expand %}}

## How To Convert Datetime To String In Dart
Use the following code to convert DateTime to String in the dart.

```dart
void main() {
  String datetime = DateTime.now().toString();
  print(datetime);
}
```



{{% expand "Show Output" "false" %}}
````plaintext
This is just sample output. This will print current date and time 
2022-04-17 08:59:21.508300
````
{{% /expand %}}

## How To Convert String To DateTime
You cannot get year, months, or day directly and cannot perform date calculation using a String if that String contains the correct DateTime value. In such a situation, you first need to convert String to DateTime. 

```dart
void main() {
  String myDateInString = "2022-05-01";
  DateTime myConvertedDate = DateTime.parse(myDateInString);
  print("Year is " + myConvertedDate.year.toString());
  print("Month is " + myConvertedDate.month.toString());
  print("Day is " + myConvertedDate.day.toString());
}
```



{{% expand "Show Output" "false" %}}
````plaintext
Year is 2022
Month is 5
Day is 1
````
{{% /expand %}}


## Methods Supported By Datetime In Dart
You can use DateTime methods if you want to add days, hours, or minutes to DateTime. Let us suppose you have created a DateTime object named mybirthday. ` DateTime mybirthday = DateTime.parse("1997-05-14");`

|  Method  |  Example  |  
| ----------- | --------- |
|  add(Duration)  |     myBirthday.add(Duration(days: 1));    |
|  subtract(Duration)  |  myBirthday.subtract(Duration(days: 1));|

{{% notice info %}}
Note: You can set a duration to `days`, `hours`, `minutes`, `seconds`, `milliseconds`, and `microseconds`. To understand it more, look at the example below.
{{% /notice %}}

## Example Add Date In Dart
```dart
void main() {
  DateTime myBirthday = DateTime.parse("1997-05-14");
  myBirthday = myBirthday.add(Duration(days: 1));
  print("Year is " + myBirthday.year.toString());
  print("Month is " + myBirthday.month.toString());
  print("Day is " + myBirthday.day.toString());
}

```



{{% expand "Show Output" "false" %}}
````plaintext
Year is 1997
Month is 5
Day is 15
````
{{% /expand %}}

## Example Subtract Date In Dart
```dart
void main() {
  DateTime myBirthday = DateTime.parse("1997-05-14");
  myBirthday = myBirthday.subtract(Duration(days: 1));
  print("Year is " + myBirthday.year.toString());
  print("Month is " + myBirthday.month.toString());
  print("Day is " + myBirthday.day.toString());
}

```


{{% expand "Show Output" "false" %}}
````plaintext
Year is 1997
Month is 5
Day is 13
````
{{% /expand %}}

## Find Difference Between Two Dates In Dart
Suppose you want to find the difference between two dates in dart. There is a straightforward way.
```dart
void main() {
  DateTime myBirthday = DateTime.parse("1997-05-14");
  DateTime today = DateTime.now();
  Duration diff = today.difference(myBirthday);
  print("Difference in days: " + diff.inDays.toString());
  print("Difference in hours: " + diff.inHours.toString());
  print("Difference in minutes: " + diff.inMinutes.toString());
  print("Difference in seconds: " + diff.inSeconds.toString());
  print("Difference in milliseconds: " + diff.inMilliseconds.toString());
  print("Difference in microseconds: " + diff.inMicroseconds.toString());
}

```


{{% expand "Show Output" "false" %}}
````plaintext
Difference in days: 9104
Difference in hours: 218505
Difference in minutes: 13110352
Difference in seconds: 786621135
Difference in microseconds: 786621135215530
Difference in milliseconds: 786621135215
````
{{% /expand %}}


|  Name  |  Description  |  
| ----------- | --------- |
|  inDays  |     Convert duration in days.   |
|  inHours  |  Convert duration in hours. |
|  inMinutes  |  Convert duration in minutes. |
|  inSeconds  |  Convert duration in seconds. |
|  inMilliseconds  |  Convert duration in milli seconds.|
|  inMicroseconds  |  Convert duration in micro seconds.|


## DateTime Comparision Methods
If you want to compare two dates, then you can use comparison methods.

|  Method Name  |  Description  |  
| ----------- | --------- |
|  IsAfter(DateTime)  |     Returns true or false. `bool`  |
|  IsBefore(DateTime)  |     Returns true or false. `bool`  |
|  IsAtTheSameMoment(DateTime)  |  Returns true or false. `bool`  |


```dart
void main() {
  DateTime myBirthday = DateTime.parse("1997-05-14");
  DateTime today = DateTime.now();

  if (myBirthday.isBefore(today)) {
    print("My Birthday is before today.");
  } else if (myBirthday.isAfter(today)) {
    print("My Birthday is after today.");
  } else if (myBirthday.isAtSameMomentAs(today)) {
    print("My Birthday date and today's date is same.");
  }
}

```


{{% expand "Show Output" "false" %}}
````plaintext
My Birthday is before today.
````
{{% /expand %}}
