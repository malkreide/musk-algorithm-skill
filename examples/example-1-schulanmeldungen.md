# Beispiel: Prozessanalyse Schulanmeldungen

## Ausgangslage

Das Schulamt der Stadt Zürich erhält jährlich ca. 3'500 Schulanmeldungen für die 1. Klasse. Der aktuelle Prozess umfasst 12 Schritte und dauert durchschnittlich 6 Wochen vom Eingang bis zur Bestätigung.

**Aktueller Prozess (vereinfacht):**

1. Eltern laden PDF-Formular von Website herunter
2. Eltern füllen Formular handschriftlich aus
3. Eltern senden Formular per Post oder scannen es ein und senden per E-Mail
4. Sekretariat empfängt und sortiert Anmeldungen
5. Sekretariat erfasst Daten manuell in Excel
6. Sekretariat leitet Excel an Schulkreis-Koordination weiter
7. Schulkreis-Koordination prüft Wohnort-Zuständigkeit
8. Schulkreis-Koordination erstellt Klassenzuteilungs-Vorschlag
9. Schulleitung genehmigt Klassenzuteilung
10. Schulkreis-Koordination erfasst finale Zuteilung in SchulDB
11. Sekretariat erstellt Bestätigungsbrief (Word-Vorlage)
12. Sekretariat druckt und versendet Brief per Post

**Problem:** Hoher manueller Aufwand, viele Medienbrüche, lange Wartezeiten.

---

## Analyse nach Musk-Algorithmus

### Schritt 1: Anforderungen hinterfragen

| # | Anforderung | Urheber | Problem das gelöst wird | Gesetzliche Grundlage? | Bewertung | Datenqualität |
|---|---|---|---|---|---|---|
| 1.1 | PDF-Formular | IT-Abteilung (2012) | "Einheitliches Layout" | Nein | 🔴 | 🔵 Belegt: IT-Doku vorhanden |
| 1.2 | Handschriftliche Ausfüllung | Unbekannt ("schon immer") | Keine klare | Nein | 🔴 | ⚪ Schätzung: Kein Urheber identifiziert |
| 1.3 | Post/E-Mail-Eingang | Datenschutz-Policy (2015) | Vermeidung Cloud-Tools | Ja (DSG ZH) | 🟢 | 🔵 Belegt: Rechtsgutachten liegt vor |
| 1.4 | Manuelle Excel-Erfassung | Sekretariat | "Zur Weiterverarbeitung" | Nein | 🔴 | 🔵 Belegt: Prozess dokumentiert |
| 1.5 | Wohnort-Prüfung | Schulkreis-Koordination | Korrekte Schulzuteilung | Ja (VSG §5) | 🟢 | 🔵 Belegt: Gesetzestext |
| 1.6 | Klassenzuteilungs-Vorschlag | Schulkreis-Koordination | Pädagogische Balance | Nein | 🟡 | ⚪ Schätzung: Benefit unklar |
| 1.7 | Genehmigung durch Schulleitung | Org-Reglement (2018) | "Vier-Augen-Prinzip" | Nein | 🟡 | 🔵 Belegt: Reglement vorhanden |
| 1.8 | Erfassung in SchulDB | IT-Abteilung | Datenhaltung für Schuljahr | Ja (VSM §12) | 🟢 | 🔵 Belegt: Verordnung |
| 1.9 | Word-Vorlage für Brief | Kommunikation (2010) | "Corporate Design" | Nein | 🟡 | 🔵 Belegt: CD-Richtlinie |
| 1.10 | Druck und Postversand | Kommunikation | "Offizieller Charakter" | Nein | 🔴 | ⚪ Schätzung: Keine Dokumentation |

**Erkenntnisse:**
- 🟢 **3 valide Anforderungen** (gesetzlich verankert)
- 🟡 **3 fragwürdige Anforderungen** (interner Ursprung, Nutzen unklar)
- 🔴 **4 Löschkandidaten** (kein klarer Urheber oder obsolet)

---

### Schritt 2: Löschen

#### Stakeholder-Analyse

