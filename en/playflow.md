---
layout: default
title: InstaPlayCompose
description: ConfigureLoop & Bar Positions
---

**English** | [日本語](../ja/playflow)

# Overview

In InstaPlayCompose, bar positions are handled differently between the **Jam Track (Track 4)** and **Other Tracks (Tracks 1〜3 / Chord / Drum)**.

When using **ConfigureLoop (Loop & Jump settings)**, the Jam Track and backing tracks follow distinct timelines.

---

## 1. Playback Architecture Differences

### ① Jam Track (Track 4)
- **Behavior**: Plays and records continuously from start (`01-1`) to finish in a **linear timeline**, unaffected by jump or loop rules.
- **Timeline**: Based on absolute elapsed time and bar count (`elapsedTicks`).

### ② Other Tracks (Tracks 1〜3 / Chord / Drum)
- **Behavior**: **Follows loop, jump, and start position rules** defined in ConfigureLoop.
- **Timeline**: Based on the dynamic backing sequence (`backingTick`).

---

## 2. Examples of Timeline Divergence

### Example 1: Starting Playback from Bar `05-1`
- **Jam Track**: Counts sequentially from the beginning `01-1`.
- **Other Tracks**: Plays the pattern at `05-1` simultaneously with the start (`01-1`) of the Jam Track.

### Example 2: Looping a 4-Bar Chorus Section
- **Jam Track**: Advances continuously: `01-1` ➔ `02-1` ➔ `03-1` ➔ `04-1` ➔ `05-1` ➔ `06-1` ...
- **Other Tracks**: Loops the section: `01-1` ➔ `02-1` ➔ `03-1` ➔ `04-1` ➔ (Loop) ➔ `01-1` ➔ `02-1` ...

> 💡 **Key Takeaway**
> When recording improvisation into the Jam Track over a looping backing track, your complete continuous performance is faithfully recorded from start to finish without being overwritten by loops.

---

## 3. Understanding Bar Number Colors

The bar counter at the bottom of the screen changes color depending on the active track and mode:

| Screen / Track | Display Color | Meaning |
| :--- | :--- | :--- |
| **Main Screen / TrackJam** | **Default (Black/White)** | **Absolute Elapsed Bar** (`elapsedTicks`) from the start of the song |
| **Main Screen / TrackJam** | **Red** | **Backing Bar Position** (`backingTick`) after loop/jump rules |
| **Track 1 / 2 / 3** | **Red** | **Backing Bar Position** (`backingTick`) currently playing |

### Tap to Switch Display Mode
Tapping the bar number (e.g. `01-1`) toggles between **Absolute Position (Default)** and **Backing Position (Red)** instantly, even during playback or when stopped.

---

## 4. ❓ FAQ

#### Q1. While recording the Jam Track, its bar number differs from other tracks. Is this a bug?
**No, this is intended behavior.**
When ConfigureLoop is active, backing tracks follow repeat/jump loops while the Jam Track captures your linear performance across total song time.

#### Q2. Why are bar numbers shown in Red on Track 1〜3 screens?
To indicate that these tracks are following ConfigureLoop rules and displaying dynamic backing positions.
