# Week 01: 1/14/26

![intro.gif](https://github.com/samheckle/code-toolkit-fa-25/blob/main/images/week_01/intro.gif)

_Source: [Casey Reas, 2010](https://reas.com/p18_s2/)_

---

## Agenda

1. [Syllabus](#syllabus)
2. Introductions
3. Intro to Coding
4. Break
5. Tutorial: Drawing with p5.js
6. In-Class

---

## Syllabus

- If I am ever going too fast through _any_ material, please interrupt me!
- Questions? Comments? Needs? Etc? Send an email. I value open communication more than anything else. If you miss class, expect to be late, or are struggling with an assignment, please let me know.

### [Statement on Technology](https://community.itp.io/community_statement#technology)

> We pledge to center creative and ethical uses of technology in our research, teaching, and making. We accept the claim that technology is a reflection of society, its histories, and its politics. We reject the claim that technology is neutral and acknowledge that every technology has the potential to do as much harm as good. We acknowledge that when technologies cause harm, the harm disproportionately affects Black, Brown, Indigenous, People of Color (BIPOC), queer, trans, disabled, femme, low-income, survivors, and all other marginalized bodies and communities worldwide.
>
> With this understanding, it is our responsibility to center these groups when hosting, participating in, or developing events (e.g. workshops or meetings), materials (e.g. courses, syllabi, resources), technologies (software, hardware, tools, etc) and creative applications made within this classroom (e.g. works of art, products, installations, experiments, etc).

### Expectations and Class Manifesto

1. Be curious!
   - what questions are you asking?
   - what do you not know?
   - how can you find those answers?
     - exploring the p5.js reference is a great past time
2. Practice!
   - learning to code takes time!
   - you _will_ have to do a lot of work outside of class to understand what is going on in the context of your own projects
3. Low Stress **NOT** Low Effort
   - did you learn something new? write it in your documentation!
   - did you struggle? write it in your documentation!
   - did you accomplish what you wanted? write it in your documentation!
   - if you made a solid attempt and wrote documentation (via a discussion post) you get full credit!

### Class Format

Broadly – this is similar to a math class.

You will be taught in class:

- syntax of how the coding language works
- application of how to use the coding language in a broad sense

Outside of class:

- practice the syntax
- contextualize the content in your own projects

A typical week structure might look like:

1. Review previous week’s assignment and questions
2. Introduce new content
3. Practice new content in class
   - You should be following along the demos!
4. Apply new content in upcoming assignment

---

## Introductions

### me

| sam heckle (they/she)                                                                                                                                                                                |                                                                                                          |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| software engineer to creative technologist pipeline                                                                                                                                                  |                                                                                                          |
| things you can ask me about: coding, software engineering, physical computing, sewing, portfolio review, resume review, grad school, games, cats, keyboards, baking, nyc/seattle/san francisco, food | ![works cited](https://github.com/samheckle/code-toolkit-fa-25/blob/main/images/week_01/works_cited.png) |
| please ask me about these things in [office hours](https://calendly.com/samanthaheckle/30min)                                                                                                        | ![phone ew](https://github.com/samheckle/code-toolkit-fa-25/blob/main/images/week_01/phone.png)          |

---

## Introduction to Code

### Tutorial: Learning about p5 Editor

Make an account: <https://editor.p5js.org/>

#### Looking at the p5 Editor

| Click the Gear Icon in the Upper left. |                                                                                                       |
| -------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| These are my preferred settings.       | ![p5 settings](https://github.com/samheckle/code-toolkit-fa-25/blob/main/images/week_01/settings.png) |

### Writing and Running Code

![p5.editor](https://github.com/samheckle/code-toolkit-fa-25/blob/main/images/week_01/p5_editor.png)

### General Flow

| How to submit homework                                 |                                                                                            |
| ------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| 1. Rename sketch to enable saving                      | ![name](https://github.com/samheckle/code-toolkit-fa-25/blob/main/images/week_01/1.png)    |
| 2. Save your sketch (you can also press ⌘+S or Ctrl+S) | ![save](https://github.com/samheckle/code-toolkit-fa-25/blob/main/images/week_01/2.png)    |
| 3. Finish your assignment                              |                                                                                            |
| 4. Tidy your code                                      | ![save](https://github.com/samheckle/code-toolkit-fa-25/blob/main/images/week_01/tidy.png) |
| 5. Retrieve the URL and submit.                        | ![save](https://github.com/samheckle/code-toolkit-fa-25/blob/main/images/week_01/url.png)  |

### Definitions: Coding Glossary vs. p5 Glossary

| coding glossary                                              | p5 glossary                                 |
| ------------------------------------------------------------ | ------------------------------------------- |
| terms that can be used _universally_ when talking about code | terms that are specific to p5 and our class |

#### Coding Glossary

| coding glossary           |                                                                                         |
| ------------------------- | --------------------------------------------------------------------------------------- |
| algorithm                 | series of steps to execute to solve a problem                                           |
| syntax                    | grammars or punctuation of the language you code in                                     |
| javascript                | a programming language [^1]                                                             |
| p5.js                     | a javascript library[^2]                                                                |
| documentation / reference | a dictionary for syntax of a particular coding language                                 |
| comment                   | a note embedded inside of code                                                          |
| function                  | an instruction or command, may or may not have **_parameters_**, also known as _method_ |
| parameter                 | value that is passed into the function, also known as _arguments_                       |

[^1]: the technical definition is a lightweight interpreted language with first-class functions
[^2]: it is **not** a programming language, but a way of interpreting plain javascript

#### Comments

A comment is a way in javascript to write notes and organize your code.

```js
// this is a comment
// we write comments in our code to explain what is going on and to organize ourselves
```

It is helpful to write comments not only to explain what a particular piece of code does, but especially so if you come back to an assignment much later on.

#### Function

```js
// the syntax of a function is the name followed by parenthesis
functionName();
```

#### Parameter

```js
// parameters go inside the parenthesis
functionName(parameterValue);
```

some p5 examples of functions with and without parameters

```js
// without parameters
beginShape();

// with parameters
fill(255);
background(255);
```

#### p5.js Glossary

<table>
<tbody>
<tr><td>sketch</td><td>

the name of the program you are making in p5.js web editor

</td></tr>
<tr><td>

`setup()` </td><td>

a function that happens before the animation loop and _executes one time_. once it completes, it moves to the next line in the code.

<img src="https://github.com/samheckle/code-toolkit-fa-25/blob/main/images/week_01/setup.gif" width="600px">

</td></tr>
<tr><td>

`draw()`</td><td>

is the animation loop, executes with framerate

<img src="https://github.com/samheckle/code-toolkit-fa-25/blob/main/images/week_01/draw_loop.gif" width="600px">

</td></tr>

<tr><td>

canvas</td><td>

the area on the screen where the code is executed, similar to an artboard. uses the cartesian coordinate system (x, y).

<img src="https://github.com/samheckle/code-toolkit-fa-25/blob/main/images/week_01/coordinates.png" width="600px">

Important to note here is the blue line represents the x-axis, increasing from left to right. The red line represents the y-axis, increasing from top to bottom.

`(0, 0)` starts from the top left corner and increases until the `width` and `height` have been reached. The width and height are determined by the parameters passed in to the `createCanvas()` function located in setup.

</td></tr>
</tbody>
</table>

#### Some p5 Functions

[rect()](https://p5js.org/reference/p5/rect/)

```
// remember any parameter wrapped in [] is optional
// x: x position, from top left corner (unless otherwise specified)
// y: y position, from top left corner (unless otherwise specified)
// w: width of rectangle, in pixels
// h: height of rectangle, in pixels
// optional rounding of edges using radius in px from top left, top right, bottom right, bottom left
rect(x, y, w, [h], [tl], [tr], [br], [bl])
```

[fill()](https://p5js.org/reference/p5/fill/)

```js
// r, g, b values with optional alpha
// from 0 - 255
fill(v1, v2, v3, [alpha]);
// color names, wrapped in quotations
// fun tool to see all the color names: https://tools-olive.vercel.app/t/css-named-colors
fill("color name");
// greyscale, with optional alpha
// from 0 - 255
fill(gray, [alpha]);
```

We also covered `circle()`, `ellipse()`, `line()`, `stroke()`, `noStroke()`

Options for your assignment next week:

- Look at any additional shapes in [2D primatives](https://p5js.org/reference/#2D%20Primitives), such as arc, quad, triangle

Challenge:

- Experiment with [curves](https://p5js.org/reference/#Curves) and [vertices](https://p5js.org/reference/#Vertex)

---

## Demos

-

## Useful Misc Links

- [curve visualization](https://editor.p5js.org/samheckle/full/VIr36n9gq)
- ![catmull-rom](https://kagi.com/proxy/catmull-rom-splines-l.jpg)

---
