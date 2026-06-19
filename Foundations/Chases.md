## Banks, Speed and Fade Time

In many DMX192 controllers, the **Speed** and **Fade Time** controls are commonly associated with chases.

However, depending on the controller design and playback mode, these controls may also influence how stored scenes are recalled from banks.

For example:

### Scene Change Without Fade

```text
Scene 1 = Red Wash

↓

Scene 2 = Blue Wash
```

Result:

```text
Red
↓
Blue
```

Instant change.

### Scene Change With Fade

```text
Scene 1 = Red Wash

↓

Scene 2 = Blue Wash
```

Result:

```text
Red
↓
Purple
↓
Blue
```

Gradual transition.

This behavior depends on the specific controller model and operating mode.

For this reason, operators should always consult the controller manual to understand exactly how **Speed** and **Fade Time** affect scene playback.

A useful practical distinction is:

```text
Speed
=
How fast playback advances between steps.
```

```text
Fade Time
=
How smoothly one lighting state transitions into another.
```

Although these controls are often discussed in relation to chases, they can also influence scene-based operation on many DMX192 consoles.

---

## Design Perspective

Fade Time is one of the most powerful atmosphere-building tools available on simple DMX controllers.

A scene change with no fade creates contrast and impact.

A scene change with a long fade creates continuity and emotional progression.

The programmed scene may be identical.

The fade time can completely change how the audience experiences it.

Example:

```text
Blue Atmosphere
↓
Amber Atmosphere
```

Without fade:

```text
Blue
↓
Amber
```

With a long fade:

```text
Blue
↓
Purple
↓
Magenta
↓
Warm Amber
```

From a technical perspective, nothing changed except the transition time.

From the audience's perspective, the entire emotional quality of the lighting can change.
