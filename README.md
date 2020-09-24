# 👨‍💻 exercism

> **“For the things we have to learn before we can do them, we learn by doing them.”** \
> ― Aristotle, _The Nicomachean Ethics_

Here are my [exercism](https://exercism.io/profiles/ofou) solutions! I'm using this amazing platform in order to improve mainly my JS skills and getting closer to the community. I love using this tool to improve my skills because it makes great use of the command line, even including great tests for your code. So, you're not only improving your skills, you're even getting a glimpse of good practices on the way. It's taking me **long hours** so far but I'm eager to finish the full JS Track (18) with all the side exercises (86). I'm tracking my coding time using [rescuetime](https://www.rescuetime.com/rp/ofou/). If you have any comments or suggestions about my code, questions on how to start coding on exercism, please [open an issue](https://github.com/ofou/exercism/issues/new), I'll very happy to help you out, or reciving any kind of feedback from the community!

I'm also using [`leetcode`](https://github.com/ofou/leetcode), [`codesignal`](https://github.com/ofou/codesignal) and [`freeCodeCamp`](https://www.freecodecamp.org/ofou), all great ways to improve your skills further.

<!-- @import "[TOC]" {cmd="toc" depthFrom=2 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [Core exercises](#core-exercises)
  - [hello-world](#hello-worldjavascripthello-worldhello-worldjs)
  - [two-fer](#two-ferjavascripttwo-fertwo-ferjs)
  - [resistor-color](#resistor-colorjavascriptresistor-colorresistor-colorjs)
  - [resistor-color-duo](#resistor-color-duojavascriptresistor-color-duoresistor-color-duojs)
  - [gigasecond](#gigasecondjavascriptgigasecondgigasecondjs)
  - [rna-transcription](#rna-transcriptionjavascriptrna-transcriptionrna-transcriptionjs)
  - [space-age](#space-agejavascriptspace-agespace-agejs)
- [Side Exercises](#side-exercises)

<!-- /code_chunk_output -->

## Core exercises

### [hello-world](/javascript/hello-world/hello-world.js)

```js
export const hello = () => {
  return "Hello, World!";
};
```

### [two-fer](/javascript/two-fer/two-fer.js)

```js
export const twoFer = (X = "you") => {
  return `One for ${X}, one for me.`;
};
```

### [resistor-color](/javascript/resistor-color/resistor-color.js)

```js
export const colorCode = (color) => {
  return COLORS[color.toLowerCase()];
};

export const COLORS = {
  black: 0,
  brown: 1,
  red: 2,
  orange: 3,
  yellow: 4,
  green: 5,
  blue: 6,
  violet: 7,
  grey: 8,
  white: 9,
};
```

### [resistor-color-duo](/javascript/resistor-color-duo/resistor-color-duo.js)

```js
import { strict } from "assert";

export const decodedValue = (resistors) => {
  var colors = {
    black: 0,
    brown: 1,
    red: 2,
    orange: 3,
    yellow: 4,
    green: 5,
    blue: 6,
    violet: 7,
    grey: 8,
    white: 9,
  };

  return parseInt(
    resistors
      .map((e) => colors[e.toLowerCase()])
      .join("")
      .slice(0, 2)
  );
};
```

### [gigasecond](/javascript/gigasecond/gigasecond.js)

```js
Date.prototype.addGigaseconds = function () {
  var gigasecond = 1000000000;
  return new Date(this.getTime() + gigasecond * 1000);
};

export const gigasecond = (moment) => {
  return moment.addGigaseconds();
};
```

### [rna-transcription](/javascript/rna-transcription/rna-transcription.js)

```js
export const toRna = (sequence) => {
  return sequence
    .split("")
    .map((nucleotide) => {
      if (nucleotide == "") return "";
      if (nucleotide == "C") return "G";
      if (nucleotide == "G") return "C";
      if (nucleotide == "T") return "A";
      if (nucleotide == "A") return "U";
    })
    .join("");
};
```

### [space-age](/javascript/space-age/space-age.js)

```js
const planets = {
  mercury: 0.2408467,
  venus: 0.61519726,
  earth: 1.0,
  mars: 1.8808158,
  jupiter: 11.862615,
  saturn: 29.447498,
  uranus: 84.016846,
  neptune: 164.79132,
};
const baseline = 31557600;

export const age = (planet, seconds) => {
  return parseFloat((seconds / (planets[`${planet}`] * baseline)).toFixed(2));
};
```

## Side Exercises
