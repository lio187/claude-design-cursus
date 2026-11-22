# 02 — LES 2: Prototype Mode — De Feedback Loop (12 min)

**Target length:** 12:00
**Shot mix:** Screen 80% / talking head 20%
**Focus:** Wireframe vs high-fi, 7-vragen loop, 4 edit-modes, live 187N hero sectie demo

---

## 0:00 — 0:30 | Les-opening (talking head)

**Dialoog bullets:**
- "Les 2. Dit is waar Claude Design echt uniek is."
- "Geen enkele andere AI design tool heeft dit."
- "De vragen-loop. Plus 4 edit-modes die het voelen als live schetsen met iemand die alles begrijpt."

**On-screen subtitle:** "Prototype Mode deep-dive"

---

## 0:30 — 1:30 | Wireframe vs High-Fidelity (talking head + screen cap)

**Talking head:**
- "Eerst: Claude Design heeft twee modes."
- "Wireframe — structuur, geen styling. Voor snelle iteratie."
- "High-fidelity — volledige design. Voor presentatie en handoff."

**Cut naar screen split:**
- Links: wireframe van 187N hero (basic boxes, grayscale)
- Rechts: high-fi van zelfde hero (full styling, 187N void black + emerald glow)

**Voice-over:**
- "Wireframe: je test layout + flow zonder dat je verliefd wordt op kleuren."
- "High-fi: als de layout klopt, upgrade je naar final styling."
- "Pro tip: start ALTIJD wireframe bij multi-page sites. Anders verspil je uren op pagina's die toch niet werken."

---

## 1:30 — 2:00 | Model selectie — Opus 4.7 default (screen)

**Cut naar Claude Design — bovenaan toont model selector**

**Voice-over:**
- "Eén ding dat veel mensen missen — bovenaan zit een model selector."
- "Default = Opus 4.7. Laat dat staan."
- "Waarom: Opus 4.7 heeft 3x hogere fidelity voor screenshots dan 4.6."
- "Sonnet alleen voor snelle wireframes. Voor echte designs: Opus 4.7."

**Screen-action:** klik op dropdown, toon opties, keer terug naar Opus 4.7.

---

## 2:00 — 3:00 | Plan Mode — de geheime prompt-techniek (screen + talking head)

**Talking head intro:**
- "Tweede geheim — plan mode in Claude Design."
- "Niet zichtbaar als knop. Het is een prompt-techniek."

**Screen-action:** in de prompt-input, type een basis prompt, en aan het einde:

```
...Ask me any questions before you begin.
```

**Voice-over:**
- "Die ene zin verandert alles."
- "Claude Design gaat 5 tot 14 vragen stellen voordat het iets bouwt."
- "Doelgroep, stijl, density, mood, content, referenties — alles."
- "Resultaat: je eerste render is bijna direct wat je wilde."
- "Bespaart je 4 revisie-rondes. En elke revisie kost quota."

**On-screen callout:** "PRO PROMPT ADDITION: 'Ask me any questions before you begin.'"

---

## 3:00 — 4:30 | De magische 7-vragen loop (live demo)

**Cut naar Claude Design (claude.ai/design) — lege chat**

**Voice-over:**
- "Hier komt de killer-feature."
- "Als ik een prompt plak — Claude Design bouwt NIET meteen."
- "Eerst stelt het 7 vragen."

**Screen-action:** plak een stripped-down versie van de 187N hero prompt (kortere versie uit dashboard):

```
Bouw de hero sectie voor 187N.AI, enterprise AI infrastructure agency.
Split layout: LEFT 40% negative space for headline, RIGHT 60% 3D infinity-loop + orbital agents scene.
Headline "AI Agents That Make Your Next Hire Irrelevant" in Halant 700, accent phrase "Your Next Hire" in emerald.
Void black #050a08 + emerald #00ff88 glow. Halant headings.
Framer Motion cascade entrance.
```

**Wacht op Claude Design's response met de vragen.**

**Voice-over bij elke vraag:**

### Vraag 1 — "Wat voor content?"
- "Marketing site — specifieker dan 'website'. Dit stuurt het systeem."

### Vraag 2 — "Stijl?"
- "Terminal-aesthetic, technical confidence — matcht design.md."

### Vraag 3 — "Kleurenpalet?"
- "USE MY DESIGN.MD — magische zin. Dit dwingt naar je tokens (void + emerald)."

### Vraag 4 — "UI dichtheid?"
- "Moderate met veel breathing room — enterprise wil nooit dense."

