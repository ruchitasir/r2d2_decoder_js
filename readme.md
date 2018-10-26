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

![](https://media.giphy.com/media/l0O2Q22fPpxR0zhba/giphy.gif)

### Walkthrough

Let's say R2D2 gave you 2 beeps and 6 boops. We'll add them together to get a total.

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

So, according to the chart, the first letter is `H`. Great!
Here is the full list of inputs you've got written down:

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

Now, this one's short enough to figure out by hand, but not every message is! In fact, there are a bunch more messages for you to decode at the end, so let's make a programmatic solution instead. We'll begin by storing those beeps and boops into an array. Stored in an array of arrays, those inputs look like this:

```javascript
let inputs = [[2, 6], [0, 5], [9, 3], [4, 8], [10, 5], 'BOP', [11, 12], [5, 10], [1, 17], [5, 7], [4, 0]]
```

> Notice we can mix different types in an array! This array holds other arrays AND strings (the BOPs)

Next let's make a JavaScript object to represent the table above. Remember that objects are made of key-value pairs. We'll use the number as the key and the letter as the value. It will look like this:

```javascript
let decoderTable = {
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

It's up to you whether to remove or write code to deal with each `BOP`! It's in the table in case you want to print out the spaces between words!

Now it's your job to figure out the rest of the message! Let's put it into code! By writing code to do this and not just solving it by hand, we can figure out any message we put in! More messages for you to decode are at the end of this assignment.


#### Expected Output

Once you've written the code to add up the totals, loop through the totals, and look them up in the decoder table, it should be printing one letter per line. This is because `console.log` adds a newline at the end.

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

## Directions

1. Find the file provided in this repository called `solution.js`. The input and table are provided as starter code.

2. Open `solution.js` in `Sublime Text`, `Atom`, `VS Code`, or your text editor of choice.

3. Write your code - solve the problem! Remember to hit `save`! There are hints in the comments of the `solution.js` file if you get confused. Refer to the [Reminders and Example Code](#reminders-and-example-code) section below for examples of using arrays, loops, and objects.

* First make an array called `letters`
* Loop over the inputs and store the total beeps + boops in the `letters` array (Refer to [exhibits A, B, C, and D](#exhibit-a-adding-to-an-array))
* A full letters array will look like this for the first message:

```javascript
[8, 5, 12, 12, 15, 'BOP', 23, 15, 18, 12, 4]
```

* Loop over the letters array and access each value ([Exhibit C](#exhibit-c-writing-a-for-loop))
* Use each element in the letters array as a key into the `decoderTable` object ([Exhibit E](#exhibit-e-accessing-a-javascript-object))
* Print the value from the decoderTable with `console.log`

4. Open your Terminal.

> **Protip**: Ask a friend or consult the class notes if you have forgotten how to do this!

5. Navigate to the correct location in your file system

> **Protip**: You may need to use the `cd` command to navigate to the location your `solution.js` file is at. `cd ..` navigates to the parent folder of the one you're currently in.

6. Type the following command: 

```bash
node solution.js
```

7. Until you get the expected output, you can make changes to your code and run it again to see if you have the answer. Repeat as needed!

8. Think your decoder is up to snuff? Try replacing the original input with the bonus inputs and see if it still works! [BONUS TIME!](#bonus-time)


## Reminders and Example Code

#### Exhibit A: Adding to an array

Remember you can use `push` to add to the end of an array.

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

#### Exhibit B: Accessing an array with an index

When you write a loop, you will often have a variable like `i` that increments each iteration of the loop. `i` is meant to be an index into your array. Here is an example of using indexes without a loop. You can use the number directly or you can use a variable that stores that number. Your computer sees it as the same thing:

```javascript
var letters = [8, 5, 12, 12, 15];
var i = 2;

console.log(letters[i]); // Prints "12"
console.log(letters[2]); // Still prints "12"
```

> Remember! Array counting starts at 0!

#### Exhibit C: Writing a For Loop

When you write a for loop, you have an index `i` that changes each time the loop is run.

```javascript
let myArr = [2, 4, 6, 8];

for(let i = 0; i < myArr.length; i++){
    console.log(myArr[i]);
}

// Prints: 
// 2
// 4
// 6
// 8
```

#### Exhibit D: Accessing an array within another array

Sometimes you need to access a value in an array that is nested within another array. In fact, these can be nested several levels deep! Let's just deal with one level for now. Let's assume we have the following array:

```javascript
let nestedArr = [[2, 3, 4], [5, 6, 7], [8, 9, 10]];
```

I would like to access the first value in each inner array: 2, 5, and 8. However, if we access it the same way we did in Exhibit C, we get the entire inner array!

```javascript
for(let i = 0; i < nestedArr.length; i++){
    console.log(nestedArr[i]);
}

// Prints: 
// [2, 3, 4]
// [5, 6, 7]
// [8, 9, 10]
```

Not what we wanted! I actually have to provide a ~second~ index for the second array. I can actually just add another set of `[]` at the end. In this case I want only the first element, so I will add `[0]`.

```javascript
for(let i = 0; i < nestedArr.length; i++){
    console.log(nestedArr[i][0]);
}

// Prints: 
// 2
// 5
// 8
```

#### Exhibit E: Accessing a JavaScript object

Remember, JavaScript objects are made up of key-value pairs. You can access the value in an object by its key. It sort of looks like accessing an array, because it uses the square brackets, but instead you are accessing the key inside the brackets rather than an index.

```javascript
let petsObject = {
  'dogs': 5,
  'cats': 2,
  'birds': 3,
  'lizards': 1
};

console.log(petsObject['dogs']); // Prints "5"
```

### Need More Hints?

If you're completely lost, take a look at the solution branch. You can access the solution branch by switching the branch dropdown (on the top left) from master to solution. Then you will see a file called `answers.js`. Take a look at the solution presented and try to work backward and understand what was originally being asked of you.

Hopefully it makes sense after that, but if not, please inform your instructional team!


## BONUS TIME!

1. Think your solution is slick? Try out the following messages in your decoder:

```javascript
// Bonus 1
[[1, 8], 'BOP', [5, 7], [13, 2], [9, 13], [1, 4], 'BOP', [2, 1], [0, 1], [10, 10], [10, 9]];

// Bonus 2
[[9, 16], [13, 2], [13, 8], 'BOP', [2, 1], [0, 1], [10, 4], 'BOP', [2, 2],  [4, 11], 'BOP',  [4, 9], [8, 7], [7, 11], [3, 2], 'BOP', [11, 9], [3, 5], [0, 1], [7, 7], 'BOP', [13, 12], [13, 2], [8, 13], 'BOP', [5, 6], [12, 2], [9, 6], [20, 3]];

// Bonus 3
[[1, 0], 'BOP', [2, 1], [3, 5], [0, 1], [4, 9], [6, 10], [3, 6],  [4, 11], [8, 6], 'BOP', [2, 7], [12, 7], 'BOP', [3, 1], [5, 0], [1, 5], [4, 5], [12, 2], [2, 3], [1, 3], 'BOP', [9, 5], [12, 3], [14, 6], 'BOP', [1, 1], [22, 3], 'BOP', [8, 12], [4, 4], [4, 1], [8, 1], [11, 7], 'BOP', [12, 11], [3, 6], [8, 6], [12, 7], 'BOP', [0, 2], [10, 11], [11, 9], 'BOP', [2, 0], [25, 0], 'BOP', [3, 5], [10, 5], [10, 13], 'BOP', [11, 9], [3, 5], [4, 1], [17, 8], 'BOP', [2, 1], [1, 0], [5, 9], 'BOP', [16, 2], [1, 4], [3, 0], [7, 8], [9, 13], [2, 3], [9, 9], 'BOP', [12, 11], [4, 4], [5, 0], [8, 6], 'BOP', [11, 9], [3, 5], [4, 1], [17, 8], 'BOP', [0, 6], [1, 0], [9, 3], [0, 12]];
```

2. If you got all 3 messages above decoded, write a coded message of your own and see if a classmate's decoder can solve it!

---

## Yay! All done!

<img src="https://media.giphy.com/media/UOpdmwKA7la0g/giphy.gif" alt="Github failed to load image. Thanks Github">

Now, if you want to know a little more about why that particular message was chosen, [read up here](https://blog.hackerrank.com/the-history-of-hello-world/)!


