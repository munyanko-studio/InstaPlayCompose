---
layout: default
title: InstaPlayCompose
description: Drum Screen
---

**English** | [日本語](../ja/drum)

# Overview

On the **Drum Screen** of InstaPlayCompose, you can program individual drum rhythm patterns (step sequencer) and arrange them across bars to build complete drum tracks.

Switch between two modes using the top tabs:
- **Sequence Mode**: Arrange patterns across song bars (1〜256).
- **Pattern Mode**: Create and edit rhythm patterns on a step grid.

![tab](../assets/images/drum/drum_tab.jpg)

# Sequence Mode

<iframe width="250" height="444" src="https://www.youtube.com/embed/tMxX5XyUuiY" frameborder="0" allowfullscreen></iframe>

## Basic Usage

1. **Select Bars**: Tap bar cells on the grid (e.g., `1-1`, `1-2`).
2. **Assign Patterns**: Tap a pattern from the **Pattern Palette** at the bottom to place it into the selected bar. Selection automatically advances to the next bar.
3. **Playback**:
   - Tap **Play Seq** to play from the selected bar.
   - When reaching the end of the sequence, it loops back to `1-1`.
   - Tap **Stop** to halt playback.

## Editing Features

![function_buttons](../assets/images/drum/drum_function_buttons.jpg)

### Silent
Mutes the selected bars.

### Erase
Empties the selected bars.  
- **Long-press**: Deletes selected bars and shifts subsequent bars left.
- **Long-press with nothing selected**: Clears all bars in the drum sequence.

### Insert
Inserts empty bars before the selected bar.

### Copy & Paste
Copies the selected bar configuration to the clipboard. Long-press a bar to choose **Insert** or **Overwrite**.

![paste](../assets/images/drum/paste_drum_data.jpg)

<iframe width="250" height="444" src="https://www.youtube.com/embed/45yfMChE4C4" frameborder="0" allowfullscreen></iframe>

### Ref (Bar Reference)
Link and reuse drum patterns without repetitive copying.

1. Select target bars.
2. Tap **Ref** to open the reference dialog.
3. Specify the source bar.
  - ![ref](../assets/images/drum/drum_ref.jpg)
4. Enable **LimitEndPosition** to loop within a specified bar range.
  - ![ref_with_endpos](../assets/images/drum/drum_ref_with_endpos.jpg)

<iframe width="250" height="444" src="https://www.youtube.com/embed/ODme7Wx9F5c" frameborder="0" allowfullscreen></iframe>
<iframe width="250" height="444" src="https://www.youtube.com/embed/40WMJR16W9U" frameborder="0" allowfullscreen></iframe>

# Pattern Mode

Design custom rhythm patterns by toggling drum instruments on the step grid.

<iframe width="250" height="444" src="https://www.youtube.com/embed/5P1elfjTKAw" frameborder="0" allowfullscreen></iframe>

## Basic Usage

Select the **Pattern** tab to enter Pattern Mode.

- The top area contains **24 pattern slots** (12 come with pre-configured factory presets, and 12 are blank). All presets are fully customizable.
- Select a slot and edit its rhythm on the step sequencer below.

Supported Drum Instruments:
- Crash Cymbal
- Open Hi-Hat
- Closed Hi-Hat
- Tom
- Snare Drum
- Kick Drum

Grid Resolution: Switch between **16-step** and **32-step** resolution.

Tap any cell on the grid to toggle the sound on/off (previews sound upon tap).

- **Reset**: Restores preset patterns to their default state.
- **Play Pattern**: Loops and previews the pattern in real time while editing.

# 💡 Tips & FAQ

- ❓ **Q. How to select multiple bars at once?**
  - Tap the start bar, then long-press the end bar to select the entire span.
- ❓ **Q. How to extend or shorten song length?**
  - Use **Insert** to add bars or long-press **Erase** to delete bars and pull subsequent bars forward.
