# Setting up the IDE, Python Syntax and Hello world!

In this lessons we will describe a bit the Python syntax and print Hello World text to the console as our very first program.
But firstly let's check how to set-up our IDE for the Python development.

## Setting up the IDE

### Visual Studio
In the Visual Studio we have in the modifier or installer possibility to choose the Python Development. If you previously installed Visual Studio go to Visual Studio Installer > Modify Visual Studio > Check the `Python development`
![image](https://user-images.githubusercontent.com/57287296/206917063-edf40a60-775d-4746-8229-d0b3d7157d89.png)

Then simply install it.

## Syntax

Note that Python will not allow you to create a "mess" in your code since the blocks of functions and so are based on TABS. But about tabbing the code later. Now we are going to make sure we will not be using semicolons after the command. I will describe here a very easy and simple printing and also compare it to the C# as promised.

## Hello world!

### Create new file

So we will start by creating our new file. In you IDE choose your Python folder and there you will create a simple file named `hellworld.py`

*Every python file will have the `.py` extension stands for `Python`.*

I will create a new project in Visual Studio 2022.
I'll start by Creating a new project

![image](https://user-images.githubusercontent.com/57287296/206917176-e35a1fb0-c0a4-417f-a0fc-11989b0a23f8.png)

Going ahead and choosing the Python application

![image](https://user-images.githubusercontent.com/57287296/206917223-02087aa1-5dd5-4020-a536-eac909677305.png)

In the next step I will call my project as `Hello World` and Create the project.

## Inside the file

There are no requirements like importing some libraries or aditional files.

So now we are goint to print the `Helo world!` message to our console:
```python
print("Hello world!")
```

Note in C# this simple task is more complex:

```csharp
Console.WriteLine("Hello world!");
```

Also notice that in C# we are using semicolon after ending the command this is not in Python so it stays clear!

## Run our program

It is very simple to run our Python program, the only thing you have to do is to click the "play" button ![image](https://user-images.githubusercontent.com/57287296/206917341-aed82890-a2d8-48d0-83fd-f61b9c4cc397.png)
 in your IDE. In Visual Studio I will choose the second icon with the stroke and transparent background. 
 
 The result of the code should be displayed in the terminal: 
 ```
 Hello world!
 Press any key to continue...
 ```
 
 In case of Linux you can run the program by the command:
 ```
 # ./helloworld.py
 ```
 Make sure you will write correctly the filename and it's path. I recommend to move to the folder and then running the command.

## Exercise

So the task for your lesson now is to setup your IDE and run the first program. You can also try to print different strings for example
```
Hello,
This is my very first Python program!
```
