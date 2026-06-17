# The Microtonal Keyboard

A microtonal MIDI-style keyboard for the browser. Pick any of **11 equal-division-of-the-octave (EDO) tunings** — from 5-EDO (whole-tone) to 53-EDO (near-just) — and play it with your mouse or touchscreen. A built-in drum machine lets you lay down beats alongside the microtonal notes.

Built on [Tone.js](https://tonejs.github.io/) for audio synthesis. Single self-contained HTML file, no build step.

**Live demo:** https://themicrotonalkeyboard.netlify.app/

## What it does

- **11 EDO tunings** — 5, 7, 9, 12, 17, 19, 22, 24, 31, 33, 53
- **1–3 octaves** of microtonal keys per EDO
- **4 synth voices** — sine, square, triangle, sawtooth
- **Drum machine** with 10 preset patterns (Standard, Electro, Techno, Pop, Rock, House, Funk, Jazz, Progressive, Progressive 2)
- **2 drum kits** — Standard, Electro
- **Pattern length** — 2 to 9 steps
- **Effects** — Reverb, Distortion, Arpeggiator
- **Volume sliders** for master, tempo, and drum mix
- **Tempo** — 30 to 240 BPM

## How to use

Open the page in a modern browser, then:

1. **Pick an EDO** from the dropdown (12-EDO is the default — that's standard Western tuning).
2. **Click any key** on the keyboard to play the microtonal note. The note's frequency follows `C4 × 2^(step / N)` where N is the chosen EDO and step is the position in the octave.
3. **Pick the synth voice** — sine for pure tones, sawtooth for a buzzy synth lead, etc.
4. **Toggle effects** — Reverb and Distortion apply to the synth voice; the Arpeggiator cycles the held notes rhythmically.
5. **Build a beat** — select a drum preset, set the rhythm length, then click drum-pad cells to toggle steps on/off. Press **Play Drum Machine** to start.

There is **no computer-keyboard mapping** — the keys are mouse/touch only.

## How to run

The page is a single static HTML file with Tone.js loaded from a CDN. Two options:

**Live demo (easiest):** visit https://themicrotonalkeyboard.netlify.app/

**Run from disk:** open `index.html` in any modern browser. No build, no install.

**Run from a local server (optional):**

```bash
python -m http.server 8000
# then open http://localhost:8000
```

The local server is only needed if your browser is fussy about opening files directly.

## What is EDO?

An equal division of the octave is a tuning system that divides the octave (a 2:1 frequency ratio) into N equal steps. Standard Western tuning is **12-EDO** — 12 equal semitones per octave, where each step is exactly 100 cents wide (1200 ÷ 12 = 100).

Microtonal EDOs split the octave into more (or fewer) notes:

| EDO | Steps per octave | Step size | Notes |
|---|---|---|---|
| 5 | 5 | 240¢ | Whole-tone scale |
| 12 | 12 | 100¢ | Standard Western |
| 17 | 17 | ~70.6¢ | 17 equal temperament |
| 19 | 19 | ~63.2¢ | 19 equal temperament (close to meantone) |
| 22 | 22 | ~54.5¢ | 22 equal temperament |
| 24 | 24 | 50¢ | Quarter-tones (essential for Arabic maqam music) |
| 31 | 31 | ~38.7¢ | 31 equal temperament (close to quarter-comma meantone) |
| 53 | 53 | ~22.6¢ | 53 equal temperament (very close to Pythagorean/just) |

Switching between EDOs while playing is a quick way to hear how the same harmonic relationships sound in different tuning contexts.

## Files

```
index.html       # the full app (UI, CSS, JS, Tone.js loaded from CDN)
LICENSE          # MIT
```

## Credits

- Audio: [Tone.js](https://tonejs.github.io/) (MIT)
- Author: [Zaher Alkaei](https://github.com/zaheralkaei)

## Project

- **Source / issues:** [github.com/zaheralkaei/the-microtonal-keyboard](https://github.com/zaheralkaei/the-microtonal-keyboard)

## License

MIT. See [LICENSE](LICENSE).
