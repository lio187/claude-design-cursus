# Raycast / Alfred Snippets Library — Claude Design Cursus (187N Edition)

> Voor during-opname quick-paste. Import deze snippets in Raycast (Cmd+Space → "Create Snippet") of Alfred (Preferences → Features → Snippets → +).
>
> **Keyword pattern:** `:cd-[context]-[variant]` — zo vind je ze snel in Raycast search.
>
> **Installatie-tip:** elk snippet-naam moet beginnen met `:cd-` voor grouping in Raycast.

---

## 🔹 LES 1 — Design MD Interview

### `:cd-interview` — De 5-vragen prompt (Les 1 Manier 1)

```
Stel me 5 vragen om een design.md te bouwen voor mijn brand. Vraag één voor één, wacht op mijn antwoord, schrijf dan een complete design.md met tabellen, hex codes, typography recommendations, en referenties.

1. Merknaam + wat doe je?
2. 3 woorden die je merk beschrijven (geen "premium, unique" — echte woorden)
3. Kleuren die voelen als jouw merk (hex codes of beschrijvingen die ik kan vertalen)
4. 3 merken die je bewondert + WAT je van elk wilt (typography / palette / motion / layout)
5. Tone — formeel / speels / direct / poëtisch / tech / luxe?

Na mijn antwoorden: schrijf een complete design.md met alle secties ingevuld, gebaseerd op mijn input. Gebruik tabellen, geen paragrafen. Wees specifiek met hex codes en font recommendations.
```

### `:cd-187n-answers` — Pre-scripted antwoorden voor live demo

```
Antwoorden voor de 5 vragen (als 187N.AI):
1. 187N.AI. Enterprise AI infrastructure agency uit Amsterdam. We deployen AI agents voor bedrijven die klaar zijn met experimenteren — full-stack, containerized, gemaintained.
2. Apple-minimalism. Terminal-precision. Builder-to-builder.
3. Pure black #000 (background), wit #fff (text), Liquid Glass cards (rgba(255,255,255,0.01) + backdrop-blur + gradient border ring). Emerald #6ee7a0 ALLEEN voor operational dots en active states. Threat red #f87171 alleen voor errors.
4. Vercel voor tech-clarity en minimalism. Linear voor motion-precision en rhythm. Stripe voor typography-discipline. Plus Apple.com voor Liquid Glass treatment.
5. Builder-to-builder Nederlands. Numbers en specifics. Geen consulting-speak — "je deployed", "zero headaches". Italic accent-woord max 1 per headline in Instrument Serif.
```

### `:cd-187n-designmd` — 187N DESIGN.md paste (voor Claude Design Additional Notes)

```
# 187N.AI — Design System Reference

## Colors (strict HSL systeem)
- Background #000000 pure black (NIET #050a08 of off-black)
- Foreground #ffffff wit
- Card hsl(0 0% 9%)
- Muted-foreground hsl(0 0% 75%)
- Border hsl(0 0% 20%)
- Emerald #6ee7a0 — ALLEEN voor operational dots + active states
- Threat red #f87171 — ALLEEN voor error/alarm states

## Typography
- Barlow (300-700) — body, headings, CTA labels
- Instrument Serif (regular + italic) — max 1 italic accent-woord per headline + ALLE numbers/metrics
- JetBrains Mono (400, 500) — section labels UPPERCASE tracking 0.32em, timestamps, agent IDs, status pills

## Signature effects
- .liquid-glass: bg rgba(255,255,255,0.01), backdrop-blur 4px, gradient border ring via ::before mask-composite xor
- .liquid-glass-strong: blur 50px, rgba(255,255,255,0.02), stronger ring
- .grid-overlay: 72×72px, opacity 0.03, radial mask naar center
- .op-dot: 6px emerald met box-shadow glow
- .pulse-dot: opacity pulse 1.6s infinite
- .tier-glow: emerald pulse box-shadow 3s (populair pricing tier)
- .hero-bg: radial 1000px 600px at 50% -10% white/8%

## Motion
- fade-up 800ms cubic-bezier(0.2, 0.8, 0.2, 1), stagger words
- breathing-pulse 6s (logo)
- pulse-dot 1.6s
- btn-hover scale 1.03

## Atmospheric layer
- Higgsfield MP4 full-bleed in hero (autoplay muted loop + dark gradient overlay)
- Grid-overlay + 2 radial white-blur orbs
- GEEN matrix rain, GEEN floating "1 8 7 N" chars (oude versie weg)

## Border radius
- Default 2px, cards 1rem (16px), featured 1.5rem (24px), CTAs en pills 9999px

## Voice
Nederlandse builder-to-builder. Numbers over vagueness. Max 1 italic accent per headline. Mono voor alles tech.
```

