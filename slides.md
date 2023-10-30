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
<p style="opacity: 75%; text-align: center">(GIF: Parker Jackson via GIPHY)</p>

<!-- Hi everybody! Today I want to talk to you about a topic we all know and love--bugs!  -->
---
layout: two-cols
---

::default::

# Introduction: Bug History

# 1. Bugs as Nuisances

# 2. Bugs as Tragedies

# 3. Bugs as Opportunities

::right::

<img alt="A cartoon spider in boots and a leather jacket holding knives and pizza" src="https://media.giphy.com/media/ZtLg38lWRcLGE/giphy.gif" style="" />
<p style="opacity: 75%; text-align: center">(GIF: Fox via GIPHY)</p>



<!-- And specifically, I want to think about bugs in 3 ways: as nuisances, as tragedies, and as opportunities  -->

---

# Introduction: Grace Hopper (maybe) and the "First actual case of bug being found"

<img alt="Photograph of logbook page with moth taped to it" src="https://our-bugs-ourselves.s3.us-west-2.amazonaws.com/moth.jpeg" style="display: block; margin: 0 auto; max-width: 60%"/>

<p style="text-align: center; opacity: 75%;">RIP Moth (Photo: Smithsonian)</p>

<!-- But first, I want to talk a little about the history of software bugs as we know them. I’m going to start with Grace Hopper’s moth. Maybe you’ve seen this image of a Harvards logbook. If you can’t read it, the text says “First actual case of bug being found,” which of course refers to this moth, which was found inside the Mark II. 
 -->

---

<img alt="Computer relays" src="https://our-bugs-ourselves.s3.us-west-2.amazonaws.com/relay.jpeg" style="display: block; margin: 0 auto; max-height: 90%"/>

<p style=" opacity: 75%; text-align: center" >A bank of relays of the Harvard Mark II (Photo: Smithsonian)</p>

<!--
This is a bank of relays on the Mark II, where the moth was found. It was finished in 1947 was an early electro-mechanical computers. It was built at Harvard and funded by the U.S. Navy to calculate ballistics. Most of the early computers were for war and astronomy. And making fabrics.

But anyway, the relays. The relays are mechanical components that could be opened and closed sequentially to execute programs. And on the day in question, September 9, 1947, a moth got jammed between points at Relay # 70, Panel F, and jammed the relay.
 -->

---
<img alt="Photograph of logbook page with moth taped to it" src="https://our-bugs-ourselves.s3.us-west-2.amazonaws.com/moth.jpeg" style="display: block; margin: 0 auto; max-width: 60%"/>

<p style="text-align: center; opacity: 75%;">RIP Moth (Photo: Smithsonian)</p>
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
<img src="https://media.giphy.com/media/3orieTf8aTrSXmonqo/giphy.gif" alt="Bart and Homer Simpson sitting at a table eating, with the caption 'Dad, there's a bug on that'" style="display: block; margin-left: 30px; max-width: 90%;" />

<p style="opacity: 75%; text-align: center; width: 100%;" >(GIF: Simpsons via GIPHY, please don't sue)</p>

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

<img alt="A caterpillar going into a cocoon and saying Goodbye" src="https://media.giphy.com/media/26ufpPR34nEWwZphC/giphy.gif" style="margin: 60px auto 0" />
<p style="opacity: 75%; text-align: center">(GIF: Parker Jackson via GIPHY)</p>

