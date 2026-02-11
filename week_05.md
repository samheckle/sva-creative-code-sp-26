# Week 05: 2/10/26

## Agenda

1. Homework Share
2. Reading Discussion
3. Tutorial: Repetition and Loops
4. [Demos, Videos, Useful Links](#demos)

---

## Homework Share

- Share your work & documentation. If there were any parts where you struggled, share those questions and see if your group can find an answer.

## Reading Discussion

Questions to consider:

1. Discuss the feedback loop between media > new media. What is the role of the computer as a "media synthesizer and manipulator"? Is this a positive or negative description in your opinion? What other roles does your computer have?

   > The pretense of modern media to create simulations of sensible reality is similarly canceled; media are reduced to their original condition as information carrier, nothing less, nothing more. In a technological remake of the Oedipal complex, a son murders his father. The iconic code of cinema is discarded in favor of the more efficient binary one. Cinema becomes a slave to the computer... Media and computer...merge into one. All existing media are translated into numerical data accessible for the computer... In short, media become new media. (pg. 25)

2. Think about the different principles Manovich defined: Numerical Representation, Modularity, Automation, Variability, Transcoding. Do you agree with these categories? Which ones would you replace, and what with? What about the term of "new media"? Starting on page 49 which defines "What New Media Is Not", do you agree with these definitions?

3. What is the importance of computer literacy in new media art? Think about the contexts in which code is created (most code examples are in English, privilege of using a computer from a young age)? What are ways we can break from these contexts to make media art more accessible?

> What I call the "computer layer" is not itself fixed but rather changes over time. As hardware and software keep evolving and as the computer is used for new tasks and in new ways, this layer undergoes continuous transformation. The new use of the computer as a media machine is a case in point. This use is having an effect on the computer's hardware and software, especially on the level of the human-computer interface, which increasingly resembles the interfaces of older media machines and cultural technologies. (pg. 46)

Question for all: _Who makes computers and determines how they are used?_

## Tutorial: Repetition and Loops

### Review

Begin by making a new sketch titled "In-Class 5.1".

- Create 20 columns
- With an if-statement, make a single column turn red when you hover over it. Each column should _not_ have a fill until they are hovered. They can either have `noFill()` or a fill of white.

### Identifying Patterns

With your sketch you just made, what pattern are we seeing? How can we mathematically relate each rectangle with one another?

### Coding Glossary: Loops

<table>
<tbody>
<tr><td>loop</td><td>

code that repeats the content inside `{}`. the `draw()` is a loop that already exists for us.

</td></tr>
</tbody>
</table>

### While Loop

A `while()` loop is very similar to an `if()` statement. They follow similar syntax that use `()` and `{}`.

When we build out an `if()` statement, we put the conditional expression inside the `()` and the code that is locked in the `{}`. A `while()` loop is the same.

```js
while(conditional expression){
    // loop something
}
```

But, there are some extra steps in order to get the loop functional.

<h1>

It is super important at this point to make sure you do not have `Auto Refresh` checked in your p5 editor.

 </h1>

1. The first thing we want is to declare a number that will control the loop and determine _when the loop stops_. This is just a normal variable.

```js
let iterator = 0;
```

2. Next, we determine how many times our loop wants to execute using our new variable and a conditional expression. Once this conditional becomes `false`, the loop stops.

```js
iterator < 10;
```

This means our loop will iterate 9 times, starting at 0. This conditional is what goes inside the `()` of our `while()`

```js
while (iterator < 10) {}
```

3. We need to change our variable inside our loop, meaning inside the `{}`. This is just like a variable changing in the draw, where it increments once it hits the bottom (or wherever the variable is located).

```js
while (iterator < 10) {
  iterator += 1;
}
```

Our final code for our loop will look something like:
![loop](https://raw.githubusercontent.com/samheckle/code-toolkit-fa-25/main/images/week_04/loop.gif)

### For Loop

A `for()` loop is a shorthand way of writing a `while()` loop. Instead of having 3 separate lines of code (declaring iterator, writing conditional, incrementing iterator), we do it all inside the `()` of the `for()`, all separated by a `;`.

To write

```js
let iterator = 0;
while (iterator < 10) {
  iterator += 1;
}
```

As a `for()` loop, we combine all these lines into one.

```js
for (let iterator = 0; iterator < 10; iterator += 1) {
  // do something 10 times
}
```

---

## Demos

## Review Videos

- [4.1: While and For Loops](https://www.youtube.com/watch?v=cnRD9o6odjk)
- [4.2: Nested Loops](https://www.youtube.com/watch?v=1c1_TMdf8b8)
