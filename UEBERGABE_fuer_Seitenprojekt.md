# Übergabe: DNA-Matches-Seite — für das Seitenprojekt

**Stand:** 2026-04-18
**Zweck:** Dieses Dokument informiert das Seitenprojekt (Pilz-Chronik Webseite, Layout und Gestaltung) über die DNA-spezifischen Fakten und Regeln, damit Layoutarbeit die Inhalte nicht versehentlich kaputt macht.

## Rollenverteilung

**Fachprojekt DNA (separate Claude-Session, Arbeitsordner `DNA AHNENFORSCHUNG`):**
- Ist inhaltlich zuständig für alle DNA-Aussagen der Seite.
- Verwaltet die Quelldaten (GEDmatch, FTDNA, Ancestry, One-to-One-Vergleiche, Tier-1-Triangulationen).
- Prüft und autorisiert inhaltliche Änderungen an DNA-Passagen.

**Seitenprojekt (hier, Ordner `Pilz-Chronik/dna-matches`):**
- Zuständig für Layout, Gestaltung, CSS, Responsiveness, Navigation, Bildeinbindung, Accessibility, Druckansicht.
- Darf Wortlaut und Tonalität verfeinern — aber **Zahlen, Namen, Kits, Chromosom-Positionen, cM-Werte, SNP-Zahlen und Aussagen über Triangulationsgruppen NICHT** ändern, ohne Rücksprache mit dem DNA-Projekt.
- Bei Unsicherheit ob eine Änderung inhaltlich ist: im Zweifel als inhaltlich behandeln.

## Sprachregel: erste Person

