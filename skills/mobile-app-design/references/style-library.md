# Style Library (General + BI/Analytics Dashboard)

Use this library when selecting visual direction in Stage C.

## Usage Rules
- Always pick **exactly one General Style** for core product direction.
- If analytics/dashboard is in scope, also pick **exactly one Dashboard Style**.
- Document why the chosen style helps task completion (not only aesthetics).
- Keep interaction clarity and accessibility above stylistic effects.

---

## A) General Styles

Each entry: **Name — Intent | Best for | Mobile adaptation**

1. **Minimalism & Swiss Style** — clarity-first | enterprise, docs, dashboards | strict grid, strong type hierarchy, one-column mobile rhythm.
2. **Neumorphism** — soft tactile look | wellness, meditation | use only on key surfaces (cards/buttons), preserve contrast.
3. **Glassmorphism** — premium layered depth | modern SaaS, finance | limit blur and provide low-end fallback.
4. **Brutalism** — raw expressive impact | portfolio, art | bold type/contrast but maintain touch targets.
5. **3D & Hyperrealism** — immersive showcase | gaming, hero product views | restrict to focal elements; keep base UI simple.
6. **Vibrant & Block-based** — energetic clarity | startup, creative | use controlled accent blocks and clear CTA hierarchy.
7. **OLED Dark** — low-light efficiency | coding, night-heavy usage | tonal surfaces, avoid flat pure-black walls.
8. **Accessible & Ethical** — inclusion-first | gov, health, education | prioritize readability, plain language, robust states.
9. **Claymorphism** — playful soft depth | kids, edu, light SaaS | simplify depth on small screens.
10. **Aurora UI** — atmospheric gradients | modern SaaS, creative | keep gradients in hero/header; guard text contrast.
11. **Retro-Futurism** — nostalgic-future blend | gaming, entertainment | keep retro cues thematic, not structural.
12. **Flat Design** — straightforward speed | product MVPs | strong state affordances to avoid ambiguity.
13. **Skeuomorphism** — familiar metaphors | niche premium, legacy patterns | use selectively for meaning-rich objects.
14. **Liquid Glass** — luxury translucency | premium SaaS/ecom | reduce transparency for readability.
15. **Motion-Driven** — narrative through motion | storytelling flows | keep durations functional (150–300ms typical).
16. **Micro-interactions** — precision feedback | touch-heavy apps | use press/loading/success patterns with haptics if relevant.
17. **Inclusive Design** — broad usability | public services, education | larger controls, tolerant input patterns.
18. **Zero Interface** — invisible interaction | voice/ambient systems | always keep visual fallback controls.
19. **Soft UI Evolution** — modern enterprise softness | enterprise SaaS | subtle depth with conservative palette.
20. **Neubrutalism** — geometric bold personality | startup, youth products | keep information density controlled.
21. **Bento Grid** — modular scannability | dashboard, product overview | mobile: stacked modules with progressive disclosure.
22. **Y2K Aesthetic** — nostalgic pop | fashion, youth media | confine to brand layer; protect readability.
23. **Cyberpunk UI** — dramatic high-tech accents | gaming, crypto | neon as accent only, never for body text.
24. **Organic Biophilic** — trustful natural tone | wellness, sustainability | natural palette + clean content scaffolding.
25. **AI-Native UI** — conversation-first utility | AI assistants/chat products | sticky input, streaming states, source/citation affordances.
26. **Memphis Design** — playful geometry | youth, creative apps | reduce pattern density on phone layouts.
27. **Vaporwave** — synth nostalgia art direction | music, entertainment | use sparingly as thematic layer.
28. **Dimensional Layering** — strong depth hierarchy | complex content apps | limit to 2–3 elevation levels.
29. **Exaggerated Minimalism** — sparse luxury focus | premium commerce/editorial | heavy whitespace with explicit CTA anchoring.
30. **Kinetic Typography** — text-led impact | hero storytelling | avoid animating long body copy.
31. **Parallax Storytelling** — scroll narrative depth | launches, brand stories | subtle-only on mobile.
32. **Swiss Modernism 2.0** — precise editorial modernity | corporate/editorial apps | strong heading rhythm and clarity.
33. **Sci-Fi HUD/FUI** — instrument-panel visual language | sci-fi, security | simplify density for usability.
34. **Pixel Art** — retro digital personality | indie, gaming | keep icon/text scale integer-like for consistency.
35. **Spatial UI (VisionOS-inspired)** — depth-first interaction cues | spatial concepts | provide clear 2D mobile fallback.
36. **E-Ink / Paper** — reading-first calm | publishing, long-form reading | high readability and low visual noise.
37. **Gen Z Chaos / Maximalism** — intentional overload energy | youth/media | maintain strict hierarchy despite visual intensity.
38. **Biomimetic / Organic 2.0** — science + organic blend | biotech, health | retain data clarity and trust cues.
39. **Anti-Polish / Raw Aesthetic** — authentic roughness | artist brands | rough visual treatment, clean interaction model.
40. **Tactile Digital / Deformable UI** — physically responsive touch feel | playful mobile brands | short, performant deformation interactions.
41. **Nature Distilled** — refined natural minimal | wellness, sustainability | soft palette with restrained components.
42. **Interactive Cursor Design** — pointer personality | desktop-heavy web | usually not primary for touch-only mobile.
43. **Voice-First Multimodal** — speech + visual hybrid | assistant, accessibility-driven apps | large mic control + robust text fallback.
44. **3D Product Preview** — inspect-before-buy | e-commerce product detail | lazy-load models, always offer image fallback.
45. **Aurora Mesh** — evolved gradient mesh atmosphere | modern brand surfaces | use overlays to maintain text contrast.
46. **Editorial Grid / Magazine** — editorial content hierarchy | media, publication | one-column mobile with strong heading cadence.
47. **Chromatic Aberration / RGB Split** — glitch-tech accent | music, gaming | accent-only usage, never body text.
48. **Vintage Analog / Retro Film** — nostalgic warmth | photo/music storytelling | avoid grain under body text.
49. **Data-App Neutral** — restrained product baseline | internal tools, productivity apps | neutral-first tokens + clear status semantics.

