---
layout: post
title: Subdivisions in the shopping malls
date:   2022-11-06 11:52:58 -0400
categories: rhythm
---

The basic unit of note duration is called a "whole note."
How long you hold a whole note depends on both the tempo (speed) of
the song and its time signature. But a half note is always half as
long as a whole note, a quarter note is half as long as that, etc.

The notation works like hangman. You start with a whole note
and then as the notes get shorter, you draw more and more extra
stuff on them.

<img src="/assets/images/note_values.png" 
	alt="Diagram showing note values."
	style="width: 100%; max-width: 200px;" />

A sixteenth note is the smallest you need to think about in most contexts.
The squiggle attached to the 8th note, and all shorter notes, is called
a flag. When you have consecutive notes with flags, you connect them together
with a straight line. Here's a diagram I stole from the real For Dummies
website.

<img src="/assets/images/beams.jpg" 
	alt="Diagram showing note values."
	style="width: 100%; max-width: 200px;" />

In 4/4 time, if you tap your foot and count each beat, each tap is 
a quarter note. "1, 2, 3, 4."

I'm going to use Dirty Little Secret a lot because it's such a simple
melody. The little "c" symbol means "common time" (4/4).

{% lilypond alt: "First measure of Dirty Little Secret chorus." %}
  \relative {
	\key a \major
	e''4 d cis d
  } 
  \addlyrics {
    I'll keep you my
  }
{% endlilypond %}

If you divide each tap in half, you have the "downbeat" (when your
foot is on the ground) and the "upbeat" (halfway between each pair
of downbeats). You count these out loud by saying "and," as in "1
and 2 and 3 and 4 and." When you say that, each syllable is an
eighth note. Each number is a downbeat, and each "and" is an upbeat.

{% lilypond alt: "First 2 measures of Dirty Little Secret chorus." %}
  \relative {
	\key a \major
	e''4 d cis d cis8 d cis d cis4 a
  } 
  \addlyrics {
    I'll keep you my dir -- ty lit -- tle se -- cret
  }
{% endlilypond %}

The next measure of Dirty Little Secret has a pause before he
starts singing again. That's called a rest. Rest durations are divided
the same way as for notes (whole rest, half rest, etc.) The symbols are
annoying. Sometimes you can use context clues to figure out how long
a rest is, but it's better to know them.

<img src="/assets/images/rest_values.png" 
	alt="Diagram showing rest values."
	style="width: 100%; max-width: 150px;" />

I remember what a half rest looks like because it's like a little
hat. "Half" sounds like "hat." That's the best I got.

Try counting it out. Once it becomes automatic it's pretty fun to do.

{% lilypond alt: "Next 2 measures of Dirty Little Secret chorus." %}
  \relative {
	\key a \major
	r1 r4 cis''4 b8 a a4
  } 
  \addlyrics {
	Don't tell a -- ny
  }
{% endlilypond %}