---

## 🔹 LES 2 — Plan Mode + Variants

### `:cd-planmode` — Plan Mode prompt addition

```
[Your main prompt here]

Ask me any questions before you begin. Give me 5 to 14 questions covering content, style, palette, UI density, mood, interactivity, inspiration, and any edge cases I haven't thought about.

When it comes to colors, typography and animation — use my design.md (attached in Additional Notes).
```

### `:cd-variants` — Variants request

```
Before you commit to one direction: give me 2 variants that are completely different in visual approach — not just color-swaps, but different layout rhythm, different hero treatment, different typography pairing.

Label them Variant A and Variant B with 1 line each describing the core difference.

Show me just the hero + one body section of each so I can pick.
```

---

## 🔹 LES 3 — One-Pager

### `:cd-187n-onepager` — 187N One-Pager prompt (condensed voor demo)

```
Bouw de complete single-page marketing site voor 187N.AI — een Amsterdam-based enterprise AI infrastructure agency. EÉN continuous scroll-driven page met 11 secties + 2 video-interludes. Feel: Apple-minimalism, terminal-precision, builder-to-builder.

UPLOAD: 187N infinity-loop logo uit ~/Downloads/ai.svg in Additional Files.

BRAND strict (matcht onze pitch deck + mobile portal):
- Background #000 pure black, foreground #fff, card hsl(0 0% 9%), muted hsl(0 0% 75%), border hsl(0 0% 20%)
- Emerald #6ee7a0 ALLEEN voor op-dots en active states
- Threat red #f87171 ALLEEN voor error states
- Fonts: Barlow (body 300-700), Instrument Serif (accent italic + numbers), JetBrains Mono (tech labels)
- Signature: Liquid Glass cards (backdrop-blur + gradient border ring via ::before mask-composite xor)
- Grid-overlay 72×72px + radial white-blur orbs als atmospheric layer

11 SECTIES (alles Nederlands):
1. HERO — Higgsfield MP4 video background full-bleed + dark gradient overlay. Headline Barlow 500 clamp(40px, 8vw, 72px) "AI Agents Die Je Volgende Hire Overbodig Maken." (woord "Volgende Hire" in Instrument Serif italic). Sub Barlow regular muted. Twee CTAs: solid wit rounded-full "Bekijk Wat Mogelijk Is →" + liquid-glass-strong "Meer Weten". Metrics row 3: 10-20u / 24/7 / 30 Dagen (Instrument Serif italic numbers). "Built with" rij onder: Claude · OpenClaw · Codex · Telegram (mono opacity 50%). Eyebrow mono 11px tracking 0.32em "ENTERPRISE AI INFRASTRUCTUUR".
2. COMMAND CENTER — "Jouw Enterprise Command Center." (Command Center italic). Liquid-glass-strong dashboard mockup: chrome (3 cirkels + path) + stats row 5 cards + sidebar 7 items + active agents lijst + activity feed right column scroll-masked.
3. MP4 INTERLUDE — full-bleed Higgsfield video (negative margin, heavy top/bottom fade naar black).
4. PROBLEM — "Krachtig om te deployen. Gevaarlijk om fout te deployen." (Gevaarlijk italic). 4 threat cards liquid-glass rounded-xl (341 Malicious Skills / CVE Data Extraction / RCE Code Injection / SC Supply Chain) met threat-red THREAT label + pulsing red dot. Advisory liquid-glass-strong blok + pull quote OpenClaw.
5. SECURITY — "Enterprise-grade security. Geen bijzaak." (Geen bijzaak italic). Liquid-glass-strong diagram card: 3 gestapelde layers (Network Firewall / Docker Container / OpenClaw Instance) met verbindingslijntjes. 4 mono badges onder: EXEC ALLOWLISTS · MALICIOUS SKILL VETTING · FIREWALL RULES · AIR-GAP READY.
6. MP4 INTERLUDE — tweede full-bleed Higgsfield video.
7. BUILT FOR — "Voor operators die schalen. Niet voor hobbyisten." (Niet italic). 4 cards grid liquid-glass rounded-2xl: Online Bedrijven (bag) / Service Bedrijven (briefcase) / Teams 4-50+ (users) / Security-Bewust (shield) — met mono 0X label + titel + body.
8. HOW IT WORKS — "Drie stappen. Volledig gedeployed. Zero headaches." (Zero headaches italic). 3 horizontale rijen liquid-glass: groot Instrument Serif italic 5xl-7xl nummer 01/02/03 links + mono week-label + titel + body (Week 1 Discovery / Week 2-3 Architectuur / Week 4 Handoff).
9. PRICING — "Eenmalige investering. Oneindig rendement. Geen abo." (Geen abo italic). 3 tier cards. Middelste Multi-Department = liquid-glass-strong + tier-glow + -mt-4 lift + wit "Populair" pill bovenop (mono tracking-widest 10px).
10. RESULTATEN — "Resultaten die harder praten dan pitch decks." 3 grote metric cards met Instrument Serif italic 7xl numbers: 20u / 24/7 / 30 Dagen.
11. TEAM — 3 portret-cards aspect-[3/4] liquid-glass: Leon Ghatas (Founder), Damian Schneider (CEO), Trevor Onueseke (COO). Grayscale foto + gradient-to-b overlay + mono 01/02/03 corner tag + naam + rol mono muted.
12. FAQ — "Everything you need to know before you deploy." Accordion rows liquid-glass.
13. FINAL CTA — "Klaar om te Deployen?" Full-bleed. Solid wit CTA + groene pulsing dot "accepteert nu 2 nieuwe deployments voor Q2 · 2026". Contact footer hello@187n.ai · Amsterdam × Dubai · @187n.

NAVIGATION fixed top: liquid-glass pill-container + 5 nav links (Security / Proces / Pricing / Team / FAQ) + CTA rechts.

SIGNATURE: Liquid Glass alle cards. Grid-overlay + radial orbs atmosphere. fade-up 800ms cubic-bezier reveals. Geen matrix rain, geen floating "1 8 7 N" chars — clean modern Apple-minimalism.

Ask me any questions before you begin.
```

