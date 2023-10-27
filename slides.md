---
# try also 'default' to start simple
theme: apple-basic
class: "text-center"
# https://sli.dev/custom/highlighters.html
lineNumbers: true
# some information about the slides, markdown enabled
info: |
  ## Our Bugs, Ourselves slides via Slidev

  Learn more at [Sli.dev](https://sli.dev)
# page transition
transition: slide-left
---

<div>

# Our Bugs, Ourselves

## <p style="opacity: 75%; padding-top: 15px;">3 ways of looking at software bugs</p>

<p>By Molly Jean Bennett 🤸‍♀️</p>

<img alt="3 animated bugs with the text Hello" src="https://media.giphy.com/media/3o7TKTRz6xTA8fiGD6/giphy.gif" style="margin: 0 auto" />
</div>

---

# Introduction

# 1. Bugs as Nuisances

# 2. Bugs as Tragedies

# 3. Bugs as Opportunities

---

# Introduction: Grace Hopper (maybe) and the "First actual case of bug being found"

<img alt="Photograph of logbook page with moth taped to it" src="https://our-bugs-ourselves.s3.us-west-2.amazonaws.com/moth.jpeg" style="display: block; margin: 0 auto; max-width: 60%"/>

<p style="text-align: center">RIP Moth (Photo: Smithsonian)</p>

---

<img alt="Computer relays" src="https://our-bugs-ourselves.s3.us-west-2.amazonaws.com/relay.jpeg" style="display: block; margin: 0 auto; max-height: 90%"/>

<p style="text-align: center">A bank of relays of the Harvard Mark II (Photo: Smithsonian)</p>
---
layout: cover
---

# Part 1: Bugs as Nuisances

---
layout: two-cols
---

<template v-slot:default>
<div style="padding-top: 50px;">

## "A developer put an image of Bart Simpson into the product as a placeholder. We forgot to replace it with the actual image that it was supposed to be, and shipped the product. Fox was not happy and 'politely' asked us to not do that and to give them some money, which we did."

<p style="margin-left: 60%">-Rolf Buchner</p>
</div>
</template>
<template v-slot:right>

<div style="padding-top: 50px;">
<img src="https://media.giphy.com/media/3orieTf8aTrSXmonqo/giphy.gif" alt="Bart and Homer Simpson sitting at a table eating, with the caption 'Dad, there's a bug on that'" style="display: block; margin-left: 30px" />
</div>
</template>

---
layout: cover
---

# Part 2: Bugs as Tragedies

---
layout: cover
---

# Part 3: Bugs as Opportunities

---

# Some Fun I Had Along the Way

Fun with loops!

```ts {all|16|18-20}
import { getRandomWordFromArray } from "./string";

const phraseBank: string[] = [
  `Actually, it's pronounced ciabatta`,
  `Actually, it's pronounced aioli`,
  `I have a lot of BLT NFTs. You should have bought in on the ground floor.`,
];

export const getAiResponse = (
  previousPhrase: string | undefined,
  phrases: string[] = phraseBank
): string => {
  if (phrases.length < 2) {
    return phrases[0];
  }
  let responsePhrase = getRandomWordFromArray(phrases);
  //regenerate phrase if it matches the previous one
  while (responsePhrase === previousPhrase) {
    responsePhrase = getRandomWordFromArray(phrases);
  }
  return responsePhrase;
};
```
---
