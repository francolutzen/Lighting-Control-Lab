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

---

Because each Scanner Button controls a dedicated 16-channel block, a DMX192 controller can directly manage up to 12 independent fixture groups.

This does not necessarily mean only 12 physical fixtures.

Multiple fixtures can share the same DMX address and therefore respond to the same Scanner Button simultaneously.

Example:

PAR 1 → Address 001

PAR 2 → Address 001

PAR 3 → Address 001

All three fixtures will respond together when Scanner 1 is selected.

The practical limitation is therefore 12 independently controlled fixture groups rather than 12 individual fixtures.

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

This example shows a basic DMX installation using three fixtures connected in a daisy-chain configuration.

Fixture 1 → FG-369 LED PAR 54 RGBW

Fixture 2 → Big Dipper L001 Half-Ball

Fixture 3 → LM30A Mini Spider 8×3W RGBW

Notice that the physical order of the fixtures in the DMX chain does not determine how they are controlled.

Control is determined by each fixture's DMX address.

For example:

Fixture 1 → Address 001

Fixture 2 → Address 017

Fixture 3 → Address 033

or

Fixture 1 → Address 033

Fixture 2 → Address 001

Fixture 3 → Address 017

Both configurations would function correctly as long as the addresses are configured properly.

### Important — Always Use a DMX Terminator

A DMX terminator should be installed on the **DMX OUT** connector of the last fixture in the chain.

Using a terminator is especially important:

* On the last fixture of a DMX daisy-chain.
* When cable runs exceed approximately 30 meters (100 ft).
* In stage lighting, concerts, live events and outdoor installations.
* When troubleshooting flickering, erratic behavior or communication problems.

A DMX terminator helps absorb signal reflections that can travel back through the cable and cause unreliable fixture behavior.

**Tip:** Even if the system appears to work correctly without a terminator, it is still recommended to use one. Signal problems may only become visible under specific conditions and can appear unexpectedly during a live show.



Each fixture receives the DMX signal through its DMX IN connector and forwards the signal through its DMX OUT connector to the next fixture in the chain.

---

# Entering Program Mode

To record scenes or chases:

1. Hold PROGRAM.
2. Wait until the Program LED activates.
3. The console is now in programming mode.

Changes can now be stored in memory.

---

## Programming a Scene on the LK-C01 DMX192

The following procedure describes how scene programming works on the LK-C01 DMX192 controller used in this project.

### Step 1 — Select the Fixture

Press the Scanner Buttons corresponding to the fixtures you want to control.

Examples:

- Scanner 1
- Scanner 2
- Scanner 3

Multiple Scanner Buttons can be selected simultaneously.

### Step 2 — Adjust the Channels

Use the channel faders to create the desired lighting state.

Examples:

- Set colors
- Adjust movement
- Configure strobe effects
- Select patterns
- Set brightness levels

The resulting combination of channel values will become the scene.

### Important — Reset Unused Faders

When programming multiple fixtures, it is good practice to lower any faders that are no longer needed before selecting and programming other fixtures.

Example:

1. Select Scanner 1.
2. Create a red color using the RGB channels.
3. Store the scene.
4. Lower the RGB faders.
5. Select Scanner 2.
6. Continue programming the next fixture.

Leaving unnecessary faders raised can make it difficult to see which channels are actively contributing to the scene and may lead to programming mistakes.

Keeping unused faders at zero helps maintain a clear workflow and makes scene programming easier to understand and troubleshoot.

### Step 3 — Enter Programming Mode

Press and hold the **PROGRAM** button until the LED display begins flashing.

This indicates that the controller has entered programming mode.

### Step 4 — Enable Scene Recording

Press the **MIDI/ADD** button.

The controller is now ready to store the current lighting state.

### Step 5 — Select the Bank and Store the Scene

Before saving the scene, verify that the correct Bank is selected.

A DMX192 controller typically stores:

- 30 Banks
- 8 Scenes per Bank
- 240 Scene locations in total

The scene will be stored in the currently selected Bank and Scene Button combination.

Example:

Bank 01 + Scene 1

Bank 01 + Scene 2

Bank 05 + Scene 4

Bank 12 + Scene 8

After confirming the desired Bank, press the **SCENE BUTTON** where the scene should be stored.

The current DMX values are now saved in that location.

### Important

A Scene Button does not uniquely identify a scene.

The same Scene Button can contain different scenes in different Banks.

Example:

Bank 01 → Scene 1 = Red Wash

Bank 02 → Scene 1 = Blue Wash

Bank 03 → Scene 1 = Strobe Effect

Although all three scenes use Scene Button 1, they are stored in different Banks and therefore remain independent.

### Step 6 — Exit Programming Mode

Press and hold the **PROGRAM** button again until the display stops flashing.

