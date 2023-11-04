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

<img alt="Photograph of logbook page with moth taped to it, close up" src="https://our-bugs-ourselves.s3.us-west-2.amazonaws.com/moth2.jpeg" style="display: block; margin: 60px auto 0; max-width: 60%"/>

<p style="text-align: center; opacity: 75%;">(Photo: Smithsonian)</p>

<!--
You may have heard the moth described as the first computer bug, or as the origin of term computer bug. And in a lot of sources, the moth in the logbook is attributed to pioneering computer scientist Grace Hopper. In reality, neither of those things are true. Hopper was certainly on the team that found the moth, but the logbook entry is not attributed to a specific person, and archivists have noted that the handwriting doesn't seem like a good match for Hopper's.
 -->

---

<img alt="Photograph of logbook page with moth taped to it" src="https://our-bugs-ourselves.s3.us-west-2.amazonaws.com/hopper.jpeg" style="display: block; margin: 60px auto 0; max-width: 60%"/>

<p style="text-align: center; opacity: 75%;">(Photo: Smithsonian)</p>

<!--
Hopper did make these doodles of computer bugs she encountered. She was known to be a big jokester. It's a little hard to read, but I think the lower left one says "...he who seeds wrong data." Or maybe it's "wormy data." And I think the top right says "Kitchie boo boo bug. He who goes around loosening relays." And in the bottom right, "he who brings good data."

And when she made those cartoons (I'm not actually sure if they're from before or after the moth, I couldn't find a year for them), the term bug was already in the engineering lexicon.
 -->

---

<div style="padding-top: 90px;">

## "It has been just so in all of my inventions. The first step is an intuition, and comes with a burst, then difficulties arise—this thing gives out and [it is] then that 'Bugs'—as such little faults and difficulties are called—show themselves and months of intense watching, study and labor are requisite before commercial success or failure is certainly reached."

<p style="margin-left: 50%">-Thomas Edison in a letter to Theodore Puskas, 1878</p>
</div>

<!--
 In fact, Thomas Edison is well known to have used the term "bug" to describe problems with electrical circuits. Here's a quote from a letter he wrote in 1878.

 And I just love this description of engineering, or honestly any kind of act of creativity and invention. Intuition in a burst, followed by difficulties.
 -->

---
layout: two-cols
---

::default::

## Bug comes from the Middle English word _bugge_, as in bugbear or bugaboo--monsters!

<img alt="Statue" src="https://our-bugs-ourselves.s3.us-west-2.amazonaws.com/bugbear.jpeg" style="display: block; max-width: 50%; padding-top: 20px;"/>

<p style="opacity: 75%;">(Images via Wikipedia, Baldur's Gate 3 Wiki, and reviewersunite.com)</p>

::right::

<img alt="Bugbear from Baldur's gate" src="https://our-bugs-ourselves.s3.us-west-2.amazonaws.com/bugbear_baldur.jpeg" style="display: block; max-width: 65%; padding: 0 0 20px 20px;"/>

<img alt="Cartoon bugbear" src="https://our-bugs-ourselves.s3.us-west-2.amazonaws.com/bugbear_pony.jpeg" style="display: block; max-width: 80%; padding-left: 20px;"/>

<!--
And the word bug itself comes from the old english bugge, which did not refer to insects but rather bugbears or bugaboos, which were monsters. And here are some bugbears, including one from Baldur's gate and My Little Pony.

So the moth in the logbook was almost definitely documented with humorous intent, a real life bug causing a real life engineering problem.

And I love how it represents a lot of how we think and talk about bugs in software, whether they're insects or monsters, as these outside interlopers who come into our code and muck things up. 
 -->

---
layout: cover
---

# Part 1: Bugs as Nuisances

<img alt="Mosquitos attacking peasants" src="https://media.giphy.com/media/D7x9O7llARKHC/giphy.gif" style="display: block; margin: 0 auto; max-width: 45%"/>

<p style="text-align: center; opacity: 75%;">(GIF: Animation Domination High-Def via GIPHY)</p>

<!--
Bugs as nuisances is perhaps one of the most familiar ways of thinking about bugs, both as makers and as users of software.
 -->

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

<div style="margin-top: 200px">

# Part 2: Bugs as Tragedies

</div>
---
layout: cover
---

# Part 3: Bugs as Opportunities

<img alt="Hands opening to reveal bugs" src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExaXV6emplNWlrbzhzZnNlN3dyc3R1aW9ocmlqOHM4b3ltd2tiM2diOSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/hfBvI2Pq6zCYo/giphy.gif" style="display: block; margin: 0 auto; max-width: 85%"/>

<p style="text-align: center; opacity: 75%;">(GIF: Max Litvinov via GIPHY)</p>

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

