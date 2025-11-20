# Python Week 8 Assessed Workshop

---

#### Note on workshop attendance...

For advanced workshops completion of the activities must be under invigilated conditions.

Please make sure you sign the workshop attendance sheet. 

Code should autosave, but you must still commit your work at the end of the workshop before leaving.

---

**Do all coding in CodeSpaces only** 

You may use the following cheat sheets if you need to look up any Python commands.

https://github.com/phil-lewis-exe/PythonCheatSheets

**This week you should not use any other websites to help you code.**

**You must ask if you need to use a website to translate the task questions**

**Mobile phones may not be used in class**

---

## TASKS

# Workshop 8b

This workshop has three sections. 

The **average 2:1** student is expected to complete **most of parts 1 and 2** within the time allocated. 

It is expected that the only the **few fastest high 1st class** students in the class will complete **all of the tasks** in the time allocated.

The weighting for each section in the advanced workshops is approximately: part 1 (40%) part 2 (35%) part 3 (25%), but may be moderated to reflect difficulty of different workshops.

---

## Part 1

This section includes 10 short tasks covering skills on the module so far. 

If you get stuck on a particular task you are advised to move on and revisit it if you have time.

---

#### Part `1abc`

The following lines define
a variable and then print
a line to describe what type of 
data object has been created

```python
x = 4.5
print("x:float")
```

Do the same for the variables below.
You should select from the folowing options:

`int` `float` `list` `dict` `tuple`
`str` `function` `bool`


```python
# file: 8b_part1abc.py

a = 7.0
print("a:")

b = "True"
print("b:")

c = [ "key", "value" ]
print("c:")
```

---

#### Part `1d`

This code below should define a list storing `12, 3, 6`

```python
# file: 8b_part1d.py

# fix this line
mylist = 12, 3, 6
```

---

#### Part `1e`

The code below should define
a string that displays on two lines
as shown below:

```
line one
line two
```

```python
# file: 8b_part1e.py

# fix the line below
mystr = "line one line two"
```

---

#### Part `1f`

The function should return
the sum of two numbers
passed as arguments

It contains an error to fix:

```python
# file: 8b_part1f.py

def add_numbers(): # fix this line
	return a + b

print( add_numbers(3,4) )
```

---

#### Part `1g`

The following code should select
the last letter in the string

It should work even if a different
string was given

```python
# file: 8b_part1g.py

letters = "abcde"
print(letters)

last_letter = letters[5] # fix this line
print(f"last letter is: {last_letter}")
```

---

#### Part `1h`

A quiz game stores a question and correct answer.

The user is asked to type in their answer (an example answer is given below).

The code should perform a **case insensitive** comparison
to print if the answer is right or wrong
but currently does not do this.

```python
# file: 8b_part1h.py

question = "What grows on apple trees?"
correct_ans = "apples"

user_ans = "APPLES"


if user_ans > correct_ans: # fix this line
	print("correct")
else:
	print("wrong")
```

---

#### Part `1i`

A program has to check a weight
value is not too heavy. 

It should return:

 - `True` : if less or equal to the given limit
 - `False` : if more than the given limit

Edit the code so it does this correctly

```python
# file: 8b_part1i.py

def check_weight_ok(x, limit = 240.0):

	if x: # fix this line
		return True
	else:
		return False

print( check_weight_ok(230) )
print( check_weight_ok(240) )
print( check_weight_ok(250) )
```

---

### Part `1j`

The code below stores information in variable `z`

Replace the `XXXX` so that the information in `z`
is displayed correctly 

i.e. lines like `grass is a plant`

```python
# file: 8b_part1j.py

z = {"apple": "fruit", "green": "colour"}

for key in z.keys():
	print( f"{XXXX} is a {XXXX}" ) # fix this line
```


---


## Part 2

Work in files `8b_part2.py` and `football_card.py`

A game is being written similar to Top Trumps / Pokemon.

Players play with character cards that list a set of attributes.

This game will use football players as the characters. 

Each card stores the following attributes:

 - `name`:	 player name (str)
 - `attack`:  value from 1-100 (int)
 - `defence`: value from 1-100 (int)
 - `speed`:   value from 1-10  (float)

---

**a)** In file football_card.py define the class `FootballCard`,
and add a constructor function that takes arguments: 

 - `name`
 - `attack`
 - `defence`
 - `speed`

in that order, storing the data into named attributes (`name`, `attack`, `defence`, `speed`)

---

**b)** In file `8b_part2.py` write code to import your class definition,
and create a football card object `mycard` with data:

```
name: Harry Kane
attack: 87
defence: 45
speed: 8.5
```

---

**c)** Edit your class file to add a `__str__` method so that you
can print the `FootballCard` objects. They should display 
on a single line in the format below.

```
Harry Kane attack:87 defence:45 speed:8.5
```

---

**d)** Add a line to your `test_class.py` file to demonstrate how this is called.

---

**e)** The game classes players into two types:
 
 - `"defender"` (when attack score is less than defence score)
 - `"attacker"` otherwise

Add a class method `get_type` that returns a string
`"attacker"` or `"defender"` according to the criteria above.

---

**f)** Add a line to your `test_class.py` file to demonstrate how this is called,
storing the result as variable `card_type`


---



## Part 3

Work in file `8b_part3.py`

Write a function `get_player_info()` that would enable a user to enter data describing a football player in the following order:

`name`: `str` (max length 50 characters)
`attack`: `int` (1-100)
`defence`: `int` (1-100)
`speed`: `float` (0-10)

It then returns this data in a tuple `(name, attack, defence, speed)`

Before asking for each input your code should print a message as below

```
"Enter your player name (max 50 char):"
"Enter attack score (1-100):"
"Enter defence score (1-100):"
"Enter speed (0-10):"
```

Then use code like below to collect input into a variable:

`____ = input("> ")`

Your code can assume that the user always enters a valid data type (string for name, and string that can be converted to an `int` for attack & defend or `float` for speed).

Your code should repeat a prompt when an entry is invalid until a valid value is given 
(i.e. `name` more than 50 char, `attack`/`defence`/`speed` outside the allowed ranges)



---

### Submitting your work

Run the following lines in the terminal to stage, commit and push your code back to your GitHub repository:

```
git add .
git commit -m "completed 8b"
git push
```

To check your work has been saved you can run the line of code below in the terminal to get the web address of the repository in GitHub. Goto the repository and check the completed code files are stored.

```
git config --get remote.origin.url
```
