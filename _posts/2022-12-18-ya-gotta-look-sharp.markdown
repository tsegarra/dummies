---
layout: post
title: Ya gotta look sharp
date:   2022-12-18 15:30:12 -0400
categories: melody
---

So far we've focused exclusively on rhythm, or how notes are arranged in time. We haven't talked about pitch, which is how high or low a note sounds.

Sound is caused by waves of vibrating air. If you measure how fast the air wave is vibrating (how many vibrations per second), that's called its **frequency** (in Hertz).

If you play the note A in the middle of a piano, for example, it produces a sound wave with a frequency of 440 Hz. Different keys produce waves with different frequencies, which is why they sound different. As you move from left to right on a piano, the note gets higher in pitch, and the frequencies correspondingly increase.

Pitches are identified by letters: A, B, C, D, E, F, and G. After G comes A again, and so on. We draw them on a set of five parallel horizontal lines called the **staff**.

<img src="{{ site.baseurl }}/assets/images/egbdf.png" 
	alt="Staff with labeled pitches."
	style="width: 100%; max-width: 200px;" />

Mnemonics are your friend. The spaces between the lines, from bottom to top, spell FACE. The lines themselves from bottom to top represent EGBDF (most commonly "Every Good Boy Deserves Fudge").

On the piano, the letters A to G represent the white notes. They're conventionally ordered starting on C: C, D, E, F, G, A, B, C.

<img src="{{ site.baseurl }}/assets/images/pianokeys.png" 
	alt="Labeled piano keys."
	style="width: 100%; max-width: 200px;" />

Some (but not all!) adjacent pairs of white keys have a black key between them. Each black key's note has two names. For example, the note between C and D can be called "C-sharp" (notated C♯) or "D-flat" (notated D♭). Sharp means higher (e.g., C♯ is higher than C) and flat means lower.

On the staff, we put sharp or flat signs to the left of the note head. So this is C-sharp:

{% lilypond alt: "C-sharp." trim: true %}
  \relative {
    \key c \major
    cis''
  }
{% endlilypond %}


These sharp and flat symbols are called **accidentals**.

An accidental sign modifies all instances of one note until the end of the measure. For example, in the first line of John Mayer's On The Way Home:

{% lilypond alt: "First measure of On the Way Home by John Mayer." trim: true %}
  \relative {
      \key c \major
      r8 fis''8 fis g16 fis~ fis~ e d d~ d8 r8
  } 
  \addlyrics {
    I am an ar -- chi -- tect
  }
{% endlilypond %}

Here the first F (on the word "I") is sharped. So you play F-sharp. Then the second note ("and") is another F without a sharp symbol. You play F-sharp there, too, since sharp signs last until the end of the measure. Same for the first syllable of "architect." The other non-F notes are not sharp.

One last symbol to know is ♮, pronounced "natural." So C♮ is "C natural," and it refers to a regular non-flat non-sharp C.

Why would you need to use a natural sign? Look at this measure from When I'm Sixty-Four:

{% lilypond alt: "Excerpt from When I'm Sixty-Four." trim: true %}
  \relative {
      \key c \major
	c''4 des d e
  } 
  \addlyrics {
	birth -- day greet -- ing
  }
{% endlilypond %}

The first D (on "day") is flat, and the second D ("greet") is not flat. Without the natural sign, both Ds would be assumed flat.
