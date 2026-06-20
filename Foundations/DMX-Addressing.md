# DMX Addressing

## Introduction

One of the most common sources of confusion when learning DMX512 comes from the way different controllers handle fixture addressing.

Many entry-level consoles, such as DMX192 controllers, organize fixtures into fixed 16-channel blocks called Scanner Buttons.

For example:

Scanner 1 → Channels 1–16

Scanner 2 → Channels 17–32

Scanner 3 → Channels 33–48

This often creates the impression that every fixture must start at addresses:

1, 17, 33, 49, 65...

However, this is not a limitation of the DMX512 protocol itself.

It is simply a way certain hardware consoles organize DMX channels for the user.

In reality, DMX512 only provides a universe containing 512 channels.

A fixture can be assigned to any valid starting address as long as sufficient channels remain available for its channel footprint.

For example:

Fixture A

Address = 1

Footprint = 4 channels

Uses:

1–4

Fixture B

Address = 5

Footprint = 8 channels

Uses:

5–12

Fixture C

Address = 13

Footprint = 9 channels

Uses:

13–21

This configuration is completely valid in DMX512 and is commonly used in lighting software such as QLC+, MagicQ and other professional control systems.

This allows channels to be used more efficiently, especially when fixtures require fewer than 16 channels.

The purpose of DMX addressing is therefore not to assign fixtures to fixed blocks, but to determine which portion of the 512 available channels each fixture will listen to.

Understanding this distinction is important because many concepts that appear to be DMX rules are actually controller-specific limitations.

DMX itself only knows channels.

Fixtures listen to channels.

Controllers simply provide different ways of organizing and controlling them.

This document explains how DMX addresses work, how fixtures occupy channels, how to calculate addresses correctly, and how to avoid channel overlap when building a lighting system.

## Physical Connection vs DMX Addressing

The physical order of fixtures in a DMX cable chain does not determine their addresses.

A fixture can be placed anywhere in the chain regardless of its DMX address.

Example:

DMX Controller

↓

Fixture A

Address = 1

Channels = 1–4

↓

Fixture B

Address = 25

Channels = 25–32

↓

Fixture C

Address = 100

Channels = 100–108

↓

DMX Terminator

In larger or professional DMX installations, a DMX terminator is often placed at the end of the chain.

A terminator helps reduce signal reflections that may cause communication errors, flickering, or unreliable fixture behavior.

Small setups often operate successfully without a terminator, but its use is considered good practice, especially when using long cable runs or multiple fixtures.

All fixtures receive the same DMX signal.

The signal travels through the entire chain regardless of the fixture addresses.

Each fixture reads only the channels assigned to its starting address and ignores all other channels.

For example:

DMX Controller

↓

RGBW PAR

Address = 50

↓

Laser

Address = 1

↓

Spider

Address = 200

This configuration works perfectly because physical position and DMX addressing are independent concepts.

# What Is a DMX Address?

A DMX address is the first channel that a fixture listens to within a DMX universe.

The fixture then automatically uses the following channels required by its channel footprint.

Example:

Fixture Start Address = 1

Fixture Channels Used = 4

The fixture will use:

Channel 1

Channel 2

Channel 3

Channel 4

The address itself only identifies the first channel.

# What Is a Channel Footprint?

The channel footprint is the total number of DMX channels required by a fixture.

Examples:

RGB Fixture = 3 Channels

RGBW Fixture = 4 Channels

Moving Head = 16 Channels

Spider Effect = 9 Channels

Different operating modes may change the footprint of the same fixture.

Example:

4 Channel Mode

or

8 Channel Mode

Always consult the fixture manual to determine the correct footprint.

## Why Fixture Manuals Matter?

The fixture manual is the most important source of information when configuring DMX equipment.

DMX itself only transports values.

The manual explains how the fixture interprets those values.

A fixture manual typically contains:

-Channel map
-Channel footprint
-DMX modes
-Addressing instructions
-Operating functions
-Value ranges for each channel

Example:

Channel 1

0–31 = Blackout

32–63 = Red

