# Week 08: 3/11/26

## Agenda

1. Reading Discussion #2
2. Review
3. Tutorial: Data Structures Part 1: Arrays
4. Tutorial: p5.js Sound
5. [Demos, Videos, Useful Links](#demos)

---

![img](https://camo.githubusercontent.com/9ef9efdeffc510330b91b3f6ee1e6bdbe4283deec85a14409fb6a8ed44c6c765/68747470733a2f2f6b6167692e636f6d2f70726f78792f696d2d6d6f72652d636f6e66757365642d776974682d7468652d72696768742d736964652d6f662d746869732d6d656d652d63616e742d6576656e2d76302d71746a72347a726a726c7765312e6a7065673f633d4d48616f454866344a413454316459456f31435230545475563155366e72756536567637706e517164474c3467727942776977784630726b2d5958536e714f6950636e485951726c5f796242476666525a52615246622d394a38794b61487570786d506c79794c67694f35306c35346548315a63473959584262766c45624c3935415f42754b4e5745592d51504a44346d796f784f4768463262737a624f44505142434f4b396d6163374b744f676f5949743830444a436b6d787a6f71764538736d754f54614b4565676e43675351416d6e7542747a2d5959494c377767546c544c4366415a5762423334253344)

## Reading Discussion #2

Take notes in [this document](https://docs.google.com/document/d/1LeVnSBy5DFiIbKNeu170M_O3tPOwu0949GNqA20Ac9Q/edit?usp=sharing)

- How are you currently using AI? Do you use AI in your artistic processes now?
- What are the different approaches you might take in using AI in the future (if you will)?
- Can technology be biased? Or is it designed that way?
- When you were younger, how did you imagine your adult life? What did you imagine yourself doing? Has AI changed that?

## Review: Questions on _anything_ so far?

Add to [this doc](https://docs.google.com/document/d/1xzrUy0LCrEwE9dHL8iapZ3kWPrcCzaqXOwCUtHTiV1I/edit?usp=sharing)

## Data Structures Part 1: Arrays

### Coding Glossary: Arrays

| Review         |                                                                                          |
| -------------- | ---------------------------------------------------------------------------------------- |
| variable       | name for a placeholder piece of data                                                     |
| declaration    | using `let` to assign a value to a variable or using `function` to create a new function |
| variable types | `boolean`, `number`, `string` (words)                                                    |

| New terms |                                                                             |
| --------- | --------------------------------------------------------------------------- |
| array     | data structure that holds a _series_ of variables, uses `[]`, order matters |
| element   | one piece of array data                                                     |
| index     | location of a particular element, starting at index of 0                    |

#### Declaring an **_Array_**

```js
let myNewArray = [];
```

#### Initializing an array with **_Elements_**

```js
let myNewArray = [10, 15, 20];
```

#### Retrieving a specific **_Element_** with the **_Index_**

The index is the location of the data we want to grab. The location is automatically assigned because of the `array`, since it is a _series_ of data, so it always starts at 0 and increases by one for every element. When we want to retrieve a specific element, we use `[]` and the index (location) we want to grab.

```js
myNewArray[0]; // 10
myNewArray[1]; // 15
myNewArray[2]; // 20
```

#### Arrays are like tables

<table>
<tbody>
<tr><td>index</td><td>0</td><td>1</td><td>2</td><td>3</td></tr>
<tr><td>value</td><td>"this"</td><td>"is"</td><td>"a"</td><td>"sentence"</td></tr>
</tbody>
</table>

```js
let data = ['this', 'is', 'a', 'sentence'];
```

In code, we typically only want an array to hold 1 type of data. So it should be _either_ a list of numbers, booleans, or strings.

#### Arrays are Living Variables

We can change the value of an element in the array by reassigning it, like we do with normal variables.

```js
let teachers = ['Sam', 'Patrick', 'Rory'];
teachers[1] = 'Sam';
// override the old value, reassign to new
// teachers is now ["Sam", "Sam", "Rory"]
```

If we use an index (location), that does not exist yet, it will add empty `undefined` items in the series until it gets to that location.

```js
let animals = ['Cat', 'Dog']; // animals has elements at 0 and 1
animals[4] = 'Giraffe';
// animals is now ["Cat", "Dog", undefined, undefined, "Giraffe"]
```

This isn't the best way to add to an array, because we don't want to accidentally create empty variables.

---

#### Unique Attributes of an Array

JavaScript is an object-oriented programming language, so whenever we create a piece of data (like a variable or an array), it is considered an `object`.

`Objects` allow us to enact specific actions _on_ them. We need to reference the specific object in order to do that action.

##### `.push()`

`push()` is a function we have seen inside of p5, but [`.push()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push) is a function that exists in an array. We need to use the name of our array, and the `.` to use the specific function.

```js
let myArray = [2, 4, 6];
myArray.push(8);
// this automatically adds 8 to the end of the array
// the new array is [2, 4, 6, 8]
```

This adds an element to the end of the array.

**Note**: This is different from p5's `push()` method. p5 has redefined `push()`/`pop()` to store states. `.push()` has different syntax and _must_ be used _on_ an array. So anytime we see the prepending `.`, it likely means it needs to be used on an object.

##### properties

Properties are variables that are unique to an object (in this instance an array). We again use the `.` to reference a specific property we want to access.

Arrays have a property called [`length`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/length). This gives us how many items exist in the array.

```js
let myArray = [2, 4, 6]; // 3 items total
myArray.length; // this is 3
```

This counts the number of **_elements_** that exist inside the array.

##### Arrays and Loops

Typically it is very cumbersome to access every element inside of a loop every time. Given an array:

```js
let pets = ['dog', 'cat', 'hamster', 'giraffe', 'horse'];
```

If we want to use or reference any one of these we would need to do something like:

```js
print(pets[0]); // prints: dog
print(pets[1]); // prints: cat
print(pets[2]); // prints: hamster
print(pets[3]); // prints: giraffe
print(pets[4]); // prints: horse
```

But, we already see a pattern of a number increasing every time. So, using the attributes we know so far, we can go through the loop. We already know our end condition, because it is the number of elements in our loop. So we could write:

```js
for (let count = 0; count < 5; count++) {
	print(pets[count]);
}
```

But, our end condition might be malleable, or we might add another pet later on. So we can use the property `.length` instead of 5.

```js
for (let count = 0; count < pets.length; count++) {
	print(pets[count]);
}
```

If we wanted to make it clearer, we could declare a local variable:

```js
for (let count = 0; count < pets.length; count++) {
	let currentPet = pets[count];
	print(currentPet);
}
```

There is a shorthand for this! If we don't need to know the number, we can automatically create and assign `currentPet`:

```js
for (let currentPet of pets) {
	print(currentPet);
}
```

This is a special loop _just for arrays_, that is shorthand for assigning a variable to the index of the current iteration.

## Tutorial: p5.js Sound

To use sound in p5, we use the [p5 sound library](https://p5js.org/reference/p5.sound/), which allows us to add, manipulate, and create sound with p5.

### Sources for sound:

- [orchestral sample library](http://virtualplaying.com/virtual-playing-orchestra/)
- [free music archive](https://freemusicarchive.org/)
- [freesoundorg](https://freesound.org/)
- [bbc sound effects](http://bbcsfx.acropolis.org.uk/)
- [free sound picture](https://www.soundofpicture.com/)

### Sound Project references

- https://teropa.info/loop/#/title
- https://www.nytimes.com/interactive/2018/09/21/magazine/voyages-travel-sounds-from-the-world.html
- http://jazz.computer/
- https://patatap.com/
- https://youtu.be/HI1raqxrUdk?si=j01yIjgDCCW91PpI
  - cassie's [sketch](https://editor.p5js.org/cassie/sketches/YZHxZ9ffl) recreating it

---

## Review Videos

- [7.1 What is an array?](https://www.youtube.com/watch?v=VIQoUghHSxU)
- [7.2 Arrays and loops](https://www.youtube.com/watch?v=RXWO3mFuW-I)

## Review Documentation (these are textbook definitions)

- [for...of](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...of) loops with arrays
- [array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
- [object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)

## Demos
