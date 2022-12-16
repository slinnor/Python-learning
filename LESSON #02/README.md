# Variables and String formatting

So we will introduce a variables here a bit because we will use them correctly in the strings, for example in print function. So first of all we will check how to declare a variable and then we will check how to print them correctly and also we will have a look on some basics of string formatting. Next we will check other operations with variables.

## Declaring a variable

In Python declaring a new variable is very simple. The only thing that has to be done is to write 
```python
name = value
```

*NOTE: We are not ending declaring a variable using `;` bud jumping on the new line.*

So, what if we want a name stored in a variable? For example my firstname:
```python
first_name = "Daniel"
```
We have to close the string into the `""` because in other case it will looks like we are trying to save a value of one variable to another which is possible and very simple. Let's have a look with numbers.
```python
x = 10
y = x
```
As you probably guess the output for `y` will be `10` because here we declared a variable `x` with a value of `10` and then we declared a new variable `y` and we give it a value of variable `x` which is `10`. 

**As you can see we don't need to specify the type of the variable, so if it's `string` or `integer` we don't have to care about this.**

### Behind the scene
So as you can see we have here something that should be mentioned. Whats really behind this code?
```python
x = 10
y = x
```
Why I am mentioning this? Of course both variables will have the value of `10` but what's behind it? Actually it is very simple since the variables works as references so we declared a new variable `x` with value `10` and we passed to the `y` variable the reference of the `10`. We didn't create another number, we just passed its address in memory. So in this case it can look like this
```
x => 10 <= y
```
As you can see both variables are pointing to the 1 object in the memory. But what will happend here if I set the value of `y` to `15` by doing `y = 15`? Well this is very simple. Our reference will not exists anymore for `y` and there will be new object created in our memory
```
x => 10
     15 <= y
```
As you can see we have now 2 references to 2 objects. 

Now. Let's say we have the beginning of this issue which was
```python
x = 10
y = x
```
and I will change the `x` variable's value to `15` by running `x = 15`. What output will be for `print(y)`?
```python
>>> print(y)
10
```
It will again be separated because `y` will be poiting to the old object which was 10. Remember that if we call the `y = x` it is not this cas
```
y => x => 10
```
in this case changing the `x` will automatically change the `y` but it's not so simple. In the correct way how it really is is this case
```
x => 10 <= y
```
so changind the `x` variable will result in
```
x => 15
     10 <= y
```
Easy, right?



Imagine you want to declare an axis `x, y, z` and you'll probably declare it like this
```python
x = 10.4
y = 27.1
z = 33.9
```
But Python alows us to do
```python
x, y, z = 10.4, 27.1, 33.9
```
See? One line declaration of 3 variables...

Great! Now if I have 2 variables declared as a `first_name` and `surname` and I want to have variable `full_name`? We can simply connect 2 or more strings together by using + between the variables
```python
first_name = "Daniel"
surname = "Random"
full_name = first_name + surname
```
This will result in output
```python
>>> print(full_name)
DanielRandom
```
We can simply add a space between the 2 variables here by using
```python
first_name = "Daniel"
surname = "Random"
full_name = first_name + " " + surname
```
This will result in output
```python
>>> print(full_name)
Daniel Random
```

### Difference with C#

In C# and other programming langueages we have to declare a type of the variables
```csharp
string first_name = "Daniel";
string surname = "Random";

int x = 10;
float y = 10.5;
```
and so... 

As you can see, Python saves us a time declaring variables bit be careful about their values then! Make sure even if you will be doing small projects to name your variables well and correctly so you will always know what the variables stores even if you see the code after a year you will have to know for the first view what it stores!

## String formatting and variables printing

So we now can declare variables but there is one huge question: How to work with strings?

Well this is not a very simple answer but we will have a look about strings later. For now we will check the very basics of strings and their printings with variables. As you probably noticed we were already connecting multiple stings together by using `+` between them and it really works
```python
print("Hello" + " I am Daniel")
```
Which will work, but... yeah it's weird, let's have a look about it more. 

Let's first introduce us into the console. Declare a variable with your first name and print it with the result `Hello, I am NAME"
```python
first_name = "Daniel"

print("Hello, I am " + first_name)
```
Which will result in
```python
>>> print("Hello, I am " + first_name)
Hellol, I am Daniel
```

Now add your surname and space between the first name and surname.
```python
first_name = "Daniel"
surname = "Random"

print("Hello, I am " + first_name + " " + surname)
```
Which will result in
```python
>>> print("Hello, I am " + first_name + " " + surname)
Hellol, I am Daniel Random
```

But isn't it a bit weird and complicated? Isn't there any other way how to format the text? Of course it is! And there are more then 1 way! I'll show you here probably the best methods but if you are interested in you can search for it. Google is your friend!

Method 1:
```python
print("Hello, I am", first_name, surname)
```
Method 2:
```python
print("Hello, I am {} {}".format(first_name, surname))
```
Method 3:
```python
print(f"Hello, I am {first_name} {surname}")
```

So which one is the best for you? I think you gonna love the **Method 3** since it's nice and friendly formatting here. Notice that `f` before we start typing, it helps us for better formatting.

Now we will have a look on some other issues.

Notice that if you go and try in the string to print `"` it will not be possible.
```python
print("I want to "print" something nice")
```
In this case the program will not be running because we use `"` to separate the string. So if we want to display the `"` in the middle of the sentence we have to use backslash before it to suppress its meaning.
```python
print("I want to \"print\" something nice")
```
And this will be running properly. This can be uset in many of special characters and so you will need tu suspend it and just print it like you need.

There are also some special characters that can be put into the strings to create a better text output:
| Char | Meaning |
|:----:|---------|
| \n | New Line|
| \t | Horizontal Tab |
| \r | Carriage Return |
| \b | Backspace |
| \f | Form Feed |
| \\' | Single Quote |
| \\" | Double Quote |
| \\ | Backslash |
| \v | Vertical Tab |

## Exercise

In this lesson we will play a bit with variables and their printing. Now it's up to you how you will done this but declare some variables and try just different outputs and play around and have a fun.