| Löschkandidat | Betroffene Stakeholder | Art der Betroffenheit | Einbezug erforderlich? | Kommunikationsmassnahme |
|---|---|---|---|---|
| 1.1 PDF-Formular | Eltern, IT | Eltern müssen neues System nutzen | Ja | Information via Newsletter, Website-Update |
| 1.2 Handschriftlich | Eltern | Keine – digitale Eingabe ist einfacher | Nein | - |
| 1.4 Excel-Erfassung | Sekretariat | Arbeitslast reduziert sich | Ja | Schulung für neue Lösung |
| 1.6 Klassenzuteilungs-Vorschlag | Schulkreis-Koordination | Entscheidungskompetenz verschiebt sich | Ja | Workshop mit Koordination |
| 1.10 Postversand | Eltern, Sekretariat | Eltern erhalten E-Mail statt Brief | Ja | Opt-in für Postversand anbieten |

**Streichungen mit Begründung:**

- ✂️ **PDF-Formular** → Ersetzt durch Online-Formular (direkt in SchulDB)
- ✂️ **Handschriftliche Ausfüllung** → Digital ist effizienter und fehlerärmer
- ✂️ **Manuelle Excel-Erfassung** → Direkte Datenbankerfassung
- ✂️ **Postversand** → E-Mail-Versand (Opt-in für Post bleibt als Ausnahme)

**Behalten (mit Begründung):**

- ✅ **Wohnort-Prüfung** – Gesetzlich erforderlich
- ✅ **SchulDB-Erfassung** – Gesetzlich erforderlich
- ⚠️ **Genehmigung Schulleitung** – Behalten, aber Prozess vereinfachen (siehe Schritt 3)

**Reversibilitätsplan:**
- PDF-Formular: 1 Woche Reaktivierung möglich (liegt archiviert auf Server)
- Excel-Erfassung: Kann jederzeit als Backup reaktiviert werden (Template vorhanden)

---

### Schritt 3: Vereinfachen

#### Vorher-Nachher-Vergleich

| Vorher (12 Schritte) | Nachher (5 Schritte) |
|---|---|
| 1. PDF herunterladen<br>2. Handschriftlich ausfüllen<br>3. Scannen/Post<br>4. Sekretariat sortiert<br>5. Excel-Erfassung<br>6. Weiterleitung<br>7. Wohnort-Prüfung<br>8. Klassenzuteilung<br>9. Genehmigung SL<br>10. SchulDB-Erfassung<br>11. Brief erstellen<br>12. Druck/Versand | 1. **Online-Formular ausfüllen** (mit Adress-Autovervollständigung)<br>2. **Automatische Wohnort-Prüfung** (Geo-API)<br>3. **Automatische Klassenzuteilung** (Algorithmus mit SL-Review)<br>4. **Automatische E-Mail-Bestätigung**<br>5. **(Optional) Schulleitung prüft Ausnahmen** |

**Vereinfachungsmassnahmen:**

1. **Medienbruch eliminiert**: Papier → Online-Formular direkt in Datenbank
2. **Rollen konsolidiert**: Sekretariat + Schulkreis-Koordination → System (mit Ausnahme-Handling)
3. **Genehmigungskaskade verkürzt**: Schulleitung genehmigt nur noch Ausnahmen (z.B. auswärtige Kinder), nicht mehr alle Zuteilungen
4. **Dateneingabe-Redundanz eliminiert**: 1x Eingabe durch Eltern, keine manuelle Nacherfassung

---

### Schritt 4: Beschleunigen

**Wartezeiten-Analyse (Vorher):**

| Schritt | Wartezeit | Grund |
|---|---|---|
| Post-Eingang | 1-3 Tage | Postlaufzeit |
| Sekretariat-Erfassung | 2-5 Tage | Batch-Verarbeitung (wöchentlich) |
| Schulkreis-Prüfung | 1-2 Wochen | Wartezeit auf Koordinations-Meeting |
| Schulleitung-Genehmigung | 1 Woche | Wartezeit auf SL-Meeting |
| Brief-Versand | 1-3 Tage | Postlaufzeit |

**Gesamte Durchlaufzeit:** 3-6 Wochen

**Beschleunigungsmassnahmen:**