This exits programming mode.

### Step 7 — Disable Blackout

On the LK-C01 DMX192, exiting programming mode automatically activates **BLACKOUT**.

To return to normal operation:

- Press the **BLACKOUT** button once.

The newly recorded scene can now be played back normally.

### Notes

This procedure is specific to the LK-C01 DMX192 controller.

Other DMX192-compatible consoles may use slightly different button combinations or programming workflows.

Always consult the original manual for the exact procedure used by your controller model.

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

- 30 Banks
- 8 Scenes per Bank

Total:

- 240 Scenes

### Example

Bank 1 — Basic Color Palette

- Scene 1 = Red Wash
- Scene 2 = Orange Wash
- Scene 3 = Yellow Wash
- Scene 4 = Green Wash
- Scene 5 = Cyan Wash
- Scene 6 = Blue Wash
- Scene 7 = Magenta Wash
- Scene 8 = White Wash

This Bank acts as a color palette that can be used during live operation or as the foundation for building chases.

## Starting Automatic Playback

1. Select the desired Bank.
2. Press the **AUTO/DEL** button.

The controller will begin cycling through the scenes stored in the selected Bank.

For example:

Bank 01

* Scene 1 → Red
* Scene 2 → Green
* Scene 3 → Blue
* Scene 4 → White

When Auto Mode is active, the controller will continuously move from one scene to the next without requiring manual input.

## Speed and Fade Time During Automatic Playback

Two controls determine how the transitions occur:

* **Speed**
* **Fade Time**

### Speed

The **Speed** control determines how quickly the controller advances from one scene to the next.

Examples:

Low Speed:

* Long delay between scene changes.

High Speed:

* Rapid scene changes.

### Fade Time

The **Fade Time** control determines how smoothly the controller transitions between scenes.

Low Fade Time:

* Instant transitions.
* Abrupt visual changes.

High Fade Time:

* Gradual transitions.
* Intermediate colors and values become visible.

### Example

Imagine Bank 01 contains:

* Scene 1 → Red
* Scene 2 → Green
* Scene 3 → Blue

If:

* Speed is set high.
* Fade Time is set low.

The controller will jump rapidly between red, green and blue.

Result:

Red → Green → Blue → Red → Green → Blue

The effect feels energetic, aggressive and rhythmic because there is very little blending between colors.

If:

* Speed remains high.
* Fade Time is increased.

The controller will gradually blend between scenes.

Result:

Red → Yellow → Green → Cyan → Blue → Magenta → Red

The intermediate colors become visible because the DMX values are being crossfaded rather than switched instantly.

### Creative Use

The relationship between Speed and Fade Time has a major impact on the atmosphere created by the lighting system.

Low Fade Time often produces:

* Sharp transitions
* Rhythmic effects
* Energetic looks
* Dancefloor-oriented lighting

Higher Fade Time often produces:

* Smooth color washes
* Ambient transitions
* Relaxed environments
* More cinematic atmospheres

Learning to balance Speed and Fade Time is one of the most important creative skills when working with a DMX192 controller.

# Chases

A Chase is a programmed sequence of scenes that plays automatically.

Unlike a Bank, which simply stores scenes together, a Chase allows scenes from different Banks to be combined into a single playback sequence.

This makes Chases one of the most powerful programming tools available on a DMX192 controller.

### What Can a Chase Contain?

A Chase does not store DMX values directly.

Instead, it stores references to previously recorded scenes.

For example:

* Bank 1 → Scene 2
* Bank 4 → Scene 3
* Bank 6 → Scene 5
* Bank 2 → Scene 7

These scenes can then be arranged into a custom playback sequence.

### Example

Imagine the following scenes have already been programmed:

Bank 1

* Scene 2 = Red Wash

Bank 4

* Scene 3 = Blue Wash

Bank 6

* Scene 5 = White Strobe

A Chase could be programmed as:

Step 1 → Bank 1, Scene 2

↓

Step 2 → Bank 4, Scene 3

↓

Step 3 → Bank 6, Scene 5

↓

Repeat

The operator only needs to press the corresponding Chase Button to play the entire sequence.

### DMX192 Chase Buttons

Most DMX192 controllers provide:

* 6 Chase Buttons

Typically labeled:

* Chase 1
* Chase 2
* Chase 3
* Chase 4
* Chase 5
* Chase 6

Each Chase Button can contain multiple scene steps.

Once programmed, the Chase can be recalled instantly during operation.

### Why Use Chases?

Without Chases, an operator would need to manually select scenes and banks throughout the performance.

A Chase automates this process.

Benefits include:

* Faster operation
* Consistent playback
* Dynamic lighting effects
* Reduced manual workload
* Easier live performance control

### Recording a Chase

To create a Chase:

