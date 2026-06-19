# Banks

## Introduction

As lighting systems become more complex, the number of stored scenes quickly increases.

A controller may contain dozens or even hundreds of scenes, making it difficult to access them efficiently during operation.

To solve this problem, many lighting controllers organize scenes into groups called banks.

A bank is simply a collection of scenes stored together for organizational purposes.

Banks do not create lighting effects.

Banks organize lighting effects.

---

## What Is a Bank?

A bank is a container that stores multiple scenes.

Think of a bank as a folder.

Example:

Bank 1

├── Scene 1

├── Scene 2

├── Scene 3

└── Scene 4

Each scene contains its own set of DMX values.

The bank simply provides a way to organize and access those scenes.

---

## Banks Do Not Exist in DMX512

One of the most important concepts to understand is that banks are not part of the DMX512 protocol.

DMX512 only transmits channel values.

Concepts such as:

* Scenes
* Banks
* Chases
* Programs

are features implemented by controllers and software.

This means that different controllers may organize scenes in completely different ways.

Banks are therefore a controller-specific organizational tool rather than a DMX requirement.

---

## Banks in DMX192 Controllers

Many entry-level DMX192 controllers use a bank-based structure.

A common configuration is:

30 Banks

×

8 Scenes per Bank

=

240 Total Scenes

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

Bank 2

Scene 1

Scene 2

Scene 3

Scene 4

Scene 5

Scene 6

Scene 7

Scene 8

...

Bank 30

Scene 1

Scene 2

Scene 3

Scene 4

Scene 5

Scene 6

Scene 7

Scene 8

This allows the controller to store a large number of lighting looks while using a limited number of physical buttons.

Different DMX192 models may vary slightly, but the 30-bank / 8-scene structure is very common.

---

## Why Banks Exist

A controller typically has only a small number of scene buttons available.

Without banks, the operator could only access a handful of scenes.

Banks multiply the available storage.

Example:

8 Physical Scene Buttons

↓

30 Banks

↓

240 Available Scene Locations

The same scene buttons are reused for different banks.

The active bank determines which scenes are currently available.

---

## Example

Imagine a controller currently displaying:

Bank 1

Scene Button 1 = Red Wash

Scene Button 2 = Blue Wash

Scene Button 3 = Green Wash

Scene Button 4 = Blackout

Switching to:

Bank 2

might produce:

Scene Button 1 = Warm White

Scene Button 2 = Sunset Atmosphere

Scene Button 3 = Deep Purple

Scene Button 4 = Festival Colors

The physical buttons remain the same.

Only the stored scenes change.

---

## Organizing Banks

Many operators organize banks according to function.

Example:

Bank 1

Basic Colors

Bank 2

Pastel Colors

Bank 3

Warm Atmospheres

Bank 4

Cool Atmospheres

Bank 5

Dance Floor Looks

Bank 6

Build-Ups

Bank 7

Peak Energy

Bank 8

Blackouts and Utility Scenes

This makes operation faster during live performances.

---

## Banks and Live Operation

During a live show, banks allow rapid access to different groups of scenes.

The operator can move between banks depending on the mood, music or stage requirements.

Example:

Ambient Music

↓

Bank 3

Warm Atmospheres

Dance Section

↓

Bank 6

Build-Ups

High Energy Moment

↓

Bank 7

Peak Energy

The bank structure becomes part of the operator's workflow.

---

## Banks in Lighting Software

Modern lighting software often removes the limitations of physical banks.

Platforms such as QLC+, MagicQ and other professional systems may use:

* Folders
* Virtual buttons
* Cue lists
* Workspaces
* Tags
* Categories

Instead of traditional banks.

However, the underlying idea remains similar:

A large collection of scenes requires organization.

Banks were one of the earliest and most common solutions to that problem.

---

## Banks and Creativity

Technically, a bank is an organizational tool.

Creatively, a bank can represent a category of visual ideas.

For example:

Atmospheres

Energy Levels

Color Families

Musical Moments

Show Sections

Many lighting designers think in terms of visual intentions rather than individual scenes.

In this context, banks become collections of related visual states.

---

## Relationship Between Scenes, Banks and Chases

A useful mental model is:

DMX Values

↓

Scenes

↓

Banks

↓

Chases

Scenes store lighting states.

Banks organize scenes.

Chases play scenes in sequence.

Understanding banks is therefore an important step before learning how chases work.

---

## Key Idea

A bank is a collection of scenes organized for easier access and operation.

Banks are not part of the DMX512 protocol itself.

They are a controller feature designed to help operators manage large numbers of scenes efficiently.

In controllers such as the DMX192, banks transform a small set of physical buttons into hundreds of available scene locations, making practical lighting programming possible.
