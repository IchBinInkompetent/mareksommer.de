# PLAN.md — v0.1 (Umfang exakt SPEC §10)

Baut: Hero (nur Name + Kontaktlink) · Sport · Kulinarik · Kontakt.
Text-only, keine Bilder. Deploy auf `*.pages.dev`. Nicht mehr.

---

## 1. Entscheidungen aus dem Q&A (fixiert)

- Hero: **nur Name**, keine Rolle, keine These, keine Tagline.
- Kontakt: **zwei Blöcke** — kleiner Link im Hero, ausführliche Sektion am Ende.
- Bilder: **keine** in v0.1.
- Sektions-Labels: **ja**, Monospace, Versalien (`SPORT`, `KULINARIK`, `KONTAKT`).
- E-Mail: `mareksommer39@gmail.com` · LinkedIn: `linkedin.com/in/marek-sommer-40a132295`
- CV-PDF: nicht in v0.1 (Werdegang offen → nichts zu verlinken).

**Eine Abweichung, bitte bestätigen:** §10 listet „Kulinarik · Sport", §3 sagt aber
„Reihenfolge ist normativ" und ordnet „Sport · Kulinarik". Ich folge §3:
**Sport vor Kulinarik.** §10 lese ich als Aufzählung des Umfangs, nicht als Reihenfolge.

---

## 2. Token-System

### 2.1 Farben — 5 Hex-Werte

| Token      | Hex       | Verwendung                                          |
|------------|-----------|-----------------------------------------------------|
| `paper`    | `#FCFCFC` | Hintergrund. Neutralweiß — bewusst kein Creme (§5). |
| `ink`      | `#1A1A1A` | Fließtext, Name.                                    |
| `muted`    | `#6E7178` | Sektions-Labels, Metatext.                          |
| `signal`   | `#0B57D0` | Links, Fokus-Ring. Die einzige Farbe.               |
| `signal-d` | `#073B8F` | Hover/Aktiv-Zustand von `signal`.                   |

Nüchternes Instrumenten-Blau statt Terrakotta oder Neongrün — funktional
(jeder erkennt es als Link), nichts Dekoratives. Kein Grün, kein Serif-Umfeld,
keine Haarlinien: Sektionen trennt Weißraum, nicht Border.

### 2.2 Schrift — 2 Schnitte, 2 Dateien

| Schnitt                 | Rolle                                        |
|-------------------------|----------------------------------------------|
| **Fira Sans Regular**   | Fließtext, Name. Humanistische Grotesk.      |
| **Fira Mono Regular**   | Zahlen, Labels, Kontaktzeilen.               |

- Selbst gehostet als woff2 (latin-Subset), `font-display: swap`, Preload.
  Kein Google-Fonts-Request → Lighthouse & Datenschutz.
- **Kein Bold-Schnitt.** Hierarchie entsteht durch Größe, Farbe und die beiden
  Schriften — nicht durch Gewicht. Das ist die strenge Lesart von „zwei Schnitte,
  mehr nicht" (§5).
- Zahlen im Fließtext („80 %", „23:43", „5 km") werden in Mono gesetzt — sie
  stechen dadurch heraus, ohne eingefärbt zu werden. Das ist das Signature-Element.
- Fallbacks: `system-ui` / `ui-monospace`.

### 2.3 Typo-Skala — 4 Stufen

| Stufe     | Größe               | Zeilenhöhe | Verwendung                              |
|-----------|---------------------|------------|------------------------------------------|
| `label`   | 0.8125rem (13 px)   | 1.4        | Mono, Versalien, +0.08em Laufweite      |
| `body`    | 1.0625rem (17 px)   | 1.65       | Fließtext                                |
| `lead`    | 1.375rem (22 px)    | 1.4        | reserviert (v0.1 ungenutzt, v1: Positionierung) |
| `display` | 2.125rem (34 px)    | 1.15       | Name im Hero                             |

Layout: einspaltig, linksbündig, `max-width: 40rem`, großzügige vertikale
Abstände zwischen Sektionen (~6rem Desktop, ~4rem mobil). Ab 375 px lesbar.

---

## 3. Dateistruktur

```
mareksommer.de/
├── SPEC.md
├── PLAN.md
├── package.json
├── astro.config.mjs              # Astro static + Tailwind-v4-Vite-Plugin
├── public/
│   ├── fonts/
│   │   ├── fira-sans-regular.woff2
│   │   └── fira-mono-regular.woff2
│   └── favicon.svg               # schlicht: „MS" in Mono, ink auf paper
└── src/
    ├── styles/global.css         # @font-face, Tokens (@theme), Basis, Fokus-Stile
    ├── layouts/Base.astro        # <html lang="de">, <head>, Meta, Font-Preload
    └── pages/index.astro         # kompletter One-Pager, alle vier Sektionen
```

Bewusst **keine Komponenten**: vier Sektionen auf einer Seite rechtfertigen
keine Abstraktion, und jeder Commit bleibt vollständig lesbar (DoD §8).
Kein clientseitiges JS — null Script-Tags.

Meta für v0.1: `<title>Marek Sommer</title>`, Description „Marek Sommer — persönliche
Seite." (bewusst inhaltsleer, bis die Positionierung existiert; keine erfundene Aussage).

---

## 4. Commit-Reihenfolge

Jeder Commit einzeln baubar (`npm run build` grün) und einzeln reviewbar:

1. `chore: Astro-Minimal-Scaffold + Tailwind` — leere Seite, Build grün.
2. `feat: Design-Tokens, Fonts, Base-Layout` — global.css, Base.astro, woff2-Dateien.
   → Nach diesem Commit ist das Token-System im Browser prüfbar.
3. `feat: Hero — Name + Kontaktlink` — Link springt zur Kontakt-Sektion.
4. `feat: Sport & Kulinarik` — Texte **wörtlich** aus SPEC §9.2/§9.1, keine Redaktion.
5. `feat: Kontakt-Sektion` — mailto + LinkedIn (`rel="me noopener"`).
6. `chore: Favicon, Meta, A11y-Feinschliff` — Fokus-Ringe, Kontrast-Check, 375-px-Test.

Danach:
7. `git init` + Push auf GitHub → Vorschlag: Repo `IchBinInkompetent/mareksommer.de`,
   **public** (Cloudflare-Git-Integration ist mit public am reibungslosesten; private geht auch — sag was dir lieber ist).
8. **Cloudflare Pages verbindest du selbst** (Konto-Login liegt außerhalb meines
   Zugriffs): Dashboard → Workers & Pages → Create → Git-Repo wählen,
   Framework-Preset „Astro", Build `npm run build`, Output `dist`.
   Ergebnis: `mareksommer-de.pages.dev` (o. ä.) — die Preview-URL aus §10.

Keine Domain, kein Werdegang, keine Positionierung. Alles Weitere ist v1.0.

---

## 5. Abnahme v0.1 (Teilmenge DoD §8)

- [ ] `npm run build` grün
- [ ] Lighthouse ≥ 95 (alle vier Kategorien, auf der pages.dev-URL)
- [ ] Kein toter Link (mailto, LinkedIn, Anker)
- [ ] 375 px lesbar, Tastaturfokus sichtbar
- [ ] Texte §9.1/§9.2 zeichengenau übernommen
