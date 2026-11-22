# `/design-prompts` — De Claude Design Prompt Machine

**De gift van Les 3.** De skill die jouw brand omzet naar een paste-ready Claude Design website prompt — **tweetalig (NL + EN)**, op 187N-niveau, in 2 minuten.

---

## Wat doet het?

Je runt `/design-prompts` in Claude Code. Twee manieren:
- **Heb je nog niks?** Beantwoord 7 korte vragen.
- **Heb je al website-copy of een `design.md`?** Plak 't — de machine bouwt de prompt om jouw echte teksten heen (Mode B).

Kies je taal (`NL` · `EN` · `Tweetalig` met NL/EN-toggle). Je krijgt 4 copy-ready outputs in 1 bericht:

| # | Output | Waar plak je 'm? |
|---|--------|------------------|
| ① | **DESIGN.md** — brand system (kleuren + hex, fonts, signature effects, motion, voice) | Claude Design → Additional Files |
| ② | **Claude Design Website Prompt** — sectie-voor-sectie, echte copy, design system, guardrails (tweetalig) | Claude Design → nieuwe session → Plan Mode |
| ③ | **Nano Banana Pro hero image prompt** — JSON met composition, lighting, palette, text-zones | Nano Banana Pro (Google AI Studio) |
| ④ | **Seedance 2.0 motion prompt** — 6-sec loop, camera + sequence + audio | Higgsfield.ai — ⚠️ Enhance Prompt: UIT |

Plus optioneel: mobile app prompt + pitch deck prompt (zeg "ja" als Claude dat vraagt).

---

## Installatie — 30 seconden

**Optie A: Je hebt Claude Code al**

1. Maak de file aan en plak de inhoud uit de cursus-resources:
   ```bash
   mkdir -p ~/.claude/commands
   nano ~/.claude/commands/design-prompts.md
   # Plak de inhoud van design-prompts.md uit de cursus-resources, save met Ctrl+O, Enter, Ctrl+X
   ```
2. Restart Claude Code (`/clear`) — de skill staat nu in je slash-menu
3. Typ `/design-prompts` → start

**Optie B: Je hebt Claude Code nog niet**