64–95 = Green

96–127 = Blue

Without the manual, it is often impossible to know what each DMX value actually does.

For this reason, it is highly recommended to keep the original manuals of every fixture used in a lighting system.

Addressing a Single Fixture

Example:

RGBW Fixture

Footprint = 4 Channels

Start Address = 1

The fixture will use:

1 → Red

2 → Green

3 → Blue

4 → White

This fixture occupies channels 1–4.

Addressing Multiple Fixtures

Example:

Fixture 1

Address = 1

Footprint = 4

Uses:

1–4

Fixture 2

Address = 5

Footprint = 4

Uses:

5–8

Fixture 3

Address = 9

Footprint = 4

Uses:

9–12

Each fixture occupies its own channel range.

# Visualizing Channel Allocation

A useful way to visualize addressing is to imagine the DMX universe as a table containing 512 channels.

Example:

1 ------------------------------------------------------------------------------------------------- 512

|----PAR----|

         |----LASER-----|

                        |----SPIDER----|

Where:

1–4 = RGBW PAR

5–12 = Laser

13–21 = Spider

Each fixture occupies a portion of the available DMX space.

# Address Calculation

A common way to calculate the next address is:

Next Address = Current Address + Footprint

Example:

Fixture 1

Address = 1

Footprint = 4

Next Address = 5

Fixture 2

Address = 5

Footprint = 4

Next Address = 9

This prevents channel overlap.

Channel Overlap

Channel overlap occurs when two fixtures occupy the same DMX channels.

Example:

Fixture 1

Address = 1

Footprint = 4

Uses Channels 1–4

Fixture 2

Address = 3

Footprint = 4

Uses Channels 3–6

Channels 3 and 4 overlap.

Both fixtures will react to the same DMX values on those channels.

In most situations, overlap is undesirable because it reduces independent control.

Shared Addresses

Sometimes multiple fixtures intentionally share the same address.

Example:

Fixture A

Address = 1

Fixture B

Address = 1

Both fixtures receive exactly the same DMX instructions.

This technique is commonly used when:

Fixtures are identical
Fixtures should always behave together
Channel count needs to be reduced

Shared addressing sacrifices independent control in exchange for simplicity.

Addressing Example

Imagine a small setup:

2 RGBW PAR Fixtures

1 Spider Effect

Fixture 1

RGBW PAR

Address = 1

Footprint = 4

Uses:

1–4

Fixture 2

RGBW PAR

Address = 5

Footprint = 4

Uses:

5–8

Spider

Address = 9

Footprint = 9

Uses:

9–17

Total channels used:

17

Remaining channels available:

512 - 17 = 495

Addressing in Lighting Software

Programs such as QLC+, MagicQ and other lighting controllers require the software address and the fixture address to match.

Example:

Physical Fixture Address = 17

Software Fixture Address = 17

If the addresses do not match, the fixture will not respond correctly.

Addressing is therefore one of the first things that should be checked during troubleshooting.

Common Beginner Mistakes
Forgetting the Fixture Footprint

A fixture may use more channels than expected.

Always verify the channel mode and footprint.

Incorrect Address Calculations

Always calculate the next address based on the total footprint.

Wrong Fixture Mode

A fixture configured in 9-channel mode will not behave correctly if the software expects 16-channel mode.

Ignoring the Manual

Always verify channel maps, modes and functions using the manufacturer's documentation.

Confusing Console Layout with DMX Rules

Many hardware controllers organize fixtures into fixed blocks.

This does not mean DMX itself requires fixtures to start at addresses 1, 17, 33 or 49.

Those are controller-specific conventions.

Key Idea

DMX does not know what a fixture is.

DMX only knows channels.

Fixtures listen to channels.

Controllers provide different ways of organizing and controlling those channels.

A DMX address identifies the first channel that a fixture will listen to.

Once the starting address is assigned, the fixture automatically occupies as many channels as required by its footprint.

Understanding addressing is essential for building reliable lighting systems, programming fixtures correctly, and maintaining independent control over every element of a lighting design.
