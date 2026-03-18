# Week 09: 3/11/26

## Agenda

1. Project #3 Groups
2. Tutorial: p5.js Sound
3. Tutorial: Generated Sound + Microphone
4. In-Class Work Time with Group
5. [Demos, Videos, Useful Links](#demos)

---

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

## Tutorial: Generated Sound + Microphone

### Generating Sound

Each note that exists from instruments is related to a specific frequency. For example, a [piano](https://en.wikipedia.org/wiki/Piano_key_frequencies) can be broken down by [this chart](https://upload.wikimedia.org/wikipedia/commons/a/ad/Piano_key_frequencies.png)

What this means for us is that we can generate tones by using the basic frequency (in the hz units) and electronically mimic the sound waves coming from each place. 

![sound waves](https://www.thedawstudio.com/wp-content/uploads/2016/08/Types_of_Soundwaves.jpg)

We can mathematically create a scale by seeing what is the ratio between the note, the hz, and the ratio. 

| note | hz | ratio | 
|---|---|---|
| C | 262 | 1 | 
| D | 294 | 1.122 | 
| E | 311 | 1.189 |
| F | 349 | 1.335 | 
| G | 392 | 1.498 | 
| A | 415 | 1.587 | 
| B | 466 | 1.782 |

#### Modifying Sound Files based on Freq (HZ)

The `.rate()` method that exists on sound files allows us to use this ratio to create a new tone!

#### Using Oscillators

We can customize sound files using the frequency, but we can also create new tones using the oscillator class in p5.sound.

```js
// p5.Oscillator takes 2 parameters:
// 1. frequency (note) to be played
// 2. type of waveform (sine, triangle, square, sawtooth)
let osc = new p5.Oscillator(261, "triangle")
```

The frequency is determined by the note (see above table), and the waveform is the literal sound wave that moves through the air. We are mimicking this electronically. 

### Microphone Input

We can create microphone input using the `new p5.AudioIn()`. This uses the class syntax of `new` to create an instance of the AudioIn class, and we can assign that to a variable. 

***Note: Some browsers hate this, so if you use Firefox or not Chrome, you might need to change the version of your p5 to 0.9.0 in `index.html`***



```js
let mic = new p5.AudioIn()
```

Once we have created it, we need to start the audio input.

```js
mic.start()
```

We can measure the volume of the microphone using
```js
mic.getLevel()
```

## Demos, Videos, Useful Links

### Demos

### Videos

* [17.1: Loading and Playing sound](https://youtu.be/Pn1g1wjxl_0?list=PLRqwX-V7Uu6aFcVjlDAkkGIixw70s7jpW)
* [17.3: Timing, Jumps and Cues](https://youtu.be/SfA5CghXw18?list=PLRqwX-V7Uu6aFcVjlDAkkGIixw70s7jpW)
* [17.4: Amplitude Analysis](https://youtu.be/NCCHQwNAN6Y?list=PLRqwX-V7Uu6aFcVjlDAkkGIixw70s7jpW)
* [17.5: Adding Sound Effects - video tutorial](https://youtu.be/40Me1-yAtTc?list=PLRqwX-V7Uu6aFcVjlDAkkGIixw70s7jpW)
* [17.6: Sound Synthesis - video tutorial](https://youtu.be/Bk8rLzzSink?list=PLRqwX-V7Uu6aFcVjlDAkkGIixw70s7jpW)
* [17.8: Microphone Input](https://youtu.be/wUSva_BnedA?list=PLRqwX-V7Uu6aFcVjlDAkkGIixw70s7jpW)
* [17.9: Sound Visualization: Graphing Amplitude](https://youtu.be/jEwAMgcCgOA?list=PLRqwX-V7Uu6aFcVjlDAkkGIixw70s7jpW)
* [17.10: Sound Visualization: Radial Graph](https://youtu.be/h_aTgOl9J5I?list=PLRqwX-V7Uu6aFcVjlDAkkGIixw70s7jpW)
* [17.11: Sound Visualization: Frequency Analysis with FFT](https://www.youtube.com/watch?v=2O3nm0Nvbi4&list=PLRqwX-V7Uu6aFcVjlDAkkGIixw70s7jpW&index=11)