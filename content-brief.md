# 4TECH — Editorial Engineering Website

Complete reusable build prompt, reference analysis, and factual content brief.

Prepared for the owner-selected **hosted Higgsfield website**. The standalone HTML variant at the end is an alternative delivery format, not the primary architecture.

## What the reference image is doing

The reference succeeds through one clear composition: a quiet editorial masthead, a tightly controlled headline, a single black action button, and two monumental hands reaching into the page. The hands create the visual drama; the navigation, paragraph, and small supporting details stay restrained.

- **Composition:** A centered text column sits above a horizontal, edge-to-edge illustration. The reaching hands converge on an empty central gap rather than touching. This negative space is essential. It makes the idea of human intention meeting technology immediately legible.
- **Material:** Warm paper, black ink, and a halftone screen create an editorial print effect. Use two scales of texture: a very quiet page-level dot matrix and much denser, locally varied halftone shading inside the hands. A uniform dot overlay alone will not reproduce the image.
- **Hierarchy:** The headline carries most of the typographic weight. The supporting paragraph is narrow, the call to action is compact, and the navigation is visually subordinate. The screenshot uses a condensed bold headline; this brief intentionally uses the owner's specified **DM Serif Display** for a more literary, premium interpretation.
- **Contrast:** Paper occupies most of the first screen. Black is reserved for type, the main button, detailed illustration shadows, and the dark sections farther down the page. Avoid turning every element into a bordered card.
- **Motion:** The composition should feel composed before it moves. Use restrained reveals, small button movements, subtle hand parallax, and a brief counter animation. Do not rotate the integrated-system illustration, spin the page, add a custom cursor, or force an intro sequence.
- **Brand adaptation:** Preserve this visual grammar, not the reference brand name, company logos, or implied endorsements. The result must clearly belong to an independent engineering practice called 4TECH.

---

## Copy-ready implementation prompt

You are an elite editorial designer, product designer, accessibility-minded front-end engineer, and motion designer. Build and publish a complete, responsive website for **4TECH**, an independent engineering practice led by **Mohammed Vashir** in Kalpakkam, Tamil Nadu, India.

The owner has selected a **hosted Higgsfield website**. Build in the platform's supported hosted React architecture, using its existing project scaffold and deployment workflow. Where that scaffold uses React 19 and TanStack Start, retain those conventions. Do not replace the hosted scaffold with Next.js or introduce a second framework. Use ordinary CSS, semantic HTML rendered by React, and small, purpose-built interactions. Google Fonts is the only external visual dependency required. Do not add an animation library or a 3D renderer to achieve effects that CSS and a small amount of JavaScript can handle well.

Deliver the complete working site, not a screenshot, wireframe, unfinished template, or collection of disconnected components. Keep the original 4TECH site and repository intact. This is a new hosted editorial presentation; publishing it does not automatically replace the existing domain, migrate customer data, or activate a new authentication backend.

### 1. The design idea

Create **engineering on paper**: a premium, monochrome editorial website that feels like a design magazine printed on textured newsprint. Draw from the supplied reference's hands, generous negative space, halftone shading, quiet masthead, and strong central typography. Aim for the discipline of an established design publication rather than generic startup software styling.

The entire palette must be black, white, warm off-white, and gray. **No red, blue, purple, gold, colored emojis, rainbow gradients, colored illustrations, or colored brand logos.** The paper tone is the owner's requested `#F5F5F0`. Small tonal gradients are acceptable; colored gradients are not.

Do not use the founder's photo anywhere on the public site. The current founder image setting is empty by intent. Do not infer permission to expose an image from an owner library or a previously supplied photograph. Use typography and technical illustration in the founder section.

### 2. Factual boundaries

Use the real company, founder, contacts, capabilities, and project stages in this prompt. The studio is an independent engineering initiative led by a second-year undergraduate; do not describe it as a 40-person established enterprise.

Do not invent client logos, customer relationships, revenue, years in business, project delivery totals, awards, certifications, testimonials, published papers, performance numbers, production deployments, or regulatory approvals.

