# bait.name Homepage Redesign — Design Spec
_2026-11-07_

## Overview

Reframe bait.name from a faceless "app studio" brand into Bruno Alexandre's personal page. The site currently reads as a corporate-ish studio with one live product. The redesign makes it honest: one person, building things for fun, friends, and anyone who needs help — no company, no profit.

The visual language (dark background, acid yellow, Bebas Neue, Space Mono, noise texture) stays entirely. Only the copy, structure, and sections change.

---

## Page Structure

Five sections in order:

1. Hero
2. Projects
3. About
4. Support
5. Contact

Nav links update: "Products" → "Projects", "Studio" → "About".

---

## Section 1: Hero

**Eyebrow:** `Build / Help — bait.name`

**Headline (Bebas Neue, existing scale):**
```
HI, I'M BRUNO.
I LIKE TO HELP
AND BUILD THINGS.
```

**Subline (small, muted):** `Games · Apps · Charities · Others`

**Body copy:**
> I like to help, find solutions to problems, build things, and help others. No company. No profit. Just me, some code, and whoever needs a hand.

**Stats (desktop sidebar + mobile inline):**
- `6` Projects
- `0` Profit
- `☕` Fuelled by coffee

**CTAs:**
- Primary: `See What I'm Building` → `#projects`
- Ghost: `Buy Me a Coffee →` → `https://buymeacoffee.com/b1t3my8b1t`

---

## Section 2: Projects

**Section label:** `What I'm Building`
**Section title:** `MY PROJECTS.`

7-card grid, 2 columns. Last card spans full width.

| # | Name | Status | Category |
|---|------|--------|----------|
| 01 | Line Crush | Live | Game · Puzzle · Web · Android · iOS |
| 02 | Paw Shelter | In Progress | Game · Mobile |
| 03 | Tia Rosa Kitchen | In Progress | Game · Mobile |
| 04 | Spot It | In Progress | Game · Mobile |
| 05 | Organiser | In Progress | App · Mobile |
| 06 | ByFabrico | Ongoing | Pro Bono · Others |
| 07 | Your Project? | Open | Charities · Friends · Anyone |

Card 06 (ByFabrico) links to `https://byfabrico.com` (external, opens in new tab).

Card 07 spans full width on desktop (single column spanning both grid columns), styled as a soft CTA: "Got something you need built? I help for free." Links to `#contact`.

Status badge colours:
- Live → acid yellow (existing `.live`)
- In Progress → gold (existing `.coming`)
- Ongoing → teal (new `.ongoing` style, mirrors `.live` pattern using `--teal`)
- Open → muted (existing `.future`)

New CSS needed: `.prod-status.ongoing { color: var(--teal); border-color: var(--teal); }`

---

## Section 3: About

Replaces the current "Manifesto" section. Same visual treatment (centered, large display type) but personal.

**Section label:** `Who I Am`
**Title:** `JUST BRUNO.`

**Body:**
> I'm a developer who builds things in my spare time. No company, no investors, no ads. Everything here is free — built out of curiosity, care, and too much coffee.
>
> BAIT stands for Bruno Alexandre IT. The name stuck.

**Three inline callouts (pill/tag style):** reuse existing `.prod-tag` style, displayed in a flex row centered under the body text.
- `Not for profit`
- `No ads ever`
- `Open to help`

**Sub-note (small, muted text):**
> If you're a charity or a friend who needs something built, reach out. I'll do my best to help.

---

## Section 4: Support

New slim section above Contact.

**Section label:** `Keep the lights on`
**Title:** `LIKE WHAT I DO?`

**Body:**
> Everything here is free and always will be. If you want to say thanks, a coffee goes a long way.

**CTA:** `☕ Buy Me a Coffee` → `https://buymeacoffee.com/b1t3my8b1t`

Single button, centered. No second CTA. Dark background (`--mid`).

---

## Section 5: Contact

Left side (info list) unchanged.

Right panel updates:
- **Headline:** `NEED HELP?`
- **Body:** Got a problem to solve, an app idea, or a charity that needs a hand? Drop me a message.
- **CTA:** `Send a message →` → `mailto:hello@bait.name`

---

## What Doesn't Change

- Visual design system (colours, fonts, noise texture, custom cursor)
- Existing animations (scroll reveal, hero entrance)
- Mobile responsive layout patterns
- Line Crush card linking to `line-crush.html`
- Footer structure (update copy: "Products" → "Projects")
- `favicon.svg`, `CNAME`, `privacy.html`, `app-ads.txt`

---

## Post-Launch Actions (not in this implementation)

- Update LinkedIn profile to mention open availability for charity work
- Remove or update `app-ads.txt` if ads are fully gone from all properties
- Add individual project pages for Paw Shelter, Tia Rosa Kitchen, Spot It, Organiser as they launch

---

## Files Changed

- `index.html` — full rewrite of copy and section structure (visual CSS largely unchanged)
- `CLAUDE.md` — update page description to reflect personal framing
