# Python
## String methods 
Python supports a variety of string methods. The most important ones are <br>
`len(str1)` : Returns length of a string. <br>
`str1.find("substr1")` : Finds and returns first occurence of the substring. <br>
`str1.capitalize` : Converts all text to camelcase. <br>
`str1.upper()` : Capitalizes all charecters. <br>
`str1.lower()` : Converts all alphabets to lower case <br>
`str1.isdigit()` : Returns True if ALL charecters are digits. <br>
`str1.isalpha()` : Returns True if ALL charecters are alphabets. <br>
`str1.count(substr1)` : Counts occurences of the substring in the string. <br>
`str1.replace(substr1,substr2)` : Replaces occurences of substr1 with substr2. <br>
### String slicing
`substr = str1[start:stop:step]` : Stop is not inclusive. Default value of start is 1st index, stop is end, step is 1. <br>Negative indexing is possible. <br>`str1.strip()` : Removes trailing and preceeding spaces in a string. <br>
### String formatting for printing
There are two methods: <br>
1) ***format() method*** : `print("The {2} {1} {0}".format("fox","brown","quick"))` : The number in brackets are the list indices. <br>
`print("The {q}{b}{f}".format(f="fox",b="brown", q="quick"))` : Variables are assigned as placeholders. <br>
`result = 100/3` `print("{r:0.3f}".format(r=result))` : Precision = 3 is set <br>
2) ***f-strings***: <br>
`name = "abcd"`
`print(f"My name is {name}")` <br>
## Math methods
`round(float1)` : Rounds the number passed. <br>
`math.ciel(float1)` : Performs cieling function. <br>
`abs(float1)` : Absolute value. <br>
`pow(int1, int2)` : Returns int1^int2. <br> 
`pow(int1, int2, int3)` : Returns (int1^int2)%int3 <br>
`float1/float2` : Returns a floating point integer. <br>
`float1//float2` : Returns an integer. <br>
`float1%float2` : Returns mod. <br>
`float1**float2` : Returns float1^float2. <br>
`math.sqrt(int1)` : Returns square root. <br>
`max(int1, int2, ---)` : Returns max value. (Also min(---) )<br>
### Random module
Has many uses. <br>
Ex: 
```
import random
x = random.randint(1,6)  #Selects a random int from 1 to 6 (6 not inclusive)
y = random.random()      #Selects a random number
list1 = ['rock', 'paper', 'scissors']
z = random.choice(list1)
cards = [1,2,3,4,5,6,7,8,9,"J","Q","K","A"]
random.shuffle(cards)
```
## Lists
Lists support ordering, indexing, slicing, etc. Indexing starts from 0. <br>
Two or more lists can be concatenated using the `+` operator. <br>
`len(list1)` : Gives the number of elements. <br>
`list1.append(item)` : Adds element to the end of the list. <br>
`list1.clear()` : Clears the list <br>
`new_list = list1.copy()` : Creates a copy of the list. <br>
`list1.count(element)` : Count the occurrence of a specific element. <br>
`list1.index(element)` : Finds index of the element. <br>
`list1.insert(index,element)` : Inserts element at specified index. <br>
`list1.pop()` : Removes last added element. (If index is specified it pops that element) <br>
`list1.remove(element)` : Removes first occurence of the element. Throws error if element doesnt occur. <br>
`list1.reverse()` : Reverses list.<br>
`list1.sort()` : Sorts the list. If you want descending order, specify `list1.sort(reverse=True)` <br>
### 2D lists
Ex: <br>
```
list1 = [1,2,3] 
list2 = [4,5,6]  
list3 = [7,8,9]  
list4 = [list1,list2,list3] 
list4[0][0] #Refers to first list and first element. 
list4[2][1] #Refers to the third list and second element. 
```
## Dictionaries
It is an ordered mapping, key-value pair type data structure that does not allow duplicate values. You can iterate through a dictionary by using `for key,value in dict.items():`<br> Ex: `dict1 = {'key1':2, 'key2':3}`<br>To access elements, we pass the keys. `dict1[key1]` returns 2. <br>To insert a new value, `dict1[new_key] = new_value` is used. This can be used for overwriting too.<br>
To get all keys in a list format, `key_list = dict1.keys()`<br>
To get all values in a list format, `value_list = dict1.values()`<br>
To get key-value pairs in tuples, `dict1.items()`<br>
## Tuples
Immutable lists (cannot be changed once created) <br> Memory efficient when compared to lists.<br>
Uses parenthesis () with elements inside. When we use the `dict.values()` method, the key-value pairs are stored in tuples, as these should never change order. <br>
`tuple1.count(element)` : Counts frequency of the element<br>
`tuple1.index(element)` : Returns first index of the element's occurrence.<br>
## Sets
Sets are an unordered collection of unique elements. These are unindexed. <br> To create an empty set, use `set1=set()`. <br> 
`set1.add(element)` : Adds element to the set. <br> 
`setdiff = set1.difference(set2)` : Stores the set difference of set1-set2 into setdiff. <br>
`set1.difference_update(set2)` : Evaluates set1-set2 and stores it back into set1. <br>
`set1.discard(element)` : Removes the element from the set. <br>
`set3 = set1.intersection(set2)` : Stores intersection of set1 and set2 into set3. <br>
`set1.isdisjoint(set2)` : Returns True or False. <br>
`set1.update(set2)` : Stores union of set1 and set2 into set1. <br>
## Looping and Control Flow
Usage of for loop: <br>
`for i in range(0,n,2)` : i starts from 0, ends at n, step = 2<br>
`for a in list1:` : Traverse in a list<br>
`for (a,b) in [(1,2),(3,4),(5,6)]` : Unpacks the tuples, assigns first one to a, second to b<br>
Enumeration : Assigns numbers to elements in a list or charecters in a string. <br> Ex: `word = 'abcdefg'` <br> `for item in enumerate(word):` : a is treated as 0, b is treated as 2, etc. You can also specify start of the enumerate by `enumerate(iterable, start = )`<br><br>
### Break, continue, pass
`break` : Breaks out of the current while, do while or for loop. Terminates the loop<br>
`continue` : Goes to the top of the closest enclosing loop (Skips the current iteration and goes to the next  iteration.) <br>
`pass` : Does nothing<br>
## Functions in Python
Function definition : 
```
def func_name(parameter_list):
	func_body
	return return_variable
```
The parameters (Positional arguments) passed to a function are temporary variables. <br>
### Keyword Arguments 			 
Unlike positional arguments, the arguments of the function are preceeded by an identifier. <br>Ex: `multiply(num1 = 23, num2 = 34, num5 = 1)` <br>
### Nested function calls
Using a return of one function as parameter for a second function and so on.
<br>`Ex: round(abs(float(input("Enter a number")))`<br>
## Scope of a variable
A variable is only availible from inside the region it is created. A global and locally scoped versions of a variable can be created. Global variables are created outside any function. <br>
You can have a global and local version of a variable at the same time.<br>Priority order: <br>1 - Local varibles <br>2 - Enclosing variable<br>3 - Global variable<br>4 - Built in variable<br>
## *args Parameter
Packs all arguments passed into a tuple that is useful for making functions that accept a varying amount of arguments. You can name the *args it whatever you want. <br>
Ex: 
```
def add(*args):
	sum = 0
	for i in args:
		sum += i
	return sum

add(1,2,3,4,5)
add(1,2,5,6)
```
<br>