Specifically omit the illustrative claims "250+ Projects Delivered," "98% Client Retention," "40+ Team Members," and "12 Years Experience." Do not present Mercury, Ramp, HEX, Vercel, Descript, Cash App, Supercell, or Runway as customers. Do not fabricate NovaPay, HealthSync, DataForge, or quotes from James Rodriguez, Sarah Kim, or Michael Park. Replace those template sections with the real engineering work and working principles provided below.

Keep development stages visible. A proposed research concept is not a completed device. CAD work is not a built robotic arm. An unvalidated PCB is not manufacturing-ready. Sensor readings are not a certified safety claim. Present these distinctions clearly and concisely without flooding the interface with disclaimers.

Do not use "easy project," "mini project," "basic project," or beginner electronics demonstrations in the main portfolio. The public positioning is: **Advanced Engineering · Robotics · Embedded Systems · RF Technology · Automation · Research & Development.**

Use the plain `4TECH` wordmark. Add a registered-trademark superscript only if the owner supplies evidence that registration applies; do not invent registration status as a decoration.

### 3. Design tokens and typography

Define a coherent token system:

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

Load **DM Serif Display** and **Inter**, weights 300, 400, 500, 600, and 700, through Google Fonts. Include sensible serif and sans-serif fallback stacks. Use `font-display: swap` and appropriate preconnects. Do not wait for a font to load before showing readable content.

- Wordmark: Inter, 700, 20px, uppercase.
- Main heading: DM Serif Display, `clamp(48px, 7vw, 86px)`, line-height 1.08, letter-spacing -1px.
- Section titles: DM Serif Display, `clamp(36px, 4.5vw, 56px)`, line-height 1.15.
- Card titles: DM Serif Display, 22px, comfortable wrapping.
- Stat numbers: DM Serif Display, 48px.
- Body and main supporting paragraphs: Inter 400, 17px, line-height 1.7, `--text-secondary`.
- Card copy: Inter 400, 14px, line-height about 1.7.
- Section kickers: Inter 600, 12px, uppercase, letter-spacing 3px.
- Buttons: Inter 500, 14px.

### 4. Paper and halftone texture

Set the body background to `#F5F5F0`, enable antialiased font smoothing, and prevent incidental horizontal overflow without masking broken layouts.

Use a fixed `body::before` or equivalent fixed decorative layer that covers the viewport:

```css
body::before {
  content: "";
  position: fixed;
  inset: 0;
  pointer-events: none;
  z-index: 0;
  opacity: .3;
  background-image: radial-gradient(rgb(208, 208, 203) 1px, transparent 1px);
  background-size: 12px 12px;
}
```

### 5. Header and mobile navigation

Fixed navigation, transparent → glassmorphism on scroll > 50px.

- Left: `4TECH` + Services, About, Work, Contact (32px gaps)
- Right: Login → `https://4tech-9cy.pages.dev/account` + Start a Project ↗ → #contact
- Mobile (<768px): hamburger → full-screen overlay with serif links

### 6. Hero — the defining composition

- Kicker: **INDEPENDENT ENGINEERING · KALPAKKAM, INDIA**
- Headline: **Technology That / Shapes Tomorrow.**
- Subtitle: **We turn engineering ideas into purposeful prototypes—connecting embedded systems, robotics, and RF research with practical, hands-on development.**
- CTA: **Explore Our Work ↗** → #work + **Start a conversation** → #contact
- Visual: SVG robotic hand (left) + human hand (right), halftone rendered, ~160-unit fingertip gap

### 7. Capability strip

- Label: **Engineering across disciplines.**
- Items: Embedded Systems · Robotics · RF Systems · Automation · Electronics · IoT · Simulation · Prototyping

### 8. Services — six cards

Label: **WHAT WE DO** / Title: **Ideas, engineered into something tangible.**

