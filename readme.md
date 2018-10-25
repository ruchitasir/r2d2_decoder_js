### ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) GA Web Development Immersive

<!---
This assignment was developed by Brandi

Questions? Comments?
1. Log an issue to this repo to alert me of a problem.
2. Suggest an edit yourself by forking this repo, making edits, and submitting a pull request with your changes back to our master branch.
3. Hit me up on Slack @brandib
--->

# JavaScript Basics: Variables and Local Files

## Overview

So, you're learning JavaScript! Let's put your skills to the test!

You will practice these programming concepts we've covered in class:

* Using mathematical operators
* Declaring, adding to, and looping through arrays
* Declaring and accessing JavaScript objects
* Running local `.js` files from your terminal with the `node` command

---

## Deliverables

For the challenges below, you will create a new `.js` file and write code to solve the problem. In this case, you will create `solution.js` for your solution code to the problem. Run the file from the command line to check your work. Detailed directions are given below

*Reminder: On your laptop, you can run the file from your command line with the following command:*

```bash
node solution.js
```

> **Hint**: Make sure you are printing something out with the `console.log()` statement! Otherwise, you won't see any output from running your program!

## Requirements:

* By the end of this, you should have a `.js` file for the solution 
* We know you're just starting out, so there is just one challenge problem!

---

## Problem: Decoding R2D2

You have a robot who communicates in a series of beeps and boops. You usually get the gist of what he means, but just once it would be nice to know what's really on his mind! You've noticed a pattern in the beeps and boops, and it seems like the number of beeps and boops correspond to specific letters. Sort of like morse code!

#### Example Code

```
let beeps = 2;
let boops = 6;
let total = beeps + boops;
console.log(total); // prints 8
```

You got a result of `8`. Now, look that up in the corresponding key-value chart:

| Code | Letter |
| ----- | ----- |
| 1 | A |
| 2 | B |
| 3 | C |
| 4 | D |
| 5 | E |
| 6 | F |
| 7 | G |
| 8 | H |
| 9 | I |
| 10 | J |
| 11 | K |
| 12 | L |
| 13 | M |
| 14 | N |
| 15 | O |
| 16 | P |
| 17 | Q |
| 18 | R |
| 19 | S |
| 20 | T |
| 21 | U |
| 22 | V |
| 23 | W |
| 24 | X |
| 25 | Y |
| 26 | Z |

So, according to the chart, the first letter is `H`. Great! Now it's your job to figure out the rest of the message! However, we don't want to look up each letter manually! Let's put it into code! You can use the following JavaScript object in your code. (Go ahead and copy it into your `solution.js` file when you're ready!

```javascript
let table = {
  1: 'A',
  2: 'B',
  3: 'C',
  4: 'D',
  5: 'E',
  6: 'F',
  7: 'G',
  8: 'H',
  9: 'I',
  10: 'J',
  11: 'K',
  12: 'L',
  13: 'M',
  14: 'N',
  15: 'O',
  16: 'P',
  17: 'Q',
  18: 'R',
  19: 'S',
  20: 'T',
  21: 'U',
  22: 'V',
  23: 'W',
  24: 'X',
  25: 'Y', 
  26: 'Z',
  'BOP': ' '
};
```

Here is the full list of inputs you've got written down.

```
2 beeps, 6 boops
0 beeps, 5 boops
9 beeps, 3 boops
4 beeps, 8 boops
10 beeps, 5 boops
BOP! (pretty sure this is a space!)
11 beeps, 12 boops
5 beeps, 5 boops
1 beep, 17 boops
5 beeps, 7 boops
4 beeps, 0 boops
```

Stored in an array of arrays, those inputs look like this:

```javascript
let inputs = [[2, 6], [0, 5], [9, 3], [4, 8], [10, 5], "BOP", [11, 12], [5, 5], [1, 17], [5, 7], [4, 0]];
```

It's up to you whether to remove or write code to deal with the "BOP"s!

#### Example Code

```
// Letters array starts out empty
let letters = [];

// First letter
let beeps = 2;
let boops = 6;
let total = beeps + boops;

// "push" adds the total to the letters array
letters.push(total);
```

A full letters array will look something like this:

```javascript
[8, 5, 12, 12, ... , 4]
```

Once you have a full letters array write a `for` (or `forEach`) loop to iterate through the items in the letters array. 

```javascript
// Array values can be accessed inside a for loop using the index, i
// Remember! Array counting starts at 0!
var letters = [8, 5, 12, 12, 15];
var i = 2;

console.log(letters[i]); // Prints "12"
```

Once you have your loop looping, inside that loop, access the value in the array and use it as a key to access the object. Remember, JavaScript objects are made up of key-value pairs. You can access the value in an object by its key.

```javascript
let petsObject = {
  'dogs': 5,
  'cats': 2,
  'birds': 3,
  'lizards': 1
};

console.log(petsObject['dogs']); // Prints "5"
```

#### Expected Output

```
S
E
C
R
E
T

M
E
S
S
A
G
E
```

### Run it!

1. Find the file provided in this repository called `solution.js`. The input and table are provided as starter code.

2. Open `solution.js` in `Sublime Text`, `Atom`, `VS Code`, or your text editor of choice.

3. Write your code - solve the problem! Remember to hit `save`! There are hints in the comments of the `solution.js` file if you get confused.

4. Open your Terminal.

> **Protip**: Ask a friend or consult the class notes if you have forgotten how to do this!

5. Navigate to the correct location in your file system

> **Protip**: You may need to use the `cd` command to navigate to the location your `solution.js` file is at. `cd ..` navigates to the parent folder of the one you're currently in.

6. Type the following command: 

```bash
node solution.js
```

7. Until you get the expected output, you can make changes to your code and run it again to see if you have the answer. Repeat as needed!


### BONUS TIME!

Think your solution is slick? Try out the following messages in your decoder:

```javascript
let bonus1 = [[1, 8], 'BOP', [13, 2], [6, 11], [1, 4], 'BOP', [2, 1], [0, 1], [10, 10], [12, 9]]; 
```

---

## Yay! All done!

<img src="https://media.giphy.com/media/UOpdmwKA7la0g/giphy.gif" alt="Github failed to load image. Thanks Github">

Now, if you want to know a little more about why that particular message was chosen, [read up here](https://blog.hackerrank.com/the-history-of-hello-world/)!


