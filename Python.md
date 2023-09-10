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
# Multilevel inheritance
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
### Method overriding
Ex: <br>
```
class Animal:
	def eat(self):
		print("The animal is eating")
class Rabit(Animal):
	def eat(self):
		print("The rabit is eating")
rabbit = Rabbit()
rabbit.eat()  #Calls Rabbit class eat() method, If there was no eat() method in rabbit class,
              #it would call the Animal class eat() method

```
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
car.turn_on().drive() #First calls turn on, then drives. You need to have the return self
                      #statement for this call to work.
```
### super() function
super() method is used to give access to the methods of a parent class. It returns a temporary object of a parent class when used. <br> 
Ex: <br>
```
class Rectangle:
	def __init__(self,length,width):
		self.length = length
		self.width = width

class Square(Rectangle):
	def __init__(self,length,width):
		super().__init__(length,width)

	def area(self):
		return self.length*self.width

class Cube(Rectangle):
	def __init__(self,length,width,height):
		super().__init__(length,width)
		self.height = height

	def volume(self):
		return self.height*self.width*self.length

square = Square(3,3)
cube = Cube(3,3,3)
print(cube.volume())
```
### Abstract classes
Abstract classes prevents a user from creating an object of that class. It is like creating a template for creation of other classes.<br>
It compels a user to override abstract methods in a child class. <br>
`Abstract class` - A class which contains one or more abstract methods. <br>
`Abstract method` - A method which only has a declaration but no implementation. <br>
You need to first import `from abc import ABC, abstractmethod` (ABC stands for abstract base class)<br> Ex:<br>
```
from abc import ABC, abstract method

class Vehicle(ABC):
	@abstractmethod
	def go(self):
		pass

class Car(Vehicle):
	def go(self):
		print("You are driving a car")

class Motorcycle(Vehicle):
	def go(self):
		print("You are riding a motorcycle")

car = Car()
motorcycle = Motorcycle()
car.go()
motorcycle.go()
```
### Passing objects as arguments
You can pass objects as arguments for a method. You can also use the same method for two or more classes.<br>
Ex: <br>
```
class Car:
	color = None

class Bike:
	color = None

def change_color(vehicle,color):
	vehicle.color = color

car_1 = Car()
car_2 = Car()
bike_1 = Bike()

change_color(car_1,"red")
change_color(car_2,"white")
change_color(bike_1,"yellow")

print(car_1.color)
print(car_2.color)
print(bike_1.color)
```
### Duck typing
It is a concept where the class of an object is less important than the methods or attributes. The class type is not checked if minimum methods or attributes are present. <br>
Ex: <br>
```
class Duck:
	def walk(self):
		print("The duck is walking")
	def talk(self):
		print("The duck is talking")

class Chicken:
	def walk(self):
		print("The chicken is walking")
	def talk(self):
		print("The chicken is talking")

class Person:
	def catch(self,duck):
		duck.walk()
		duck.talk()
		print("You caught the animal")

duck = Duck()
chicken = Chicken()
person = Person()

#You can use the chicken object or the duck object as both classes contain the methods walk() and talk()
person.catch(chicken)
person.catch(duck)
```
## Walrus operator :=
It is a new feature to Python 3.8. Assigns values to variables as part of a larger expression.<br>Ex: <br>
```
foods = list()

#Normal assignment:
while True:
	food = input("What food do you like?")
		if food == "quit":
			break
	foods.append(food)

#Walrus operator:
while food := input("What food do you like?") != "quit":
	foods.append(food)

```
## Assigning functions to a variable
Ex: <br>
```
def hello():
	print("Hello")

hi = hello
hi()   #This is an ALIAS to hello() now.
say = print
say("This can be used for predefined methods too!")
```
## Higher order functions
A function that either : 1) Accepts a function as an argument or 2) Returns a function
Ex: 1) Accepting a function as an argument<br>
```
def loud(text):
	return text.upper()

def quiet(text):
	return text.lower()

def hello(func):
	text = func("Hello")
	print(text)

hello(loud)  #Prints "HELLO"
hello(quiet) #Prints "hello"
```
Ex: 2) Returning a function<br>
```
def divisor(x):
	def dividend(y):
		return y/x
	return dividend

divide = divisor(2)  #Becomes an ALIAS for dividend where divisor is 2
print(divide(10))
```
## Lambda functions
A function written in 1 line using the lambda keyword. It accepts any number of arguments, but has only one expression. (like a shortcut). <br>Syntax: lambda parameters:expression. This returns the expression. <br>
Ex:<br>
```
def double(x):
	return x*2
