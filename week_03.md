# Week 03: 1/28/26

## Agenda

1. How to Write Good Documentation
2. Lecture: Interaction
3. Tutorial: Conditionals
4. [Demos, Videos, Useful Links](#demos)

---

## How to Write Good Documentation

Feel free to reference this for future documentation

If it is easier to write about your assignment in google doc, figma, ppt that is totally fine, just make it accessible to me in some way.

1. No high level overviews! Literally walk me through what you did:
   - what did you try?
   - What images/references did you pull?
   - How did you determine color?
   - Inspirational artists? How did you land on the aesthetic?
2. Include any sketches!
   - Illustrator is helpful to get shapes correctly
   - Procreate to play with different designs
   - Any moodboards, figma, miro, google docs
   - Pen and paper
3. What were things you experimented with?
   - What experiment put you on the path for your final design? Take screenshots & screen recordings of any visual outputs.
4. Include any links
   - Citation of AI usage
   - Links to StackOverflow, Youtube Tutorials, p5 reference
   - Any other p5 sketches you might have looked at.

## Lecture: Interaction with Conditionals and Events

### Coding Glossary

<table>
<tbody>
<tr><td>boolean</td><td>in reference to boolean expression, can be

`true` or `false`, `0` or `1`

</td></tr>
<tr><td>conditional statement</td><td>uses specific phrases

`if`, `else if`, and `else`

uses comparison and logical operators

</td></tr>
</tbody>
</table>

#### Comparison Operators

In an expression, we have seen both assignment (`=`), and mathematical operators (`+`, `-` etc). We can also use comparison operators to compare between two values of a variable against a number.

This is a way for us to create environments that have particular logic to the interaction, and we need to be explicit about what we are telling the computer in order to make the interaction happen.

| comparison operators     |       |
| ------------------------ | ----- |
| equal                    | `==`  |
| NOT equal                | `!=`  |
| strict equal             | `===` |
| strict NOT equal         | `!==` |
| greater than             | `>`   |
| greater than or equal to | `>=`  |
| less than                | `<`   |
| less than or equal to    | `<=`  |

When we use comparison operators in an expression, it would look something like:

```js
let num = 1;

num < 15; // what does this evaluate to? is it being used anywhere?
```

Comparison expressions evaluate to either `true` or `false`, which is a `boolean`.

#### Differences Between `=`, `==` and `===`?

These are all different syntaxes!

<table>
<tbody>
<tr><td>assignment</td><td>
gives a value to a variable

`=`

</td></tr>
<tr><td>comparison</td><td>checks if two values (like strings or numbers) are equal

`==`

</td></tr>

<tr><td>strict comparison</td><td>checks if two values are even more equal (ie. matches capitalization)

`===`

</td></tr>
</tbody>
</table>

So we should know the distinct differences between `=` and `==`, but we should **_never_** be using `===`.

### Conditional Statements

A conditional statement is an expression that evaulates to `true` or `false` and does code based on that action. Think of it like a flowchart:

<img src="https://kagi.com/proxy/conditional-statements-3-638.jpg?c=OvWOGeaOTSdcGCVl2otm07WhSg9hGsLVk3dKvcnxgwpckV6LOqfeUCn4AcSIFEk4dB-yGQzgYeV0Enh4Sj1xS2Pxgj0IpDrJuQYuj02WnwdD8RfZGbz1JgOUdgk1dK9qv36szAsSWtnbWVjDDdW_GvZhi6rZFYLUDX-hUV6W6AI%3D" width="400px">

We write conditional statements using the syntax `if()` and putting our comparison expression inside the `()`. We also need `{}`, so any code inside of the if-statement's `{}` will be locked behind that logic, and won't execute unless the comparison expression evaluates to `true`.

```js
let num = 1;

fill("red");

if (num < 7) {
  fill("green");
}

circle(width / 2, height / 2, 30);
```

If statements need a different syntax that changes the logic of the flowchart. This is where logical operators come in. We can determine if something has more than one conditional expression, but only if the logical operators are true.

#### Nested Conditional Statements

If statements can be nested, or written inside, of one another.

```js
let num1 = 10;
let num2 = 20;

fill("red");

if (num1 < 7) {
  if (num2 < 25) {
    fill("green");
  }
}

circle(width / 2, height / 2, 30);
```

This means that **_both_** comparisons need to evaluate to true in order for us to have a fill of green. But, we can also use a shorthand with the logical operators.

#### Logical Operators

Logical operators allow us to use more than one expression at a time.

| logical operators |                                                           |
| ----------------- | --------------------------------------------------------- |
| AND               | `&&` if both expressions evaluate to true                 |
| OR                | `\|\|` if either side of the expression evaluates to true |
| NOT               | `!` if the expression is true, make it false              |

So if we wanted to use more than one comparison expression, we need to determine how their logic connects to the previous expression.
This is different functions, where we can pass in multiple parameters delineated by a period, eg. `fill(255, 0, 0)`.

##### `&&`

```js
let num1 = 10;
let num2 = 20;

if (num1 < 7 && num2 < 25) {
  fill("green");
}
```

This does the exact same thing as the example code above, where we nested one if statement inside the other. But now, we need to think about the resulting booleans (from the comparison expressions) + the operators they use. So, we need to evaluate each side of the expression, and then evaluate their total, similar to order of operations.

First, we look at `num1 < 7`, which evaluates to?
Then, we look at `num2 < 25`, which evaluates to?

If it uses the `&&` syntax, BOTH sides need to be true in order to evaluate to true.

##### `||`

With `||`, only ONE expression needs to be true.

```js
let num1 = 10;
let num2 = 20;

if (num1 < 7 || num2 < 25) {
  fill("green");
}
```

So in this example, the fill would be green because ONE side of the logic operator is true.

##### `!`

The NOT operator does a couple of things, but it also means opposite. So it also allows us to assign boolean variables to the opposite of what it was previously. Think of it as multiplying by `-1`.

```js
let event = false;

// if something happens, set event to be the opposite of what it was previously
event = !event;
```

#### Cascading If-Statements

With if-statements, we can cascade them and make an entire flowchart with our code. So `if` something happens, do this. `otherwise`, do something else.

The way this is written in code is using `if`, `else if` and `else`. `if()` and `else if()` need to have a conditional statement inside the parenthesis, but `else` does NOT have a parenthesis because it is a catch all.

```js
let num = 1;
if (num < 7) {
  fill("green");
} else if (num < 10) {
  fill("blue");
} else {
  fill("red");
}
circle(width / 2, height / 2, 60);
```

### Events

<table>
<tbody>
<tr><td>event</td><td>something that happens based off user input
</td></tr>
<tr><td></td><td>

`mouseX`, `mouseY`, `mousePressed()`

</td></tr>
</tbody>
</table>

There are [lots of different types of events in p5.js](https://p5js.org/reference/#Events)

Specifically in this class, we will look at keyboard and mouse events.

#### Difference between `mousePressed()` and mouseIsPressed

Or any other function vs. variable in events.

We know that `mousePressed()` is a function because of `()`

- this happens ONE time when the mouse button is pressed

`mouseIsPressed` is a variable

- this is a `boolean` that evaluates to `true` or `false` if the mouse is CURRENTLY being pressed (and held down)

## Demos

-

## Review Videos

If you struggled with any of the material this week, please review these coding train videos!

- [3.1 - conditional statements](https://thecodingtrain.com/tracks/code-programming-with-p5-js/code/3-conditionals/1-conditionals)
- [3.2 - making a ball bounce](https://thecodingtrain.com/tracks/code-programming-with-p5-js/code/3-conditionals/2-bouncing)
- [3.3 - else, else if, and, or](https://thecodingtrain.com/tracks/code-programming-with-p5-js/code/3-conditionals/3-else-if-and-or)
- [3.4 - boolean variables](https://thecodingtrain.com/tracks/code-programming-with-p5-js/code/3-conditionals/4-boolean)

## Useful Misc Links

-
