# Claude Design Cursus

Interactieve cursus. Lees instructies in je Claude Code terminal, voer uit in Claude Design browser, volg je voortgang live in het dashboard. 9 lessen, ~75 minuten, gratis.

---

## Voor Kijkers — Installatie (2 min)

**Wat je nodig hebt:**
- [Claude Code](https://claude.com/claude-code) geïnstalleerd
- Claude Pro of Max abonnement (voor `claude.ai/design` toegang)
- Python 3 op je machine (`python3 --version` moet werken)
- Voor Les 6: GitHub CLI (`gh`) + Vercel CLI (`vercel`)
- Voor Les 5 (optioneel): Higgsfield.ai account

**Installeren:**

```bash
# 1. Unzip (als je ZIP download kreeg)
unzip claude-design-cursus.zip
cd claude-design-cursus

# 2. Run installer
./install.sh
```

Het script:
1. Kopieert de 9 skills naar `~/.claude/commands/design/`
2. Maakt progress folder in `~/.claude-design-cursus/`
3. Start lokaal dashboard op `http://localhost:8765/dashboard.html`
4. Opent je browser automatisch

**Starten met de cursus:**

Typ in Claude Code terminal:
```
/design:00-intro
```

Het dashboard updatet automatisch mee — voltooide lessen krijgen een ✓, huidige les highlight.

**Problemen?**
- Dashboard opent niet? Plak zelf in browser: `http://localhost:8765/dashboard.html`
- Skill niet herkend? Check `ls ~/.claude/commands/design/` — moeten 9 .md bestanden staan
- Server stoppen? `lsof -ti:8765 | xargs kill -9`

---

## Lessen Overzicht

| # | Skill | Duur | Onderwerp |
|---|-------|------|-----------|
| 0 | `/design:00-intro` | 3 min | Welkom + token economics warning + setup check |
| 1 | `/design:01-design-md` | 10 min | Design.md — 3 manieren om je brand-fundament te bouwen |
| 2 | `/design:02-prototype-mode` | 12 min | 7-vragen loop + 4 edit-modes + 50% quota-besparing |
| 3 | `/design:03-multi-page` | 10 min | One-pager website — live Orbis.Nft build |
| 4 | `/design:04-mobile-decks` | 10 min | Mobile app + investor deck (10-15K bundle) |
| 5 | `/design:05-hero-video` | 10 min | Cinematic hero — Nano Banana → Seedance |
| 6 | `/design:06-live-website` | 12 min | /build-page + /deploy-site naar Vercel |
| 7 | `/design:07-command-center` | 6 min | Alles in 30 min — victory lap |
| 8 | `/design:08-outro` | 30 sec | Recap + volgende stappen |

---

---

# Voor Leon — Opname Scripts (187N Live-Build Edition)

> 9 markdown files, één per les/segment. Naast camera open houden. Leon praat vrij vanaf bullets, script is houvast niet keurslijf. Live build: 187N.AI enterprise AI agency.

De originele shoot-prep dashboard (4 modes: PREP/Pre-Opname/SHOOT/LIVE) staat in `shoot-prep.html` als backup.

---

## Volgorde van Opname

| # | File | Duur | Focus |
|---|------|------|-------|
| 0 | `00-intro.md` | 3:30 | Hook, 3 proof-demos, token economics warning, 7-lessen preview |
| 1 | `01-design-md.md` | 10:00 | 3 import-methodes + 187N interview + Design Systems |
| 2 | `02-prototype-mode.md` | 12:00 | 7-vragen loop + Plan Mode + Variants→Tweaks + 4 edit-modes |
| 3 | `03-multi-page.md` | 10:00 | **One-pager** — 11 secties live 187N build + Dribbble methode |
| 4 | `04-mobile-decks.md` | 10:00 | 187N Client Portal + Agency Vision Deck → .pptx |
| 5 | `05-hero-video.md` | 10:00 | 🎬 Nano Banana → Claude Design → Seedance (187N Agent Command Scene) |
| 6 | `06-live-website.md` | 12:00 | /build-page + /deploy-site live (187n.ai) |
| 7 | `07-command-center.md` | 6:00 | /design-command-center victory lap — 3 deliverables in 30 min |
| 8 | `08-outro.md` | 0:30 | Bridge naar Routines + masterclass CTA |

**Totaal:** ~75 minuten video

---

## Opname Workflow

### Ochtend (pre-studio, ~1u)

1. **Dry-run `/design-command-center`** met 187N design.md — moet <30 min complete bundle opleveren
2. **Dry-run `/build-page`** met 187N export — check of alles buildt zonder errors
3. **Backup live URL** — `187n.ai` blijft altijd live op laatste successful deploy (geen aparte preview nodig)
4. **Check auth**: Claude Pro Max, `gh auth status`, `vercel whoami`, Higgsfield login
5. **Pre-gen hero video**: Nano Banana → Seedance pre-gen als Les 5 backup
6. **Pre-load alle tabs** in browser:
   - Claude Design (claude.ai/design)
   - 187n.ai live site (voor Les 3 referentie)
   - `~/projects/187n-website/` folder (voor codebase import demo)
   - getdesign.md (voor methode 2 demo)
   - Dribbble (voor one-pager layout refs)
   - Higgsfield.ai (voor Les 5)
   - 187n.ai open in tab (backup = live site zelf)
7. **Pre-copy alle prompts** in Raycast/Alfred snippets library:
   - 187N DESIGN.md (Additional Notes paste)
   - 187N One-Pager prompt
   - 187N Client Portal Mobile prompt
   - 187N Agency Vision Deck prompt
   - 187N Command Center Run prompt
   - Nano Banana: Agent Command Scene still
   - Seedance: Concept A motion

### Studio (middag)

**9 takes in volgorde.** Tussen elke les: `/clear` in Claude Code terminal, reset browser tabs waar nodig.

**Per les:**
1. Open script in secondary monitor of op iPad naast camera
2. Lees eerste bullet → praat vrij
3. Als demo: volg screen-actions uit script
4. Gift moment: screen-overlay naar gift file locatie
5. Transitie: cut naar volgende les thumbnail

### Tussen lessen (reset checklist):

- [ ] Terminal `clear` + `/clear` in Claude Code
- [ ] Browser: close unused tabs, keep primary demo-tab active
- [ ] Screen-recording check (OBS of ScreenFlow running?)
- [ ] Camera framing check (nog steeds center?)
- [ ] Audio level check (mic nog gemount?)
- [ ] Water drink + reset energy

---

## Gift Files Overview

| Les | Gift Files | Pad |
|-----|------------|-----|
| L1 | design-md-template.md + design-import-methods.md | `~/.Lio_The_Ai_Operator/gifts/` |
| L2 | claude-design-prompt-pack.md + claude-design-token-economics.md | `~/.Lio_The_Ai_Operator/gifts/` |
| L3 | dribbble-reference-library.md + multi-page-mega-prompts.md | `~/.Lio_The_Ai_Operator/gifts/` |
| L4 | mobile-app-template.md + pitch-deck-template.md | `~/.Lio_The_Ai_Operator/gifts/` |
| L5 | hero-video-prompt-pack.md (187N Agent Command Scene) | `~/.Lio_The_Ai_Operator/gifts/` |
| L6 | claude-md-webapp-blueprint.md + gsap-prompt-library.md | `~/.Lio_The_Ai_Operator/gifts/` |
| L7 | agency-onboarding-template.md | `~/.Lio_The_Ai_Operator/gifts/` |

---

## Demo Content — 187N Live Build

| Asset | Locatie |
|-------|---------|
| **187N production repo** | `~/projects/187n-website/` (Trevor's Next.js repo) |
| **187N workspace** | `~/my-ai-workspace/187n-ai/` (DESIGN.md, knowledge bases) |
| **187N DESIGN.md** | `~/my-ai-workspace/187n-ai/DESIGN.md` |
| **187N logo** | `~/Downloads/ai.svg` (upload to Claude Design Additional Files) |
| **Live site** | `https://187n.ai` |
| **Backup (= live)** | `https://187n.ai` |

### Guardrails (uit `_course-prep/OUTLINE.md`)

- **NO client names** — geen Paw Parent, Voltera, Winners, Forge Waters
- **NO other Leon brands** — geen @lio, @liogpt, LIO OS
- **Pitch deck vision-only** — geen omzet, geen ARR, geen "X klanten"
- **Team photos mogen** — Leon, Damian, Trevor, Tim zijn publiek

---

## Skills Gebruikt in Cursus

| Skill | Introduceert in | Locatie |
|-------|-----------------|---------|
| `/design-prompts` | Les 3 (viewer gift — 7 vragen → volledige design kit) | `~/.claude/commands/design-prompts.md` |
| `/build-page` | Les 6 | `~/.claude/commands/build-page.md` |
| `/deploy-site` | Les 6 | `~/.claude/commands/deploy-site.md` |
| `/design-command-center` | Les 7 | `~/.claude/commands/design-command-center.md` |

---

## Post-Opname Checklist

- [ ] Ruwe takes uploaden naar Frame.io / Google Drive (backup)
- [ ] Geluidsloze intro-kaart + outro-kaart maken
- [ ] B-roll collectie (187N.AI site scroll, mobile portal swipes, deck flip)
- [ ] Captions — NL hardcoded + EN als soft-sub optie
- [ ] Thumbnails voor elke les (serie-consistent, 187N brand tokens)
- [ ] Gift files finaliseren (check al in `~/.Lio_The_Ai_Operator/gifts/`)
- [ ] YouTube description per les (met timestamps + gift links)
- [ ] Instagram posts voor launch (carousel: 7 lessen overview + CTA)
- [ ] Email naar email-list: "De 2e gratis cursus is live — 187N live build"

---

## Backup Plans

### Als Claude Design langzaam is tijdens opname:
→ Pre-record Claude Design renders + voice-over achteraf

### Als Vercel deploy faalt:
→ Cut naar 187n.ai (live site blijft op laatste successful deploy), "and here's what it looks like live"

### Als Seedance faalt tijdens Les 5:
→ Pre-gen'd `187n-hero-motion.mp4` klaar als fallback voor MP4 swap demo

### Als internet haperend:
→ Alle demos lokaal gedraaid, Claude Code terminal werkt zonder internet voor meeste acties

### Als Leon geblokt raakt tijdens live demo:
→ "En hier in Claude Code" + cut naar pre-recorded segment

---

## Dashboards

**Interactieve cursus dashboard** (primair — voor Leon tijdens live demo + kijkers):
- `dashboard.html` — toont huidige les, stappen, prompts copy-buttons, polled `progress.json` live
- Draait op `http://localhost:8765/` na `./install.sh`

**Shoot-prep dashboard** (backup — originele 4-mode opname tool):
- `shoot-prep.html` — PREP / Pre-Opname / SHOOT / LIVE modes, 187N + Orbis prompts + timing budgets
- Open direct in browser: `open shoot-prep.html`

---

*Claude Design Cursus — 187N Live-Build Edition — Lio The AI Operator*
