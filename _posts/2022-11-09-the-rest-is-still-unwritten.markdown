---
layout: post
title: The rest is still unwritten
date:   2022-11-09 11:21:14 -0400
categories: rhythm
---

So far we've been over how to notate note durations. We accomplished the dubious feat of reading the first two measures of the chorus to Dirty Little Secret by The All-American Rejects.

{% lilypond alt: "First 2 measures of Dirty Little Secret chorus." %}
  \relative {
	\key a \major
	e''4 d cis d cis8 d cis d cis4 a
  } 
  \addlyrics {
    I'll keep you my dir -- ty lit -- tle se -- cret
  }
{% endlilypond %}

The next measure has a pause before he starts singing again. That's called a rest.

# Rests

Rest durations are divided the same way note durations are (whole rest, half rest, etc.). The symbols are annoying. Sometimes you can infer them from context clues.

<img src="{{ site.baseurl }}/assets/images/rest_values.png" 
       alt="Diagram showing rest values."
       style="width: 100%; max-width: 150px;" />

The set of five horizontal lines, upon which all music is written, is called the **staff**.

The whole and half rest are distinguished by their position with respect to the staff line. The whole rest hangs down from the line, and the half rest pops up, like a top hat. "Hat" shares two letters with "hat." That's the best I got.

So in the song, we now have a full measure without any notes (four beats, or a whole rest), followed by one quarter rest (one beat) before he starts singing again.

```
count: | 1 & 2 & 3 & 4 & | 1 & 2     & 3    & 4  & |
vocal: |                 |     Don't   tell a-ny   |
```

Or, nicely typeset:

{% lilypond alt: "Next 2 measures of Dirty Little Secret chorus." %}
  \relative {
       \key a \major
       r1 r4 cis''4 b8 a a4
  } 
  \addlyrics {
       Don't tell a -- ny
  }
{% endlilypond %}

Try tapping out the whole thing. It takes some mental effort at first but once it becomes automatic it's very fun.

{% lilypond alt: "First 2 measures of Dirty Little Secret chorus." %}
  \relative {
	\key a \major
	e''4 d cis d cis8 d cis d cis4 a r1 r4 cis4 b8 a a4
  } 
  \addlyrics {
    I'll keep you my dir -- ty lit -- tle se -- cret Don't tell a -- ny
  }
{% endlilypond %}

