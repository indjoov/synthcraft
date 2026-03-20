# 🎹 SynthCraft

**An open-source, accessible subtractive synthesizer for the web.**

SynthCraft is a browser-based synthesizer built with React and the Web Audio API. It features large, accessible controls, computer keyboard mapping, preset sounds, and full accessibility support — designed so everyone can create music, regardless of ability.

Part of the **Craft Audio** family alongside [PitchCraft](https://github.com/indjoov/pitchcraft) and [DrumCraft](https://github.com/indjoov/drumcraft).

---

## ✨ Features

### 🎛️ Subtractive Synthesis Engine
- **4 waveforms**: Sine, Square, Sawtooth, Triangle
- **Lowpass filter** with cutoff (20–8000 Hz) and resonance (Q) control
- **ADSR envelope** with visual curve display — Attack, Decay, Sustain, Release
- **LFO** with adjustable rate and depth, routable to filter or pitch
- **Octave shift** control (±2 octaves)
- **Volume control** per voice

### 🎹 Keyboard
- **On-screen piano keyboard** — 17 keys (C4 to E5) with click/touch support
- **Computer keyboard mapping** — Z through M for lower octave, Q through E for upper
- **Polyphonic** — play multiple notes simultaneously
- **Visual feedback** — keys light up when pressed
- **Key labels toggle** — show/hide computer key mappings on the piano

### 🎚️ 8 Built-in Presets
| Preset | Sound Character |
|--------|----------------|
| Warm Pad | Slow attack, rich sawtooth, filtered |
| Deep Bass | Tight envelope, heavy resonance |
| Pluck | Instant attack, zero sustain |
| Wobble | LFO on filter for dubstep-style modulation |
| Organ | Sine wave with vibrato |
| Siren | LFO on pitch for sweeping effect |
| Strings | Slow attack sawtooth with subtle vibrato |
| Retro Lead | Square wave with mid resonance |

### ♿ Accessibility
- **High Contrast Mode** — increased contrast for low-vision users
- **Reduced Motion Mode** — disables all animations
- **Large Text Mode** — scales text up 25%
- **Large touch targets** — no tiny knobs, all controls are slider-based
- **Full keyboard navigation** — every control reachable via Tab
- **Screen reader support** — ARIA roles, labels, and pressed states throughout
- **Haptic feedback** — vibration on key press for supported devices
- **Color-coded sections** — Oscillator (blue), Filter (pink), Envelope (green), LFO (yellow)

---

## 🚀 Getting Started

### Prerequisites
- [Node.js](https://nodejs.org/) v18 or later
- npm or yarn

### Installation

```bash
git clone https://github.com/indjoov/synthcraft.git
cd synthcraft
npm install
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser.

### Building for Production

```bash
npm run build
```

---

## 🛠️ Tech Stack

- **React 19** — UI framework
- **Vite** — Build tool and dev server
- **Web Audio API** — Sound generation (OscillatorNode, BiquadFilterNode, GainNode)
- **Vibration API** — Haptic feedback
- **No external audio libraries** — pure Web Audio API

---

## 🎛️ Architecture

```
User Input (click/keyboard)
    ↓
OscillatorNode (sine/square/saw/triangle)
    ↓
BiquadFilterNode (lowpass, cutoff + Q)
    ↓
GainNode (ADSR envelope)
    ↓
AudioContext.destination (speakers)

LFO (OscillatorNode) → GainNode → Filter.frequency OR Oscillator.frequency
```

---

## 🗺️ Roadmap

- [ ] Effects chain (reverb, delay, distortion)
- [ ] Multiple oscillators with detuning
- [ ] MIDI input support
- [ ] Waveform scope visualization
- [ ] Save/load custom presets
- [ ] PWA support for offline use
- [ ] Recording / export to WAV
- [ ] Localization / i18n

---

## 🤝 Contributing

Contributions are welcome! Please read our [Contributing Guide](CONTRIBUTING.md) for details.

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.

---

## 🔗 Related Projects

- [PitchCraft](https://github.com/indjoov/pitchcraft) — Open-source accessible chromatic tuner
- [DrumCraft](https://github.com/indjoov/drumcraft) — Open-source accessible drum tuner

---

<p align="center">
  Made with 🎹 by <a href="https://github.com/indjoov">indjoov</a> and the SynthCraft community
</p>