---

## 🔹 LES 4 — Mobile + Deck

### `:cd-187n-mobile` — 187N Client Portal Mobile (8 screens)

```
Bouw een interactieve mobile app prototype voor 187N.AI — een client portal die enterprise AI operators gebruiken om hun deployed agents te monitoren. Format: iPhone 15 Pro viewport (393x852). 8 schermen met echte transitions.

BRAND (matcht onze website + pitch deck):
- Background #000, foreground #fff, card hsl(0 0% 9%), muted hsl(0 0% 75%), border hsl(0 0% 20%)
- Emerald #6ee7a0 ALLEEN voor op-dots + active states (niet dominant)
- Threat red #f87171 ALLEEN voor error states
- Fonts: Barlow (body), Instrument Serif (accent italic + numbers), JetBrains Mono (status pills, timestamps, IDs)
- Signature: Liquid Glass alle cards + inputs, gradient border ring via ::before
- Border-radius default 2px, cards 1rem
- Max 1 italic accent per headline

DE 8 SCHERMEN:
1. SPLASH — 187N infinity logo breathing pulse 6s + "187N.AI" wordmark Barlow semibold + mono tagline "COMMAND CENTER · ENTERPRISE AI INFRASTRUCTUUR" tracking 0.32em. Grid-overlay + radial orbs.
2. LOGIN — Logo small top. Headline "Welkom terug." (terug italic Instrument Serif). Liquid-glass inputs email + password. Solid wit rounded-full "Sign In" CTA.
3. DASHBOARD — Header + greeting "Goedemorgen, Leon". 3 metric cards grid: AGENTS 12 / UPTIME 14d 6u / TASKS 47 (Instrument Serif italic numbers). Section "Active Agents" mono 11px. 5 agent-rows met status pills (RUNNING emerald / IDLE muted).
4. AGENTS LIST — Filter chips horizontal (Alle · Running · Queued · Error). 8 agent cards liquid-glass rounded-xl: mono AGT-ID top-left, status pill top-right, Barlow medium naam, muted body, mono last-run timestamp.
5. AGENT DETAIL — Back + naam header. Tabs Overview / Logs / Config (actieve onderstreept emerald 2px). Logs tab: terminal-style JetBrains Mono 12px, emerald timestamps, threat-red ERROR lines, shimmer bottom band. 10 realistische logs.
6. ACTIVITY STREAM — Header + mono filter "Vandaag · 42 events". Pull-to-refresh chevron top. 10 events: mono timestamp (now/2m/28m/1u) + agent badge + Barlow event text.
7. CHAT — Header "187N Team". Threaded messages: user rechts (emerald-border liquid-glass bubbles), team links (muted bubbles). 6 Nederlandse messages. Quick-reply chips row. Input bottom met send-icon.
8. SETTINGS — Profile card: avatar + "Leon Ghatas" + email + plan badge "MULTI-DEPARTMENT · €10K–€15K" emerald tint mono. 6 setting rows liquid-glass (Account / Billing / Integrations / Security / Notifications / Logout) met chevron right.

BOTTOM NAV (schermen 3-8): 5 tabs Dashboard / Agents / Activity / Chat / Settings. SVG Lucide icons, mono 10px labels, actieve tab emerald dot + full opacity. Schermen 1-2 GEEN bottom nav.

TRANSITIONS: fadeUp 250ms, haptic-feel tap (scale 0.98), Liquid Glass hover subtle.

Alles Nederlands, geen emojis. Ask me any questions before you begin.
```

