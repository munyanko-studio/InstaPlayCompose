---
layout: default
title: InstaPlayCompose
description: Chord Screen
---

**English** | [日本語](../ja/chord)

# Overview

![chord](../assets/images/chord/chord.jpg)

On the **Chord Screen** of InstaPlayCompose, you can build chord progressions and use them as rich multi-instrument accompaniments.

Diatonic chords matching the selected musical key are displayed at the bottom.
You can select Triads (3-note), 7th chords (4-note), and 9th tension chords (5-note).
Multiple arpeggio and strumming playback patterns are available to assign to each bar along with the chord.

Chord sequences copied to the clipboard can also be pasted directly onto the Track screen's piano roll.

Furthermore, you can overlay Chord notes onto the Track screen's piano roll editor for easy melodic reference while composing.

When **Voicing** is enabled, the app analyzes chord transitions to create smooth voice leading, automatic inversions, and anti-clashing voicing for natural, professional harmonic depth.

For details on the voicing algorithm, see [About Voicing](voicing).

# Basic Usage

1. Tap a bar cell on the grid to select it.
2. Tap your desired chord from the chord palette at the bottom.
3. The chord is set to the cell, and the selection automatically advances to the next bar.

When multiple bars are selected, tapping a chord applies it to all selected bars simultaneously.

The selected playback pattern (Arpeggio/Strum) is assigned along with the chord.

Tap **Apply** to update only the playback pattern across selected bars while keeping the chord names unchanged.

<iframe width="250" height="444" src="https://www.youtube.com/embed/NppUaIvcEGU" frameborder="0" allowfullscreen></iframe>

# Chord Palette

The chord palette at the bottom displays chords tailored to the current Key and chord types:

- **Key**: Change root pitch (C〜B) and Major / Minor scale.
- **Chord Type**:
  - **Triad**: 3-note basic chords (C, Dm, Em, etc.)
  - **7th**: 4-note 7th chords (Cmaj7, Dm7, G7, etc.)
  - **9th**: 5-note tension chords (Cmaj9, Dm9, G9, etc.)

| Type | Description |
|---|---|
| **Diatonic** | The 7 foundational chords (Ⅰ〜Ⅶ) of the key. Build solid song structures easily. |
| **Sec Dom** *(Secondary Dominant)* | Chords that introduce temporary key shifts and dynamic harmonic hooks. |
| **Sub V** *(Tritone Substitution)* | Popular jazz/pop substitute dominant chords that resolve smoothly by half-step. |
| **Borrow** *(Borrowed / Modal Interchange)* | Emotional chords borrowed from parallel major/minor keys. |

# Key Settings

When opening the Chord screen, the key is synchronized with the global project key from the hamburger menu. You can also modify it locally.

If you need chords outside the current key, try switching the key on the Chord screen.
The key setting will resynchronize with the global project key when re-entering from other screens.

# Bar Selection

Tap a bar cell on the grid to select it. Repeated taps toggle selection states.

You can also select only the first or second half of a bar by tapping near the left or right side of a cell to assign different chords and patterns to each half.

<iframe width="250" height="444" src="https://www.youtube.com/embed/4ibO_k1YdmQ" frameborder="0" allowfullscreen></iframe>

# Editing Features

![function_buttons](../assets/images/chord/chord_function_buttons.jpg)

### Silent
Mutes the selected bars (silent playback).

### Erase
Empties the selected bars.  
- **Long-press**: Deletes selected bars and shifts subsequent bars to the left.
- **Long-press with no bars selected**: Clears all bars across the entire chord track.

### Insert
Inserts empty bars before the selected bar.

### Copy & Paste
Copies the selected bar configuration to the clipboard.  
After selecting a bar, long-press it to choose **Insert** (shifts subsequent bars right) or **Overwrite**.

![paste](../assets/images/chord/chord_paste.jpg)

<iframe width="250" height="444" src="https://www.youtube.com/embed/3TfnGvo-_ZA" frameborder="0" allowfullscreen></iframe>

Copied chord data can also be pasted directly onto the Track screen's piano roll:

<iframe width="250" height="444" src="https://www.youtube.com/embed/wqdJ8IkYFOo" frameborder="0" allowfullscreen></iframe>

### Ref (Bar Reference)
Link and reuse recurring chord progressions without repetitive copying. When the reference source is modified, all linked bars update automatically.

References operate on full bars (not half bars).

1. Select the target bars you wish to link.
2. Tap **Ref** to open the reference dialog.
3. Specify the source bar number.
  - ![ref](../assets/images/chord/chord_ref.jpg)
4. Enable **LimitEndPosition** if you want to loop a specific range of source bars.
  - ![ref_with_endpos](../assets/images/chord/chord_ref_with_endpos.jpg)

For example, when 4 bars are selected with reference set to `1-1`:
- If `LimitEndPosition` is disabled: references `1-1, 1-2, 1-3, 1-4`.
- If `LimitEndPosition` is set to `1-2`: loops `1-1, 1-2, 1-1, 1-2`.

<iframe width="250" height="444" src="https://www.youtube.com/embed/nX6oB9yRdIo" frameborder="0" allowfullscreen></iframe>
<iframe width="250" height="444" src="https://www.youtube.com/embed/VTHSTHZTu-w" frameborder="0" allowfullscreen></iframe>

# Tips & FAQ

- **Q. How to select multiple bars at once?**
  - Tap the first bar, then long-press the end bar of your desired range to select all bars in between.
- **Q. How to preview chord sounds?**
  - With no bars selected, hold down any chord button in the palette to audition the chord with its active pattern.
