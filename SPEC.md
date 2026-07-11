# SPEC.md — Persönliche Website v1

Status: Entwurf. Alles unter „Locked" wird nicht mehr diskutiert.
Alles unter „Von Marek zu füllen" blockiert den Bau.

---

## 1. Zweck

Positionierungsseite. **Keine** Bewerbungsseite, **kein** Blog, **kein** Lebenslauf im Web-Format.

Sie soll passiv für zwei Zielgruppen funktionieren:

- **A — Entscheider im Mittelstand / Fachcommunity:** „Der versteht unser Problem und kann liefern."
- **B — Potenzielle Arbeitgeber:** „Den will ich sprechen."

Konsequenzen aus dem Doppel-Zielgruppen-Kompromiss (bewusst gewählt):

- **Kompetenz vor Charme.** Reihenfolge ist Teil der Spec, nicht Geschmack.
- **Kein „open to work"-Signal.** Kein „suche neue Herausforderung", kein Verfügbarkeitsdatum.
  Die Seite sagt *wofür ich stehe*, nicht *stellt mich ein*. Das funktioniert für beide
  Zielgruppen und ist gegenüber dem aktuellen Arbeitgeber unproblematisch.
- Sprache: **Deutsch.** Kein i18n in v1.

---

## 2. Kernaussage (These)

> **Ich mache messbar, was andere nach Gefühl machen.**

Trägt Hero, Positionierung und Werdegang. Wird **nirgends behauptet** — sie wird durch
konkrete Belege sichtbar oder sie steht nicht.

Sport und Kulinarik argumentieren die These **nicht**. Ihr Job ist ein anderer (→ §4.4).
Wenn sie konkret genug geschrieben sind, belegen sie die These beiläufig. Das ist stärker,
als sie zu behaupten.

---

## 3. Struktur (One-Pager, Reihenfolge ist normativ)

```
1  Hero            Name · eine Zeile Positionierung · Kontakt
2  Positionierung  3–5 Sätze. Was ich mache, für wen, mit welchem Ergebnis.
3  Werdegang       Stationen. Wirkung statt Aufgabenbeschreibung.
4  Persönliches    Sport · Kulinarik. Kurz.
5  Kontakt         mailto · LinkedIn · optional CV-PDF
```

Keine separate Projekt-/Portfolio-Sektion in v1. Belege leben **als Einzeiler in §2 und §3**
(z. B. Thesis, stellenradar, Geschmackslabor). Projektseiten sind v2-Kandidat, jetzt out of scope.

---

## 4. Inhaltliche Anforderungen

### 4.1 Gilt für jede Sektion

- **Austauschbarkeitstest (hartes Abnahmekriterium):** Jeden Satz einzeln prüfen.
  *Könnte ein beliebiger anderer AI-Consultant mit Sport- und Kochhobby diesen Satz
  über sich schreiben?* Wenn ja → streichen oder konkretisieren, bis er nur über mich wahr ist.
- **Mindestens ein verifizierbarer Beleg pro Sektion.** Eine Zahl **oder ein Artefakt** —
  etwas, das existiert und das ein Skeptiker prüfen könnte: ein Tool, das läuft. Eine Note.
  Eine Publikation. Ein gebautes Ding ist ein ebenso guter Beleg wie ein KPI.
- **Keine erfundene Zahl. Niemals.** Lieber gar keine Zahl als eine plausible.
  Wo keine Messung existiert, wird das Artefakt genannt — nicht geschätzt.
- **Vorlesetest:** Laut lesen. Klingt es wie ich in einem Gespräch? Sonst umschreiben.
- Aktiv statt Passiv. Zahlen statt Adjektive. Kurze Sätze.

### 4.2 Verbotene Formulierungen (nicht verhandelbar)

`leidenschaftlich` · `ganzheitlich` · `Mehrwert` · `Synergien` · `Digital Native` ·
`Ich brenne für …` · `In meiner Freizeit …` · `Es ist wichtig zu betonen, dass …` ·
jede Hobby-Aufzählung · jeder Satz, der mit „Als …" beginnt

### 4.3 Werdegang

Pro Station: **Was war das Problem, was habe ich gebaut oder verändert, was davon ist heute
noch überprüfbar.**

Realität: Für die zurückliegenden Stationen existieren keine sauberen Vorher-/Nachher-Messwerte.
Das wird **nicht** durch geschätzte Prozentzahlen kaschiert. Der Beleg ist dann das Artefakt und
die Konkretheit der Beschreibung — nicht eine Zahl, die niemand nachrechnen kann.