### `:cd-187n-deck` — 187N Agency Vision Deck (10 slides)

```
Bouw een 10-slide agency vision deck voor 187N.AI. Export .pptx + .pdf. 16:9 per slide (1920×1080).

HARD GUARDRAILS: GEEN client names. GEEN traction cijfers ("X klanten", "€Y ARR"). Vision-only.

UPLOAD: 187N logo uit ~/Downloads/ai.svg in Additional Files.

BRAND strict (matcht website + mobile portal):
- Background #000 pure black, foreground #fff, card hsl(0 0% 9%), muted hsl(0 0% 75%), border hsl(0 0% 20%)
- Emerald #6ee7a0 ALLEEN voor op-dots en populair-tier pulse
- Threat red #f87171 ALLEEN voor error/alarm states
- Fonts: Barlow (body 300-700), Instrument Serif (accent italic + ALLE cijfers), JetBrains Mono (11px tracking 0.32em UPPERCASE voor micro-labels)
- Signature: Liquid Glass cards + grid-overlay 72×72px + radial orbs
- Max 1 italic accent per headline
- Border-radius default 2px, cards 1rem / 1.5rem

10 SLIDES (alles Nederlands, elke slide: mono micro-label → H2 met italic accent → content):

1. COVER — Micro "ENTERPRISE AI INFRASTRUCTUUR". Headline "AI Agents Die Je Volgende Hire Overbodig Maken." (Volgende Hire italic). Sub over full-stack AI deployment. 3 metric cards (10-20u / 24/7 / 30 Dagen) Instrument Serif italic. "Built with" rij mono: Claude · OpenClaw · Codex · Telegram. Logo top-left.
2. HET PROBLEEM — "Krachtig om te deployen. Gevaarlijk om fout te deployen." 4 threat cards liquid-glass: 341 Malicious Skills / CVE Data Extraction / RCE Code Injection / SC Supply Chain (threat-red THREAT labels + pulsing dots). Advisory blok liquid-glass-strong met rood "!" April 2026 (Microsoft/CrowdStrike/CyberArk). Pull quote over OpenClaw 247k stars.
3. COMMAND CENTER — "Jouw Enterprise Command Center." (Command Center italic). Liquid-glass-strong dashboard mockup: chrome (3 cirkels + path + op-dot + "all systems operational") + stats row 5 cards + sidebar 7 items + Active Agents lijst 5 agents + Activity feed right scroll-masked.
4. SECURITY — "Enterprise-grade security. Geen bijzaak." (Geen bijzaak italic). 3-layer diagram liquid-glass-strong: 01 Network Firewall / 02 Docker Container / 03 OpenClaw Instance (increasing indent). 4 mono badges: EXEC ALLOWLISTS · MALICIOUS SKILL VETTING · FIREWALL RULES · AIR-GAP READY.
5. GEBOUWD VOOR — "Voor operators die schalen. Niet voor hobbyisten." (Niet italic). 4 cards grid liquid-glass rounded-2xl: Online Bedrijven (bag) / Service Bedrijven (briefcase) / Teams 4-50+ (users) / Security-Bewust (shield) — elk met mono 0X label + titel + body.
6. HOE HET WERKT — "Drie stappen. Volledig gedeployed. Zero headaches." (Zero headaches italic). 3 horizontale rijen liquid-glass: groot Instrument Serif italic 7xl 01/02/03 + mono week-label (WEEK 1 / WEEK 2-3 / WEEK 4) + Barlow medium titel + body (Discovery & Scope / Architectuur & Deployment / Handoff & Training).
7. RESULTATEN — "Resultaten die harder praten dan pitch decks." 3 grote metric cards liquid-glass-strong: 20u / 24/7 / 30 Dagen (Instrument Serif italic 7xl).
8. PRICING — "Eenmalige investering. Oneindig rendement. Geen abo." (Geen abo italic). 3 tier cards. Middelste Multi-Department (€10-15K) = liquid-glass-strong + tier-glow emerald pulse + -mt-4 lift + wit "Populair" pill bovenop (mono tracking-widest 10px). Prijzen in Instrument Serif italic 5xl.
9. HET TEAM — "Het Team" (Team italic). 3 portret-cards aspect-[3/4] liquid-glass: Leon Ghatas (Founder) / Damian Schneider (CEO) / Trevor Onueseke (COO). Grayscale foto + gradient-to-b overlay + mono 01/02/03 corner tag.
10. FINAL CTA — Micro "DEPLOY · SCALE · SECURE". Gigantische "Klaar om te Deployen?" (Deployen italic). Solid wit CTA "Bekijk Wat Mogelijk Is →" rounded-full px-10 py-4. Onder button: mono + groene pulsing dot "accepteert nu 2 nieuwe deployments voor Q2 · 2026". Contact footer hello@187n.ai · Amsterdam × Dubai · Instagram @187n.

Slide transitions fade 200ms. Numbers count-up on enter. Print-ready 1920×1080 per slide.

Ask me any questions before you begin.
```

