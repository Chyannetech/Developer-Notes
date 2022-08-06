
What is Control Flow?

Conditional Expressions

Branching Statements

Looping Statements


#### What is Control Flow? 
"The execution sequence of instructions in a program determined at run time with the use of control structures".

#### Basic Types of Control Flow
* Sequence:Statements execute one at a time in sequence.
* Branching:Different code paths are executed based upon a conditional expression.
* Looping:Code is repeatedly executed while a condition is truthy.

##### Conditional Expressions
In JavaScript, what is considered to be True/Truthy & False/Falsey?

Comparison Expressions



What is True/Truthy & What is False/Falsey?
To test what is truthy and what is falsey, let's type the following code into script.jsinside our repl.it:

if (true) {
  console.log('truthy!');
} else {
  console.log('falsey!');
}
We can "run" this code using repl.it's built in JavaScript Engine by pressing the [ run ]button

Now we can easily test expressions by typing it in the place of true

Why this truthy and falsey business? Why not just use true and false?

Answer: Truthy and falsey are conceptual and an attempt to treat non-boolean expressions as booleans (trueor false) during runtime. The concept of truthiness/falseyness will often allow us to write code that is more concise

For example, the number 3, is considered to be truthy - test it out



What is True/Truthy & What is False/Falsey? (cont)
Most things in JS are truthy, so it's easier to remember what's falsey...

There are two data types that are always falsey: nulland undefined

There are four values that are falsey: false, 0(zero), NaN(special value of number), and an empty string (FYI, a string with a value of a space is not empty)

Everything else is truthy!

Take a couple of minutes to test a few of the above



The Not Operator
The not operator (!), also known as the "bang" operator, "flips" a true or truthy expression to the boolean value of false, and vice-versa.

For example, test the following expressions:

!false === true // true
!null === true // true
!3 === false // true
!'' === true // true
A double !operator is a great way to force an expression into its actual boolean value of trueor false:

console.log(!!3); // outputs true


Boolean Logic Comparison Operators
Let's review these Comparison Operators that you saw in the pre-work:

===strict equality - best practice
==performs type conversion (called coercion) if necessary
!==strict inequality
!=inequality
<less than
>greater than
<=less than or equal
>=greater than or equal
The logical operators ||and &&are more powerful than meets the eye

The logical ||(OR) operator always returns the first operand if it is truthy, otherwise the second operand is returned:

'hello' || 'goodbye'  // evaluates to 'hello'
0 || null  // evaluates to null
The logical &&(AND) operator always returns the first operand if it is falsey, otherwise the second operand is returned:

'hello' && 'goodbye'  // evaluates to 'goodbye'
0 && null  // evaluates to 0


Conditional Expressions
The if, forand whilestatements all require a conditional expression. For example:

let x = 1;
while (x <= 10) {
  var msg = 'Item ' + x;
  console.log(msg);
  x++;
}
Where, x <= 10is the conditional expression.

❓ If x <= 10was replaced with just x, would it still be considered a valid conditional expression?



Review Questions
❓ Is the value of 0 (zero) truthy or falsey?

❓ Is an empty string truthy or falsey

❓ Is an "empty" object (an object with no properties) truthy or falsey?

❓ What value does !!0evaluate to?



The if..else Branching Statement
As you saw in the pre-work, the ifand the optional elseclause allows us to conditionally execute code


The if Branching Statement Single Path
Single path if:                

if (val === 1) {
	console.log('This code will run only if val equals 1');
}
Conditional expression must be surrounded by parens

If you have only a single statement that needs to execute, you can write that statement without using curly braces (used to define a block statement):

if (val === 1) console.log('This code will run only if val equals 1');
This code is the same as the example above.



The if..else (dual path)
Dual paths ifwith else:

if (val === 1) {
	console.log('val is one');
} else {
	console.log('val is not one');
}


The if..else..if (three or more paths)
If you have three or more code paths use ifwith as many else ifstatements as necessary and optionally a final else:

if (val === 1) {
	console.log('val is one');
} else if (val === 2) {
	console.log('val is two');
} else if (val === 3) {
	console.log('val is three');
} else {
	console.log('not one, two, or three');
}
As always, the final elseis optional

Any questions regarding branching with if...else?



💪 Exercise - Branching Statements (5 mins)
Write the if...else..ifstatement that console.logs the following based upon the value of a variable named color:

If the value is green, log Go
If the value is yellow, log Slow
If the value is red, log Stop
If the value is anything else, log Whatever
Hint: Don't forget to declare and initialize a variable named color

As always, be sure to ask your instructional team for help if you get stuck!



Looping Statements
Looping statements provide us with the ability to execute a block of code multiple times while a conditional expression is truthy

We'll take a look at these statements:

while

do while

for



Looping Statements while
The first looping statement we'll look at is while:

let word = '';
let words = [];
while (word !== 'end') {
	word = prompt('Enter a word ("end" to quit)');
 	if (word !== 'end') words.push(word);
	alert("You've entered: " + words.join(', '));
}
Use whilewhen you want to continue to execute a block of code while a condition is true

Beware of infinite loops!



Looping Statements do...while
You may choose to use the do...whilestatement instead of whileto force the code block to always execute at least once

let num = 0;
do {
	console.log(num);
	num += 2;
} while (num <= 10);
Do you see why the code block will always run at least once?

Again, beware of infinite loops!



Looping Statements for
The next looping statement we'll look at is the forstatement:

let colors = ['red', 'white', 'blue'];
for (let idx = 0; idx < colors.length; idx++) {
	console.log(colors[idx]);
}
Notice the forloop has three parts after the for keyword:
The initializer which runs only once before looping begins. It is used to declare and initialize a looping variable.
The condition which will be evaluated before each loop. If truthy, the code block will execute.
The last part will execute after each loop and is typically used to increment or decrement the looping variable by one or more units.


Looping Statements break
Use the breakstatement within any whileor forloop to immediately exit the loop:

let word = '';
let words = [];
while (true) {
word = prompt('Enter a word ("end" to quit)');
	if (word === 'end') break;
	words.push(word);
	alert("You've entered: " + words.join(', '));
}
Note how the ifstatement does not require braces in this case.