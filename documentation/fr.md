<!-- ELUCENIA technical documentation · tamanho-amostral-duas-proporcoes · fr · no clinical/professional/rights approval -->

# Taille d’échantillon pour comparer deux proportions

[conditions, sources et autorisations](https://elucenia.org/fr/outils/tamanho-amostral-duas-proporcoes)

## Mode d’emploi

Utilisez l’outil sur le portail ou ouvrez index.html via un serveur HTTP local. Sélectionnez la langue, remplissez les champs et lancez le calcul.

## Données d’entrée et unités

### Proportion attendue dans le groupe 1 (p. ex., témoin)

`p1`

% · intervalle: 0,1–99,9

### Proportion attendue dans le groupe 2 (p. ex., intervention)

`p2`

% · intervalle: 0,1–99,9

### Seuil de signification (bilatéral)

`alfa`

- `1` — α = 1%
- `5` — α = 5%

### Puissance statistique

`poder`

- `80` — 80%
- `90` — 90%

### Pertes attendues (facultatif)

`perdas`

% · facultatif · intervalle: 0–50

## Édition de la méthode

Cohortes indépendantes, Charan/Biswas 2013 p. 123, m=1 ; quantiles normaux à six décimales ; sans correction de continuité ; WHO 1991 non vérifié directement

## Formule documentée

n par groupe = \[zα/2 × √(2 p̄ q̄) + zβ × √(p1q1 + p2q2)\]² / (p1 − p2)²; p̄ = (p1 + p2)/2; q = 1 − p.

L’implémentation utilise des coefficients à six décimales : zα/2 = 1,959964 (α 5 %) ou 2,575829 (α 1 %) ; zβ = 0,841621 (puissance 80 %) ou 1,281552 (puissance 90 %). Groupes de même taille, sans correction de continuité.

L’équation correspond à la forme pour cohortes indépendantes de Charan et Biswas (2013, p. 123), avec m = 1 ; la forme pour essais à variance entièrement regroupée de la p. 124 est différente. Les quantiles normaux ont été vérifiés mathématiquement et arrondis à six décimales ; cela ne valide pas le choix du plan d’étude. La référence WHO 1991 reste sans vérification directe du manuel.

## Limites et population

Cette approximation calcule l’effectif par groupe pour deux proportions binaires indépendantes, avec allocation égale et test bilatéral. Définissez une différence cliniquement pertinente, les proportions attendues, le seuil de signification et la puissance ; ne considérez pas la différence souhaitée comme un résultat connu. Elle n’intègre ni appariement, ni grappes, ni mesures répétées, ni allocation inégale, qui exigent des méthodes propres. L’ajustement pour pertes augmente le recrutement, mais ne corrige ni biais ni plan inapproprié. L’intégralité du manuel WHO 1991 n’a pas été vérifiée. L’équation correspond à la forme pour cohortes indépendantes de Charan et Biswas (2013, p. 123), avec m = 1 ; la forme pour essais à variance entièrement regroupée de la p. 124 est différente. Les quantiles normaux ont été vérifiés mathématiquement et arrondis à six décimales ; cela ne valide pas le choix du plan d’étude. La référence WHO 1991 reste sans vérification directe du manuel.

## Références

- [Charan J, Biswas T. How to calculate sample size for different study designs in medical research? Indian J Psychol Med, 2013.](https://doi.org/10.4103/0253-7176.116232)

- [Lwanga SK, Lemeshow S. Sample size determination in health studies: a practical manual. Organização Mundial da Saúde, 1991.](https://iris.who.int/handle/10665/40062)

- [Charan/Biswas2013 original article content reprinted in course PDF](https://www.yoursearchevidence.com/sites/g/files/vrxlpx50391/files/2024-10/M2_ParticularidadesInvestigacion.pdf)

## Reproduire les tests techniques

Exécutez node test.cjs dans le répertoire racine de ce dépôt pour reproduire les cas synthétiques enregistrés. Les données d’entrée, les résultats attendus et les tolérances d’origine sont conservés. Les tests techniques ne constituent pas une validation clinique.

```sh
node test.cjs
```

tool.json contient les sources, l’édition et le périmètre de la revue. examples.json conserve les données d’entrée et les résultats attendus des cas synthétiques ; results.json consigne les résultats obtenus.

[Fiche et références](../tool.json) · [Code JavaScript](../calculator.js) · [Cas de référence](../examples.json) · [results.json](../results.json)

## Revue et conditions d’utilisation

Aucune révision clinique indépendante n’a été effectuée.

Cette interface est une traduction réalisée par nos soins, et non une édition officielle ou certifiée. La revue clinique indépendante, la révision linguistique professionnelle et l’autorisation des droits sur les instruments n’ont pas été réalisées.

Résultat de la formule ou de la classification. L’interprétation, la conduite et l’applicabilité dépendent de l’évaluation professionnelle et de la source sélectionnée.

## Licence et attribution

Apache-2.0 s’applique uniquement au code d’ELUCENIA. Les droits sur les instruments, publications, traductions et données restent ceux de leurs titulaires respectifs. Conservez LICENSE et NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
