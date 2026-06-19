# Fixtures

## Introduction

A fixture is any device capable of receiving DMX data and converting that data into a physical action.

Fixtures are the components that transform numerical DMX values into visible lighting effects, movement, atmosphere, or environmental changes.

While DMX controllers transmit information, fixtures are responsible for interpreting that information and producing a result.

Without fixtures, DMX data would simply be a stream of numbers with no visual output.

---

## What Is a Fixture?

A fixture is any lighting or effects device that can receive and respond to DMX signals.

Examples include:

* LED PAR fixtures
* Moving heads
* Scanners
* Spider effects
* Strobes
* Lasers
* Fog machines
* Haze machines
* LED bars
* Pixel fixtures

Each fixture contains one or more DMX channels used to control its available functions.

---

## Fixtures Interpret DMX Data

DMX itself only transmits values between:

0–255

The fixture determines what those values mean.

For example:

Channel 1 = Red Intensity

0 = Off

255 = Full Red

Another fixture may use:

Channel 1 = Pattern Selection

0–15 = Pattern 1

16–31 = Pattern 2

32–47 = Pattern 3

In both cases DMX is transmitting numbers.

The fixture decides how to interpret them.

---

## Channel Maps

Every DMX fixture contains a channel map.

A channel map is a list that defines the function of every DMX channel used by the fixture.

Example:

RGBW Fixture

Channel 1 → Red

Channel 2 → Green

Channel 3 → Blue

Channel 4 → White

Example:

Moving Head

Channel 1 → Pan

Channel 2 → Tilt

Channel 3 → Pan Fine

Channel 4 → Tilt Fine

Channel 5 → Color

Channel 6 → Gobo

Channel 7 → Dimmer

Channel 8 → Strobe

The channel map is the fixture's interpretation guide for incoming DMX data.

---

## Why Fixture Manuals Are Essential

One of the most important habits in lighting control is preserving the original fixture manual.

Without the manual, it is often impossible to know exactly what each DMX channel controls.

The fixture manual typically contains:

* Channel maps
* DMX modes
* Addressing instructions
* Operating modes
* Menu settings
* Technical specifications

Two fixtures that look nearly identical may use completely different channel layouts.

For this reason, the fixture model and its original manual should always be documented and preserved.

A lighting operator should never assume that two fixtures behave the same way simply because they appear similar.

---

## Fixture Modes

Many fixtures offer multiple DMX operating modes.

Example:

RGBW Fixture

4-Channel Mode

Channel 1 → Red

Channel 2 → Green

Channel 3 → Blue

Channel 4 → White

8-Channel Mode

Channel 1 → Master Dimmer

Channel 2 → Red

Channel 3 → Green

Channel 4 → Blue

Channel 5 → White

Channel 6 → Strobe

Channel 7 → Programs

Channel 8 → Speed

The same fixture can therefore occupy different numbers of DMX channels depending on the selected mode.

This is known as the fixture footprint.

---

## Fixture Footprint

A fixture footprint is the number of DMX channels occupied by a fixture.

Examples:

RGB Fixture

Footprint = 3 Channels

RGBW Fixture

Footprint = 4 Channels

Moving Head

Footprint = 16 Channels

Laser

Footprint = 10 Channels

The footprint determines how much space the fixture occupies inside the DMX universe.

It also determines the next available address for additional fixtures.

---

## Types of Fixtures

### Static Fixtures

Fixtures that do not physically move.

Examples:

* LED PARs
* LED Bars
* Flood Lights

These fixtures primarily control color, brightness and effects.

---

### Moving Fixtures

Fixtures capable of changing their physical position.

Examples:

* Moving Heads
* Scanners

These fixtures typically include:

* Pan
* Tilt
* Color Selection
* Gobos
* Prisms
* Focus

---

### Effects Fixtures

Fixtures designed to create dynamic visual effects.

Examples:

* Spider Lights
* Derby Effects
* Moonflowers
* Multi-beam Effects

These fixtures often use channels for:

* Pattern Selection
* Rotation
* Speed
* Program Control

---

### Atmospheric Fixtures

Fixtures that modify the environment rather than producing light directly.

Examples:

* Fog Machines
* Haze Machines

These fixtures can dramatically change how lighting appears within a space.

---

## Fixtures and Creativity

From a technical perspective, fixtures are DMX devices that interpret channel values.

From a creative perspective, fixtures are the instruments used to shape visual experiences.

Different fixture types provide different creative possibilities.

A RGBW PAR may create color and atmosphere.

A moving head may create motion and direction.

A laser may create geometric structures.

A fog machine may reveal light beams that would otherwise remain invisible.

Understanding a fixture's capabilities is therefore not only a technical task but also a creative one.

---

## Key Idea

DMX sends numbers.

Fixtures interpret those numbers.

The fixture's channel map determines what every DMX value means.

For this reason, understanding the fixture itself is just as important as understanding DMX.

A lighting designer who understands fixtures gains access to the visual vocabulary needed to create atmospheres, synchronize with music and build immersive lighting experiences.

Related Repository Sections

Fixtures/
    Individual fixture documentation

Assets/
    Manuals and manufacturer documentation

Experiments/
    Fixture testing and discoveries

Atmospheres/
    Practical applications of fixture capabilities
