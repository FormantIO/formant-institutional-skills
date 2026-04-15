# Formant Institutional Skills

Formant brand and institutional knowledge encoded as [Claude Code](https://claude.ai/claude-code) skills. These give Claude deep context on Formant's brand voice, design system, visual language, icons, and positioning — so it can produce on-brand work out of the box.

## Skills

| Skill | What it covers |
|-------|---------------|
| `formant-brand-voice` | Voice & tone principles, do/don't rules, brand glossary, voice samples |
| `formant-brand-design-system` | Color palette (CSS vars), typography (3 fonts + scale), buttons, tags, alerts, inputs, cards |
| `formant-brand-visual` | 4 visual pillars, photography/video direction, generative image master prompt |
| `formant-brand-icons` | 20 icon library with file names, format/grid rules, color rules, size scale |
| `formant-brand-story` | Brand positioning, Metaphysics 4-layer architecture, key statements, messaging framework |

## Installation

Copy the skill folders into your global Claude Code skills directory:

```bash
git clone https://github.com/FormantIO/formant-institutional-skills.git
cp -r formant-institutional-skills/formant-brand-* ~/.claude/skills/
```

## Usage

In any Claude Code session, invoke a skill by name:

```
/formant-brand-voice
/formant-brand-design-system
/formant-brand-visual
/formant-brand-icons
/formant-brand-story
```

## Source

These skills are derived from the [Formant Brand Style Guide](https://github.com/FormantIO/formant-style-guide) (2026).