1. **Embedded Systems** — "Connect sensors, controllers, and interfaces through practical firmware and hardware integration."
2. **Robotics & Motion** — "Explore mechanisms, kinematics, and control strategies with mechanical design and computational studies."
3. **RF & Instrumentation** — "Develop experimental approaches to antenna measurement, signal acquisition, and repeatable technical observation."
4. **IoT & Automation** — "Bring device state, environmental observations, and control workflows into clear, usable interfaces."
5. **Prototype Development** — "Translate a project brief into components, design decisions, milestones, and reviewable engineering work."
6. **Practical Learning** — "Build understanding through guided work with microcontrollers, simulation, electronics, and system integration."

### 9. About — the person and the practice

Label: **WHY 4TECH** / Title: **Engineer by study. Builder by instinct.**

Founder: Mohammed Vashir, B.Tech EEE, B.S. Abdur Rahman Crescent Institute. Second-year undergraduate · Vandalur, Tamil Nadu.

Buttons: Explore My Portfolio ↗ → `https://4tech-9cy.pages.dev/portfolio` + View Résumé → `https://4tech-9cy.pages.dev/resume`

Fact grid (catalogue facts, not delivery claims):
- **4** — Featured engineering workstreams
- **3** — Core skill disciplines
- **15** — Portfolio records, including proposed research
- **1** — Independent founder

Skills: ESP32, Arduino Nano, I²C, SPI, UART · C, Arduino C++, Python, MATLAB · SOLIDWORKS, KiCad, inverse kinematics, neural-network modelling

### 10. Selected work — four projects

Label: **SELECTED WORK** / Title: **Questions worth building for.**

View All → `https://4tech-9cy.pages.dev/projects`

| # | Project | Domain | Stage | URL |
|---|---------|--------|-------|-----|
| 1 | Automated Antenna Radiation Pattern Measurement System | RF / Automation | Prototype development | /projects/antenna |
| 2 | Advanced Robotic Arm Systems | Robotics / Mechanical / Computation | CAD & computational studies | /projects/robot-arm |
| 3 | ESP32 Drone Platform | PCB / Embedded | Engineering development | /projects/drone |
| 4 | SewerSense | IoT / Environmental sensing | Hardware integration | /projects/sewersense |

#### Full project catalogue (15 records)

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

### 11. Working principles (replaces testimonials)

Label: **HOW WE WORK** / Title: **Clear thinking. Reviewable progress.**

1. **Define the question** — "Clarify the problem, constraints, and intended outcome before selecting components or promising a result."
2. **Make progress visible** — "Break the work into reviewable stages, document decisions, and distinguish a concept from a tested subsystem."
3. **Leave understanding behind** — "Explain the design, share the relevant documentation, and make the next development step clear."

### 12. Contact CTA

Label: **LET'S BUILD** / Heading: **Ready to Build Something Extraordinary?**

- WhatsApp: `https://wa.me/919360108408`
- Email: `mailto:mohammedvashir75@gmail.com`
- Location: Kalpakkam, Tamil Nadu 603102 · India

### 13. Footer

Four-column grid (2fr 1fr 1fr 1fr):

- **Brand:** 4TECH wordmark + description
- **Explore:** Services, About, Selected Work, Contact
- **More from 4TECH:** Project Library, Founder Portfolio, Résumé, Customer Login
- **Connect:** Location + social icons (WhatsApp, GitHub, LinkedIn, Instagram, Reddit, Email)

Social links:
- WhatsApp: `https://wa.me/919360108408`
- GitHub: `https://github.com/4techno`
- LinkedIn: `https://www.linkedin.com/in/mohammed-vashir-793b89378/`
- Instagram: `https://www.instagram.com/_.herculex._/`
- Reddit: `https://www.reddit.com/user/mohammedvashir75/`
- Email: `mailto:mohammedvashir75@gmail.com`

Bottom: © 2026 4TECH. All rights reserved. Privacy → `https://4tech-9cy.pages.dev/privacy`

---

## Content provenance

- Founder education and skill groups: `4tech-next/lib/profile.ts`
- Project names, classifications, stages, validation limits: `4tech-next/lib/projects.ts`
- Contact destinations and founder image setting: `4tech-next/config.js`
- Records current as of 29 September 2026
