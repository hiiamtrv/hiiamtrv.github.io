+++
draft = false
title = 'ChordLens: Roman numeral chord analyzer'
tags = ['TypeScript', 'Music', 'AI-Assisted']
categories = ['Test']
description = "A browser-based chord progression viewer built in under 12 hours using AI with imperative guidance — converts any song into Roman numeral analysis with real-time transposition and a Circle of Fifths reference"
+++

## PROJECT LINK

[{{<icon "github">}} Project link](https://github.com/hiiamtrv/ts-chords-viewer)

## TECH STACK

|                |                                                                  |
| :------------- | :--------------------------------------------------------------- |
| **Platform**   | Web (browser)                                                    |
| **Frontend**   | TypeScript, Vite, HTML/CSS                                       |
| **Showcasing** | AI Assisted Development, Imperative AI Guidance, Music knowledge |

# CHORDLENS

A chord progression viewer and editor with Roman numeral analysis — built in under **12 hours** using AI with **imperative control** (every prompt was precise, directive, and reviewed rather than passively accepted). Write chord progressions in standard notation (e.g. `[C] [G] [Am] [F]`) and the app instantly displays the Roman numeral analysis, key-aware chord names, and a Circle of Fifths reference.

## FEATURES

- [x] Real-time chord parsing and Roman numeral conversion
- [x] Key transposition (up/down/reset) with visual key display
- [x] Circle of Fifths reference panel
- [x] Lyrics/chords toggle view
- [x] Saved songs with sidebar management
- [x] Copy to clipboard
- [x] Custom chord function rules legend

## DEVELOPMENT

Built in under **12 hours** using **imperative AI guidance** — every feature was directed through precise, declarative prompts with full human review before acceptance. Zero black-box generation; all logic was understood and validated before commit.

## LIVE DEMO

<div style="position:relative;width:100%;max-width:900px;margin:1rem 0;">

<iframe id="demo-frame" src="https://dapper-crumble-ee4d9a.netlify.app/" style="width:100%;height:500px;border:1px solid #444;border-radius:6px;" allowfullscreen loading="lazy"></iframe>

<div style="display:flex;gap:0.5rem;margin-top:0.5rem;">
  <button onclick="document.getElementById('demo-frame').requestFullscreen()" style="padding:0.4rem 1rem;cursor:pointer;border:1px solid #444;border-radius:4px;background:#222;color:#eee;">⛶ Fullscreen</button>
  <a href="https://dapper-crumble-ee4d9a.netlify.app/" target="_blank" rel="noopener" style="padding:0.4rem 1rem;border:1px solid #444;border-radius:4px;background:#222;color:#eee;text-decoration:none;">↗ Open in new tab</a>
</div>

</div>

### How to use

1. Type chords in the **Editor** panel using `[Chord]` notation (e.g. `[C] [G] [Am] [F]`)
2. The **Viewer** panel shows the Roman numeral analysis in real time
3. Use the **Key** dropdowns to set the song's key and quality (Major/Minor)
4. Transpose up/down with the arrow buttons or reset to original key
5. Save songs with the sidebar for later editing
6. Toggle between chord-only and chord+lyrics view modes
7. Review the **Rules** panel for custom chord function definitions

### Example

Input: `[C] [G] [Am] [F]` in key of C Major

Output: `I   V   vi  IV`

Transpose up 2 semitones → `[D] [A] [Bm] [G]` with `I  V  vi IV` (numerals don't change LOL)

### Notes

- Chords are parsed as root + quality (e.g. `Cm7`, `G#dim`, `F#m7b5`)
- The Circle of Fifths updates dynamically based on the current key
- Legend rules are loaded from `chord-function-rules.md`
