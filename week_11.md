# Week 11: 4/1/26

## Agenda

1. Reading Discussion #3
2. Tutorial: The Web
3. Project #3 Feedback
4. [Demos, Videos, Useful Links](#demos)

---

## Reading Discussion #3

There will be 3 groups taking notes in [this document](https://docs.google.com/document/d/1vpPYizEthHrkRrqiKKxHDj_UncUVE4a26VfkZ-0-l_c/edit?usp=sharing).

Group 1:

> Names are functionally territories. I become a landscape...Language shapes worlds and selves, drawing the territories that we then inhabit. Naming then, is placemaking: as naming identifies a domain of control, it becomes the act of domaining itself.

What digital territories do you inhibit? How did your online persona (username, domain name, other identities you might be referred as) become to be? How is this different from your "birth" name?

Group 2:

> The cloud is no longer just a warehouse. It is a climate model, a forecasting machine. And just as weather was institutionalized mostly for war and profit, memory is now being captured, modeled, and selectively mediated not just by the platforms we see (TikTok, Instagram), but by the cloud providers, ad networks, and analytics firms behind them. These systems sell our attention through targeted advertising, shape daily tools like search, maps, and recommendation feeds, and in some cases extend into defense or surveillance work. All of it happens largely outside our control.

How do you see yourself disengaging from these systems? How do you imagine continued use of them going forward?

Group 3:

> To program a television show is to schedule or to broadcast it; to program a computer is to produce a series of stored instructions that supposedly guarantee—and often stand in for—a certain action. One is descriptive, the other prescriptive.

What role does the algorithm play in prescribing labels to you? Does that match the descriptions you have about yourself?

## The DOM

| coding glossary       |                                                                                                         |
| --------------------- | ------------------------------------------------------------------------------------------------------- |
| HTML/CSS              | markup languages that determine the structure + style of web pages, inside `index.html` and `style.css` |
| Document Object Model | the way that javascript perceives the structure of the webpages                                         |

| HTML      | CSS   | JS          |
| --------- | ----- | ----------- |
| structure | style | interaction |

### HTML

Hyper-text markup language (HTML) defines the structure of a webpage using a series of tags, enclosed in `< >`.

```html
<!-- this is a comment -->
<!-- this is an opening tag -->
<html>
	<!-- this is a closing tag -->
</html>
```

Looking at the default `.html` file inside our p5 editor:

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<script src="https://cdn.jsdelivr.net/npm/p5@1.11.10/lib/p5.js"></script>
		<script src="https://cdn.jsdelivr.net/npm/p5@1.11.10/lib/addons/p5.sound.min.js"></script>
		<link rel="stylesheet" type="text/css" href="style.css" />
		<meta charset="utf-8" />
	</head>
	<body>
		<main> </main>
		<script src="sketch.js"></script>
	</body>
</html>
```

`<html>` has two "child" elements, meaning tags that are nested between the opening and closing tags.

- `<head>` gives us extra data about the webpage, but it isn't seen inside the page
- `<body>` is the actual content of the page

Other html tags (not a definitive list):

- `<p>` - paragraphs
- `<em>` - emphasis / italics
- `<strong>` - bold
- `<img>` - images, use `src` attribute to determine paths to files
- `<a>` - links, uses `href` attribute to go to another file or site

Take a look at the [full list of html tags on the docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements).

### CSS

Cascading style sheets determine the style, or what the web page looks like. This is a series of rules that look very similar to objects with properties. They are given via a selector.

```css
/* this is a comment in css */

p {
	/* selector, or which tag/element we want to apply the style to*/
	color: blue; /* rule in key:value pair */
}
```

We can see a [full list of css properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties) in the documentation.

Looking at the default `.css` in the p5.editor:

```css
html,
body {
	margin: 0;
	padding: 0;
}
canvas {
	display: block;
}
```

### DOM

The Document Object Model is the way that Javascript is able to perceive and reference HTML code to make changes to it.

![dom](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/using_the_w3c_dom_level_1_core-doctree.jpg)

This enables us to programatically add items to the DOM using p5.js: https://p5js.org/reference/#DOM

## Project #3 Feedback

There will be two roles for this critique:

1. the "artist", represented by the group presenting their work
2. the "audience", represented by the people listening to the presentation

We will take notes in [this document](https://docs.google.com/document/d/11t37adACGHf4BHLgbZIFSdTH1Gm-RuPAUEXuWFy9v24/edit?usp=sharing) following this structure:

1. Audience states what they value
   - what is meaningful, evocative, interesting, exciting, and/or striking? what is working for you?
2. Artist asks their questions, guiding where they would like feedback and audience answers the questions
3. Audience asks questions
   - what are you curious about? can be concept, theme, technical implementation, etc.
4. Audience suggests
   - if you were to take this concept, what would you do? how would it change or improve?

## Demos and Videos

- DOM demo [in p5 editor](https://editor.p5js.org/samheckle/sketches/rLkGVYrhd)
- DOM demo [in p5 full screen](https://editor.p5js.org/samheckle/full/rLkGVYrhd)
- Code uploaded to github https://github.com/samheckle/sva-sp-26-github-page
- Code published on https://samheckle.github.io/sva-sp-26-github-page/

### Resources / Videos

- Allison Parrish [Browser Controls](https://creative-coding.decontextualize.com/browser-controls/)
- Coding Train [HTML/CSS/DOM Playlist](https://www.youtube.com/watch?v=URSH0QpxKo8&list=PLRqwX-V7Uu6bI1SlcCRfLH79HZrFAtBvX) (videos 8.1-8.16)

#### Projects referenced
- [Adnose](https://adnanaga.com/Adnose) | [Video presentation](https://vimeo.com/826939103) | [Raspberry Pi News](https://www.raspberrypi.com/news/this-massive-nose-sniffs-things-then-prints-a-description-of-the-smell/)
- [American Artist](https://americanartist.us/)
- [max fowler](https://mfowler.info/)
- [Internet Phone Book](https://internetphonebook.net/index.html)

### Misc Links

- [Open Processing](https://openprocessing.org/sketch/create) for live collaboration (you and your group would all need an account)
- [`loadFont()`](https://p5js.org/reference/p5/loadFont/) to load a font from a font file
- Extra credit:
    - read a book and post about it in our extra credit thread
    - do the [bibliomancy exercise](https://web.archive.org/web/20250218222440/https://querent.substack.com/p/bibliomancy-for-the-living-autobiography)
