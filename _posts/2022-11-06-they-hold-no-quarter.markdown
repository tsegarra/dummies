---
layout: post
title: They hold no quarter
date:   2022-11-06 11:52:58 -0400
categories: rhythm
---

When you're transcribing music, you need to express how long to hold
each note. That's what rhythm notation is for.

The basic unit of note duration is called a "whole note." The precise amount of time you hold a whole note depends on a few factors, but if the time signature is 4/4 (and in pop music it usually is), a whole note always lasts four beats. A half note is half as long as a whole note (2 beats), a quarter note is half as long as that (1 beat), etc.

# How to draw

The notation works like hangman: you start with a circle and then
draw more and more extra stuff on it.

<img src="{{ site.baseurl }}/assets/images/note_values.png" 
	alt="Diagram showing note values."
	style="width: 100%; max-width: 200px;" />

- The circle is called the **note head**
- The stick attached to the circle is called a **stem**
- The squiggle attached to the stem is called a **flag**

When you have consecutive notes with flags, it's conventional to draw them connected together with straight lines (called **beams**).

<img src="{{ site.baseurl }}/assets/images/beams.jpg" 
	alt="Diagram showing note values."
	style="width: 100%; max-width: 200px;" />

# Quarter notes

In 4/4 time, if you tap your foot and count each beat, each tap is 
a quarter note. You can say it out loud while you tap: "1, 2, 3, 4."

I'll use Dirty Little Secret a lot because it's such a simple melody.

```
count: 1    2    3   4
vocal: I'll keep you my
```

Here's how you'd draw that measure. The little "c" symbol means "common time" (another name for 4/4).

{% lilypond alt: "First measure of Dirty Little Secret chorus." trim: true %}
  \relative {
	\key a \major
	e''4 d cis d
  } 
  \addlyrics {
    I'll keep you my
  }
{% endlilypond %}

A quarter note lasts for one beat, so each note in this measure is a quarter note.

# Eighth notes

If you divide the time between each foot-tap in half, then each half represents an **eighth note**. You can count eighth notes out loud by adding the word "and" evenly between each tap: "1 and 2 and 3 and 4 and."

```
count: 1    &   2   &   3   &   4   &   | 1   &   2   &   3   &   4   &
vocal: I'll     keep    you     my        dir-ty  lit-tle se-     cret
```

The first four words last 2 eighth notes each. That's why they're quarter notes. The syllables of "dirty little" are each half that length, so we write them as eighth notes.

{% lilypond alt: "First 2 measures of Dirty Little Secret chorus." trim: true %}
  \relative {
	\key a \major
	e''4 d cis d cis8 d cis d cis4 a
  } 
  \addlyrics {
    I'll keep you my dir -- ty lit -- tle se -- cret
  }
{% endlilypond %}

The last quarter note's stem goes up instead of down, but the direction doesn't matter. It just saves visual space to draw it that way, so the stem doesn't stick way up above the line.
