# YouTube Channels — Documentary Project

> 4 Polish-language documentary YouTube channels. Topics: katastrofy (catastrophes), true crime, biznes (business), biografie (biographies).

**Audience.** AI agents producing scripts, thumbnails, descriptions, and packaging for these channels. NOT a content calendar (that lives elsewhere — TBD).

---

## 1. The 4 channels

| # | Channel | Topic | Tone | Accent color |
|---|---|---|---|---|
| 1 | **Błąd Krytyczny** | Katastrofy (catastrophes) | dramatic, dark, smoke/embers | red `#c41e3a` |
| 2 | **Sprawa: Nierozwiązana** | True crime | noir, desaturated, suspense | cold blue `#3a4a5c` |
| 3 | **Kod Sukcesu** | Biznes (successes + failures + rivalries) | corporate, clean, light | gold `#ffb700` |
| 4 | **Cena Sławy** | Biografie (biographies) | glam portrait, dramatic light | purple `#6a4c93` |

**Important note on Kod Sukcesu:** user explicitly requested **broader scope** than just business failures — also covers successes and inter-company rivalries/battles. Do NOT limit research to "upadki firm" (failed companies).

---

## 2. Standard production pipeline (per video)

```
┌────────────────────────────────────────────────────────────┐
│  1. Research (Tavily / web search)                         │
│     • Find topic with strong narrative + controversy       │
│     • Gather primary sources + key dates + people          │
│     • Identify "hook moment" (first 5 sec retention)       │
└────────────────────────────────────────────────────────────┘
                              ▼
┌────────────────────────────────────────────────────────────┐
│  2. Script (Claude / Sonnet, ~2-3K words for 15min video)  │
│     • Hook (5 sec, grab attention)                         │
│     • Context (who/what/when/where)                        │
│     • Buildup (escalation, tension)                        │
│     • Climax (the reveal / the disaster / the decision)    │
│     • Aftermath / takeaway (respect for victims)           │
└────────────────────────────────────────────────────────────┘
                              ▼
┌────────────────────────────────────────────────────────────┐
│  3. Thumbnail (Nano Banana / GPT Image 2)                  │
│     • 1280×720, JPG, max 4MB                               │
│     • 3-element: subject + emotion + context               │
│     • Face/hero occupies left 60%                          │
│     • Text overlay: 2-3 words, bottom 1/3, ALL CAPS        │
│     • Channel accent color background or border            │
└────────────────────────────────────────────────────────────┘
                              ▼
┌────────────────────────────────────────────────────────────┐
│  4. Voiceover (ElevenLabs / TTS)                           │
│     • Polish, male/female per channel vibe                 │
│     • Slow pace for true crime, dramatic for catastrophes  │
└────────────────────────────────────────────────────────────┘
                              ▼
┌────────────────────────────────────────────────────────────┐
│  5. B-roll + visuals (Kling 3.0 / Luma / stock)            │
│     • Recreate scenes as short clips                       │
│     • Maps, timelines, archive photo zooms                 │
└────────────────────────────────────────────────────────────┘
                              ▼
┌────────────────────────────────────────────────────────────┐
│  6. Edit + publish                                         │
│     • Capcut / DaVinci Resolve                             │
│     • Title, description (SEO Polish), tags, chapters      │
│     • Schedule + monitor comments (early engagement)       │
└────────────────────────────────────────────────────────────┘
```

---

## 3. Per-channel specifics

### 3.1 Błąd Krytyczny (catastrophes)

**Examples:** lotniska, promy, samoloty, kopalnie, katastrofy naturalne (trzęsienia, tsunami), budowlane (mosty, wieżowce), przemysłowe (Czarnobyl, Bhopal, Halifax).

**Style notes:**
- Respect for victims. NEVER glorify the disaster.
- Focus on **systemic causes** (chain of small failures), not single "villain"
- Show the human story alongside the technical analysis

**Thumbnail formula:** Subject (victim/survivor/expert) + disaster scene (smoke, fire, water) + text "Co poszło nie tak?" or "Jak to się stało?"

### 3.2 Sprawa: Nierozwiązana (true crime)

**Examples:** zaginione osoby (Iwona Wieczorek, Madeleine McCann), nierozwiązane morderstwa, głośne sprawy sądowe, sprawy z XIX/XX wieku z nowymi dowodami.