Keine Aufgabenlisten. Lücken und Umwege werden nicht kaschiert — sie sind der interessante Teil.

**Ab jetzt gilt:** Vor jedem Projekt Baseline festhalten, nachher messen. Nicht für diese
Website — dafür, dass die Belege in zwölf Monaten existieren.

### 4.4 Persönliches (Sport · Kulinarik) — Job: „menschlich abholen"

Operationalisierung, weil „menschlich" allein kein Abnahmekriterium ist:

- **Menschlichkeit entsteht durch Spezifität, nicht durch Themenwahl.**
  „Ich koche und laufe gern" holt niemanden ab. Ein konkretes, leicht unvorteilhaftes,
  wahres Detail schon.
- **Mindestens eine Reibung oder ein Scheitern pro Sektion.** Erfolgsmeldungen sind
  nicht menschlich, sie sind Marketing.
- **Länge: max. 120 Wörter pro Sektion.** Wärme braucht keine 500 Wörter.
  Zu lang = selbstverliebt = Gegenteil des Ziels.
- Kein Ton, der Kompetenz untergräbt. Selbstironie ja, Selbstabwertung nein.
- Je Sektion max. 1 Bild. Echtes eigenes Bild oder keins. Kein Stock.

### 4.5 Autorschaft (nicht verhandelbar)

Alle Texte schreibt Marek. Das Modell **redigiert, kürzt, streicht, widerspricht und verhört** —
es erfindet nicht.

Grund, unabhängig vom Stil: Die Spec verlangt echte Zahlen und echtes Scheitern. Das Modell
kennt sie nicht. Es müsste sie erfinden. Erfundene Belege auf einer Seite, deren einziger Zweck
Glaubwürdigkeit ist, sind der teuerste Fehler, den dieses Projekt machen kann.

---

## 5. Design-Richtung (Leitplanken, kein Endzustand)

Richtung: **Messprotokoll.** Die Ästhetik technischer Dokumentation — nüchtern, präzise,
nichts Dekoratives.

- **Signature-Element: die Zahlen.** Jede Sektion trägt eine echte Messgröße. Sie sind das
  Einzige, was optisch heraussticht. Das ist die visuelle Übersetzung der These.
- Typografie trägt die Seite: humanistische Grotesk für Fließtext, Monospace für Zahlen,
  Daten, Labels. Zwei Schnitte, mehr nicht.
- Eine einzige Signalfarbe, funktional eingesetzt (Links, aktive Zustände). Sonst Papier/Schwarz.
- Keine Gradients. Keine Hero-Illustration. Keine Scroll-Animationen. Kein Parallax.
- Einspaltig, linksbündig, großzügiger Weißraum.

**Explizit unerwünscht** (das sind die Defaults, die jede KI-gebaute Seite gerade produziert):
Creme-Hintergrund + hoher Serif + Terrakotta-Akzent · Fast-Schwarz + Neongrün · Zeitungslayout
mit Haarlinien. Wenn der Plan in eine dieser Richtungen kippt: zurückweisen.

Der Agent liefert das Token-System (4–6 Hex-Werte, 2 Schriftschnitte, Typo-Skala) im **PLAN.md**.
Ich reviewe es, bevor Code entsteht.

---

## 6. Tech (Locked — nicht neu diskutieren)

- Astro (Static, kein SSR)
- Tailwind
- Cloudflare Pages
- Kein Framework-JS. Kein React. Kein clientseitiges JS außer, wenn es ohne nicht geht.
- Repo: GitHub, Deploy via Cloudflare-Git-Integration.

---

## 7. Non-Goals (v1)

- ❌ Blog. **Erst wenn drei fertige Texte in der Schublade liegen.** Ein Blog mit zwei Posts
  signalisiert „aufgegeben", nicht „aktiv".
- ❌ CMS, Headless-CMS, Notion-Anbindung
- ❌ Dark-Mode-Toggle
- ❌ i18n / englische Version
- ❌ Kontaktformular mit Backend (`mailto:` reicht)
- ❌ Analytics-Suite
- ❌ Eigenes Design-System
- ❌ **Ein neuer Skill oder ein neues Tool für dieses Projekt.** Kein `website-generator`.

---

## 8. Definition of Done

