<!-- ELUCENIA technical documentation · tamanho-amostral-duas-proporcoes · de · no clinical/professional/rights approval -->

# Stichprobengröße zum Vergleich zweier Anteile

[Bedingungen, Quellen und Berechtigungen](https://elucenia.org/de/werkzeuge/tamanho-amostral-duas-proporcoes)

## Verwendung

Verwenden Sie das Werkzeug im Portal oder öffnen Sie index.html über einen lokalen HTTP-Server. Wählen Sie die Sprache, füllen Sie die Felder aus und berechnen Sie das Ergebnis.

## Eingaben und Einheiten

### Erwarteter Anteil in Gruppe 1 (z. B. Kontrolle)

`p1`

% · Bereich: 0,1–99,9

### Erwarteter Anteil in Gruppe 2 (z. B. Intervention)

`p2`

% · Bereich: 0,1–99,9

### Signifikanzniveau (zweiseitig)

`alfa`

- `1` — α = 1%
- `5` — α = 5%

### Statistische Teststärke

`poder`

- `80` — 80%
- `90` — 90%

### Erwartete Verluste (optional)

`perdas`

% · optional · Bereich: 0–50

## Fassung der Methode

Unabhängige Kohorten, Charan/Biswas 2013 S. 123, m=1; Normalverteilungsquantile mit sechs Dezimalstellen; keine Stetigkeitskorrektur; WHO 1991 nicht direkt geprüft

## Dokumentierte Formel

n je Gruppe = \[zα/2 × √(2 p̄ q̄) + zβ × √(p1q1 + p2q2)\]² / (p1 − p2)²; p̄ = (p1 + p2)/2; q = 1 − p.

Die Implementierung verwendet Koeffizienten mit sechs Dezimalstellen: zα/2 = 1,959964 (α 5 %) oder 2,575829 (α 1 %); zβ = 0,841621 (Teststärke 80 %) oder 1,281552 (Teststärke 90 %). Gleich große Gruppen, ohne Stetigkeitskorrektur.

Die Gleichung entspricht der Form für unabhängige Kohorten bei Charan und Biswas (2013, S. 123) mit m = 1; die Studienform mit vollständig gepoolter Varianz auf S. 124 ist anders. Die Normalverteilungsquantile wurden mathematisch geprüft und auf sechs Dezimalstellen gerundet; dies bestätigt nicht die Wahl des Studiendesigns. Die Referenz WHO 1991 bleibt ohne direkte Prüfung des Handbuchs.

## Grenzen und Population

Diese Näherung berechnet die Stichprobengröße je Gruppe für zwei unabhängige binäre Anteile mit gleicher Zuteilung und zweiseitigem Test. Legen Sie eine klinisch relevante Differenz, erwartete Anteile, Signifikanzniveau und Teststärke fest; behandeln Sie die angestrebte Differenz nicht als bekanntes Ergebnis. Paarung, Cluster, wiederholte Messungen oder ungleiche Zuteilung werden nicht berücksichtigt und erfordern eigene Methoden. Die Anpassung für Ausfälle erhöht die Rekrutierung, korrigiert aber weder Verzerrung noch ein ungeeignetes Design. Das vollständige WHO-Handbuch von 1991 wurde nicht geprüft. Die Gleichung entspricht der Form für unabhängige Kohorten bei Charan und Biswas (2013, S. 123) mit m = 1; die Studienform mit vollständig gepoolter Varianz auf S. 124 ist anders. Die Normalverteilungsquantile wurden mathematisch geprüft und auf sechs Dezimalstellen gerundet; dies bestätigt nicht die Wahl des Studiendesigns. Die Referenz WHO 1991 bleibt ohne direkte Prüfung des Handbuchs.

## Referenzen

- [Charan J, Biswas T. How to calculate sample size for different study designs in medical research? Indian J Psychol Med, 2013.](https://doi.org/10.4103/0253-7176.116232)

- [Lwanga SK, Lemeshow S. Sample size determination in health studies: a practical manual. Organização Mundial da Saúde, 1991.](https://iris.who.int/handle/10665/40062)

- [Charan/Biswas2013 original article content reprinted in course PDF](https://www.yoursearchevidence.com/sites/g/files/vrxlpx50391/files/2024-10/M2_ParticularidadesInvestigacion.pdf)

## Technische Tests reproduzieren

Führen Sie node test.cjs im Stammverzeichnis dieses Repositorys aus, um die dokumentierten synthetischen Fälle zu wiederholen. Ursprüngliche Eingaben, erwartete Ergebnisse und Toleranzen bleiben erhalten. Technische Tests stellen keine klinische Validierung dar.

```sh
node test.cjs
```

tool.json enthält Quellen, Ausgabe und Umfang der Überprüfung. examples.json bewahrt die synthetischen Eingaben und erwarteten Ergebnisse; results.json dokumentiert die tatsächlich erhaltenen Ergebnisse.

[Eintrag und Referenzen](../tool.json) · [JavaScript-Code](../calculator.js) · [Referenzfälle](../examples.json) · [results.json](../results.json)

## Überprüfung und Nutzungsbedingungen

Eine unabhängige klinische Prüfung wurde nicht durchgeführt.

Diese Benutzeroberfläche ist eine selbst erstellte Übersetzung und keine offizielle oder zertifizierte Ausgabe. Eine unabhängige klinische Überprüfung, eine professionelle sprachliche Prüfung und eine Klärung der Rechte an den Instrumenten wurden nicht durchgeführt.

Ergebnis der Formel oder Klassifikation. Interpretation, Vorgehen und Anwendbarkeit hängen von der fachlichen Beurteilung und der ausgewählten Quelle ab.

## Lizenz und Urheberangaben

Apache-2.0 gilt nur für den ELUCENIA-Code. Die Rechte an Instrumenten, Veröffentlichungen, Übersetzungen und Daten verbleiben bei den jeweiligen Rechteinhabern. Bewahren Sie LICENSE und NOTICE auf.

ELUCENIA · Felipe Guedes · Copyright © 2026
