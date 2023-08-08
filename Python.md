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
`substr = str1[start:stop:step]` : Stop is not inclusive. Default value of start is 1st index, stop is end, step is 1. <br>Negative indexing is possible. <br>
### String formatting for printing
There are two methods: <br>
1) ***format() method*** : `print("The {2} {1} {0}".format("fox","brown","quick"))` : The number in brackets are the list indices. <br>
`print("The {q}{b}{f}".format(f="fox",b="brown", q="quick"))` : Variables are assigned as placeholders. <br>
`result = 100/3` `print("{r:0.3f}".format(r=result))` : Precision = 3 is set <br>
2) ***f-strings***: <br>
`name = "abcd"``print(f"My name is {name}")` <br>
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
## Dictionaries
It is an ordered mapping, key-value pair type data structure that does not allow duplicate values. <br> Ex: `dict1 = {'key1':2, 'key2':3}`<br>To access elements, we pass the keys. `dict1[key1]` returns 2. <br>To insert a new value, `dict1[new_key] = new_value` is used. This can be used for overwriting too.<br>
To get all keys in a list format, `key_list = dict1.keys()`<br>
To get all values in a list format, `value_list = dict1.values()`<br>
To get key-value pairs in tuples, `dict1.items()`<br>
## Tuples
Immutable lists (cannot be changed once created) <br> Memory efficient when compared to lists.<br>
Uses parenthesis () with elements inside. When we use the `dict.values()` method, the key-value pairs are stored in tuples, as these should never change order. <br>
`tuple1.count(element)` : Counts frequency of the element<br>
`tuple1.index(element)` : Returns first index of the element's occurrence.<br>