**Style notes:**
- NO speculation presented as fact. Use "podejrzewa się", "według jednej z teorii"
- Respect for victims and families
- Cover Polish AND international cases (don't limit to PL)

**Thumbnail formula:** Black-and-white or desaturated photo + red question mark or eye overlay + text "Co się stało?" or "Gdzie są?"

### 3.3 Kod Sukcesu (business)

**Scope (broader than just upadki!):**
- Sukcesy (Apple, Netflix, SpaceX, InPost, CD Projekt)
- Upadki (Borders, Blockbuster, Blackberry, Toys R Us)
- Rywalizacje (Apple vs Samsung, Pepsi vs Coca-Cola, Uber vs Lyft, Epic vs Apple)
- Kontrowersje (Cambridge Analytica, Dieselgate)

**Style notes:**
- Data-driven: revenue charts, market share, user growth
- Founder psychology + strategic decisions, not just numbers
- Show both sides (success requires failure analysis too)

**Thumbnail formula:** CEO portrait or logo + chart/arrow overlay + text "Sekret X" or "Jak X zrobił Y"

### 3.4 Cena Sławy (biographies)

**Examples:** muzycy (Krzysztof Krawczyk, Tupac, Cobain), aktorzy (River Phoenix, Heath Ledger), sportowcy (Maradona, Senna), przedsiębiorcy (Jobs, Musk, Nutella Ferrero), celebryci (Diana, Monroe).

**Style notes:**
- Cover rise AND fall. Avoid hagiography.
- Use private moments (interviews, letters) where possible
- Context of the era (not just the person)

**Thumbnail formula:** Portrait + era-typical background + text "Kim był X?" or "Koszt sławy"

---

## 4. Script template

```markdown
# [Tytuł]

## Hook (5 sekund)
[Jedno mocne zdanie, które sprawi, że widz nie scrolluje. Najlepiej pytanie lub szokujący fakt.]

## Kontekst (30 sekund)
[Kto? Co? Kiedy? Gdzie? Dlaczego w ogóle o tym mówić?]

## Tło (1-2 minuty)
[Co doprowadziło do momentu zero. Budowanie napięcia.]

## Moment zero (2-3 minuty)
[Właściwe wydarzenie. Tu jest climax. Detale, świadkowie, liczby.]

## Eskalacja (3-5 minut)
[Co się działo dalej. Reakcje, decyzje, błędy, szczęście.]

## Punkt zwrotny (3-5 minut)
[Co zmieniło bieg wydarzeń. Decyzja kluczowa, bohater, antybohater.]

## Skutki (2-3 minuty)
[Co z tego wynikło dla branzy / ludzi / świata.]

## Zamknięcie (30 sekund)
[Refleksja. Pytanie do widza. CTA: subów, like, komentarz.]
```

---

## 5. Thumbnail rules (universal + per-channel)

**Universal:**
- 1280×720 px
- JPG, max 4MB
- 3-element composition: subject (face/object) + emotion (text overlay) + context (background)
- Face/expression = hero (occupies left 60%)
- Text overlay: 2-3 words MAX, bottom 1/3, ALL CAPS, sans-serif, drop shadow
- High contrast background (saturated, complementary to text)
- Subject emotion = exaggerated (shock, fear, rage)

**Per-channel accents** (use as background tint or border):
| Channel | Accent |
|---|---|
| Błąd Krytyczny | red `#c41e3a` |
| Sprawa: Nierozwiązana | cold blue `#3a4a5c` |
| Kod Sukcesu | gold `#ffb700` |
| Cena Sławy | purple `#6a4c93` |

For full Nano Banana prompting rules (universal: max 4 inputs, no "keep exactly as shown", etc.) see `nano-banana-workflows/README.md`.

---

## 6. Voiceover guidelines (Polish)

- **Pace:**
  - True crime: wolny, przeciągły, napięcie
  - Katastrofy: dramatyczny, momenty ciszy
  - Biznes: rzeczowy, energiczny
  - Biografie: nostalgiczny, refleksyjny
- **Tone:** nigdy clickbait, szanuj fakty, unikaj spekulacji jako faktów
- **Sources:** w opisie podaj wszystkie źródła (ważne dla wiarygodności i SEO)

---

## 7. Existing assets

- `yt-historie/kursk/` — pre-worked example: Kursk submarine disaster
  - `skrypt_kursk.md` — script draft
  - `kursk_thumbnail_nb.png` — Nano Banana thumbnail test
- Use this as a reference for quality + tone

---

## 8. Tech stack & accounts

**YouTube accounts:** TBD (one per channel, or one brand account managing all 4?)

**AI tools:**
- Script: Claude Sonnet 4.5 or Opus 4.6 (via OpenClaw)
- Thumbnail: Nano Banana (via Higgsfield CLI) or GPT Image 2
- Voiceover: ElevenLabs (TTS), Polish voices
- B-roll: Kling 3.0 or Luma Dream Machine (via Higgsfield)

**API keys** (in workspace auth-profiles.json or .secrets):
- TBD — ElevenLabs not yet integrated
- Tavily (for research)
- Higgsfield (already integrated, see `nano-banana-workflows`)

---

## 9. Open items

| Item | Status | Action |
|---|---|---|
| YouTube account(s) | TBD | Decide: 4 separate or 1 brand account |
| Channel art / avatars | not started | Generate via Nano Banana (per-channel accent) |
| Intro/outro templates | not started | Generic for all 4 or per-channel |
| First 4 episodes scripts | not started | Pick topics, research, write |
| Upload schedule | TBD | Weekly per channel = 4 videos/week |
| SEO strategy | TBD | Polish keywords, tags, descriptions |

---

## 10. Related

- `nano-banana-workflows` — thumbnail generation rules (§2.5)
- Memory: `memory/2026-03-25.md` — original naming session
- Memory: `MEMORY.md` lines 64-71 — channel list (curated)

## 11. Brand spec at-a-glance

| Channel | Color | Tone | B-roll style |
|---|---|---|---|
| Błąd Krytyczny | red `#c41e3a` | dramatic dark | smoke, fire, debris |
| Sprawa: Nierozwiązana | cold blue `#3a4a5c` | noir suspense | archival, fog, BW |
| Kod Sukcesu | gold `#ffb700` | corporate clean | charts, office, skyline |
| Cena Sławy | purple `#6a4c93` | glam dramatic | portraits, era-typical |