---
layout: default
title: InstaPlayCompose
description: About Voicing
---

**English** | [日本語](../ja/voicing)

# Overview

- **Voicing OFF (Root Position)**: Plays all chords in standard root position (close harmony with root in the bass). When chords change, the entire harmony shifts in parallel, causing large pitch jumps and a rigid, mechanical sound.
- **Voicing ON (Auto Voice Leading & Optimized Distribution)**: Dynamically analyzes chord progressions to apply smooth voice leading, automatic inversions, and anti-clashing open voicings in real time, delivering lush, natural harmonies akin to a skilled pianist or guitarist.

# Algorithm

When Voicing is ON, the engine separates harmony into **Bass Notes** and **Upper Structure Notes (Ensemble)**.

## 1. Smooth Voice Leading Heuristic

- **Pitch Center Memory (Anchor Point)**: Remembers the average pitch center of the previous chord's upper structure.
- **Closest Octave Selection**: For each note in the new chord (C, E, G, etc.), calculates and assigns the octave closest to the previous anchor. Common tones are held in place and moving voices shift by minimal step intervals, automatically creating natural chord inversions.
- **Range Clamping**: Restricts the anchor point within optimal registers (centered around C4/Middle C in Normal mode) to prevent harmonies from drifting excessively high or low.

## 2. Anti-Clashing & Open Voicing

- **2nd Interval Expansion**: When upper voices contain narrow minor/major 2nd intervals (1〜2 semitones apart) that cause muddy clashes, the engine automatically raises the higher note by an octave into an open/spread voicing.

## 3. Instrument-Specific Voicing Modes

| Mode | Bass Range | Upper Center Pitch | Special Algorithm |
| :--- | :--- | :--- | :--- |
| **NORMAL**<br>*(Piano / Keyboards)* | **C2 〜 B2**<br>(MIDI 36〜47) | **Around C4 (Middle C)** | Raises clashing 1st/2nd intervals in upper voices by an octave to maintain harmonic clarity. |
| **GUITAR**<br>*(Guitar)* | **E2 〜 D3**<br>(MIDI 36/40〜50) | **Around D4** | Emulates open chord shapes by ensuring the root tone is reinforced in upper registers when needed. Expands narrow 2nds and clamps upper range below high frets (C6 / MIDI 84). |
| **BASS**<br>*(Bass)* | **C1 〜 B1**<br>(MIDI 24〜35) | **Around F2** | Enforces strict Low Interval Limits. Shifts intervals narrower than a minor 3rd in low registers up an octave to prevent boomy dissonance. |

# Summary

**Voicing ON** programmatically simulates human performance nuances—inversions, fingerings, and theoretical voice leading—transforming simple chord tracks into polished, professional arrangements. Toggle between ON and OFF depending on your musical style and genre needs.
