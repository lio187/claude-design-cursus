# 06 — LES 6: Van Design naar Live Website (12 min) · Orbis.Nft Deploy

**Target length:** 12:00
**Shot mix:** Screen 90% / talking head 10% (zwaarste demo)
**Focus:** Handoff Claude Design → /build-page → Vite + React + Tailwind → /deploy-site → live URL (`orbis-nft.vercel.app`)

**⚠️ MEEST KRITIEKE LES — hier faalt het live vaak. PRE-RECORD ALS BACKUP.**

---

## 0:00 — 0:30 | Les-opening (talking head)

**Dialoog:**
- "Les 6. Dit is waar 90% van de mensen afhaakt."
- "Prachtig Orbis.Nft design in Claude Design. Mooi."
- "Maar hoe wordt het een LIVE URL?"
- "Hoe neemt de klant het over? Hoe werkt SEO? Performance? Analytics?"
- "Dit is productie. Geen prototype meer."

---

## 0:30 — 1:30 | De Handoff

**Shot:** Claude Design — Orbis.Nft one-pager project uit Les 3

**Screen action:**
- Open je Orbis.Nft Claude Design project
- Click Export dropdown → "Handoff to Claude Code"
- Claude Design genereert lange prompt
- Copy to clipboard

**Voice:**
- "Hier is onze Orbis.Nft one-pager uit Les 3."
- "Klik Export. Handoff to Claude Code."
- "Claude Design genereert een lange prompt. Letterlijk honderden regels specs."
- "Kleuren (#010828 / cream / neon), fonts (Anton / Condiment / mono), liquid-glass CSS, video URLs, secties — alles."
- "Dit is Claude Design's cheatcode. Claude Code krijgt perfect briefing."

---

## 1:30 — 3:30 | De CLAUDE.md Webapp Blueprint

**Shot:** Editor split — `CLAUDE.md` + `ORBIS-DESIGN.md`

**Voice (scroll through CLAUDE.md):**
- "Voor Claude Code echt kan bouwen, heeft het een handboek nodig."
- "Dit is CLAUDE.md. Maar dan voor je webapp."

### Key secties highlighten:

**Tech Stack:**
```
Vite + React 18 + TypeScript. Tailwind CSS 3+.
lucide-react voor icons. Google Fonts: Anton + Condiment.
Vastgelegd. Niet onderhandelbaar.
```

**Folder Structure:**
- "Components in `src/components/`, sections in `src/components/sections/`, assets in `public/`."
- "`public/texture.png` vereist — subtle grain overlay."
- "Named exports. TypeScript strict."

**Liquid Glass Rules:**
- ".liquid-glass class op navbar, social buttons, NFT cards, overlay bars."
- "backdrop-filter blur(4px), inset shine 1px, conic border mask."
- "NIET op bg-only elementen — alleen op containers met content."

**Video Rules:**
- "Alle 6 CloudFront URLs autoPlay loop muted playsInline."
- "Hero section: object-cover. CTA section: w-full h-auto block (native aspect)."

**Voice:**
- "Dit is waarom de cursus werkt: ORBIS-DESIGN.md + CLAUDE.md + Claude Design export = Claude Code kan niet falen."

---

## 3:30 — 4:30 | /build-page skill

**Shot:** Claude Code terminal screen

**Screen action:**
```
/build-page
```

**Claude Code vraagt:** heb je een Claude Design export?

**Screen action:** paste de export prompt.

**Claude Code vraagt:** output folder?

**Answer:** `~/my-ai-workspace/design-builds/orbis-nft`

**Claude Code vraagt:** welke secties?

**Answer:** de 4 secties uit Les 3 (Hero / About / Collection / CTA)

**Voice:**
- "Claude Code start de build."
- "Scaffold Vite + React + TypeScript project. Install Tailwind, lucide-react."
- "Verwerkt Tailwind config met Orbis design tokens — bg #010828, cream, neon."
- "Registreert Anton + Condiment via Google Fonts in index.html."
- "Bouwt secties in components/sections: Hero, About, Collection, CTA."
- "Maakt liquid-glass class in index.css met de complete conic border-mask."
- "Download texture.png of placeholder naar public/."

---

## 4:30 — 7:00 | Lokale Preview + Performance Check

**Shot:** Terminal + browser

**Screen action:**
```
cd design-builds/orbis-nft
pnpm dev
```

**Wait voor "Ready on localhost:5173".**

**Open browser localhost:5173.**

**Voice:**
- "Build klaar. Nu lokale test."
- "Dat wat we in Claude Design bouwden voor Orbis. Nu echt. Werkend. Vite + React onder de motorkap."

