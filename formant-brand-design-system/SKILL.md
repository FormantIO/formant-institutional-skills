---
name: formant-brand-design-system
description: Formant brand design system — colors, typography, and UI component patterns. Use when building UI, writing CSS, implementing components, or making design decisions for Formant applications.
metadata:
  tags: formant, brand, design, colors, typography, ui, components, css
  audience: user
trigger: When building UI components, writing CSS/styles, choosing colors or fonts, or implementing interface patterns for Formant
---

# Formant Brand Design System

Colors, typography, and UI component patterns for Formant's "Systems Architect" aesthetic. Deep Command base, atmospheric accents, precision typography.

## Color System

Every color references a quality of light, terrain, or industrial precision — grounding the brand in the physical world it serves.

### Primary Neutrals — 70–80% of Usage

| Name | Hex | CSS Variable | Usage |
|------|-----|-------------|-------|
| Deep Command | `#0A0F11` | `--deep-command` | Backgrounds, base layer |
| Slate Mist | `#202428` | `--slate-mist` | Cards, secondary surfaces |
| Formant White | `#F2F3F4` | `--formant-white` | Primary text, headlines |
| System Neutral | `#A3ABA9` | `--system-neutral` | Body text, captions |

### Atmospheric Accents — 40–60% of Usage

| Name | Hex | CSS Variable | Usage |
|------|-----|-------------|-------|
| Fog Green | `#4B5E53` | `--fog-green` | Borders, dividers, muted accents |
| Ethereal Teal | `#2C4142` | `--ethereal-teal` | Active states, panels |
| Horizon Glow | `#ACC3B3` | `--horizon-glow` | Primary CTAs, interactive elements |

### Functional UI Accents — Under 5% of Usage

| Name | Hex | CSS Variable | Usage |
|------|-----|-------------|-------|
| Terminal Amber | `#E8AB7F` | `--terminal-amber` | Warnings, eyebrow text, labels |
| Interface Iris | `#8B8CF4` | `--interface-iris` | AI states, system intelligence |

### CSS Variables Block

```css
:root {
  --deep-command: #0A0F11;
  --slate-mist: #202428;
  --formant-white: #F2F3F4;
  --system-neutral: #A3ABA9;
  --fog-green: #4B5E53;
  --ethereal-teal: #2C4142;
  --horizon-glow: #ACC3B3;
  --terminal-amber: #E8AB7F;
  --interface-iris: #8B8CF4;
}
```

### Common Translucent Patterns

- Borders: `rgba(163,171,169,0.1)` (System Neutral at 10%)
- Card hover: `rgba(44,65,66,0.2)` (Ethereal Teal at 20%)
- Fog Green muted: `rgba(75,94,83,0.3)`
- Amber subtle bg: `rgba(232,171,127,0.1)`
- Iris subtle bg: `rgba(139,140,244,0.1)`

## Typography

Three typefaces, each with a distinct role.

### Font Stack

| Role | Family | Weights | Key Properties |
|------|--------|---------|---------------|
| Display / Headlines | `'Space Grotesk', sans-serif` | 300, 500, 600, 700 | Tracking: −0.02em to 0.08em |
| Body / Interface | `'Inter', sans-serif` | 300, 400, 500, 600 | Leading: 1.65 – 1.80 |
| Monospace / Data | `'JetBrains Mono', monospace` | 300, 400, 500 | Tracking: 0.05em – 0.25em |

### Google Fonts Import

```css
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Space+Grotesk:wght@300;400;500;600;700&family=JetBrains+Mono:wght@300;400;500&display=swap');
```

### Type Scale

| Level | Size | Font | Weight | Tracking | Color |
|-------|------|------|--------|----------|-------|
| Display | `clamp(32px, 5vw, 96px)` | Space Grotesk | 300 | −0.02em | `--formant-white` |
| H1 | `clamp(24px, 3vw, 52px)` | Space Grotesk | 500 | −0.02em | `--formant-white` |
| H2 | `clamp(20px, 2vw, 32px)` | Space Grotesk | 500 | default | `--formant-white` |
| H3 | `20px` | Space Grotesk | 600 | default | `--horizon-glow` |
| Body | `16px` | Inter | 400 | default | `--system-neutral` |
| Caption | `12px` | JetBrains Mono | 400 | 0.1em, uppercase | `--fog-green` |
| Eyebrow | `10–11px` | JetBrains Mono | 400 | 0.2–0.3em, uppercase | `--terminal-amber` |

### Hierarchy Pattern

Eyebrows use JetBrains Mono 10px in Terminal Amber with wide letter-spacing and uppercase. Headlines use Space Grotesk 600. Body uses Inter 400 at 14–16px. Captions/meta use JetBrains Mono 10px in Fog Green.