1. **Parallelisierung**: Wohnort-Prüfung + Klassenzuteilung passieren automatisch beim Formular-Absenden
2. **Echtzeit-Feedback**: Eltern erhalten sofort Bestätigung statt nach 6 Wochen
3. **Batch-Elimination**: Keine wöchentliche Verarbeitung mehr, sondern kontinuierlich
4. **Meeting-Reduktion**: Schulleitung prüft nur noch Ausnahmen (asynchron, bei Bedarf)

**Neue Durchlaufzeit:** < 24 Stunden (für Standardfälle)

---

### Schritt 5: Automatisieren

**Automatisierungsplan:**

| Schritt | Tool/Technologie | Priorität | Aufwand | Begründung |
|---|---|---|---|---|
| Online-Formular | Webflow / TypeForm | 🟢 Quick Win | 2-3 Tage | Einfach zu implementieren |
| Adress-Autovervollständigung | Google Places API | 🟡 Strategisch | 1 Woche | Reduziert Tippfehler |
| Wohnort-Prüfung (Geo) | OpenStreetMap API | 🟢 Quick Win | 3-5 Tage | Eliminiert manuelle Prüfung |
| Klassenzuteilungs-Algorithmus | Python-Script (Klassenkapazität + Geo) | 🟡 Strategisch | 2-3 Wochen | Komplex, aber hoher Nutzen |
| E-Mail-Bestätigung | SendGrid / Postmark | 🟢 Quick Win | 1 Tag | Standard-Integration |
| SchulDB-Anbindung | API-Integration | 🟡 Strategisch | 2-4 Wochen | Abhängig von DB-Architektur |

**Warnung:** Klassenzuteilungs-Algorithmus erst automatisieren, nachdem der manuelle Prozess 1 Schuljahr lang stabil gelaufen ist (Schritt-5-Regel).

---

### Zusammenfassung

**Erwartete Wirkung:**

- **Zeitersparnis (Sekretariat):** ~80% (von 40h/Jahr auf 8h/Jahr für Ausnahmen)
- **Zeitersparnis (Eltern):** 6 Wochen Wartezeit → 24h
- **Fehlerreduktion:** ~90% (keine manuelle Dateneingabe mehr)
- **Kostenreduktion:** ~CHF 12'000/Jahr (Druck, Porto, Arbeitszeit)

**Risiken:**

- Technisches Risiko: Ausfall des Online-Formulars → Lösung: PDF-Backup bleibt verfügbar
- Akzeptanzrisiko: Eltern ohne Internet-Zugang → Lösung: Opt-in für Papier-Anmeldung

---

### Quick-Win-Matrix

```
                      Hohe Wirkung
       ┌────────────────────┬────────────────────┐
       │  STRATEGISCH       │   QUICK WINS       │
       │                    │                    │
       │  • Klassenzuteilung│  • Online-Formular │
       │    -Algorithmus    │  • E-Mail-Versand  │
       │  • SchulDB-        │  • Geo-Prüfung     │
       │    Integration     │                    │
Hoher ─┼────────────────────┼────────────────────┼─ Niedriger
Aufwand│  VERMEIDEN         │   MITNEHMEN        │  Aufwand
       │                    │                    │
       │  • Umfassende      │  • Adress-         │
       │    Prozess-        │    Autovervoll-    │
       │    Neugestaltung   │    ständigung      │
       │                    │                    │
       └────────────────────┴────────────────────┘
                      Niedrige Wirkung
```

**Empfohlene Umsetzungsreihenfolge:**

1. **Sofort (1-2 Wochen):** Online-Formular + E-Mail-Bestätigung + Geo-Prüfung
2. **Mittel (3-6 Monate):** SchulDB-Integration + Adress-Autovervollständigung
3. **Langfristig (1-2 Jahre):** Klassenzuteilungs-Algorithmus (erst nach Bewährung des manuellen Prozesses)

---

**Nächste Schritte:**

1. GL-Entscheid: Freigabe für Quick-Wins (Budget: ~CHF 5'000 für Webflow + APIs)
2. Stakeholder-Information: Newsletter an Eltern (Februar 2026)
3. Pilot: 1 Schulkreis testet neuen Prozess (März 2026)
4. Rollout: Alle Schulkreise (Schuljahr 2026/27)