### Scroll through live site

**Voice (bij elke sectie):**
- "Hero sectie: full-bleed CloudFront video loop. Anton heading 'Beyond earth'. Condiment cursive 'Nft collection' in neon rechts."
- "Liquid-glass navbar met 5 links (Homepage, Gallery, Buy NFT, FAQ, Contact). Hover → text-neon."
- "Social icons rechts boven — 3 stuks, 56×56 liquid-glass."
- "Scroll naar About — tweede video background, 'I'm orbis' + Condiment overlay."
- "Collection Grid — 3 NFT cards met rarity 8.7 / 9.0 / 8.2. Purple gradient chevron buttons."
- "Final CTA — full-bleed video, 'JOIN US. REVEAL. DEFINE. FOLLOW.' met 'Go beyond' cursive."

### Performance check

**Screen:** Chrome DevTools, mobile viewport + Lighthouse

**Voice:**
- "Mobile test. iPhone 14 Pro viewport. Social icons stacken onder heading. Nav verdwijnt (hidden lg:block)."
- "Video loops stoppen op low-power mode — check playsInline."
- "Reduced-motion toggle — videos houden auto-play maar transitions disable."
- "Lighthouse audit — 90+ performance (videos zijn zwaar maar CloudFront handles CDN)."
- "Dit is waar handmatige builds 3 dagen over doen. Wij: 5 minuten."

---

## 7:00 — 10:00 | /deploy-site naar Vercel

**Shot:** Terminal

**Screen action:**
```
/deploy-site
```

**Antwoorden:**
- Folder? `orbis-nft`
- Repo naam? `orbis-nft`
- Private/public? Private
- Custom domain? Skip voor nu

**Claude Code acties (screen log):**
- `git init`
- `git add . && git commit`
- `gh repo create orbis-nft --private`
- `vercel link`
- `vercel deploy --prod`

**Wait 60-90 seconden.**

**Output:**
```
✓ Production: orbis-nft.vercel.app
```

**Screen action:** copy URL → open in new tab → scroll door live site

**Voice:**
- "En daar is het. Live. Op Vercel. Met SSL. Met CDN."
- "Orbis.Nft is nu online. Klaar voor drop."

---

## 10:00 — 11:00 | Custom Domain (als klant dat wil)

**Shot:** Terminal

**Screen action:**
```
vercel domains add orbis-nft.com
vercel alias set orbis-nft.vercel.app orbis-nft.com
```

**DNS update demo:**
- "Bij je registrar: A record naar Vercel IP of CNAME naar cname.vercel-dns.com."
- "5 minuten. SSL automatisch."

**Voice:**
- "Voor NFT klanten: custom domain essentieel voor trust."
- "Orbis.Nft heeft orbis-nft.com of .xyz of .io — web3 branding."

---

## 11:00 — 11:45 | Recap

**Shot:** Return talking head

**Dialoog:**
- "Even terugkijken. In deze les hebben we:"
- "1. Claude Design export genomen van Orbis.Nft."
- "2. /build-page gebruikt. Vite + React + Tailwind scaffold."
- "3. Lokaal getest. 4 secties werkend. Mobile ok. Videos loopen. Lighthouse 90+."
- "4. /deploy-site. GitHub + Vercel production."
- "5. Custom domain flow getoond."
- "Totaal: ~10 minuten van design naar live URL."
- "Zonder deze stack? 2-3 dagen minimum. En dit is voor een merk dat niet eens van jou is."

---

## 11:45 — 12:00 | Gift + transitie

**Dialoog:**
- "Gift voor les 6: /build-page skill + CLAUDE.md webapp blueprint voor Vite/React + liquid-glass prompt library."
- "Complete deploy recipe. Kijker runs this, deployt zijn eigen project."
- "Les 7: één pagina live = leuk. Site + mobile + deck in 30 min voor Orbis = explosief."
- "Victory lap."

---

## Production Notes

- **KRITIEK:** pre-record hele demo als backup. Als live deploy faalt → cut naar pre-recorded deploy flow.
- **Fallback URL:** `orbis-nft.vercel.app` (pre-deployed als safety net)
- **Terminal font zoom:** 16pt+ voor leesbaarheid
- **Screen recording dubbele buffer** voor als live build traag is (invoegen in montage)
- **texture.png** moet in `public/` staan voor de Vercel build slaagt — placeholder of pre-gen Nano Banana grain

---

<!-- 06-live-website — Claude Design Cursus — Orbis.Nft Deploy Edition -->