---

## 🔹 LES 5 — Hero Video (Operator Command Scene)

### `:cd-nanobanana-187n` — Nano Banana Pro 187N still

```
Cinematic hero image voor 187N.AI — "Operator Command Scene": één humanoid AI operator figure in de zwarte controle-omgeving van een enterprise AI infrastructuur agency. Feel: Apple keynote hardware-reveal meets Blade Runner 2049.

COMPOSITION: 16:9 aspect ratio. FULL-BLEED zwart ops-center scene — geen gereserveerde dead-space zone (headline gaat over-top via CSS overlay, niet in-frame).

CENTERPIECE: één humanoid operator figure (wireframe chrome outline, face silhouet, Apple-clean hardware aesthetic) geplaatst in een zwarte enterprise ops-omgeving. Positioned center-right in frame, lichte 3/4 angle. De figure voelt premium en deliberate — niet cute, niet dystopian — pure controlled precision.

ENVIRONMENT: minimalistic infrastructure room met subtle vertical light-pillars op afstand (rack-panels suggestie), zeer minimal, very sparse. Grote negatieve ruimte helpt het subject isoleren. Geen rommel, geen cables, geen machinery.

LIGHTING: primary cool-white rim-light vanaf links die de figure outlines definieert. Secondary subtle warm under-light from below (tungsten accent) voor cinematic contrast. Dark ambient fill.

COLORS strict (geen emerald dominance, geen cyan): Pure black #000000 canvas, deep neutral chrome #1a1a1a - #333333 voor operator figure, off-white #ffffff voor subtle specular highlights, minimal warm amber #ffc266 accent alleen als sparingly under-light. NO emerald, NO cyan, NO purple, NO heavy color grading.

SURFACE DETAIL: operator figure heeft zichtbare maar rustige surface details — lichte matte chrome texture, subtle body-geometry definition zonder overdreven robot-features. Face silhouet leesbaar maar zonder identiteit.

ATMOSPHERE: zeer subtiele fine film-grain (analog noise), dust particles alleen in depth (3-5 total max), vage horizontal scan-lines 0.04 opacity (cinematic display feel zonder overdrive).

STYLE: Apple product keynote shot meets cinematic thriller still. Mystery through restraint. Premium hardware reveal.

OUTPUT: 1920x1080 PNG hi-res. No text, no baked logos, no watermarks, no UI overlays.
```

