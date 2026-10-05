<!-- ELUCENIA technical documentation · tamanho-amostral-duas-proporcoes · it · no clinical/professional/rights approval -->

# Dimensione del campione per confrontare due proporzioni

[condizioni, fonti e autorizzazioni](https://elucenia.org/it/strumenti/tamanho-amostral-duas-proporcoes)

## Come usare

Usi lo strumento nel portale oppure apra index.html tramite un server HTTP locale. Selezioni la lingua, compili i campi ed esegua il calcolo.

## Dati di ingresso e unità

### Proporzione attesa nel gruppo 1 (ad es., controllo)

`p1`

% · intervallo: 0,1–99,9

### Proporzione attesa nel gruppo 2 (ad es., intervento)

`p2`

% · intervallo: 0,1–99,9

### Livello di significatività (bilaterale)

`alfa`

- `1` — α = 1%
- `5` — α = 5%

### Potenza statistica

`poder`

- `80` — 80%
- `90` — 90%

### Perdite previste (facoltativo)

`perdas`

% · facoltativo · intervallo: 0–50

## Edizione del metodo

Coorti indipendenti, Charan/Biswas 2013 p. 123, m=1; quantili normali con sei cifre decimali; senza correzione di continuità; WHO 1991 non verificato direttamente

## Formula documentata

n per gruppo = \[zα/2 × √(2 p̄ q̄) + zβ × √(p1q1 + p2q2)\]² / (p1 − p2)²; p̄ = (p1 + p2)/2; q = 1 − p.

L’implementazione utilizza coefficienti con sei cifre decimali: zα/2 = 1,959964 (α 5%) oppure 2,575829 (α 1%); zβ = 0,841621 (potenza 80%) oppure 1,281552 (potenza 90%). Gruppi di uguale numerosità, senza correzione di continuità.

L’equazione corrisponde alla forma per coorti indipendenti di Charan e Biswas (2013, p. 123), con m = 1; la forma per studi sperimentali con varianza interamente aggregata a p. 124 è diversa. I quantili normali sono stati verificati matematicamente e arrotondati a sei cifre decimali; ciò non valida la scelta del disegno dello studio. La citazione WHO 1991 resta senza verifica diretta del manuale.

## Limiti e popolazione

Questa approssimazione calcola la numerosità per gruppo per due proporzioni binarie indipendenti, con allocazione uguale e test bilaterale. Definire differenza clinicamente rilevante, proporzioni attese, significatività e potenza; non trattare la differenza desiderata come risultato noto. Non include appaiamento, cluster, misure ripetute o allocazione disuguale, che richiedono metodi specifici. L’aggiustamento per perdite aumenta il reclutamento, ma non corregge distorsioni o un disegno inadeguato. Il manuale WHO 1991 non è stato interamente verificato. L’equazione corrisponde alla forma per coorti indipendenti di Charan e Biswas (2013, p. 123), con m = 1; la forma per studi sperimentali con varianza interamente aggregata a p. 124 è diversa. I quantili normali sono stati verificati matematicamente e arrotondati a sei cifre decimali; ciò non valida la scelta del disegno dello studio. La citazione WHO 1991 resta senza verifica diretta del manuale.

## Riferimenti

- [Charan J, Biswas T. How to calculate sample size for different study designs in medical research? Indian J Psychol Med, 2013.](https://doi.org/10.4103/0253-7176.116232)

- [Lwanga SK, Lemeshow S. Sample size determination in health studies: a practical manual. Organização Mundial da Saúde, 1991.](https://iris.who.int/handle/10665/40062)

- [Charan/Biswas2013 original article content reprinted in course PDF](https://www.yoursearchevidence.com/sites/g/files/vrxlpx50391/files/2024-10/M2_ParticularidadesInvestigacion.pdf)

## Riprodurre i test tecnici

Esegua node test.cjs nella cartella principale di questo repository per ripetere i casi sintetici registrati. Gli input, i risultati attesi e le tolleranze originali sono conservati. I test tecnici non costituiscono validazione clinica.

```sh
node test.cjs
```

tool.json contiene le fonti, l’edizione e l’ambito della revisione. examples.json conserva gli input e i risultati attesi dei casi sintetici; results.json registra i risultati ottenuti.

[Scheda e riferimenti](../tool.json) · [Codice JavaScript](../calculator.js) · [Casi di riferimento](../examples.json) · [results.json](../results.json)

## Revisione e condizioni d’uso

Non è stata effettuata una revisione clinica indipendente.

Questa interfaccia è una traduzione realizzata dagli autori, non un’edizione ufficiale o certificata. Non sono state eseguite la revisione clinica indipendente, la revisione linguistica professionale né la verifica delle autorizzazioni relative ai diritti sugli strumenti.

Risultato della formula o classificazione. Interpretazione, condotta e applicabilità dipendono dalla valutazione professionale e dalla fonte selezionata.

## Licenza e attribuzione

Apache-2.0 si applica solo al codice di ELUCENIA. I diritti su strumenti, pubblicazioni, traduzioni e dati restano ai rispettivi titolari. Conservi LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