## **kwargs

It is a Parameter similar to *args, but this packs all arguments into a dictionary. It is useful so that a function can accept a varying amount of keyword arguments. <br>
Ex:<br>
```
def hello(**kwargs):
	print("Hello "+ kwargs['first'] + " " + kwargs['last'])

(or)

def hello(**kwargs):
	print("Hello", end=" ")
	for key,value in kwargs.items():
		print(value, end=" ")

hello(title = "Mr", first = "Bro", last = "Code")
hello(first = "Bro")
```
<br>

## Exception handling 
Exception is an event generated during execution that interrupts the flow of a program. Uses `try:` `except:` blocks. Any exception in a `try` block is thrown to the `except` block.
Ex: <br>
```
try:
	num1 = int(input())
	num2 = int(input())
	result = num1/num2

except ZeroDivisionError as e:
	print(e)
	print("You cannot divide by zero!")
except ValueError as e:
	print("Enter numbers only!")
else: 
	print(result)
finally:
	print("This will always execute")
```
## File handling
File paths need to be in double backslashes. 
Ex: <br>
```
import os
path = "C\\Users\\Desktop\\test.txt"
if os.path.exists(path):
	print("The location exists!")
	if os.path.isfile(path):
		print("This is a file")
	elif os.path.isdir(path):
		print("This is a directory")
else:
	print("Path not found")
```
### Reading and writing on files
Always use try blocks for any kind of exceptions.<br>
```
with open('test.txt','w') as file:
	print(file.read())

#Writing
text = "Heyy\n hello world\n 123493"

with open('test.txt','w') as file:
	file.write(text)

```
### Copying files
`copyfile()` : Copies content of a file<br>
`copy()` : `copyfile()` + permission mode + destination can be a directory<br>
`copy2()` : `copy()` + copies the metadata of the file<br>
Ex: <br>
```
import shutil
shutil.copyfile('test.txt','copy.txt') # Source, destination
```
### Moving files
`os.replace(source,destination)` : Moves file from source to destination<br>
### Deleting a file
`os.remove(path)` : Deletes the file.<br>
`os.rmdir(path)` : Delets a directory.<br>
`shutil.rmtree(path)` : Deletes a directory and all files in it. Proceed with caution when using this function.<br>
## Classes and Objects
You can combine attributes and methods to create an object. Class is a blueprint for object creation.<br>
Ex: <br>
```
class Car:
	make = None
	model = None
	year = None
	color = None

	def __init__(self,make,model,year,color): #This is a constructor.
		self.make=make
		self.model=model
		self.year=year
		self.color=color

	def drive(self):
		print("Driving")

car1 = Car("Chevy","Corvette",2021,"blue")
print(car1.make)
car1.drive()
```
### Inheritence
Classes can inherit attributes and methods from other classes. <br>
Ex: <br>
```
#Multilevel inheritance
class Parent:
	data = True

class Child(Parent):
	def eat(self):
		print("This animal is eating")

class Grandchild(Child):
	def bark(self):
		print("Dog is barking")

dog = Dog()
print(dog.alive)
dog.eat()
dog.bark()
```
<br>Multiple inheritence - Two or more children from one parent
### Method chaining 
Calling multiple methods sequentially, each call performs an action on the same object and returns self. <br>
Ex: <br>
```
class Car:
	def turn_on(self):
		print("You are starting the engine")
		return self
	def drive(self):
		print("You are driving")
		return self

car = Car()
car.turn_on().drive() #First calls turn on, then drives
```