1. Enter Program Mode.
2. Press the desired Chase Button.
3. Select the Bank containing the scene.
4. Press the Scene Button.
5. Press MIDI/ADD to store the step.
6. Repeat for additional scenes.
7. Exit Program Mode.

The Chase is now stored in memory.

### Example Programming Sequence

Imagine the following scenes have already been programmed:

#### Bank 1 — Scene 2

Fixture 1 → FG-369 LED PAR 54 RGBW

* Amber Wash

Fixture 2 → Big Dipper L001 Half-Ball

* Slow Multicolor Rotation

Fixture 3 → LM30A Mini Spider

* Red Beam Movement

Result:

Warm and welcoming atmosphere.

---

#### Bank 4 — Scene 3

Fixture 1 → FG-369 LED PAR 54 RGBW

* Blue Wash

Fixture 2 → Big Dipper L001 Half-Ball

* Blue and White Rotation

Fixture 3 → LM30A Mini Spider

* Fast Blue Chase

Result:

Cool and energetic atmosphere.

---

#### Bank 6 — Scene 5

Fixture 1 → FG-369 LED PAR 54 RGBW

* Full White

Fixture 2 → Big Dipper L001 Half-Ball

* Fast RGB Rotation

Fixture 3 → LM30A Mini Spider

* White Strobe Effect

Result:

High-energy atmosphere for musical peaks.

---

#### Bank 2 — Scene 7

Fixture 1 → FG-369 LED PAR 54 RGBW

* Cyan Wash

Fixture 2 → Big Dipper L001 Half-Ball

* Slow Blue Rotation

Fixture 3 → LM30A Mini Spider

* Cyan Static Pattern

Result:

Relaxed ambient atmosphere.

### Chase 1

The following Chase could be programmed:

Step 1 → Bank 1, Scene 2

↓

Step 2 → Bank 4, Scene 3

↓

Step 3 → Bank 6, Scene 5

↓

Step 4 → Bank 2, Scene 7

↓

Repeat

During playback, all three fixtures change simultaneously because each scene contains DMX information for every programmed fixture.

The Chase is therefore not simply changing colors or effects.

It is transitioning between complete lighting looks involving the entire lighting system.

### Important

A scene can store the state of multiple fixtures at the same time.

As a result, a Chase is typically a sequence of complete lighting states rather than a sequence of individual fixture commands.

In practical use, operators often build Chases from scenes that already contain coordinated colors, movements and effects across all fixtures in the setup.



### Speed and Fade Time

Just like automatic scene playback, Chases can be influenced by:

* Speed
* Fade Time

Speed determines how quickly the Chase advances from one step to the next.

Fade Time determines how smoothly the controller transitions between steps.

This allows the same Chase to create very different visual atmospheres depending on the settings used.

### Mental Model

Scene

↓

Stored inside a Bank

↓

Selected and added to a Chase

↓

Automatically played back during a show

A useful way to think about a Chase is as a playlist.

Scenes are the individual songs.

Banks organize those songs.

The Chase is the playlist that determines the order in which they are played.

---

# Music Mode

Most DMX192 controllers include a built-in microphone that allows scenes or chase steps to change automatically in response to sound.

When Music Mode is activated, the controller listens to the surrounding audio environment and advances scenes or chase steps whenever it detects sound peaks.

The microphone does not analyze musical notes, melodies or song structure.

Instead, it reacts primarily to changes in sound intensity.

Examples:

* Kick drums
* Snare hits
* Bass impacts
* Loud rhythmic elements

Typical operation:

Sound Peak

↓

Microphone Detection

↓

Controller Trigger

↓

Next Scene or Chase Step

Because of this behavior, Music Mode often works best with music that contains a strong and consistent rhythm.

### Practical Example

Imagine a Chase containing:

* Scene 1 = Red
* Scene 2 = Blue
* Scene 3 = Green
* Scene 4 = White

With Music Mode enabled:

Kick Drum

↓

Scene changes from Red to Blue

Next Kick Drum

↓

Scene changes from Blue to Green

Next Kick Drum

↓

Scene changes from Green to White

The result is a simple audio-reactive lighting effect synchronized to the energy of the music.

### Limitations

The built-in microphone provides a basic form of synchronization and should not be confused with professional audio analysis systems.

Common limitations include:

* Sensitivity to ambient noise.
* Inconsistent triggering in quiet environments.
* Reduced accuracy with complex musical material.
* No beat detection or BPM analysis.
* No frequency analysis.

### Creative Use

Despite its simplicity, Music Mode can be very effective for:

* Small parties.
* Home events.
* Beginner lighting setups.
* Quick audio-reactive effects without software.

For many users, Music Mode provides an easy introduction to the relationship between music, rhythm and lighting before moving to more advanced software-based control systems.

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