1. Installeer Claude Code: `brew install claude-code` (Mac) of volg instructies op [claude.ai/code](https://claude.ai/code)
2. Ga verder met Optie A

---

## De 7 Vragen (vooraf invulbaar)

Je kunt deze vooraf uitwerken zodat je in Claude Code alleen hoeft te plakken:

```
1. Bedrijfsnaam + wat doe je in 1 zin:
   _______________________________________________

2. Wie is je ideale klant? 1 zin — wie koopt, waar pijn:
   _______________________________________________

3. Sector/vibe (kies 1):
   [ ] SaaS / dev tool
   [ ] AI agency / enterprise
   [ ] E-commerce / fysiek product
   [ ] Coach / expert / personal brand
   [ ] Creator / influencer
   [ ] Technisch B2B / industrie
   [ ] Anders: _______________

4. 3 kleuren die voelen als jouw brand (hex of omschrijvend):
   • _______________
   • _______________
   • _______________

5. 3 referentie-merken + wat je van elk wilt stelen:
   • _______________ → _______________
   • _______________ → _______________
   • _______________ → _______________

6. Tone (kies 1-2): formeel / speels / premium / direct / cinematic / technisch / warm / provocatief
   → _______________

7. Hero-concept — wat zien we in het eerste scherm? (kies 1):
   [ ] Product shot
   [ ] Persoon / founder / team
   [ ] Dashboard / UI / scherm
   [ ] Abstract / motion / particles
   [ ] Environment / lifestyle
   [ ] Anders: _______________
```

Als je alle 7 al hebt: plak ze in 1 keer in Claude Code na `/design-prompts` — Claude herkent dat je al hebt geantwoord en skipt de interview.

---

## Plak-volgorde (aanbevolen)

1. **DESIGN.md eerst** — save als `design.md` in je project folder. Dit is de "source of truth" voor alle andere outputs.
2. **Nano Banana Pro prompt** → genereer je hero image → download als 4K PNG/JPG
3. **Seedance prompt** → upload de Nano Banana image als reference → genereer motion (6 sec, 60fps) → download MP4
4. **Claude Design One-Pager prompt** → nieuwe Claude Design session → paste DESIGN.md in Additional Notes → upload hero image/video als reference → paste prompt → Plan Mode → Build

---

## Guardrails (uit de skill)

- **"Ask me any questions before you begin"** — zit ingebakken in de one-pager prompt. Dit triggert Claude Design's Plan Mode zodat je eerst afstemt voor 'ie 120 sec gaat bouwen.
- **"Enhance Prompt: UIT"** — staat als ⚠️ waarschuwing in de Seedance prompt. Als 'ie aan staat herschrijft Seedance je prompt en krijg je iets anders dan je vroeg.
- **Geen tekst in Nano Banana prompt** — tekst komt via HTML/CSS overlay in Claude Design, niet via het beeld. Nano Banana maakt typo's in rendered text.

---

## Sector-smart defaults

De skill shift automatisch op basis van vraag 3:

| Sector | Kleurpalet | Fonts | Signature |
|--------|------------|-------|-----------|
| SaaS / AI agency | Dark (#000 / off-black) | Barlow + Instrument Serif + Mono | Liquid Glass cards, grid overlay |
| E-commerce | Off-white / warm neutral | Satoshi / Söhne + editorial serif | Warm shadows, lifestyle photography |
| Coach / expert | Warm cream of deep navy | Fraunces / Canela (serif-first) | Zachte shadows, generous whitespace |
| Creator | Editorial magazine | Editorial New / Migra (big type) | Full-bleed, mixed type scales |
| B2B technisch | Blueprint blue / grijs | Inter / IBM Plex | Schematische lines, precise grids |

Wil je de SaaS-styling maar je bent e-com? Zeg dat in de tone vraag — "ik wil SaaS feel" — en Claude mixt.

---

## Alternatieve motion stijlen

De default Seedance output past motion bij je sector. Voor andere stijlen:

- Cinematic live-action → `/seedance:01-cinematic`
- 3D CGI renders → `/seedance:02-3d-cgi`
- Motion design ad (SaaS) → `/seedance:06-motion-design-ad`
- E-commerce product showcase → `/seedance:07-ecommerce-ad`
- Social hook (15-sec) → `/seedance:11-social-hook`
- Brand story → `/seedance:12-brand-story`
- Fashion lookbook → `/seedance:13-fashion-lookbook`
- Food & beverage → `/seedance:14-food-beverage`
- Real estate tour → `/seedance:15-real-estate`

---

## Troubleshooting

**"Claude geeft me geen 4 outputs — alleen text"**
→ Je hebt `/design-prompts` niet als slash command geïnstalleerd. Check `ls ~/.claude/commands/design-prompts.md`. Als 'ie er niet staat → installatie opnieuw doen.

**"De outputs zijn generiek — ze voelen niet als mijn brand"**
→ Vraag 5 (referentie-merken) is waarschijnlijk te oppervlakkig beantwoord. Wees specifiek: niet "Apple", maar "Apple's generous whitespace" of "Apple's product photography stijl". Claude werkt met wat je geeft.

**"Claude Design ignores mijn DESIGN.md"**
→ Je hebt 'm in "Additional Notes" geplakt ipv "Additional Files". Upload als `.md` bestand, dan leest Claude Design 'm als reference document.

**"Seedance geeft me iets compleet anders dan mijn prompt"**
→ Enhance Prompt staat aan in Higgsfield UI. Dubbel-check rechtsbovenin de Seedance 2.0 interface.

---

## Volgende stappen

1. Run `/design-prompts` met jouw brand
2. Plak alle 4 outputs volgens de volgorde hierboven
3. Claude Design bouwt je one-pager → export → plak in je project folder
4. Les 6: `/build-page` — van Claude Design export naar NextJS op Vercel (live URL)
5. Les 7: `/design-command-center` — volledige pipeline (site + mobile + deck) in 30 min

---

<\!-- Gift voor Les 3 van de Claude Design cursus · 2026 -->
