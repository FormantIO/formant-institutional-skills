---
name: formant-brand-icons
description: Formant brand icon library — 20 purpose-built icons with usage rules, sizing, and color guidelines. Use when working with icons in Formant UI or marketing materials.
metadata:
  tags: formant, brand, icons, svg, ui
  audience: user
trigger: When selecting, sizing, or implementing icons in Formant UI or marketing materials
---

# Formant Brand Icon Library

20 purpose-built icons representing the core concepts of Formant's physical AI vocabulary. Each icon is drawn at 64x64 on a 2px stroke grid — precise, open, and built to breathe in context.

## Icon Set

| File | Name | Category |
|------|------|----------|
| `01-physical-agent.svg` | Physical Agent | Core concept |
| `02-fleet.svg` | Fleet | Core concept |
| `03-mission.svg` | Mission | Core concept |
| `04-guardrail.svg` | Guardrail | Safety |
| `05-the-brain.svg` | The Brain | Architecture |
| `06-context.svg` | Context | Architecture |
| `07-the-interface.svg` | The Interface | Architecture |
| `08-anomaly.svg` | Anomaly | Warning |
| `09-resolution.svg` | Resolution | Status |
| `10-telemetry.svg` | Telemetry | Data |
| `11-blueprint.svg` | Blueprint | Planning |
| `12-digital-twin.svg` | Digital Twin | Core concept |
| `13-operator.svg` | Operator | People |
| `14-horizon.svg` | Horizon | Vision |
| `15-command.svg` | Command | Action |
| `16-propagate.svg` | Propagate | Action |
| `17-fde.svg` | FDE | People |
| `18-alarm.svg` | Alarm | Warning |
| `19-savings.svg` | Savings | Outcome |
| `20-bounded-autonomy.svg` | Bounded Autonomy | Core concept |

## Format & Grid

- **Format:** SVG — scalable at any resolution
- **ViewBox:** 64x64
- **Stroke weight:** 2px
- **Linecap:** round
- **Style:** Open stroke, no fill. Do not fill or outline in UI contexts — keep them open and atmospheric.
- **Usage:** Use inline SVG for color theming, or as `<img>` for static contexts.

## Color Rules

| Context | Color | Variable |
|---------|-------|----------|
| Default / standard icons | Horizon Glow (`#ACC3B3`) | `--horizon-glow` |
| Warning icons (Anomaly, Alarm, Guardrail) | Terminal Amber (`#E8AB7F`) | `--terminal-amber` |
| AI/intelligence states | Interface Iris (`#8B8CF4`) | `--interface-iris` |
| Muted/secondary | System Neutral (`#A3ABA9`) | `--system-neutral` |

## Size Scale

| Size | Use Case |
|------|----------|
| 16px | Inline text |
| 24px | UI labels |
| 32px | Buttons |
| 48px | Cards |
| 64px | Feature blocks |
| 96px | Hero sections |

## Icon Source

All icon SVG files are located in the `/public/` directory of the `formant-style-guide` repository at `https://github.com/FormantIO/formant-style-guide`.
