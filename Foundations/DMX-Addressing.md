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