### Vraag 5 — "Algemene mood?"
- "Confident en technisch. Cybersecurity ops-center at night."

### Vraag 6 — "Wat moet aanpasbaar zijn?"
- "Hero headline, pricing cards, team photos, tech stack pills."

### Vraag 7 — "Inspiratie?"
- "Vercel voor clarity, Linear voor motion-rhythm."

**Voice-over:**
- "Dit is plan-mode voor design. Je lost blinde vlekken op VÓÓR de code er is."
- "De 4 revisies die je normaal zou doen — die voorkom je hier."

---

## 4:30 — 6:00 | Claude Design bouwt live (real-time scroll-through)

**Screen:** Claude Design render, speeding through in real-time (of gecomprimeerd als te langzaam voor video).

**Voice-over:**
- "Nu bouwt het. In 30-60 seconden komt de high-fi hero."
- "Infinity-loop rendered in 3D, agents orbiting, data-beams, emerald glow — alles op basis van onze vragen."

**Screen:** zoom in op details terwijl het laadt:
- Hero met Halant italic headline
- Void black #050a08 achtergrond (klopt!)
- Emerald #00ff88 accents op "Your Next Hire" met glow
- CTA "See What's Possible" in emerald fill

**Voice-over:**
- "Kijk dit. Eerste render. Geen revisies. On-brand vanaf frame 1."
- "Dit is het verschil dat design.md maakt."

---

## 6:00 — 7:30 | De Workflow Die 50% Quota Bespaart (talking head + screen)

**Shot:** direct in camera, serieus moment

**Dialoog bullets:**
- "Dit is het belangrijkste stuk van deze les."
- "Iedereen doet dit verkeerd."
- "Ze maken één render. Vinden het niet goed. Beginnen dan met tweaks, tweaks, tweaks."
- "Ze blazen hun quota op binnen een dag."

**On-screen graphic:**

```
❌ FOUTE WORKFLOW:
1 render → tweak → tweak → tweak → tweak → tweak = ~20% quota

✅ JUISTE WORKFLOW:
1 render + 2 varianten (macro) → kies 1 → 15 tweaks (micro) = ~10% quota
```

**Voice-over:**
- "Juiste workflow heeft TWEE levels: macro + micro."
- "Macro = varianten. Totaal andere lay-outs."
- "Je vraagt Claude Design: 'Give me 2 variants that are completely different.'"

**Cut naar Claude Design:**

**Screen-action:** type in chat: `Give me 2 variants that are completely different — one more editorial, one more brutalist.`

**Voice-over tijdens render:**
- "Claude Design komt met totaal andere richtingen. Terminal-stijl. Synthwave. Editorial maximalist. Brutalist."
- "Wat past bij je brand."

**Screen:** toon de 2 nieuwe varianten naast origineel.

**Voice-over:**
- "Kies er één."
- "Pas DAN doe je tweaks. Binnen de gekozen variant."

**Regel-callout:**
```
REGEL: Varianten eerst. Tweaks daarna.
```

**Voice-over:**
- "Ik begin altijd met 1 basis + 2 varianten = 3 opties."
- "Kies er één. Dan 15 tweaks."
- "Bespaart 50% quota vergeleken met 'tweak tot ik het mooi vind'."

---

## 7:30 — 9:30 | De 4 Edit-Modes (live demo, elk ~30 sec)

**Talking head intro (10s):**
- "Oké, first render. Nu komt het ECHT interessante. 4 manieren om te bewerken."

### Mode 1 — Tweaks (30s)

**Cut naar Claude Design tweaks panel**

**Screen-action:**
- Click "Tweaks"
- Slider voor "Density" naar meer spacious
- Color picker: shift gold warmer

**Voice-over:**
- "Tweaks = parameters. Sliders, color pickers. Systeem-brede aanpassingen."
- "'Make everything 20% more spacious' — kan in één slider-beweging."

### Mode 2 — Comments (30s)

**Screen-action:**
- Switch naar Comments mode
- Click op hero headline, laat comment: "Te groot, schaal naar 85%"
- Click op product grid, comment: "Voeg sub-tagline toe onder elke naam"
- Click op CTA, comment: "Meer contrast, bijna black background"
- Click "Apply all"

**Voice-over:**
- "Comments mode — queue meerdere wijzigingen."
- "Dit is UX-review modus. 8 dingen tegelijk bewerken."
- "Claude Design werkt ze als batch af."

### Mode 3 — Draw (30s)

