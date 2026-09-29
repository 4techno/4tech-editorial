# 4TECH Editorial Website — Content Brief & Design Specification

> Complete reusable build prompt, reference analysis, and factual content brief.
> Prepared for the owner-selected hosted Higgsfield website.

---

## What the Reference Image Is Doing

The reference succeeds through one clear composition: a quiet editorial masthead, a tightly controlled headline, a single black action button, and two monumental hands reaching into the page. The hands create the visual drama; the navigation, paragraph, and small supporting details stay restrained.

- **Composition:** A centered text column sits above a horizontal, edge-to-edge illustration. The reaching hands converge on an empty central gap rather than touching. This negative space is essential.
- **Material:** Warm paper, black ink, and a halftone screen create an editorial print effect. Use two scales of texture: a very quiet page-level dot matrix and much denser, locally varied halftone shading inside the hands.
- **Hierarchy:** The headline carries most of the typographic weight. The supporting paragraph is narrow, the call to action is compact, and the navigation is visually subordinate.
- **Contrast:** Paper occupies most of the first screen. Black is reserved for type, the main button, detailed illustration shadows, and the dark sections farther down the page.
- **Motion:** The composition should feel composed before it moves. Use restrained reveals, small button movements, subtle hand parallax, and a brief counter animation.
- **Brand adaptation:** Preserve this visual grammar, not the reference brand name, company logos, or implied endorsements.

---

## Factual Boundaries

Use the real company, founder, contacts, capabilities, and project stages. The studio is an independent engineering initiative led by a second-year undergraduate; do not describe it as a 40-person established enterprise.

**Do not invent:**
- Client logos, customer relationships, revenue, years in business
- Project delivery totals, awards, certifications, testimonials
- Published papers, performance numbers, production deployments
- Regulatory approvals

**Specifically omit:**
- "250+ Projects Delivered," "98% Client Retention," "40+ Team Members," "12 Years Experience"
- Mercury, Ramp, HEX, Vercel, Descript, Cash App, Supercell, Runway as customers
- NovaPay, HealthSync, DataForge, or quotes from fictional people

---

## Design Tokens

```css
:root {
  --bg-primary: #f5f5f0;
  --bg-dark: #0a0a0a;
  --bg-card: #ffffff;
  --text-primary: #1a1a1a;
  --text-secondary: #6b6b6b;
  --text-light: #999999;
  --text-white: #ffffff;
  --accent: #000000;
  --border: #e0e0e0;
  --ease-editorial: cubic-bezier(.4, 0, .2, 1);
}
```

---

## Typography System

- **Fonts:** DM Serif Display + Inter (300–700) via Google Fonts
- **Wordmark:** Inter, 700, 20px, uppercase
- **Hero Headline:** DM Serif Display, clamp(48px, 7vw, 86px), line-height 1.08
- **Section Titles:** DM Serif Display, clamp(36px, 4.5vw, 56px), line-height 1.15
- **Body Text:** Inter 400, 17px, line-height 1.7
- **Card Copy:** Inter 400, 14px
- **Kicker Labels:** Inter 600, 12px, uppercase, letter-spacing 3px
- **Buttons:** Inter 500, 14px

---

## Section Architecture

