# Python Week 7 Assessed Workshop

---

#### Note on workshop attendance...

Please make sure you sign the workshop attendance sheet. 

Work that has been submitted via remote working for core workshops will only be accepted if:

 - students have arranged this with module lead (Phil)
 - students agree that inclusion of remote work in assessed portfolio may require a viva discussion to check understanding

---

Work in CodeSpaces. 

You may use the following cheat sheets if you need to look up any Python commands.

https://github.com/phil-lewis-exe/PythonCheatSheets

**This week you should not use any other websites to help you code.**

**You must ask if you need to use a website to translate the task questions**

**Mobile phones may not be used in class**

---

## TASKS

Look at the following statements. Can you guess which are True and which are False?

 - A typical cloud weighs around a million tonnes
 - 900 million years ago a day lasted 48 hours
 - A chicken once lived for over a year without a head
 - Chainsaws were first invented for brain surgery
 - Ants are the smallest insect to have functioning lungs
 - One in 18 people have a third nipple
 - Hippos have been recorded as swimming up to 3 miles

Three of the above are True(!)

Our aim today is to make a Python quiz in which players have to successfully guess which statements are `True` or `False`. 

After each attempt they get feedback on how many they have correct. 

If they get all 7 correct within 4 attempts they win.

You can try a version of this game coded (by GenAI) in JavaScript as a webpage here:

https://gemini.google.com/share/8ca9566b360d

To code the game we will put the statements and associated data into a list, each item in the list is a dictionary with keys:

 - `'text'` stores the statement which may be True or False
 - `'answer'` stores a `'T'` or `'F'` character according to the correct answer
 - `'guess'` is used as a place to store the player's current guess for that question

An example question dictionary is below where the player has entered a guess `True`, (but the answer is actually `False`)

```python
item = {"text": "Hippos have been recorded as swimming up to 3 miles",
        "answer": "F",
        "guess": "T"}
```

(Actually Hippo's can't really swim at all!).

A set of three questions will be stored as a `list` of dictionaries like:

```
q_list = [
    {"text": "Two plus two equals seven",
     "answer": "F",
     "guess": None},
    {"text": "A carrot is the same colour as an orange",
     "answer": "T",
     "guess": None},
    {"text": "Ten divided by two is five",
     "answer": "T",
     "guess": None}  
]
```

and we can loop over the questions using code like:

```python
for item in q_list:
    # how to get parts of the question
    text = item['text']
    answer = item['answer']
    guess = item['guess']

    # display them
    print(f"{text}... T or F?")
    print(f"You said {guess} and the answer is {answer}!")
```

Your job is to develop some functions that will let us run this quiz in Python.

### Part 1: 

Work in code file `7b_part1.py`

This contains starter code with a `q_list` in which the `'guess'` entries are all intialised to `None`.

We want a function `init_guesses(q_list)` that can initialise or reset all the entries in `q_list` so they store a `'?'` question mark character.

It should work for a set of questions of any size in the above format.

The code file has been set up to automatically test the `init_guesses` function when the following command is run:

```
python 7b_part1.py
```

The expected output is to see the `q_list` with the `guess` entries all storing a `?` character.

### Part 2: 

Work in code file `7b_part2.py`

The next step is to work on the code that accepts a set of answers from the player. This should be provided as a string containing the appropriate number of T or F characters. For example if our guesses are:

 -  "Two plus two equals seven" is False
 -  "A carrot is the same colour as an orange" is True 
 -  "Ten divided by two is five" is True

We would type in `FFT` and hit enter. The function includes code to convert this into a list of characters and write the guesses into the question dictionaries already.

Your task is to add validation to the user input, in a function called `take_valid_guess(q_list)` using the part completed template provided this should:

 - loop to request player input until a valid guess string has been entered
 - before validation your code should convert the string to UPPER CASE
 - your validation should check the string is the right length (one character for each question)
 - it should also check that after coverting case all entries store "T" or "F" only

The code is set up so that when you run the file you will see the question list and can check your guesses have been entered, and that non-valid guesses are rejected, i.e. run

```
python 7b_part2.py
```

### Part 3: 

Once valid input has been provided and guesses have been entered into the question list entries we need to count the number of correct guesses.

The function `check_results(q_list)` needs to check the `guess` and `answer` for each item in `q_list` to see if they match, if so it should increment the count of correct answers. This count should then be returned by the function.

The code is set up so that when you run the file using the command below a set of different guesses will be made. 

```
python 7b_part3.py
```

The correct output if your counts are correct should be:

```
Result for ['T', 'F', 'F']: 0
Result for ['T', 'F', 'T']: 1
Result for ['T', 'T', 'F']: 1
Result for ['F', 'F', 'F']: 1
Result for ['F', 'F', 'T']: 2
Result for ['F', 'T', 'F']: 2
Result for ['T', 'T', 'T']: 2
Result for ['F', 'T', 'T']: 3
```

### Part 4: 

This file contains copies of the remaining functions we need to run a copy of the game. `play_game(q_list)` runs the main game loop, and `print_questions(q_list)` displays the question board with the players current guesses and how many correct answers they have.

The code provided will work except that the correct answer count is missing. (You can copy your `check_results(q_list)` over the incomplete one included to fix this).

Your task is to examine the `play_game(q_list)` function and edit so that the game will end after the maximum allowed attempts are made, i.e. the game loop will
exit setting `finished = False`, and `success = False` so the correct end message is shown.

The code is set up so that when you run the file using the command below and enter four unsuccessful guesses you should see the message:

```
python 7b_part4.py
```

```
You used all your attempts! Bad luck!
```

The final part of this task is to fully complete the code by copying in working code from parts 1-3 to replace all the template functions
at the bottom of this file i.e.
 -  `init_guesses(q_list)`
 -  `take_valid_guess(q_list)` 
 -  `check_results(q_list)`
and to edit the code play_game() to make use of `take_valid_guess()` function assuming you have it working.

When this is complete you can play the game!

As an (optional - non marked) extension you can create file `7b_part6.py` and set up a set of alternative questions and explore making any changes you think would improve the game!


---

### Submitting your work

Run the following lines in the terminal to stage, commit and push your code back to your GitHub repository:

```
git add .
git commit -m "completed 7b"
git push
```

To check your work has been saved you can run the line of code below in the terminal to get the web address of the repository in GitHub. Goto the repository and check the completed code files are stored.

```
git config --get remote.origin.url
```