**Screen-action:**
- Switch naar Draw mode
- Omcirkel een gebied in de testimonial sectie
- Typ: "Maak dit meer cinematic — grotere quotes, donkerder, meer film-strip feeling"
- Apply

**Voice-over:**
- "Draw mode — voor als je geen woorden hebt."
- "Omcirkel, beschrijf in natural language, Claude Design snapt het."
- "Voor grote layout-revisies zonder technisch te worden."

### Mode 4 — Element-select (30s)

**Screen-action:**
- Click direct op hero headline
- Property panel opent — font size, color, spacing
- Pas aan

**Voice-over:**
- "Element-select — chirurgisch. Één element, precise control."
- "Voor microscopische tweaks in een al-goede layout."

**Return to talking head (20s):**
- "Vier modes. Verschillende doelen."
- "Tweaks voor systeem. Comments voor batch. Draw voor mood. Element voor precision."
- "Meeste designers gebruiken alleen Element — mis je 80% van de kracht."

---

## 9:30 — 10:15 | Full-screen preview + design file inkijken (screen)

**Screen-action:**
- Click "Full-screen preview" — homepage toont zonder Claude Design UI
- Scroll door — animaties zichtbaar, particle trails, gradient morph werkt
- Return, click "View design file" — onder motorkap
- Layers panel, component tree zichtbaar

**Voice-over:**
- "Full-screen preview — zo voelt het voor je user."
- "Check motion, check responsive (er zijn device-switches)."
- "Design file onder motorkap — alles gecategoriseerd, layers, tokens."
- "Dit is wat straks naar Claude Code gaat in Les 5."

---

## 10:15 — 11:15 | Pro tips + veel-gemaakte fouten (talking head)

**Dialoog bullets:**

### Pro tips:
1. "Antwoord altijd specifiek op de 7 vragen. 'Medium' is niks. 'Moderate density, 2-3 sections per viewport' is bruikbaar."
2. "Start wireframe voor multi-page. Layout eerst, styling later."
3. "Gebruik 'use my design.md' zo vaak mogelijk."
4. "Comments mode voor client-review sessies — batch 10 wijzigingen in één shot."

### Mistakes:
1. "Skip geen vragen. Claude Design raadt — raadt vaak verkeerd."
2. "Geen 'verras me'. Geef richting. Dit is engineering, niet art class."
3. "Niet 7 keer opnieuw prompten. Bouw eens, dan iterate met edit-modes."

---

## 11:15 — 11:40 | Gift unlock

**Dialoog:**
- "Gift voor les 2."
- "10 mega alpha prompts — kant-en-klaar te plakken in Claude Design."
- "Plus een complete gids voor de 4 edit-modes."
- "Niet vage prompts. Echte prompts met hex codes, typography, animatie-types, referentie-merken."

**Screen:** toon `claude-design-prompt-pack.md` in editor, scroll kort door de 10 prompts.

**Voice-over:**
- "Cinematic ecom, SaaS landing, agency portfolio, coach brand, pitch deck, mobile app, editorial, event, DTC product, portfolio case study."
- "Plak één. Vul placeholder in. Bouw."
- "Link in description."

---

## 11:40 — 12:00 | Transitie naar Les 3

**Dialoog:**
- "Oké. Je kan nu één pagina bouwen. Mooi."
- "Les 3: multi-page sites. Hoe je van één prompt naar een hele 5-pagina architectuur gaat."
- "Dit is waar het agency-verdienmodel zit."

**Cut to:** Les 3 thumbnail

---

## Production Notes

- **Claude Design chat pre-cleared** voor demo
- **187N DESIGN.md pre-loaded** in Additional Notes + `ai.svg` logo uploaded
- **Prompt pre-copied** in clipboard
- **Bij edit-modes demo:** zorg dat homepage al gebuild is (uit eerste demo-segment)
- **Als rendering te langzaam:** pre-record + montage

---

## Gift Moment Timing

9:30 — 9:50

**Gift file:**
- `~/.Lio_The_Ai_Operator/gifts/claude-design-prompt-pack.md`

---

## Escape hatches

- **Edit-modes demo** kan naar 1:30 (elk mode 22s ipv 30s)
- **Full-screen preview sectie** kan naar 30s
- **Pro tips** kan naar 30s (alleen tip #1 + #3)

Target: onder 10:30 absolute max.

---

<!-- 02-prototype-mode — Claude Design Cursus Les 2 — Lio The AI Operator -->
