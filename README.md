# 🎛️ Strudel Flow

> A visual node-based interface for creating music with [Strudel](https://strudel.cc) — drag, connect, and compose without writing code.

![Stars](https://img.shields.io/github/stars/xyflow/strudel-flow?style=flat-square) ![License](https://img.shields.io/badge/License-AGPL--3.0-blue?style=flat-square) ![React Flow](https://img.shields.io/badge/Built%20with-React%20Flow-purple?style=flat-square)

---

## What is this?

Strudel Flow is a visual programming environment for [Strudel](https://strudel.cc) — the browser-based live coding music language. Instead of writing pattern code by hand, you build music by connecting nodes in a drag-and-drop graph.

Connect an instrument node to an effects node to an output node, tweak the knobs, and hear your pattern come to life — all in the browser, no installation needed.

**Based on** the open source [strudel-flow](https://github.com/xyflow/strudel-flow) project by xyflow.

---

## Features

- 🎹 **Instrument nodes** — Piano, synths, samples, drums
- 🎛️ **Effect nodes** — LPF, distortion, gain, pan, phaser, room, jux, crush, FM, ADSR and more
- ⏱️ **Time modifier nodes** — Fast, slow, reverse, palindrome, mask, ply, late
- 🎵 **Pattern nodes** — Polyrhythm, pad sequencer, chords (I ii iii IV V vi vii°)
- 🔗 **Visual connections** — Drag nodes to connect them, React Flow powered graph
- 💾 **Save & Load** — Persist your patches locally
- ⚡ **Live output** — Generates and plays Strudel code in real time

---

## Getting Started

### Run locally

```bash
git clone https://github.com/YOUR_USERNAME/my-strudel-flow.git
cd my-strudel-flow
npm install
npm run dev
```

Open [http://localhost:5173](http://localhost:5173)

### Or try the live demo

👉 [xyflow.com/strudel-flow](https://xyflow.com/strudel-flow)

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| UI Framework | React + Vite |
| Node Graph | [React Flow](https://reactflow.dev) |
| Music Engine | [Strudel](https://strudel.cc) |
| Styling | Tailwind CSS + shadcn/ui |
| Language | TypeScript |

---

## Node Types

### Instrument Nodes
Produce sound — connect to effect nodes or directly to output.

| Node | Description |
|------|-------------|
| Synths | Select from Strudel's synth waveforms |
| Pad | Grid-based note sequencer |
| Polyrhythm | Multi-voice euclidean rhythm builder |

### Audio Effect Nodes
Chain these together to shape your sound.

| Node | Strudel function |
|------|----------------|
| LPF | `.lpf()` — low-pass filter |
| Distortion | `.distort()` — waveshaper |
| Gain | `.gain()` — volume |
| Pan | `.pan()` — stereo position |
| Phaser | `.phaser()` — phaser effect |
| Room | `.room()` — reverb |
| Jux | `.jux(rev)` — stereo widening |
| Crush | `.crush()` — bit crusher |
| PostGain | `.postgain()` — post-fx gain |
| FM | `.fm()` — FM synthesis |

### Time Modifier Nodes
Change how patterns unfold over time.

| Node | Strudel function |
|------|----------------|
| Fast | `.fast()` |
| Slow | `.slow()` |
| Reverse | `.rev()` |
| Palindrome | `.palindrome()` |
| Mask | `.mask()` |
| Ply | `.ply()` |
| Late | `.late()` |
| ADSR | `.attack().decay().sustain().release()` |

### Harmony Nodes
| Node | Description |
|------|-------------|
| Chords | I ii iii IV V vi vii° — Roman numeral chord selector with major/minor/diminished |

---

## Usage Guide

1. **Add a node** — drag from the left panel onto the canvas
2. **Connect nodes** — drag from an output handle to an input handle
3. **Configure** — expand the Controls panel on any node to adjust parameters
4. **Listen** — audio plays automatically as you build
5. **Save** — use the Save button to persist your patch

---

## Development

```bash
npm run dev      # Start dev server
npm run build    # Build for production
npm run lint     # Run ESLint
```

---

## Roadmap

- [ ] More instrument node types (MIDI input, custom samples)
- [ ] Export generated Strudel code to clipboard
- [ ] Preset library — save and share patches
- [ ] Integration with sheet-music-to-strudel for importing transcriptions
- [ ] Mobile-friendly touch interface
- [ ] Collaborative editing

---

## Credits

- Original project: [strudel-flow](https://github.com/xyflow/strudel-flow) by [xyflow](https://github.com/xyflow)
- Music engine: [Strudel](https://strudel.cc) by Felix Roos & contributors
- Node graph: [React Flow](https://reactflow.dev) by xyflow

---

## License

AGPL-3.0 — see [LICENSE](LICENSE) for details.

If you modify and deploy this publicly, you must make your source code available under the same license.