Die Seite wird in der Ich-Form von Wolfgang Pilz geschrieben. Nicht: „Wolfgang teilt…", „Wolfgang ist 1–2 Gen. ferner". Sondern: „ich teile…", „ich bin 1–2 Gen. ferner". Ausnahmen sind zulässig bei:
- Bildunterschriften und Labels (Tabellenzellen, Badges, alt-Texte)
- Technischen Vergleichsetiketten in DNA-Notation (z.B. `Pilz↔Z.` oder `Wolfgang↔Z.` als Kurzform für einen One-to-One-Vergleich)
- Der Selbstvorstellung („Mein Name ist Wolfgang Pilz.")

## Änderungen am 2026-04-18

Das DNA-Projekt hat folgende inhaltliche Fehler korrigiert (die vorherige Version war an mehreren Stellen falsch):

**1. Herbert E. Fisher ist NICHT Teil der Chr-9-Kleinsegmentgruppe.**
- Alte Seite behauptete, Fisher erscheine in Tier-1 bei 136 Mb. Das ist falsch: Fisher kommt in Tier-1 null Mal vor.
- Die 136-Mb-Angabe stammt aus dem One-to-One Zeisl↔Fisher (13.4.2026): Chr 9, 136.807.238–138.026.999, 7,8 cM, nur 417 SNPs.
- Diese Position liegt ausserhalb der Kleinsegmentgruppe (2,6M–5,3M).
- Zwischen mir (Wolfgang, Kit QU4148768) und Fisher gibt es **kein** Chr-9-Segment, nur eines auf Chr 13 (92.913.176–97.586.348, 10,3 cM).
- Fisher-Zeile aus der Tabelle entfernt, Fisher-Badge aus Chr-9-Gruppe entfernt, JS-Daten aktualisiert (triangulation: false, chr: 'Chr 13', kit: 'T725386').

**2. Renee F. IST in der Chr-9-Kleinsegmentgruppe.**
- Segmentdaten aus Tier-1 eingetragen: Kit M524793, Segment 2.746.548–5.317.534, 7,5 cM (Zeisl↔Renee F., aus Tier-1-Triangulation).

**3. Schönberg-Absatz entmärchenhaft.**
- Alt: „Im April 2026 bestätigte die Familie die Bereitschaft zur Zusammenarbeit… Abgleich der Stammbäume in Vorbereitung."
- Neu: „Ich habe E. Randol Schönberg angeschrieben, er hat geantwortet. Damit besteht Kontakt — mehr ist zum jetzigen Stand nicht."

**4. Dritte-Person-Stellen in Ich-Form umgeschrieben** (Zeilen 603, 938, 1084 sowie JS-Note zu Walter Steven Z.).

## DNA-Kernfakten — nicht ohne Rücksprache ändern

### Bestätigte Chr-9-Kleinsegmentgruppe (Position 2,6M–5,3M)
5 Personen im kleinen Segment per One-to-One verifiziert (6 inkl. mir): Wolfgang (QU4148768), Walter Steven Zeisl (T405845), petctdoc (T093054), Reeva Jacobson Kimble (T286556), Renee Fisher (M524793). Bestätigt bei FTDNA UND GEDmatch. Kimble bleibt Gruppenmitglied, aber als MRCA verworfen (Herkunft Lomza/Mir). Victor Neumann (T080523) hat ebenfalls Chr-9-Segment (1.866.537–7.375.925, 12,7 cM, 2.075 SNPs, One-to-One 14.4.2026). Sechs weitere Personen haben Tier-1-Belege ohne eigenen One-to-One-Lauf: Irving G., Aaron Oscar K., Pearl F., Judy A. R., Mark K., Shoshanna A.

### Grosssegment Chr 9 (76M–96M)
Zeisl↔Wolfgang-One-to-One: 29,1 cM (4.843 SNPs), im Abschnitt 76,4M–95,8M. Triangulation 12.4.2026 (Greer, Jovings, Cohen) bestätigt. Drei Sub-Cluster. Nur Zeisl matcht auf beiden Chr-9-Segmenten (klein + gross).

### Fischer-Linie (eigenständig, NICHT Teil der Chr-9-Gruppe)
Zeisl↔Fisher: 56 cM auf 6 Segmenten (One-to-One 13.4.2026). Segmente auf Chr 2, 3, 9, 10, 12, 14. Grösstes: Chr 14, 12,7 cM, 2.867 SNPs. Das Chr-9-Segment dieser Paarung (136,8M–138,0M) liegt ausserhalb der Kleinsegmentgruppe und ist SNP-arm (417). Mit mir teilt Fisher nur Chr 13 (10,3 cM).

### Bekannte Altfehler (nicht „wiederbeleben"!)
- „Chr 8" statt „Chr 9" in Mails vom 6.4.2026 — Tippfehler, die GEDmatch-Rohdaten waren immer korrekt.
- „45,6 cM" taucht in keinem echten One-to-One-Bericht auf. Phantomzahl.
- „Fisher 83,3 cM" war der Fehler, nicht die 56 cM.
- Ancestry-Seitenzuordnungen (A/B/C) generell unzuverlässig.

## Häufige Fallstricke für das Seitenprojekt

1. **cM und SNPs nicht auf/ab-runden.** Die Zahlen auf der Seite sind aus den GEDmatch-Originalberichten. Wer „7,8 cM" zu „~8 cM" rundet, fälscht stillschweigend die Datenlage.
2. **„Segmentdaten nachzutragen" oder „Verifikation ausstehend" NICHT als allgemeine Füllformel verwenden.** Solche Aussagen suggerieren, es fehle Wissen, wo tatsächlich Daten vorliegen. Wenn die Information in Tier-1 oder den One-to-One-Dateien steht, gehört sie konkret hingeschrieben.
3. **Kit-Nummern nicht erraten oder ersetzen.** Jede Kit-Nummer entspricht einer realen Person auf GEDmatch. Bei Zweifel: Feld leer lassen oder beim DNA-Projekt rückfragen.
4. **Personen-Badges in Abschnitt 5.1 = Mitglieder der Chr-9-Kleinsegmentgruppe.** Wer nicht in der Gruppe ist, gehört nicht in die Badge-Leiste.
5. **Technische Vergleichsetiketten** wie `Zeisl↔Fisher` oder `Pilz↔Z.` sind DNA-Fachnotation und dürfen stehen bleiben. Das ist keine „dritte-Person-Narrative".

## Datenquellen (liegen alle im DNA-Projekt-Arbeitsordner)

- **Tier-1-Triangulationen:** `DNA AHNENFORSCHUNG/GEDmatch_Triangulation_Tier1_2026-04-12.csv` (12.136 Zeilen, Source-Kit Zeisl T405845)
- **One-to-One-Vergleiche:** `DNA AHNENFORSCHUNG/One-to-One_Ergebnisse_2026-04-06.md` plus neuere Läufe (Victor N. 14.4., Zeisl↔Fisher 13.4.)
- **Beide Kits kombiniert:** `DNA AHNENFORSCHUNG/GEDmatch/BothKits_WP_Zeisl_2026-04.csv`
- **Kompaktzusammenfassung:** `DNA AHNENFORSCHUNG/RETTUNG_01_Faktenblock_aus_Dachprojekt.md`
- **Statusblatt:** `DNA AHNENFORSCHUNG/STATUSBLATT.md`

Wenn das Seitenprojekt eine DNA-Frage beantworten muss: **nicht raten, sondern im DNA-Projekt rückfragen** oder die obigen Dateien konsultieren.

## Was das Seitenprojekt gerne selbstständig machen darf

- CSS, Responsive Design, Druckstylesheet, Dark-Mode
- Navigation, Ankerlinks, Table of Contents
- Bildintegration, Alt-Texte (technisch), Lazy Loading
- Accessibility (ARIA, Kontraste, Tastaturnavigation, Screenreader)
- Performance (minify, critical CSS, Bildoptimierung)
- Browser-Kompatibilität
- Jekyll-Konfiguration, Build-Pipeline
- SEO-Technik (Meta-Tags, sitemap, robots.txt) — ohne inhaltliche Keywords zu erfinden
- Umstrukturierung der Abschnitte aus Layoutgründen, wenn der Inhalt unangetastet bleibt
- Rechtschreibung/Grammatik/Typografie (Bindestriche, Anführungszeichen, Leerzeichen) — ohne Fachzahlen zu verändern
- Verfeinerung der Ich-Sprache, solange die Aussage identisch bleibt

## Was immer beim DNA-Projekt rückgefragt werden muss

- Inhalt aller Tabellen in Abschnitt 5 (Triangulationscluster)
- Alle cM-, SNP-, Positions- und Generationsangaben
- Alle Kit-Nummern und Personenzuordnungen
- Jede Aussage über Triangulationsbestätigung oder -widerlegung
- JSON-artige Datenstruktur `matchesData` im Script-Block
- Aussagen über Kontaktstatus mit Matches (wer hat geantwortet, was wurde besprochen)
- Aussagen über Verwandtschaftsgrade, MRCA-Schätzungen, Endogamie-Interpretation