- [ ] `npm run build` grün
- [ ] Lighthouse ≥ 95 in allen vier Kategorien
- [ ] Kein toter Link
- [ ] Mobil lesbar (375 px), Tastaturfokus sichtbar
- [ ] Deployed auf Cloudflare Pages, eigene Domain
- [ ] **Jeder Text besteht Austauschbarkeits- und Vorlesetest**
- [ ] Jeder Commit einzeln gelesen und verstanden. Kein gemergter Code, den ich nicht erklären kann.

---

## 9. Inhalte

Stand: **2 von 6 fertig.** Was fertig ist, ist final — von Marek geschrieben, von mir nur gekürzt.

### 9.1 Kulinarik — ✅ FINAL

> Seit sechs Jahren Sauerteig. Für den ersten Starter habe ich zwei Anläufe gebraucht.
> Inzwischen backe ich Brote mit bis zu 80 % Hydration.
>
> Neulich hat die Hitzewelle meine Kultur gekippt. Ich suche gerade neues Anstellgut.

Nicht anfassen. Kein Bogen zur Arbeit, keine Moral, kein „das lehrt einen Demut".
Die 80 % erledigen das allein.

### 9.2 Sport — ✅ FINAL

> Seit zwei Jahren wieder Kraftsport, inzwischen mit Cardio ergänzt.
> Habacher Firmenlauf, 5 km in 23:43. Bei Hitze.

„wieder" bleibt unerklärt stehen. Das Wort trägt die Reibung. Nicht auflösen, nicht streichen.

### 9.3 Belege für §2/§3 — 1 von 3

- [x] **Thesis** — LLM-Soziopragmatik in deutscher Geschäftskommunikation. 1,0.
      Publikation JICD 2026. Existiert, prüfbar. Locked.
- [ ] **stellenradar** — Python/GitHub Actions, dedupliziert, Match-Scoring.
      Offen: *Was ist rausgekommen?* Eine Zahl, die du heute nachschlagen kannst.
- [ ] **Kandidat 3** — offen. Test: *Was existiert, weil es dieses Ding gibt?*
      Keine Antwort → kein Beleg.

Gestrichen: Geschmackslabor. Exploriert, nie damit gekocht. Hätte den Test nicht bestanden.

### 9.4 Werdegang — ❌ OFFEN

Pro Station drei Zeilen. Format ist bindend:

    Problem:             was lag im Argen
    Gebaut/verändert:    was ich konkret getan habe
    Heute überprüfbar:   was davon noch existiert (Artefakt ODER Zahl — nie geschätzt)

- [ ] Krämer IT Cloud Services — AI Consultant
- [ ] Umwelt-Campus Birkenfeld — B.A. Umwelt- und Betriebswirtschaft
- [ ] Smart InsurTech AG — CRM-Plattformberatung, ~3 Jahre
- [ ] PwC Luxembourg — Audit, deutsche Investmentfonds
- [ ] Bayerische Landesbrandversicherung — Digitalisierungsprojekt.
      *Das selbstgebaute Excel-Gehaltscontrolling ist ein Artefakt. Was ging vorher nicht?*

Wo keine Messung existiert: Artefakt nennen, nicht schätzen (→ §4.3).

### 9.5 Positionierung — ❌ OFFEN, zuletzt

3–5 Sätze. Wird **nach** dem Werdegang geschrieben. Sie ist die Abstraktion über 9.1–9.4,
nicht deren Vorwort.

Nicht vom Modell zu schreiben (→ §4.5). Auch nicht „als Entwurf zum Anpassen".

### 9.6 Domain — ❌ OFFEN, 60-Sekunden-Entscheidung

Regel: `vorname-nachname.de`. Kein Kunstname, keine `.ai`/`.io`-Spielerei, kein Wortwitz.
Dauert es länger als eine Minute, ist es Prokrastination.

---

## 10. Release-Gate

**Die Bau-Sperre aus der Vorversion war zu breit.** Sie sollte Lorem Ipsum verhindern,
nicht den Start. Korrigiert:

**v0.1 — jetzt bauen.**
Hero (Name + Kontakt) · Kulinarik · Sport · Kontakt.
Echter Content, kein einziger Platzhalter. Deploy auf die `*.pages.dev`-Preview-URL.
Kein Werdegang, keine Positionierung, keine Domain.

**v1.0 — Release.**
Werdegang und Positionierung landen als zwei weitere Commits. Erst dann zeigt die Domain
auf die Seite.

**Die Domain ist das Gate, nicht das Startsignal.** Solange 9.4 und 9.5 offen sind, läuft die
Seite auf einer URL, die niemand kennt. So kommt nie ein Platzhalter live — und du fängst
trotzdem heute an.
