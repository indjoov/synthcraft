# Contributing to SynthCraft

Thank you for your interest in contributing to SynthCraft! Whether you're adding effects, improving accessibility, creating presets, or fixing bugs — every contribution helps make music creation more accessible.

---

## Code of Conduct

This project follows the [Contributor Covenant Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/).

---

## How Can I Contribute?

### 🐛 Report a Bug
Open an issue with steps to reproduce, expected vs. actual behavior, and browser/OS info.

### 💡 Suggest a Feature
Open an issue describing the problem, your proposed solution, and any alternatives.

### 🎛️ Add a New Preset
See the "Adding a Preset" section below.

### ♿ Improve Accessibility
Accessibility is a core value. If you find barriers, please report or fix them.

### 📝 Improve Documentation
Documentation PRs are always welcome.

---

## Getting Started

1. Fork the repository
2. Clone your fork: `git clone https://github.com/YOUR-USERNAME/synthcraft.git`
3. Install dependencies: `npm install`
4. Create a branch: `git checkout -b feature/your-feature`
5. Start the dev server: `npm run dev`

---

## Accessibility Guidelines

All contributions must meet these standards:

1. **Large touch targets** — no controls smaller than 44x44px
2. **Keyboard navigation** — every control reachable via Tab
3. **Screen reader support** — ARIA labels, roles, and states
4. **Color contrast** — WCAG 2.1 AA (4.5:1 for text)
5. **Motion** — respect the reducedMotion setting
6. **No tiny knobs** — use sliders with visible tracks and thumbs

---

## Adding a Preset

Add an entry to the `PRESETS` array in `synthcraft-tuner.jsx`:

```javascript
{
  name: "Your Preset",
  icon: "🎵",
  osc: "sawtooth",        // sine, square, sawtooth, triangle
  filterCutoff: 1200,     // 20–8000 Hz
  filterQ: 2,             // 0.1–20
  attack: 0.01,           // 0.005–2 seconds
  decay: 0.2,             // 0.01–2 seconds
  sustain: 0.7,           // 0–1
  release: 0.3,           // 0.01–3 seconds
  lfoRate: 0,             // 0–20 Hz
  lfoDepth: 0,            // 0–1000
  lfoTarget: "filter",    // "filter" or "pitch"
  gain: 0.5,              // 0–1
}
```

---

## Questions?

Open an issue or start a discussion. Thank you for helping make SynthCraft better! 🎹
