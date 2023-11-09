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

<!-- But first, I want to talk a little about the history of software bugs as we know them. I’m going to start with Grace Hopper’s moth. Maybe you’ve seen this image of a Harvard logbook. If you can’t read it, the text says “First actual case of bug being found,” which of course refers to this moth, which was found inside the Mark II.
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

<img alt="Mosquitos attacking Pedro Pascal" src="https://media.giphy.com/media/13QfNyksL4MBaw/giphy-downsized-large.gif" style="display: block; margin: 0 auto; max-width: 45%"/>

<p style="text-align: center; opacity: 75%;">(GIF: Four Rest Films via GIPHY)</p>

<!--
Bugs as nuisances is perhaps one of the most familiar ways of thinking about bugs, both as makers and as users of software. Those facepalm moments.
 -->

---
layout: two-cols
---

::default::

<img alt="A screenshot of backwards text" src="https://our-bugs-ourselves.s3.us-west-2.amazonaws.com/backwards.png" style="display: block; margin-top: 60px"/>

::right::

<img alt="A cartoon spider shaking its head no" src="https://media.giphy.com/media/3oz8xZLqPGjVbDfda8/giphy.gif" style="display: block; margin: 60px 0 0 50px;max-width: 65%"/>

<p style="opacity: 75%; margin-left: 50px;">(GIF: Parker Jackson via GIPHY)</p>


<!--
Here's a fun one that I was responsible for recently. This is from telehealth, but it was caught before the beta release thankfully (thanks Sofia, I think).
 -->
---

# A class applied to the wrong element 🤦‍♀️

```js {all|12|16|all}

export function VideoThumbnail({
  name,
  isMirrored,
  videoRef,
  videoTransmissionEnabled,
}) {
 return (
  <div
    className={twMerge(
      classNames("flex justify-center items-center rounded-2xl", {
        "scale-x-[-1]": isMirrored,
      })
    )}>
    {
      videoTransmissionEnabled ? <video ref={videoRef} /> : <p> {name} <p/>
    }
  </div>
 )
};
```

<!--
What happened here is that I needed to add a tailwind class to mirror the video thumbnail. But when the video is off, the thumbnail display's the user's name instead. Buttttt I applied the mirroring class to the div that wraps the video itself rather than the video, and I never tested what that would look like with the video off.
 -->

---

# The case of the 0 minute mile

<img alt="A screenshot that says 'Race Page: 0:00/mi'" src="https://our-bugs-ourselves.s3.us-west-2.amazonaws.com/pace.png" style="display: block; max-width: 40%; margin: 0 auto;  "/>

<img alt="A smiling group of people at the Hood to Coast relay finish line" src="https://our-bugs-ourselves.s3.us-west-2.amazonaws.com/htc.jpg" style="display: block; margin: 30px auto; max-width: 45%"/>


<!--
And here's on I saw as a user. This year I ran the Hood to Coast relay. When you register, you need to enter a pace from a previous race, which the organizers will use to figure out how fast your team is and hence, what your start time should be. But at some point, the entered values were converted from one system to another, and any values without a seconds input were converted to zeroes. Which means that multiple teammates were registered with a 0 minute mile. Now this is a fast, good-looking group of people, but none of them can run a 0 minute mile. So it was a pretty big headache for our team captain to get our start time adjusted.
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

<p style="opacity: 75%; margin-left: 30px;" >(GIF: Simpsons via GIPHY, please don't sue)</p>

</div>
</template>

<!--
And here's a good one from Rolf, from his time at a major Seattle area tech company.
 -->

---
layout: two-cols
---

::default::

# Y2K

* ## Approximately 500 residents in Philadelphia received jury duty summonses for dates in 1900

<p></p>

* ## In Denmark, the first baby born on January 1 was recorded as being 100 years old

<p></p>

* ## In New York, a video store accidentally generated a $91,250 late fee because the store computer determined a tape rental was 100 years overdue

::right::

<img src="https://our-bugs-ourselves.s3.us-west-2.amazonaws.com/y2k.jpeg" alt="A bug plushy wearing a tee shirt that says y2k" style="display: block; margin-left: 30px; max-width: 70%;" />

<p style="opacity: 75%; margin-left: 30px;" >(Photo: eBay)</p>


<!--
Y2K is mainly remembered as the bug that wasn't. Well actually, I was ten at the turn of the new millennium, so what I remember is this bug plushy that my grandpa had. If you bonked it against something it made a crashing noise. Did anyone else have this? It's now worth like $8 on ebay I learned. But anyway. The use of two digit shorthand for years of course predates computers, but was standard in early computing due to ruthless bit conservation needs. As the year 2000 approached, there was widespread concern that computer systems would be unable to distinguish dates, causing major chaos.

So while there wasn't widespread crises, there is an amazing list you can find on Wikipedia of things that did go wrong. These are a few of my favorites. And who among hasn't battled
 -->

---
layout: cover
---

<div style="margin-top: 200px">

# Part 2: Bugs as Crises

</div>

<!--
Though of course, not all bugs live in the territory of minor bother or humorous historical footnote. While our jobs may not be as high stakes as surgeons or nuclear power engineers, what we build matters. The things we fail to account for, the unhandled edge cases, the mistakes that no one caught in review can have real consequences sometimes.
 -->
---
layout: cover
---

# Deadly race conditions

* ## The Therac-25, a computer-controlled radiation therapy machine, was involved in at least 6 deaths when it gave patients radiation doses that were hundreds of times greater than expected

<p></p>

* ## The Northeast blackout of 2003, which resulted in approximately 100 deaths, was set into motion by a race condition in the alarm system at the control room of FirstEnergy, an Akron, Ohio

<!--
Race conditions are one of those classic programming problems that we all encounter from time to time
 -->

---

# The National Eating Disorders Association's Dangerous ChatBot

<p></p>

## "The recommendations that Tessa gave me was that I could lose 1 to 2 pounds per week, that I should eat no more than 2,000 calories in a day, that I should have a calorie deficit of 500-1,000 calories per day...All of which might sound benign to the general listener. However, to an individual with an eating disorder, the focus of weight loss really fuels the eating disorder."

<p></p>

<p style="margin-left: 40%">-Sharon Maxwell, eating disorder survivor and recovery consultant </p>

---

# Part 3: Bugs as Opportunities

<img alt="Hands opening to reveal bugs" src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExaXV6emplNWlrbzhzZnNlN3dyc3R1aW9ocmlqOHM4b3ltd2tiM2diOSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/hfBvI2Pq6zCYo/giphy.gif" style="display: block; margin: 0 auto; max-width: 85%"/>

<p style="text-align: center; opacity: 75%;">(GIF: Max Litvinov via GIPHY)</p>

---

# Solving bugs can...

* ## Deepen understanding

<p></p>

* ## Strengthen relationships

<p></p>

* ## Improve processes

<p></p>

* ## Improve systems

---

<img alt="A caterpillar going into a cocoon and saying Goodbye" src="https://media.giphy.com/media/26ufpPR34nEWwZphC/giphy.gif" style="margin: 60px auto 0" />
<p style="opacity: 75%; text-align: center">(GIF: Parker Jackson via GIPHY)</p>

