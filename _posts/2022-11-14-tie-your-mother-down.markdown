---
layout: post
title: Tie your mother down
date:   2022-11-14 09:55:07 -0400
categories: rhythm
---

There are a few common symbols that can change the written duration of a note.

# Dots

You may see a note head followed by a small dot. That's called, *creatively*, a **dotted** note. A dotted note lasts 1.5 times as long as its non-dotted counterpart. E.g.: since a quarter note is one beat, a dotted quarter note is one and a half beats. A dotted eighth note is one and a half eighth notes, or three-fourths of a beat.

Here's an example from The Word by The Beatles:

```
count: 1 & 2 & 3 & 4 &     | 1 & 2 & 3 & 4 &
lyric: So    fine    it's    sun   shine
```

The first word, "so," lasts for the count "1 and 2," but doesn't continue to the second "and." That's a duration of three eighth notes, or equivalently one and a half quarter notes. So you can write it as a dotted quarter note.

{% lilypond alt: "Dotted notes from The Word by The Beatles." trim: true %}
  \relative {
    \key f \major
    a'4. g r8 c,8 g'4. f
  }
  \addlyrics {
    So fine, it's sun -- shine
  }
{% endlilypond %}

Rests can be dotted, too. This measure from Dirty Little Secret starts with a dotted quarter rest (1.5 beats).

{% lilypond alt: "Dotted rests in the verse of Dirty Little Secret." trim: true %}
  \relative {
    \key a \major
    r4. a'8 e'4 e8 e~ e4 e8 e4 fis4 cis8~ cis4
  }
  \addlyrics {
    I go a -- round a time or two
  }
{% endlilypond %}

Some of these notes extend across the measure boundaries. That's what those curved lines are for.

# Ties

If you connect two note heads with an arc, the arc is called a **tie**. It's played as a single note with the combined durations of the notes it connects. So if you tie together two eighth notes, they sound like a single quarter note. Here we tie an eighth note to a quarter note:

{% lilypond alt: "Bars from Dirty Little Secret illustrating a tie." trim: true %}
  \relative {
    \key a \major
    r2 b'4 cis cis b a b8 a~ a4
  }

  \addlyrics {
    when I've known this all a -- long
  }
{% endlilypond %}

A measure boundary (bar line) is the most common place to use a tie.

# Things wouldn't be so confused

Let's walk through the first two measures of the chorus of Linger by The Cranberries.

```
 beat: 1   e   &   a   2   e   &   a   3   e   &   a   4   e   &   a   |   1   e   &   a
vocal:                         but I'm i-          in          so          deep
```

Try counting this out slowly. Usually I tap each sixteenth note on my fingers. I tap my index finger for each numeral, middle finger for "e," ring finger for "and," and pinky for "a." Index, middle, ring, pinky. Over and over. Each tap is a sixteenth note and that helps me figure out where each note should be placed.

```
  beat: 1   e   &   a   2   e   &   a   3   e   &   a   4   e   &   a   |   1   e   &   a
finger: 1   2   3   4   1   2   3   4   1   2   3   4   1   2   3   4   |   1   2   3   4
linger:                         but I'm i-          in          so          deep
```

There aren't any notes sung until the second "&." So we start with a rest. It lasts for the full first beat, and half of the second beat. 1.5 beats = a dotted quarter rest.

{% lilypond alt: "A dotted quarter rest." trim: true %}
  \relative {
    \key d \major
    r4.
  }
{% endlilypond %}

The first two words, "but I'm," are each one finger-tap, or one sixteenth note. Picturesque.

{% lilypond alt: "First two notes of Linger." trim: true %}
  \relative {
    \key d \major
    r4. d'16 d
  }

  \addlyrics {
    but I'm
  }
{% endlilypond %}

The next word, "in," is sung with two syllables. The first syllable lasts three finger-taps, which is three sixteenth notes.

```
  beat: 3   e   &   a   4   e   &   a
finger: 1   2   3   4   1   2   3   4
linger: i-          in          so   
```

If it lasted *two* sixteenth notes, it'd be an eighth note. If it lasted *four* sixteenth notes, it'd be a quarter note. But it's in between. It's 1.5 eighth notes: a dotted eighth.

{% lilypond alt: "First 3 notes of Linger." trim: true %}
  \relative {
    \key d \major
    r4. d'16 d b'8.
  }

  \addlyrics {
    but I'm i
  }
{% endlilypond %}

The second syllable of "in" lasts the same amount of time.

{% lilypond alt: "First 4 notes of Linger." trim: true %}
  \relative {
    \key d \major
    r4. d'16 d b'8. a8.
  }

  \addlyrics {
    but I'm i -- in
  }
{% endlilypond %}

Then "so" is two finger-taps, or two sixteenth notes, or one eighth note. We can connect this non-dotted eighth note with the previous two dotted ones.

{% lilypond alt: "First measure of Linger chorus." trim: true %}
  \relative {
    \key d \major
    r4. d'16 d b'8. a8. e8
  }

  \addlyrics {
    but I'm i -- in so
  }
{% endlilypond %}

The word "deep" lasts an entire measure by itself, so we draw a whole note.

{% lilypond alt: "First 2 measures of Linger chorus." trim: true %}
  \relative {
    \key d \major
    r4. d'16 d b'8. a8. e8 fis1
  }

  \addlyrics {
    but I'm i -- in so deep
  }
{% endlilypond %}

Ain't that satisfying?

# It's never quite as it seems

One last thing. Advanced extra credit addendum.

What's shown above is a perfectly valid way to write this melody. But the dotted eighth notes are a little awkward. It takes some mental effort to keep track of where each downbeat falls. Especially beat 4, because there isn't a note that starts on beat 4. The second syllable of "in" hits right before beat 4, and "so" hits right after, with "in" straddling the beat boundary.


```
  beat: 3   e   &   a   4   e   &   a
finger: 1   2   3   4   1   2   3   4
linger: i-          in          so   
```

What we can do is break up this troublesome second syllable of "in." We can separate it into the part before the downbeat (a sixteenth note), and the part on/after (an eighth note), and then connect them with a tie.

```
                    this part is before the downbeat
                    |
                    *
  beat: 3   e   &   a   4   e   &   a
finger: 1   2   3   4   1   2   3   4
linger: i-          in          so   
                        *   *
                        |   |
                        ------------ this part is on/after the downbeat
```

Check it out:

{% lilypond alt: "First 2 measures of Linger chorus." trim: true %}
  \relative {
    \key d \major
    r4. d'16 d b'8. a16~ a8 e8 fis1
  }

  \addlyrics {
    but I'm i -- in so deep
  }
{% endlilypond %}

Now the third and fourth beats are neatly visually separated. With practice you'll find that really helps readability.

If you didn't follow that section, don't worry about it. It comes naturally with time once you see enough of these. I just wanted to explain why you sometimes see a tie in the middle of a measure. It doesn't really matter why as long as you can read it.