---

## B) BI/Analytics Dashboard Styles

Use these when dashboard/analytics scope exists.

1. **Data-Dense Dashboard** — maximize information while preserving scanability.
   - Best for: operations/product analytics with many KPIs.
   - Mobile adaptation: focus panel per KPI cluster, bottom-sheet filters, progressive lists.

2. **Heatmap Dashboard** — rapid intensity and distribution insights.
   - Best for: geo, behavior, time-slot intensity.
   - Mobile adaptation: larger cells, tap tooltip, always show numeric legend.

3. **Executive Dashboard** — concise decision summary.
   - Best for: weekly/monthly leadership review.
   - Mobile adaptation: KPI brief mode + top insight card.

4. **Real-Time Monitoring** — live status and anomaly detection.
   - Best for: DevOps, logistics, IoT.
   - Mobile adaptation: critical alerts first, compact sparklines, actionable notifications.

5. **Drill-Down Analytics** — overview to root-cause exploration.
   - Best for: investigating metric changes.
   - Mobile adaptation: tap-to-expand detail, sticky mini breadcrumb.

6. **Comparative Analysis Dashboard** — side-by-side segment/period comparison.
   - Best for: A/B and trend comparisons.
   - Mobile adaptation: A/B toggle, highlight deltas with consistent axes.

7. **Predictive Analytics** — forecast with uncertainty visibility.
   - Best for: demand/risk/planning.
   - Mobile adaptation: default one forecast horizon + expandable assumptions.

8. **User Behavior Analytics** — funnel, cohort, retention behavior.
   - Best for: product growth and UX optimization.
   - Mobile adaptation: emphasize highest drop-off and actionable segment cards.

9. **Financial Dashboard** — financial health and risk tracking.
   - Best for: accounting, treasury, unit economics.
   - Mobile adaptation: quick-glance highlights, on-demand detailed drill.

10. **Sales Intelligence Dashboard** — pipeline and quota performance guidance.
    - Best for: CRM and sales operations.
    - Mobile adaptation: daily brief + next-best-action card.

---

## C) Naming Normalization (Canonical)

Use canonical naming below to avoid conflicts:
- `Bento Box Grid` / `Bento Grids` → **Bento Grid**
- `Heat Map & Heatmap Style` → **Heatmap Dashboard**
- `Dark Mode (OLED)` → **OLED Dark**
- `HUD / Sci-Fi FUI` → **Sci-Fi HUD/FUI**
- `Gradient Mesh / Aurora Evolved` → **Aurora Mesh**
