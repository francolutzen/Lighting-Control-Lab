# Introduction

The DMX192 controller is one of the most common entry-level lighting consoles used for learning DMX512 programming.

Although limited compared to modern software controllers, it provides an excellent environment for understanding the core principles of fixture control, scene programming, banks and chases.

For many lighting operators, the DMX192 serves as the first practical step from theoretical DMX knowledge into real-time lighting control.

This document focuses on operating the controller as a practical lighting tool rather than explaining DMX theory.

---

## Learning Objectives

After completing this document, you should understand how to:

* Connect fixtures to a DMX192 controller.
* Assign fixture addresses correctly.
* Use Scanner Buttons.
* Control fixture channels.
* Record scenes.
* Organize scenes into banks.
* Create chases.
* Use automatic and music modes.
* Adjust speed and fade times.
* Understand the limitations of DMX192 controllers.

---

# Physical Layout

<img width="3936" height="2214" alt="IMG_1566" src="https://github.com/user-attachments/assets/fe406128-ae36-4d04-892e-1e525b920a9e" />

The console is divided into several functional sections:

* Scanner Buttons
* Channel Faders
* Page A / Page B
* Scene Buttons
* Bank Controls
* Chase Buttons
* Program Controls
* Playback Controls

Understanding these sections is essential before attempting programming.

---

# Scanner Buttons

Scanner Buttons are used to select which fixture is currently being controlled.

A typical DMX192 controller contains:

* 12 Scanner Buttons

Each Scanner Button controls a block of 16 DMX channels.

Example:

Scanner 1 → Channels 1–16

Scanner 2 → Channels 17–32

Scanner 3 → Channels 33–48

Scanner 4 → Channels 49-64

Scanner 5 → Channels 65-80

Scanner 6 → Channels 81-96

Scanner 7 → Channels 97-112

Scanner 8 → Channels 113-128

Scanner 9 → Channels 129-144

Scanner 10 → Channels 145-160

Scanner 11 → Channels 161-176

Scanner 12 → Channels 177–192

This organization is a limitation of the controller and should not be confused with DMX512 addressing itself.

[Insert image highlighting Scanner Buttons]

---

# Channel Faders

The console contains 8 physical faders.

Using Page A and Page B, these become:

Channels 1–8

and

Channels 9–16

for the selected Scanner.

Example:

Scanner 1 selected

# Page A:

Fader 1 → DMX Channel 1

Fader 2 → DMX Channel 2

...

Fader 8 → DMX Channel 8

# Page B:

Fader 1 → DMX Channel 9

Fader 2 → DMX Channel 10

...

Fader 8 → DMX Channel 16

---

# Connecting Fixtures

A basic DMX chain may look like:


All fixtures receive the same DMX signal.

Each fixture responds only to the channels associated with its DMX address.

# Example Real Setup

<img width="3768" height="2120" alt="B662E5DC-452A-44DE-9A07-C8DE2B148BC0" src="https://github.com/user-attachments/assets/cb78e7f8-bf7c-45b8-9830-663e04f1206f" />

Each fixture receives the DMX signal through its DMX IN connector and forwards the signal through its DMX OUT connector to the next fixture in the chain.
---

# Entering Program Mode

To record scenes or chases:

1. Hold PROGRAM.
2. Wait until the Program LED activates.
3. The console is now in programming mode.

Changes can now be stored in memory.

[Insert photo showing Program button]

---

# Recording a Scene

Step 1

Select the desired Scanner.

Step 2

Adjust channel values using the faders.

Step 3

Choose the target Bank.

Step 4

Press MIDI/ADD.

Step 5

Press the desired Scene Button.

The scene is now stored.

---

# What Is Stored Inside a Scene?

A scene stores a snapshot of all active DMX values at the moment it is recorded.

Examples:

* Colors
* Positions
* Gobos
* Movement speeds
* Strobe settings

Scenes are the basic building blocks of programming.

---

# Banks

A Bank is a collection of scenes.

Most DMX192 controllers provide:

* 30 Banks
* 8 Scenes per Bank

Total:

240 Scenes

Example:

Bank 1

Scene 1 = Red Wash

Scene 2 = Blue Wash

Scene 3 = Green Wash

Scene 4 = White Wash

---

# Playing Scenes

Scenes can be triggered manually by pressing Scene Buttons.

Alternatively, they can be played automatically using:

* Auto Mode
* Music Mode

Speed and Fade controls can influence scene transitions.

---

# Recording a Chase

A Chase is a sequence of scenes played automatically.

To create a Chase:

1. Enter Program Mode.
2. Select a Chase Button.
3. Add scenes using MIDI/ADD.
4. Repeat until the sequence is complete.
5. Exit Program Mode.

The chase can now be played back automatically.

---

# Speed and Fade

The console provides two important controls:

## Speed

Controls how quickly the console moves from one step to the next.

## Fade Time

Controls how smoothly transitions occur.

These controls affect:

* Chases
* Automatic scene playback

They are among the most powerful expressive tools available on a DMX192 controller.

[Insert photo highlighting Speed and Fade controls]

---

# Music Mode

Music Mode allows the controller to advance scenes or chase steps according to sound detected by the internal microphone.

This creates basic audio-reactive lighting effects without external software.

---

# Limitations of DMX192 Controllers

While useful for learning, DMX192 controllers have several limitations:

* Fixed 16-channel fixture blocks.
* Limited memory.
* No visual fixture layout.
* No advanced effects engine.
* No timeline programming.
* Limited scalability.

These limitations often motivate users to transition toward software controllers such as QLC+.

---

# Relationship to Other Documents

This document explains how to operate a DMX192 controller.

For the underlying concepts, see:

* Foundations/What-Is-DMX512.md
* Foundations/DMX-Addressing.md
* Foundations/Fixtures.md
* Foundations/Scenes.md
* Foundations/Banks.md
* Foundations/Chases.md

The Foundations documents explain the theory.

This document explains how that theory is applied in practice using a DMX192 controller.
