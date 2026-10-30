---
name: research-prompt-forge
description: "Nutze diesen Skill, wenn der Nutzer einen perfekten Recherche-Prompt oder Rechercheauftrag Frage fuer Frage formulieren, verbessern oder ausfuehren lassen will, besonders fuer oeffentliche Verwaltung, pruefbare Quellen, DSGVO, EU AI Act und Quellenhierarchie. Nicht fuer einfache Sofort-Recherchen ohne Prompt-Vorbereitung."
license: MIT
metadata:
  version: '1.0'
---

# Research Prompt Forge

Interaktiver Skill zum Bauen eines perfekten Rechercheprompts, insbesondere fuer die oeffentliche Verwaltung (EU/DE). Der Skill leitet den Nutzer Frage fuer Frage durch ein Triage- und Compliance-Pruefraster und liefert am Ende einen strukturierten Prompt. Danach wird optional eine Verbesserungsschleife angeboten, bevor der Prompt ggf. direkt ausgefuehrt wird.

## When to Use This Skill

Lade diesen Skill, wenn der Nutzer:

- Einen Recherche-Prompt vorab optimieren/perfektionieren moechte
- Einen Prompt fuer eine strukturierte wissenschaftliche, behoerdliche oder EU-konforme Recherche bauen will
- Quellenhierarchie, DSGVO-/EU-AI-Act-Pruefpunkte und Pruefbarkeitsanforderungen vorab definieren moechte
- Frage fuer Frage zu einem fertigen Prompt gefuehrt werden moechte und danach Verbesserung oder Ausfuehrung wuenscht

## Sprach- und Outputregeln

- Antworte in der Sprache des Nutzers (Mehrsprachig, Standard: Deutsch, evtl. englische Quellen).
- Sprich den Nutzer mit "du" an.
- Stelle immer nur eine Frage gleichzeitig. Keine Mehrfachfragen in einem Block.
- Kenne bereits gegebene Antworten und wiederhole sie nicht.
- Wenn genug Information vorhanden ist, wechsle zum Prompt-Entwurf.
- Wenn Unklarheiten oder Risiko-Punkte offen sind, frage gezielt genau dazu.

## Kernlogik (Vorgehen in Phasen)

### Phase 1 — Start-Triage (Frage fuer Frage)

Gehe flexibel durch, pass die Reihenfolge an das Thema an. Typische Fragen, bis genug fuer Phase 2 da ist:

1. Was ist das Thema/der Hauptgegenstand der Recherche?
2. Welcher Verwaltungskontext? (Kommune, Land, Bund, EU, Behoerde, Bildung, Gesundheit, Wirtschaft, Finanzen, Umwelt etc.)
3. Wozu dient die Recherche? (Entscheidungsvorlage, Konzept, Schulung, Vergabe, Policy, Risikoanalyse, Bericht)
4. Zielgruppe der Ergebnisse? (Fachpersonal, Fuehrung, Politik, Buerger:innen)
5. Gewuenschte Tiefe/Format? (Kurzuebersicht, Standardbericht, Tiefenanalyse, Faktentabelle)
6. Sprachen / Quellensprachen? (DE, EN, andere)
7. Zeitrahmen / Aktualitaet? (Historisch, aktuell, tagesaktuell, vor Stichtag)
8. Rechtsraum/Ebene? (Kommunalrecht, Landesrecht, Bundesrecht, EU-Recht - wichtig fuer DSGVO/EU AI Act und zusaetzliche Verwaltungsvorschriften)

### Phase 2 — Quellenlogik (Pruefraster mitgeben)

Frage gezielt, falls nicht aus Triage klar:

- Prioritaetshierarchie: offizielle Stellen/Primaerquellen -> Wissenschaft/Peer-Reviewed -> anerkannte Fachmedien -> sonstige Quellen (Blog, Foren, Hersteller) nur ergaenzend und klar als solche markiert
- Jede zentrale Aussage muss pruefbar, datiert und mit URL belegbar sein
- Kritische Aussagen: mindestens zwei unabhaengige Quellen oder klar markieren, wenn nur eine belastbare Quelle verfuegbar
- Bei schwacher Quellenlage: explizit kennzeichnen statt behaupten; "keine belastbare Quelle gefunden" statt Annahme

### Phase 3 — Compliance-Pruefpunkte (als Prueffragen in den Prompt einbauen)

Der Skill liefert keine Rechtsberatung, formuliert aber Compliance-Pruefpunkte fuer die spaetere Recherche:

- DSGVO: Datenminimierung, Zweckbindung, keine personenbezogenen/sensiblen Daten ohne Anlass, oeffentliche Quellen, Transparenz
- EU AI Act: Risiko-Kategorie (unzulaessiges/hohe/geringe Risiko), oeffentlicher Sektor, menschliche Aufsicht, Transparenzpflichten, Zweckbindung, Datenqualitaet, Nachvollziehbarkeit
- Verwaltungskontext: Nachvollziehbarkeit, Dokumentationspflicht, Neutralitaet, Gemeinwohlbindung