### `:cd-seedance-187n` — Seedance 2.0 motion

```
8-second animation van de "Operator Command Scene" voor 187N.AI.

GEEN rotation. GEEN 360 spin. Operator blijft stabiel in-place.

CAMERA: z-axis only — eerste 4s subtiele dolly back (reveal meer van de environment), laatste 4s gentle push-in (operator wordt intiemer in frame). NOOIT yaw. NOOIT sideways pan.

OPERATOR: blijft in positie throughout. Subtle motions only:
- Hoofd beweegt zeer traag (head-tilt 2 graden) rond 3s
- Hand komt langzaam omhoog rond 5s alsof iets wordt bestudeerd
- Ademhaling-suggestie — subtle shoulder rise/fall op 4s cycle

RIM-LIGHT: zeer subtle breathing (intensiteit 0.95 → 1.0 → 0.95 op 4s cycle) — living-quality zonder flicker.

ENVIRONMENT: achtergrond vertical light-pillars flicker zeer zeldzaam (1 flicker elke 3-4 seconden, één pillar per keer, 200ms). Film-grain constant, particles drift zeer langzaam.

SCAN-LINES: constant subtle 0.04 opacity + één bright scan-band sweep elke 5s (bottom-to-top 600ms) — cinematic display refresh feel.

FRAMING: operator stays center-right throughout. Ruimte voor headline overlay (CSS) blijft usable — motion mag niet aggressive zijn rond de text-zone.

PACING: zeer traag, meditatief. Dit is een observation, niet een action-shot. 24fps cinematic grade.

OUTPUT: 16:9 1920x1080, 8 seconden, MP4 H.264. Seamless loop (start en eind-frame matchen in mood + operator positie).

CRITICAL: Enhance Prompt UIT. Gebruik mijn prompt letterlijk. GEEN 360 rotation. GEEN yaw. GEEN pan. GEEN tilt. GEEN lens flares. GEEN fade-to-white. GEEN facial features die opeens verschijnen. Elegance through restraint — Apple-grade minimalism.
```

