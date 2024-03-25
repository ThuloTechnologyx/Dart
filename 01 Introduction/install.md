+++
title = "Install Dart"
weight = 2
description = "Learn how to install dart SDK. After reading this, you can install a dart on your operating system. Install dart SDK for windows & mac."
keywords = "install dart sdk, install dart sdk on windows, install dart sdk on mac, how to install dart, install dart, dart programming language"
+++

## Dart Installation
There are multiple ways to install a dart on your system. You can install Dart on **Windows, Mac, and Linux** or run it from the browser.

## Requirements
- **Dart SDK**,
- **VS code or other editors** like Intellij [We will use VS Code here].

## Dart Windows Installation
Follow the below instructions to install a dart on the windows operating system. 

###**Steps:**
- Download Dart SDK from [here](https://dart.dev/get-dart/archive).
- Copy **dart-sdk** folder to your C drive.
- Add **C:\dart-sdk\bin** to your environment variable. Watch the video below to be more clear.
- Open the command prompt and type **`dart --version`** to check it.
- Install [VS Code](https://code.visualstudio.com/download) and Add Dart Extension.

## Dart Windows Installation 


{{% notice info %}}
###**Note**: Dart SDK provides the tools to compile and run dart program.
{{% /notice %}}

## Dart Mac Installation
- Install Homebrew From [here](https://brew.sh/). 
- Type `brew tap dart-lang/dart` in the terminal.
- Type `brew install dart` in the terminal.  
- If you have any issues installing the dart, watch the video below.

## Homebrew Install Command
Copy and paste this command on your terminal to install Homebrew.
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
To set the homebrew path, copy and paste this command on your terminal.
```bash
export PATH=/opt/homebrew/bin:$PATH
```

## Dart Mac Installation 


## Dart Linux Installation
To install a dart on Linux, open your terminal and **copy/paste** the below commands.
```bash
sudo apt-get update
sudo apt-get install apt-transport-https
wget -qO- https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo gpg --dearmor -o /usr/share/keyrings/dart.gpg
echo 'deb [signed-by=/usr/share/keyrings/dart.gpg arch=amd64] https://storage.googleapis.com/download.dartlang.org/linux/debian stable main' | sudo tee /etc/apt/sources.list.d/dart_stable.list
```
Then, install the dart using the below command.
```bash
sudo apt-get update
sudo apt-get install dart
```

To set the dart path, copy and paste this command on your terminal.
```bash
export PATH="$PATH:/usr/lib/dart/bin"
```

## Check Dart Installation
Open your command prompt and type **`dart --version`**. The dart is successfully installed on your system if it gives you a version code. If not, watch the video above.

## Some Useful Commands
|  Command  |  Description  |
| ----------- | --------- | 
|  `dart --help`  |    Show all available commands.  |
|  dart filename.dart  |    Run the dart file.  |
|  dart create <projectname>  |   Create a dart project.  |
|  dart fix  |   Update dart project to new syntax.  |
|  dart compile exe bin/dart.dart  |    Compile dart code.  |
|  dart compile js bin/dart.dart  |    Compile dart to javascript. You can run this file with Node.js.  |


## Run Dart On Web
You can run the dart program on your browser without installing any software. Dartpad is a web tool to write and run your dart code.
- [Run Dart Programming on Web](https://dartpad.dev)

## Install Dart Official Link
- [Install Dart Official Link](https://dart.dev/get-dart)

## Can You Run Dart From Mobile?
Yes, you can use [DartPad](https://dartpad.dev) to run simple dart programs from your phone without installing any software. For bigger projects, using DartPad is not recommended.
