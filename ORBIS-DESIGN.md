# ORBIS.NFT — DESIGN.md

> Paste-ready voor Claude Design Additional Notes. Cursus live-build merk vanaf Les 3.

---

## Brand

| | |
|---|---|
| **Name** | Orbis.Nft |
| **Product** | NFT collection — 10,000 pieces, space objects & digital artifacts |
| **Niche** | Web3 / NFT / art collection |
| **Positioning** | "A digital object fixed beyond time and place. An exploration of distance, form, and silence in space." |
| **Stack** | ERC-721A · Ethereum + Base |
| **Tagline (Condiment accent)** | Beyond earth · Nft collection · Go beyond |

## Voice

- Terse · cosmic-minimal · uppercase body
- Proud of negative space — text sparzaam
- Mono for descriptions, Anton for claims, Condiment for emotional overlay
- Short sentences. Full stops. Silence.

## Fonts (Google Fonts)

```
https://fonts.googleapis.com/css2?family=Anton&family=Condiment&display=swap
```

| Family | Tailwind alias | Usage |
|---|---|---|
| **Anton** | `font-grotesk` | All headings, navigation, stat numbers, buttons. ALWAYS uppercase. |
| **Condiment** | `font-condiment` | Cursive accent overlays. Normal-case. Always in neon, mix-blend-exclusion. |
| System mono | `font-mono` | Body paragraphs, labels, metadata. Uppercase for labels, normal-case for descriptions. |

## Color System (Tailwind config)

```js
colors: {
  background: '#010828',  // deep dark navy — default bg
  cream:      '#EFF4FF',  // all text
  neon:       '#6FFF00',  // accent, Condiment overlays, underline bars, active states
}
```

**Rules:**
- Default bg = `#010828` (no gradients on bg — texture overlay handles depth)
- Text always `cream` or `cream/70` or `cream/20` — never pure white
- Neon reserved for: Condiment cursive, active nav items, underline bars under buttons, score highlights, "filled" timeline states

## Liquid Glass CSS effect

Applied via `.liquid-glass` class. Used on: navbar · social icon buttons · NFT cards · card overlays · deck stat bars · mobile tab bar.

```css
.liquid-glass {
  background: rgba(255, 255, 255, 0.01);
  background-blend-mode: luminosity;
  backdrop-filter: blur(4px);
  -webkit-backdrop-filter: blur(4px);
  border: none;
  box-shadow: inset 0 1px 1px rgba(255, 255, 255, 0.1);
  position: relative;
  overflow: hidden;
}
.liquid-glass::before {
  content: '';
  position: absolute;
  inset: 0;
  border-radius: inherit;
  padding: 1.4px;
  background: linear-gradient(180deg,
    rgba(255,255,255,0.45) 0%, rgba(255,255,255,0.15) 20%,
    rgba(255,255,255,0) 40%, rgba(255,255,255,0) 60%,
    rgba(255,255,255,0.15) 80%, rgba(255,255,255,0.45) 100%);
  -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
  -webkit-mask-composite: xor;
  mask-composite: exclude;
  pointer-events: none;
}
```

## Texture Overlay

Full-screen fixed overlay on top of everything:
- `/texture.png` (subtle grain/noise)
- `position: fixed; inset: 0; z-index: 50; pointer-events: none;`
- `mix-blend-mode: lighten`
- `opacity: 0.6`
- `background-size: cover`

## Signatures (reuse across all outputs)

1. **Condiment cursive accents** always positioned absolute over a heading, slight `rotate(-1deg)` to `rotate(-2deg)`, `mix-blend-exclusion`, `text-neon`, `opacity-90`.
2. **Purple gradient chevron buttons** on NFT cards — `bg-gradient-to-br from-[#b724ff] to-[#7c3aed]`, 48×48px rounded-full, white chevron-right SVG, `shadow-lg shadow-purple-500/50 hover:scale-110`.
3. **Neon underline bars** under CTA buttons and active nav — `bg-neon h-[6px]` to `h-[10px]` responsive, full width of button.
4. **Max content width 1831px** across all sections on all outputs (site / deck / mobile backdrop).
5. **All videos:** `autoPlay loop muted playsInline`.

## CloudFront Video Assets (reuse across site / deck / mobile)

| Role | URL |
|---|---|
| Hero (section 1, splash, deck title bg, mobile backdrop) | `https://d8j0ntlcm91z4.cloudfront.net/user_38xzZboKViGWJOttwIXH07lWA1P/hf_20260331_045634_e1c98c76-1265-4f5c-882a-4276f2080894.mp4` |
| About / Intro (section 2) | `https://d8j0ntlcm91z4.cloudfront.net/user_38xzZboKViGWJOttwIXH07lWA1P/hf_20260331_151551_992053d1-3d3e-4b8c-abac-45f22158f411.mp4` |
| NFT card A — Rarity 8.7/10 | `https://d8j0ntlcm91z4.cloudfront.net/user_38xzZboKViGWJOttwIXH07lWA1P/hf_20260331_053923_22c0a6a5-313c-474c-85ff-3b50d25e944a.mp4` |
| NFT card B — Rarity 9.0/10 | `https://d8j0ntlcm91z4.cloudfront.net/user_38xzZboKViGWJOttwIXH07lWA1P/hf_20260331_054411_511c1b7a-fb2f-42ef-bf6c-32c0b1a06e79.mp4` |
| NFT card C — Rarity 8.2/10 | `https://d8j0ntlcm91z4.cloudfront.net/user_38xzZboKViGWJOttwIXH07lWA1P/hf_20260331_055427_ac7035b5-9f3b-4289-86fc-941b2432317d.mp4` |
| CTA / Final section | `https://d8j0ntlcm91z4.cloudfront.net/user_38xzZboKViGWJOttwIXH07lWA1P/hf_20260331_055729_72d66327-b59e-4ae9-bb70-de6ccb5ecdb0.mp4` |

## Tech Stack

- React 18 + TypeScript + Vite + Tailwind CSS
- `lucide-react` for icons (Mail, Twitter, Github, Bell, Search, Filter, ChevronRight)
- `framer-motion` for mobile screen transitions (optional, only for mobile app)
- No other packages needed

## Responsive

Mobile-first. Breakpoints: `sm:` 640 · `md:` 768 · `lg:` 1024 · `xl:` 1280.
All sections max-w-[1831px] centered with responsive horizontal padding.

## Guardrails

- NO stock photos — all visuals are the CloudFront videos
- NO traction numbers ("X holders sold") on deck — vision-only, projected market figures OK
- NO buttons without neon underline OR liquid-glass surface — these two are the only button styles
- NO lowercase headings — Anton is always uppercase, Condiment cursive is always normal-case accent
- NO deviation from `#010828` bg — gradients happen via texture overlay, not bg