print(double(5)
# This function can be written as
double = lambda x:x*2
multiply = lambda x,y: x*y
add = lambda x,y,z: x+y+z
print(multiply(5,6))
print(add(5,6,7))

age_check = lambda age: True if age>= 18 else False
print(age_check(age))
```
## Sorting
`sort()` method can be used with lists or iterables. It can be used to sort strings Alphabetically too. An iterable is any Python object capable of returning its members one at a time, permitting it to be iterated over in a for-loop. Familiar examples of iterables include lists, tuples, and strings.<br>
`sort(reverse = True)` : Sorts in descending order<br>
`sort()` method cant be used for tuples. For iterables, we use `sorted()` method.<br>
By default, `sort()` method sorts using the first elemtent in case of a 2D list. To use other entries refer the example, <br>
```
students = [("S1","F",60),("A1","A",33),("D1","B",50)]
students.sort() #Will sort using the first entries.

age = lambda ages: ages[2]
students.sort(key=age)  #Returns second column and sorts using their ages.
#For a tuple of tuples, we use
sorted_students = sorted(students, key=age)
```
## Map function 
Applies a function to each item in an iterable. <br>
Syntax : map(function, iterable) <br>
Ex: <br>
```
#To change value in a tuple,
store = [("Shirt",40.0),("Pant",50.0)]
price_to_euro = lambda data: (data[0],data[1]*0.82)
store_euros = list(map(to_euros,store))
```
## Filter function 
Creates a collection of elements from an iterable for which a function returns True. It is similar to a search result with filters.<br>
Ex: <br>
```
friends = [("Raj",19),("Ravi",17),("Chandler",21)]
age_check = lambda data: data[1] >=18
drinking_buddies = list(filter(age_check, friends))
```
## Reduce function 
Applies a function to an iterable and reduces it to a single cumulative value. Performs its function on first two elements and repeats this process till only a single value remains. <br>Syntax: reduce(function,iterable) <br>
Ex: <br>
```
import functools
letters = ["H","E","L","L","O"]
word = functools.reduce(lambda x,y: x+y, letters)  #Calls itself for x+y first, then uses letters 
                                                   #and continues

factorial = [5,4,3,2,1]
result = functools.reduce(lambda x,y: x*y, factorial)
```
## List comprehension
A way to create a new list with less syntax. It can mimic certain lambda functions, is easier to read.<br>Syntax: list = \[expression for item in iterable if conditional]  Ex: <br>
```
squares = []
for i in range(1,11):
	squares.append(i*i)

# This can be done easily with list comprehension
squares = [i*i for i in range(1,11)]
```
```
students = [100,90,80,70,60,55,32,0,41]
#Using filter() method
passed_students = list(filter(lambda x: x>=60, students))

#Using List comprehensions
passed_students2 = [i if i>=60 else "FAILED" for i in students]
```
## Dictionary comprehension
A way to create dictionaries using an expression. Can replace for loops and lambda functions. <br>Syntax : dictionary = {key: expression for (key,value) in iterable if conditional}<br>Ex:<br>
```
city_temp = {'New york':32, 'Boston':75, 'LA':100, 'Chicago':50}
cities_in_Celcius = {key: round((value-32)*(5/9)) for (key,value) in city_temp.items()}

#Using if conditional
weather = {'New york':"snowing",'LA':"sunny",'CA':"sunny"}
sunny = {key: value for (key,value) in weather.items() if value == "sunny"}
#You can use functions too.
```
## zip(*iterables) function
Aggregates elements from two or more iterables (lists, tuples, sets, etc). Creates a zip object with paired elements stored in tuples. <br>Ex:<br>
```
usernames = ["A","B","C"]
passwords = ("abc","def","ghi")

users = zip(usernames,passwords)
#To make it a list or a dictionary,
user_list = list(zip(usernames,passwords))
user_dict = dict(zip(usernames,passwords))

#You can even zip more than 2 iterables together
login = ["1/1/2020",""2/2/2022","3/3/2023"]
user_trio = zip(usernames,passwords,login)
```
## if __name__ == '__main__'
Python interpretor sets "Special variables", one of which is `__name__`. Python assigns the `__name__` variable a value of `__main__` if it is the initial module being run.<br>A module can either be run as a standalone program, or can be imported by other modules. To check if the parent module is calling a particular method, the `if __name__ == '__main__'` can be used.<br>
## Time module
Many useful modules to deal with times and dates.<br>`time.ctime(0)` : Converts a time expressed in seconds since "epoch" to a readable sting. Epoch is when your computer thinks time began. (Reference starting point).<br>
`time.time()` : Returns current seconds since epoch.<br>
Combining both, `time.ctime(time.time())` Returns current time.<br>
`time_object` can also be used. It has a lot of atributes like year,month,day,hour,min,secs,weekday etc. <br>
`time_object = time.localtime()` : Returns current time.<br>
`time.strftime(format,time_object)` : Many format specifiers are used to do different tasks like return year, date, etc.<br>We can also convert a tuple into a time object using `asctime()`: 
```
# Usage (year,month,day,hours,minutes,secs,#day of the week,#day of the year,daylight savings)
time_tuple = (2020,4,20,4,20,0,0,0,0)
time_string = time.asctime(time_tuple)
```
# Threading
A thread is a flow of execution. It is like a separate order of instructions. However, each thread takes a turn running to achieve concurrency.<br>GIL - Global interpreter lock - Allows only one thread at a time. But other threads can take turns when one thread is idle. <br>
Programs can be divided into - <br>
CPU bound : When programs spend most of its time waiting for internal events (CPU intensive). This uses Multiprocessing. <br>
IO bound : When programs spend most of its time waiting for external events (User input, web scraping,etc). This uses Multithreading.<br>
Ex: <br>
```
import threading
import time

def eat():
	time.sleep(3)  #Puts the main thread to sleep for 3s
	print("Ate")

def drink():
	time.sleep(4)
	print("Drank")

def study():
	time.sleep(5)
	print("Studied")

x = threading.Thread(target=eat,args=())  #Creation of a thread
x.start()

y = threading.Thread(target=drink, args=())
y.start()

z = threading.Thread(target=drink, args=())
z.start()

x.join()  #Main thread should wait for x to finish before it can move on to the next lines.


#eat()
#drink()
#study()
#Program will take 12 secs to complete. These tasks completed sequentially. We can create 3 #additional threads so that these 3 methods can run concurrently.
#After creating three treads x,y,z the program only takes 5s to execute.

print(threading.active_count())  #prints the number of threads running currently.
print(threading.enumerate())  #Prints a list of the threads currently running.
print(time.perf_counter())  #Prints how long main thread takes to complete.

#You can add a countdown for user input using 2 threads, one for taking input and one main #thread.
```
## Daemon threads
A thread that runs in the background. It is not important for program execution. Program does not wait for daemon threads to complete before exiting. Daemon threads are usually used for background tasks, garbage collection, waiting for input, long running processes,etc. Non daemon threads do not stop on their own.<br>
Ex: <br>
```
import threading
import time
def timer():
	print()
	count = 0
	while True:
		time.sleep(1)
		count+=1
		print("logged in for :",count, "seconds")

x = threading.Thread(target=timer)
x.start()
answer = input("Do you wish to exit?")

# This function would keep running even if the answer was given. To fix this, we use daemon #threads. 
#To make a thread daemon,
x2 = threading.Thread(target=timer(), daemon = True)
#Now as soon as all other tasks are finished, the daemon thread will be killed.
```
`thread.setDaemon(True/False)` : To change a thread into daemon/non daemon.<br>
`thread.isDaemon()` : Returns True/False.<br>
## Multiprocessing
Running tasks in parallel on different CPU cores. It bypasses GIL used for threading. <br>
Multiprocessing - Better for CPU bound tasks.<br>
Multithreading - Better for IO bound tasks. <br>
Ex:<br>
```
from multiprocessing import Process, cpu_count
import time

def counter(num):
	count=0
	while count < num:
		count+=1

def main():
	print(cpu_count())  #Optimal when number of processes = number of cpu's
	a = Process(target=counter, args=(1000000000,)) #Assigns one core for this process
	a.start()
	a.join()	

	b = Process(target=counter, args=(50000000,)) #Divide the task into 2 processes.
	c = Process(target=counter, args=(50000000,))

	b.join()
	c.join()
	
	print("Finished in",time.perf_counter(),"seconds") #Faster when 2 processes are used.



#For windows systems, if we create a child, it copies the module and creates its own children.
#To avoid this, use this block:
if __name__ == '__main__':
	main()

```
# Graphical User Interface
 