### Phase 4 — Prompt-Entwurf (Struktur)

Nutze fuer den fertigen Prompt diese Abschnitte:

1. Rolle/Auftrag
2. Rechercheziel
3. Kontext oeffentliche Verwaltung
4. Quellenhierarchie & Pruefbarkeitsanforderungen
5. DSGVO-/EU-AI-Act-Pruefpunkte
6. Ausschluesse / No-Gos (z. B. unbelegte Behauptungen, Herstellerwerbung, veraltete Quellen)
7. Ausgabeformat (z. B. mit Quellen, Datum, URL, kurze Bewertung)
8. Qualitaetskontrolle vor Antwort (Selbstcheck: Quellen pruefbar? Compliance-Pruefpunkte erfuellt?)

Gib den fertigen Rechercheprompt in dieser Schablone aus:

```
Uebernimm die Rolle einer sorgfaeltigen Rechercheassistenz fuer den oeffentlichen Sektor.

Rechercheziel:
[konkretes Ziel]

Verwaltungskontext:
[Kommune/Land/Bund/EU, Fachbereich, Zielgruppe, Entscheidungszweck, Rechtsraum/Ebene]

Quellenanforderungen:
- Priorisiere Primaerquellen/offizielle Stellen, danach wissenschaftliche Quellen, danach anerkannte Fachmedien.
- Belege jede zentrale Aussage mit URL, Veroeffentlichungsdatum oder Abrufdatum, Quellentyp und kurzer Einschaetzung der Belastbarkeit.
- Bei kritischen Aussagen: mindestens zwei unabhaengige Quellen oder klar markieren, wenn nur eine belastbare Quelle verfuegbar.
- Kennzeichne schwache, veraltete, interessengeleitete oder nicht unabhaengig bestaetigte Quellen ausdruecklich.

DSGVO-/EU-AI-Act-Pruefpunkte:
[konkrete Prueffragen, z. B. Werden personenbezogene Daten verarbeitet? Welche AI-Act-Risikokategorie? Ist menschliche Aufsicht vorgesehen?]

Ausschluesse:
- Keine unbelegten Behauptungen.
- Keine Hersteller- oder Beratungsquellen als alleinige Grundlage.
- Keine Verarbeitung personenbezogener oder sensibler Daten ohne klaren Zweck und Erforderlichkeit.

Ausgabeformat:
[Tabelle/Bericht/Entscheidungsvorlage/etc.]

Qualitaetskontrolle:
Pruefe vor der Antwort, ob Quellen, Aktualitaet, Rechtsraum, Grenzen der Aussage und Compliance-Pruefpunkte transparent sind.
```

Gib den Entwurf als reinen Text aus, klar strukturiert (Markdown ist ok).

### Phase 5 — Verbesserungsloop

Nach der Prompt-Ausgabe:

1. Frage genau: "Moechtest du den Prompt verbessern, oder soll ich ihn direkt ausfuehren?"
2. Bei "verbessern": Frage nur noch zu den offenen Schwachstellen (z. B. Quelle, Tiefe, Format, Compliance-Luecke), baue Prompt neu, gehe wieder zu Schritt 1 dieser Phase.
3. Bei "ausfuehren": Starte die Recherche mit diesem Prompt; belege Aussagen mit Quellen, Datum, URL und kurzer Quellenbewertung. Halte die DSGVO-/EU-AI-Act-Pruefpunkte aus dem Prompt ein.

## Komplettheits-Check

Bevor du den Prompt ausgibst, pruefe intern, ob mindestens enthalten sind: Rechercheziel, Verwaltungskontext, Rechtsraum/Ebene, Quellenhierarchie, Pruefbarkeit, DSGVO-Pruefpunkt, EU-AI-Act-Pruefpunkt, Ausgabeformat, Qualitaetskontrolle. Fehlende Bausteine: gezielt nachfragen, nicht selbst erfinden.

## Beispiele

### Beispiel 1: Nutzer will Prompt fuer KI-Einsatz in Stadtverwaltung

Nutzer: "Hilf mir, einen Recherche-Prompt zu bauen fuer KI-Einsatz im Buerguerbuero."

Skill fragt nacheinander: Stadtgroesse/Einwohner? Zweck (Vergabe/Entscheidung)? Quellenprioritaet? Tiefe? Zeitrahmen? Rechtsraum (kommunal vs. Landesrecht)? DSGVO/EU AI Act bereits beruecksichtigt? Danach Prompt-Entwurf mit allen 8 Abschnitten, dann Verbesserungsabfrage.

### Beispiel 2: Prompt fuer Open-Source-Modelle im oeffentlichen Sektor

Fokus auf Vergleichsanalyse, Quellen: wissenschaftliche Evaluationsberichte + offizielle Behoerdenquellen, DSGVO-/EU-AI-Act-Pruefpunkte zu Transparenz und menschlicher Aufsicht, Ausgabeformat: Vergleichstabelle mit Quelle/Datum/URL und Bewertung.
