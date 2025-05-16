## **Strings**
If we use a single only one pair of single quote or double quote in python to assign strings it only takes the first line and not the other lines so in order to assign a multiline string we use three double quotes like this:
```Python
a="""first line
second line
third line fourth line """
```
we could have also used three single quotes as in python both single quote and double quote are the same thing.

**String Slicing**
```Python
A="This is a random String"
print(a[5,10])
```
this is the syntax for string slicing 
1. the first value is the starting index
2. the second value is the n+1 index that is it will stop at n-1 index
3. if we give negative indexes for the arguments then the slicing will start from the end of the list 

**String Methods**
1. replace()- This method is used to replace a string with another since strings are immutable it creates a new string and replaces the strings there
2. split()- this method splits a string into lists by default it splits from whitespaces it takes two parameters the separator and the total no of splits to be done there. There is also rsplit() which splits a string from the right side 
3. strip()- removes trailing and leading characters it removes whitespaces by default and takes the character to be removed as the argument. There are also lstrip and rstrip which removes characters in left and right of the string respectively
4. partition()- this method takes an argument it looks for the first occurrence of the argument and splits the string in to a tuple where the first element is the part before the match 2nd is the match and 3rd is all after the match. There is also rpartition() which searches for the last occurrence of the argument not the first.
5. zfill()- This method takes a number as an input and add zeros at the beginning of the string till the specified length is achieved
6. swapcase()- This method swaps the case upper case becomes lower case and vice versa
7. startswith()- This method an argument and check if the string starts with the argument

we can use numbers in strings using F-strings
```python
a=20
b=f"My age is {a} years old"
```

\ is an escape character we use escape character to insert illegal characters in the program

## **Operators**

**Python Arithmetic Operators**

| operator | operation      | example       |
| -------- | -------------- | ------------- |
| `+`      | Addition       | `5 + 2 = 7`   |
| `-`      | Subtraction    | `4 - 2 = 2`   |
| `*`      | Multiplication | `2 * 3 = 6`   |
| `/`      | Division       | `4 / 2 = 2`   |
| `//`     | Floor Division | `10 // 3 = 3` |
| `%`      | Modulo         | `5 % 2 = 1`   |
| `**`     | Power          | `4 ** 2 = 16` |
**Python Assignment Operators**

| Operator | Name                      | Example                  |
| -------- | ------------------------- | ------------------------ |
| `=`      | Assignment Operator       | `a = 7`                  |
| `+=`     | Addition Assignment       | `a += 1 # a = a + 1`     |
| `-=`     | Subtraction Assignment    | `a -= 3 # a = a - 3`     |
| `*=`     | Multiplication Assignment | `a *= 4 # a = a * 4`     |
| `/=`     | Division Assignment       | `a /= 3 # a = a / 3`     |
| `%=`     | Remainder Assignment      | `a %= 10 # a = a % 10`   |
| `**=`    | Exponent Assignment       | `a **= 10 # a = a ** 10` |
**Python Comparison Operators**

| Operator | Meaning                  | Example                   |
| -------- | ------------------------ | ------------------------- |
| `==`     | Is Equal To              | `3 == 5` gives us `False` |
| `!=`     | Not Equal To             | `3 != 5` gives us `True`  |
| `>`      | Greater Than             | `3 > 5` gives us `False`  |
| `<`      | Less Than                | `3 < 5` gives us `True`   |
| `>=`     | Greater Than or Equal To | `3 >= 5` give us `False`  |
| `<=`     | Less Than or Equal To    | `3 <= 5` gives us `True`  |
**Python Logical Operators**

|Operator|Example|Meaning|
|---|---|---|
|`and`|a **and** b|**Logical AND**:  <br>`True` only if both the operands are `True`|
|`or`|a **or** b|**Logical OR**:  <br>`True` if at least one of the operands is `True`|
|`not`|**not** a|**Logical NOT**:  <br>`True` if the operand is `False` and vice-versa.|*
**Python Bitwise Operators**

| Operator | Meaning             | Example                   |
| -------- | ------------------- | ------------------------- |
| `&`      | Bitwise AND         | x & y = 0 (`0000 0000`)   |
| `\|`     | Bitwise OR          | x \| y = 14 (`0000 1110`) |
| `~`      | Bitwise NOT         | ~x = -11 (`1111 0101`)    |
| `^`      | Bitwise XOR         | x ^ y = 14 (`0000 1110`)  |
| `>>`     | Bitwise right shift | x >> 2 = 2 (`0000 0010`)  |
| `<<`     | Bitwise left shift  | x 0010 1000)              |
**Python Special Operators**

|Operator|Meaning|Example|
|---|---|---|
|`in`|`True` if value/variable is **found** in the sequence|`5 in x`|
|`not in`|`True` if value/variable is **not found** in the sequence|`5 not in x`|

## **Lists**
1. Lists are mutable that is their values can be changed after assigning them
2. Lists are ordered that is they have a definite order and that order will not change 
3. There can be duplicate values inside a list
4. Lists can contain various data types like string integers and Boolean values even the same list can have all data type in them
5. List can be assigned using the [ ] brackets or the list() function

Traverse through the list using a for loop
```Python
list=["Apple", "Banana", "Orange"]
[print(i) for i in list]
```

**List Comprehension**
List comprehension offers a shorter syntax when you want to create a new list based on the values of an existing list. 
For ex if we already had a list of fruits and we only wanted the fruits that has an "a" in them in another list we can write the following code
```Python
List1 = ["Apple", "Banana", "Mango", "Orange", "Cherry", "Kiwi"]
list2=[i for i in fruits if "a" in x]
print(List2)
```
The syntax:
```Python
newlist = [_expression_ for _item_ in _iterable_ if _condition_ == True]
```

**List Methods**
1. sort()- This method is used to sort lists alphanumeric and ascending by default. We can use "reverse=True" parameter to sort descending order using the "key" parameter we can also give custom sorting parameters 
2. reverse()- This method reverses the order of  the list 
3. append()- This method is used to add an element at the end of the list takes only 1 argument of any datatype and adds it at the end of the list
4. extend()- This method is used to add specific number of elements or an iterable at the end of the list
5. insert()- This method is used to add an element at any given index it takes two arguments the index value first then the element
6. pop()- This method removes the last element of the list by default but can take an index value as an parameter and delete that value instead
7. remove()- this method removes the first occurrence of the argument passed on

## **Tuples**
1. Tuples are immutable 
2. 