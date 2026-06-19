# Chases

## Introduction

A chase is a sequence of scenes played automatically one after another.

While a scene represents a single lighting state, a chase creates movement by continuously transitioning between multiple scenes over time.

Chases are among the most commonly used tools in lighting programming because they allow operators to create dynamic visual effects without manually activating every scene.

In many controllers and software platforms, chases form the foundation of automated lighting playback.

---

## What Is a Chase?

A chase is an ordered collection of scenes.

Example:

```text
Scene 1 → Scene 2 → Scene 3 → Scene 4
```

The controller automatically activates each scene according to a defined timing.

For example:

```text
Red
↓
Blue
↓
Green
↓
Yellow
↓
Repeat
```

The sequence continues until the chase is stopped.

---

## Scenes vs Chases

A useful distinction is:

```text
Scene
=
Single Lighting State
```

```text
Chase
=
Sequence of Lighting States
```

Example:

Scene:

```text
Blue Atmosphere
```

This remains unchanged until another scene is activated.

Chase:

```text
Blue Atmosphere
↓
Purple Atmosphere
↓
Pink Atmosphere
↓
Blue Atmosphere
```

The lighting continuously evolves over time.

---

## How Chases Work

Internally, a chase does not usually store DMX values directly.

Instead, it references previously created scenes.

Example:

```text
Scene 1 = Red

Scene 2 = Blue

Scene 3 = Green

Scene 4 = White
```

Chase:

```text
Scene 1
↓
Scene 2
↓
Scene 3
↓
Scene 4
↓
Repeat
```

This approach allows the same scenes to be reused in multiple chases.

---

## Chase Speed

One of the most important chase parameters is speed.

Speed determines how quickly the chase advances from one scene to the next.

Example:

Slow Chase:

```text
Scene 1 → 3 seconds

Scene 2 → 3 seconds

Scene 3 → 3 seconds
```

Fast Chase:

```text
Scene 1 → 0.2 seconds

Scene 2 → 0.2 seconds

Scene 3 → 0.2 seconds
```

The same chase can create completely different visual results depending on its speed.

---

## Fade Time

Many controllers allow transitions to occur gradually instead of instantly.

Without Fade:

```text
Red
↓
Blue
```

Instant change.

With Fade:

```text
Red
↓
Purple
↓
Blue
```

Smooth transition.

Fade Time controls how long the transition takes between scenes.

A long fade generally produces smoother and more atmospheric visual results.

A short fade produces sharper and more energetic changes.

---

## Speed vs Fade Time

A common source of confusion is the difference between Speed and Fade Time.

```text
Speed
=
How fast playback advances between scenes
```

```text
Fade Time
=
How smoothly one scene transitions into the next
```

Example:

```text
Fast Speed
+
Long Fade
```

creates continuous flowing movement.

```text
Fast Speed
+
No Fade
```

creates rapid and aggressive changes.

Although both controls influence chase behavior, they affect different aspects of playback.

---

## Chase Direction

Some systems allow different playback directions.

Forward:

```text
1 → 2 → 3 → 4
```

Reverse:

```text
4 → 3 → 2 → 1
```

Bounce:

```text
1 → 2 → 3 → 4
          ↓
1 ← 2 ← 3 ← 4
```

Random:

```text
3 → 1 → 4 → 2 → 4 → 1
```

Different directions can dramatically change the visual feel of a chase.

---

## Chases in DMX192 Controllers

Most DMX192 controllers allow operators to create chases using previously stored scenes.

A typical workflow is:

1. Program scenes.
2. Store scenes into banks.
3. Select scenes to include in a chase.
4. Save the chase.
5. Control playback using Speed and Fade Time.

Example:

```text
Bank 1

Scene 1 = Red

Scene 2 = Blue

Scene 3 = Green

Scene 4 = White
```

Chase:

```text
Red
↓
Blue
↓
Green
↓
White
↓
Repeat
```

The controller automatically cycles through the sequence.

Many DMX192 controllers provide dedicated Speed and Fade Time controls specifically for chase playback.

---

## Chases in Lighting Software

Modern lighting software provides significantly more flexibility than entry-level hardware controllers.

Platforms such as:

* QLC+
* MagicQ
* Freestyler DMX
* Onyx

allow chases to contain:

* Scenes
* Effects
* Audio synchronization
* MIDI triggers
* Complex timing structures
* Multiple fixtures running independently

However, the fundamental concept remains unchanged:

A chase is still a sequence executed over time.

---

## Types of Chases

### Color Chase

```text
Red
↓
Blue
↓
Green
↓
Yellow
```

Creates color movement.

---

### Movement Chase

```text
Position A
↓
Position B
↓
Position C
```

Common with moving heads and scanners.

---

### Strobe Chase

```text
Lights On
↓
Lights Off
↓
Lights On
↓
Lights Off
```

Creates flashing effects.

---

### Atmosphere Chase

```text
Warm Amber
↓
Soft Orange
↓
Sunset Pink
↓
Deep Purple
```

Creates gradual mood evolution.

---

## Chases and Musical Timing

Many chases are synchronized to music.

Examples:

```text
One Scene Change
=
One Beat
```

or

```text
One Scene Change
=
One Musical Bar
```

Synchronization helps connect lighting movement with musical structure.

This is one of the foundations of live lighting performance.

---

## Chases and Visual Design

From a technical perspective:

```text
A chase is a sequence of scenes.
```

From a creative perspective:

```text
A chase is a sequence of visual moments.
```

The audience does not see scenes.

The audience experiences:

* Movement
* Rhythm
* Tension
* Release
* Energy
* Atmosphere

For this reason, good chase design is often more important than complex fixture programming.

---

## Design Perspective

A beginner often programs chases to create movement.

An experienced lighting designer programs chases to create emotion.

The technical sequence may be identical.

The intention behind it is what transforms lighting control into lighting design.

Example:

```text
Blue
↓
Purple
↓
Pink
↓
Blue
```

Technically:

A color chase.

Creatively:

A slow atmospheric progression.

The same chase can be interpreted very differently depending on context, timing and musical accompaniment.

---

## Relationship Between Scenes, Banks and Chases

A useful mental model is:

```text
DMX Values
↓
Scenes
↓
Banks
↓
Chases
↓
Lighting Show
```

DMX values create scenes.

Scenes are organized into banks.

Chases play scenes in sequence.

Multiple chases can be combined to build complete lighting experiences.

---

## Key Idea

A chase is a sequence of scenes executed automatically over time.

Technically, it is a playback mechanism.

Creatively, it is a tool for generating movement, rhythm and visual evolution.

Chases transform static lighting states into dynamic experiences and form one of the most important building blocks of modern lighting programming, show design and immersive visual storytelling.
