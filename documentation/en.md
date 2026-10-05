<!-- ELUCENIA technical documentation · tamanho-amostral-duas-proporcoes · en · no clinical/professional/rights approval -->

# Sample size for comparing two proportions

[conditions, sources and permissions](https://elucenia.org/en/tools/tamanho-amostral-duas-proporcoes)

## How to use

Use the tool in the portal or open index.html through a local HTTP server. Select the language, complete the fields and calculate.

## Inputs and units

### Expected proportion in group 1 (e.g., control)

`p1`

% · range: 0.1–99.9

### Expected proportion in group 2 (e.g., intervention)

`p2`

% · range: 0.1–99.9

### Significance level (two-sided)

`alfa`

- `1` — α = 1%
- `5` — α = 5%

### Statistical power

`poder`

- `80` — 80%
- `90` — 90%

### Expected losses (optional)

`perdas`

% · optional · range: 0–50

## Method edition

Independent cohorts, Charan/Biswas 2013 p. 123, m=1; normal quantiles to six decimal places; no continuity correction; WHO 1991 not directly checked

## Documented formula

n per group = \[zα/2 × √(2 p̄ q̄) + zβ × √(p1q1 + p2q2)\]² / (p1 − p2)²; p̄ = (p1 + p2)/2; q = 1 − p.

The implementation uses coefficients with six decimal places: zα/2 = 1.959964 (α 5%) or 2.575829 (α 1%); zβ = 0.841621 (power 80%) or 1.281552 (power 90%). Equal-sized groups, without continuity correction.

The equation corresponds to the independent-cohort form in Charan and Biswas (2013, p. 123), with m = 1; the trial form using entirely pooled variance on p. 124 is different. The normal quantiles were checked mathematically and rounded to six decimal places; this does not validate the choice of study design. The WHO 1991 citation remains without direct verification of the manual.

## Limits and population

This approximation calculates sample size per group for two independent binary proportions, with equal allocation and a two-sided test. Specify a clinically relevant difference, expected proportions, significance level and power; do not treat the desired difference as a known result. It does not incorporate matching, clusters, repeated measurements or unequal allocation, which need their own methods. Allowing for losses increases recruitment but does not correct bias or an unsuitable design. The full WHO 1991 manual has not been checked. The equation corresponds to the independent-cohort form in Charan and Biswas (2013, p. 123), with m = 1; the trial form using entirely pooled variance on p. 124 is different. The normal quantiles were checked mathematically and rounded to six decimal places; this does not validate the choice of study design. The WHO 1991 citation remains without direct verification of the manual.

## References

- [Charan J, Biswas T. How to calculate sample size for different study designs in medical research? Indian J Psychol Med, 2013.](https://doi.org/10.4103/0253-7176.116232)

- [Lwanga SK, Lemeshow S. Sample size determination in health studies: a practical manual. Organização Mundial da Saúde, 1991.](https://iris.who.int/handle/10665/40062)

- [Charan/Biswas2013 original article content reprinted in course PDF](https://www.yoursearchevidence.com/sites/g/files/vrxlpx50391/files/2024-10/M2_ParticularidadesInvestigacion.pdf)

## Reproduce the technical tests

Run node test.cjs in the root directory of this repository to repeat the recorded synthetic cases. Original inputs, expectations and tolerances are preserved. Technical tests do not constitute clinical validation.

```sh
node test.cjs
```

tool.json contains sources, edition and review scope. examples.json retains synthetic inputs and expectations; results.json records the obtained results.

[Record and references](../tool.json) · [JavaScript code](../calculator.js) · [Reference cases](../examples.json) · [results.json](../results.json)

## Review and conditions of use

Independent clinical review has not been performed.

This interface is an authorial translation, not an official or certified edition. Independent clinical review, professional language review and instrument rights clearance have not been performed.

Formula or classification result. Interpretation, care and applicability depend on professional assessment and the selected source.

## License and attribution

Apache-2.0 applies only to ELUCENIA code. Rights to instruments, publications, translations and data remain with their respective holders. Preserve LICENSE and NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
