# 4TECH Editorial Website — Redesign

A monochromatic, halftone-textured editorial website for **4TECH** — an independent engineering practice led by Mohammed Vashir, specialising in embedded systems, robotics, RF research, and practical prototyping.

![Design Style](https://img.shields.io/badge/style-editorial%20monochrome-1A1A1A?style=flat-square)
![Status](https://img.shields.io/badge/status-development-6B6B6B?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-000000?style=flat-square)

---

## Overview

This repository contains a complete website redesign for 4TECH, inspired by editorial print design — think Pentagram portfolios and Bloomberg Businessweek. The defining visual identity is a **halftone dot-matrix texture**, monochrome palette, generous whitespace, and a hero illustration referencing Michelangelo's *Creation of Adam* with a robotic hand reaching toward a human hand.

### Design Principles

- **Monochrome only** — black, white, warm off-white (`#F5F5F0`), and grays. Zero colour.
- **Halftone texture** — a fixed radial-gradient dot pattern simulating newsprint across the entire viewport.
- **Editorial typography** — DM Serif Display for headlines, Inter for body text.
- **Generous whitespace** — sections breathe with 120px vertical spacing on desktop.
- **Honest content** — all project stages, skills, and claims are factual and verifiable.

---

## Repository Structure

```
4tech-editorial/
├── index.html              # Complete self-contained website
├── content-brief.md         # Full design specification & content brief
├── prompt.md                # Master build prompt for AI-assisted rebuilds
├── assets/
│   └── og-cover.svg         # Open Graph social sharing cover
├── .gitignore
├── LICENSE
└── README.md                # This file
```

---

## Quick Start

```bash
# Clone the repository
git clone https://github.com/4techno/4tech-editorial.git
cd 4tech-editorial

# Open directly in browser — no build step required
start index.html          # Windows
open index.html           # macOS
xdg-open index.html       # Linux
```

No dependencies. No build tools. No Node modules. One HTML file with inline CSS and JS.

---

## Design Tokens

| Token | Value | Usage |
|-------|-------|-------|
| `--bg-primary` | `#F5F5F0` | Page background (warm paper) |
| `--bg-dark` | `#0A0A0A` | Dark sections |
| `--bg-card` | `#FFFFFF` | Card surfaces |
| `--text-primary` | `#1A1A1A` | Headlines, primary text |
| `--text-secondary` | `#6B6B6B` | Body text, descriptions |
| `--text-light` | `#999999` | Kicker labels, muted text |
| `--accent` | `#000000` | Buttons, active states |
| `--border` | `#E0E0E0` | Card borders, dividers |

---

## Typography

| Role | Font | Weight | Size |
|------|------|--------|------|
| Wordmark | Inter | 700 | 20px |
| Hero headline | DM Serif Display | 400 | clamp(48px, 7vw, 86px) |
| Section titles | DM Serif Display | 400 | clamp(36px, 4.5vw, 56px) |
| Body text | Inter | 400 | 17px |
| Buttons | Inter | 500 | 14px |
| Kicker labels | Inter | 600 | 12px, uppercase |

---

## Sections

1. **Navigation** — Fixed glassmorphism header with scroll state
2. **Hero** — Full-viewport with SVG robotic/human hand illustration
3. **Capability Strip** — Discipline labels (not client logos)
4. **Services** — Six engineering capability cards
5. **About** — Founder profile with factual metrics
6. **Selected Work** — Four curated project cards with development stages
7. **Working Principles** — Three-column methodology (not fake testimonials)
8. **Contact CTA** — Dark rounded container with direct contact links
9. **Footer** — Four-column layout with verified links

---

## Featured Projects

| Project | Domain | Stage |
|---------|--------|-------|
| Antenna Radiation Pattern System | RF / Automation | Prototype development |
| Advanced Robotic Arm Systems | Robotics / Mechanical | CAD & computational studies |
| ESP32 Drone Platform | PCB / Embedded | Engineering development |
| SewerSense | IoT / Environmental | Hardware integration |

---

## Accessibility

- Semantic HTML5 (`<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`)
- Single `<h1>`, section `<h2>`, card `<h3>` hierarchy
- Skip-to-content link
- `aria-expanded`, `aria-controls` on mobile menu
- `prefers-reduced-motion` respected — no animation, counters show final values
- WCAG AA contrast on all essential text

---

## Contact

- **WhatsApp**: [wa.me/919360108408](https://wa.me/919360108408)
- **Email**: mohammedvashir75@gmail.com
- **GitHub**: [github.com/4techno](https://github.com/4techno)
- **LinkedIn**: [Mohammed Vashir](https://www.linkedin.com/in/mohammed-vashir-793b89378/)
- **Location**: Kalpakkam, Tamil Nadu 603102, India

---

## License

MIT License. See [LICENSE](LICENSE) for details.

---

<p align="center">
  <strong>4TECH</strong> — Independent Engineering · Kalpakkam, India
</p>