### 1. Navigation
- Fixed, transparent → glassmorphism on scroll
- Left: 4TECH + Services, About, Work, Contact
- Right: Login (→ https://4tech-9cy.pages.dev/account) + Start a Project ↗
- Mobile: hamburger → full-screen overlay

### 2. Hero
- Kicker: INDEPENDENT ENGINEERING · KALPAKKAM, INDIA
- Headline: "Technology That Shapes Tomorrow."
- Subtitle: "We turn engineering ideas into purposeful prototypes—connecting embedded systems, robotics, and RF research with practical, hands-on development."
- CTA: Explore Our Work ↗ + Start a conversation
- Visual: SVG robotic hand (left) + human hand (right), halftone rendered

### 3. Capability Strip
- Label: "Engineering across disciplines."
- Items: Embedded Systems · Robotics · RF Systems · Automation · Electronics · IoT · Simulation · Prototyping

### 4. Services (6 cards)
1. Embedded Systems
2. Robotics & Motion
3. RF & Instrumentation
4. IoT & Automation
5. Prototype Development
6. Practical Learning

### 5. About (dark section)
- Founder: Mohammed Vashir, B.Tech EEE, B.S. Abdur Rahman Crescent Institute
- Location: Kalpakkam, Tamil Nadu
- Factual metrics: 4 workstreams, 3 disciplines, 15 portfolio records, 1 founder
- Links: Portfolio, Résumé

### 6. Selected Work (4 projects)

| Project | Domain | Stage |
|---------|--------|-------|
| Antenna Radiation Pattern System | RF / Automation | Prototype development |
| Advanced Robotic Arm Systems | Robotics / Mechanical | CAD & computational studies |
| ESP32 Drone Platform | PCB / Embedded | Engineering development |
| SewerSense | IoT / Environmental | Hardware integration |

### 7. Working Principles (replaces testimonials)
1. Define the question
2. Make progress visible
3. Leave understanding behind

### 8. Contact CTA
- Heading: "Ready to Build Something Extraordinary?"
- WhatsApp: https://wa.me/919360108408
- Email: mohammedvashir75@gmail.com
- Location: Kalpakkam, Tamil Nadu 603102, India

### 9. Footer
- Social: WhatsApp, GitHub (4techno), LinkedIn, Instagram, Reddit, Email
- Links: Services, About, Work, Contact, Project Library, Portfolio, Résumé, Login
- © 2026 4TECH. All rights reserved.

---

## Full Project Catalogue

| Difficulty | Project | Slug | Stage |
|---|---|---|---|
| Research Level | Automated Antenna Radiation Pattern Measurement System | antenna | Prototype development |
| Research Level | Passive RF Drone Detection Receiver | passive-rf-drone | Proposed R&D concept |
| Research Level | RF Direction Finder | rf-direction-finder | Proposed R&D concept |
| Research Level | Autonomous Disaster Rescue Vehicle | rescue | Proposed R&D concept |
| Research Level | AR Heads-Up Display Goggles | ar-hud | Proposed R&D concept |
| Research Level | Wireless EV Charging System | power | Lower-power design study |
| Research Level | Magnetic Anomaly Detector | magnetic-anomaly | Proposed R&D concept |
| Advanced | Advanced Robotic Arm Systems | robot-arm | CAD & computational studies |
| Advanced | ESP32 Drone Platform | drone | Engineering development |
| Advanced | Autonomous Vision Tracking Platform | vision-tracking | Proposed R&D concept |
| Advanced | RF Shielding / Faraday Cage System | rf-shielding | Proposed R&D concept |
| Advanced | Composite Material Drop-Test System | composite-drop-test | Proposed R&D concept |
| Advanced | Digital Night-Vision Monocular | night-vision | Proposed R&D concept |
| Intermediate | SewerSense | sewersense | Hardware integration |
| Intermediate | Desktop Wind Tunnel | wind-tunnel | Proposed R&D concept |

---

## Contact & Links

- **Site:** https://4tech-9cy.pages.dev
- **Customer Login:** https://4tech-9cy.pages.dev/account
- **Portfolio:** https://4tech-9cy.pages.dev/portfolio
- **Résumé:** https://4tech-9cy.pages.dev/resume
- **Projects:** https://4tech-9cy.pages.dev/projects
- **Privacy:** https://4tech-9cy.pages.dev/privacy
- **WhatsApp:** https://wa.me/919360108408
- **GitHub:** https://github.com/4techno
- **LinkedIn:** https://www.linkedin.com/in/mohammed-vashir-793b89378/
- **Instagram:** https://www.instagram.com/_.herculex._/
- **Reddit:** https://www.reddit.com/user/mohammedvashir75/