### `:cd-mp4swap` — MP4 swap prompt voor Claude Design

```
Can we swap the still image for the video I just uploaded? Keep everything else identical (layout, text, CTAs, colors). Video should autoplay, muted, loop seamlessly. On mobile: fall back to the original still image for data savings.
```

---

## 🔹 LES 6 — /build-page Handoff

### `:cd-buildpage` — /build-page trigger

```
/build-page

Input: Claude Design export (paste the handoff-prompt Claude Design gave me below)

Build this as a NextJS 15+ App Router project with:
- TypeScript strict mode
- Tailwind CSS 4
- Framer Motion for scroll-driven animations (smoothEase + fade-up stagger)
- next/font for Barlow (300-700) + Instrument Serif (regular + italic) + JetBrains Mono (400, 500)
- Mobile-first (test 375px first)
- Respect prefers-reduced-motion
- Lighthouse target 95+

Signature CSS classes to implement in globals.css:
- .liquid-glass: rgba(255,255,255,0.01), backdrop-blur(4px), gradient border ring via ::before mask-composite xor
- .liquid-glass-strong: blur(50px), rgba(255,255,255,0.02), stronger ring
- .grid-overlay: 72×72px grid, 3% opacity, radial-masked
- .op-dot + .pulse-dot: 6px emerald #6ee7a0 met glow shadow
- .tier-glow: emerald pulse box-shadow 3s infinite
- .hero-bg: radial 1000px 600px at 50% -10% white/8%

Reference files in project root:
- design.md (brand tokens — kleuren #000/#fff/#6ee7a0, typografie, Liquid Glass, animaties — VASTGELEGD)
- CLAUDE.md (webapp blueprint — volg de build-regels)

After scaffold: localhost:3000 should render the page. Then I run /deploy-site.

--- Claude Design handoff prompt below ---

[PLAK HIER DE HANDOFF-PROMPT]
```

---

## 🔹 LES 7 — Command Center Run

### `:cd-187n-run` — Full /design-command-center orchestration

```
/design-command-center

Client: 187N-AI (self)
Input: 187N DESIGN.md (paste in Additional Notes) + logo ai.svg

OUTPUTS — all 3:
1. One-pager site (11 sections)
2. Mobile client portal (8 screens)
3. Agency vision deck (10 slides, vision-only, NO client names, NO traction)

ORCHESTRATION:
- Generate 3 Claude Design prompts (site, mobile, deck)
- Paste each in new Claude Design chat
- Export all 3 back to Claude Code
- /build-page → NextJS scaffold for site
- /deploy-site → GitHub + Vercel (187n-web)
- Bundle mobile shareable link + deck .pptx in /delivery/187n/

Target: live URL + mobile preview + .pptx in 30 minutes.
```

---

## 🔹 CLAUDE CODE QUICK COMMANDS

### `:cd-clear` — Clear Claude Code terminal (tussen lessen)

```
clear
```

(Plus: `/clear` apart in Claude Code chat voor context clearing.)

---

## 🔹 RECAP — Tijdens opname

### `:cd-recap-site` — Recap zin voor Les 6 einde

```
Totaal tijd: ongeveer 10 minuten van design naar live URL. Zonder deze stack? 2 tot 3 dagen minimum.
```

### `:cd-recap-agency` — Recap zin voor Les 7 einde

```
Jouw tijd per bundle: 30 minuten. Marge: 90% plus. One-time, geen subscriptions. Eén solo operator: €30 tot 50K per maand.
```

---

## Installatie in Raycast

1. Cmd+Space → "Snippet" → Create
2. Name: `CD-[snippet name]`
3. Keyword: `:cd-[context]` (match patroon hierboven)
4. Content: paste uit deze file
5. Save

**Pro tip:** groepeer alle `:cd-` snippets in één category in Raycast voor makkelijk overzicht.

---

*Raycast Snippets — Claude Design Cursus — 187N Live-Build Edition — Lio The AI Operator*