## UI Component Patterns

### Buttons

```css
/* Base button */
.btn {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 12px 24px;
  border-radius: 3px;
  font-family: 'Inter', sans-serif;
  font-size: 13px;
  font-weight: 500;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  cursor: pointer;
  border: none;
  transition: all 0.2s;
}

/* Primary — Horizon Glow bg, Deep Command text */
.btn-primary { background: var(--horizon-glow); color: var(--deep-command); }
.btn-primary:hover { background: var(--formant-white); }

/* Secondary — transparent with Horizon Glow border */
.btn-secondary { background: transparent; border: 1px solid rgba(172,195,179,0.4); color: var(--horizon-glow); }
.btn-secondary:hover { border-color: var(--horizon-glow); background: rgba(172,195,179,0.08); }

/* Ghost — transparent with System Neutral border */
.btn-ghost { background: transparent; border: 1px solid rgba(163,171,169,0.2); color: var(--system-neutral); }
.btn-ghost:hover { border-color: var(--system-neutral); color: var(--formant-white); }

/* Accent — Terminal Amber bg for alerts/warnings */
.btn-accent { background: var(--terminal-amber); color: var(--deep-command); }
.btn-accent:hover { background: #f0c090; }
```

### Status Tags

```css
.tag {
  display: inline-flex;
  align-items: center;
  padding: 4px 12px;
  border-radius: 2px;
  font-family: 'JetBrains Mono', monospace;
  font-size: 11px;
  letter-spacing: 0.1em;
  text-transform: uppercase;
}

.tag-mist { background: rgba(75,94,83,0.3); color: var(--horizon-glow); border: 1px solid rgba(75,94,83,0.4); }
.tag-teal { background: rgba(44,65,66,0.4); color: var(--horizon-glow); border: 1px solid rgba(44,65,66,0.6); }
.tag-amber { background: rgba(232,171,127,0.1); color: var(--terminal-amber); border: 1px solid rgba(232,171,127,0.25); }
.tag-iris { background: rgba(139,140,244,0.1); color: var(--interface-iris); border: 1px solid rgba(139,140,244,0.25); }
```

### System Alerts

```css
.alert {
  display: flex;
  align-items: flex-start;
  gap: 12px;
  padding: 14px 16px;
  border-radius: 3px;
  font-size: 13px;
}

/* Info — Ethereal Teal, Horizon Glow text */
.alert-info { background: rgba(44,65,66,0.3); border: 1px solid rgba(44,65,66,0.6); color: var(--horizon-glow); }

/* Warning — Terminal Amber */
.alert-warning { background: rgba(232,171,127,0.08); border: 1px solid rgba(232,171,127,0.2); color: var(--terminal-amber); }

/* AI/Iris — Interface Iris */
.alert-iris { background: rgba(139,140,244,0.08); border: 1px solid rgba(139,140,244,0.2); color: var(--interface-iris); }
```

Alert dots: 6px circle with the matching accent color, `flex-shrink: 0`, `margin-top: 4px`.

### Form Inputs

```css
.form-label {
  font-family: 'JetBrains Mono', monospace;
  font-size: 10px;
  color: var(--system-neutral);
  letter-spacing: 0.15em;
  text-transform: uppercase;
  margin-bottom: 6px;
  display: block;
}

.form-input {
  background: var(--deep-command);
  border: 1px solid rgba(163,171,169,0.2);
  border-radius: 3px;
  padding: 12px 16px;
  color: var(--formant-white);
  font-family: 'Inter', sans-serif;
  font-size: 14px;
  width: 100%;
  outline: none;
  transition: border-color 0.2s;
}

.form-input::placeholder { color: rgba(163,171,169,0.5); }
.form-input:focus { border-color: var(--horizon-glow); }
```

### Cards & Surfaces

- Card background: `var(--slate-mist)` or `var(--deep-command)`
- Card border: `1px solid rgba(163,171,169,0.1)`
- Card border-radius: `4px`
- Card padding: `28px 32px`
- Card hover: `background: rgba(44,65,66,0.2)`

### Data Display — Terminal Style

Use JetBrains Mono 13px with `line-height: 2.2`. Header row uses System Neutral with `letter-spacing: 0.1em`. Field names in Fog Green, values in Formant White, status values in their semantic color (Horizon Glow, Interface Iris, or Terminal Amber).

## General Design Principles

- Border radius is always `3px` or `4px` — never rounded/pill except for avatar badges
- Transitions are `0.2s` for interactive states
- Minimal ornamentation, maximum signal
- Deep Command is the base layer — data is the primary light source
- Use translucent backgrounds over solid fills for layered depth
