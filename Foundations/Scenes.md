# Scenes

## Introduction

A scene is one of the most fundamental concepts in lighting control.

A scene is a stored collection of DMX values that defines the state of one or more fixtures at a specific moment.

Instead of manually adjusting every channel each time a lighting look is needed, the desired channel values can be saved as a scene and recalled instantly.

Scenes allow lighting operators to transform hundreds of individual DMX values into meaningful visual states.

They are the foundation of most lighting programming workflows.

---

## What Is a Scene?

A scene is a snapshot of channel values.

For example:

Fixture 1 (RGBW PAR)

Red = 255

Green = 0

Blue = 0

White = 0

Fixture 2 (RGBW PAR)

Red = 255

Green = 0

Blue = 0

White = 0

When these values are stored together, they become a scene.

Activating the scene recalls all stored values simultaneously.

---

## A Scene Is Not an Effect

A common misconception is that a scene is an animation or a movement sequence.

A scene is simply a lighting state.

Examples:

* Red Wash
* Deep Blue Atmosphere
* Warm White Front Light
* Blackout
* Ambient Purple

Each of these represents a static visual condition.

Movement occurs when multiple scenes are played in sequence.

That sequence is called a chase.

---

## Scenes Simplify Lighting Control

Consider a system containing:

* 2 RGBW PAR fixtures
* 2 Spider fixtures
* 1 Laser

The total number of channels may exceed 30 or 40.

Manually setting every channel each time would be impractical.

Instead, the operator creates scenes such as:

Scene 1

Warm Amber Atmosphere

Scene 2

Deep Blue Atmosphere

Scene 3

Energy Build-Up

Scene 4

Blackout

Each scene stores the required DMX values internally.

Pressing a single button can recall dozens of channel values instantly.

---

## Scenes Are Built From Channel Values

Every scene ultimately consists of DMX values.

Example:

Channel 1 = 255

Channel 2 = 0

Channel 3 = 0

Channel 4 = 0

Channel 17 = 255

Channel 18 = 255

Channel 19 = 255

The operator may see:

"Warm White"

But internally the controller is storing numerical DMX data.

Scenes provide a human-friendly way of organizing that information.

---

## Scenes and Fixtures

A scene can control:

* One fixture
* Multiple fixtures
* An entire lighting system

Example:

Scene: Blue Atmosphere

RGBW PAR 1 → Blue

RGBW PAR 2 → Blue

Spider 1 → Slow Blue Pattern

Spider 2 → Slow Blue Pattern

Laser → Off

Fog Machine → Off

All fixtures respond simultaneously when the scene is activated.

---

## Scene Transitions

Many lighting systems allow smooth transitions between scenes.

Example:

Scene A

Deep Blue

↓

Fade

↓

Scene B

Warm Amber

Instead of changing instantly, the controller gradually modifies the DMX values over time.

This process is known as fading.

Fade times are one of the most important tools in atmosphere creation.

---

## Scenes in Hardware Controllers

In controllers such as a DMX192 console, scenes are usually stored inside banks.

Example:

Bank 1

Scene 1

Scene 2

Scene 3

Scene 4

Scene 5

Scene 6

Scene 7

Scene 8

The bank acts as a container for multiple scenes.

This organizational structure helps operators access lighting looks quickly during a performance.

---

## Scenes in Software Controllers

Software platforms such as QLC+ organize scenes differently.

Instead of being limited by physical buttons, scenes can be:

* Named
* Categorized
* Assigned to virtual controls
* Triggered by MIDI devices
* Triggered by keyboards
* Triggered automatically

The underlying concept remains the same:

A scene is still a stored collection of DMX values.

---

## Scenes and Lighting Design

From a technical perspective, a scene is a collection of channel values.

From a creative perspective, a scene is a visual decision.

A scene can communicate:

* Energy
* Calmness
* Tension
* Warmth
* Mystery
* Celebration
* Anticipation

For this reason, scenes are often named according to their visual purpose rather than their technical settings.

Examples:

* Sunset Wash
* Deep Ocean
* Warm Lounge
* Peak Energy
* Dark Build-Up
* Festival Colors

The lighting designer thinks about the visual result rather than the numerical DMX values behind it.

---

## Scenes as Building Blocks

Scenes are the basic building blocks of lighting programming.

More advanced structures are created from scenes.

Examples:

Scenes

↓

Banks

↓

Chases

↓

Shows

A chase is a sequence of scenes.

A lighting show is typically a collection of scenes and chases organized into a complete performance.

Understanding scenes is therefore essential before learning banks and chases.

---

## Mental Model

A useful way to think about scenes is:

DMX Channels

↓

Fixture Behavior

↓

Scene

↓

Visual Atmosphere

The operator programs channels.

The fixtures interpret channels.

The scene stores the result.

The audience experiences the atmosphere.

---

## Key Idea

A scene is a stored lighting state.

Technically, it is a collection of DMX values.

Creatively, it is a visual moment.

Scenes transform individual channel values into meaningful lighting looks and serve as the foundation for all lighting programming, atmosphere creation and show design.
