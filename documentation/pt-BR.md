<!-- ELUCENIA technical documentation · tamanho-amostral-duas-proporcoes · pt-BR · no clinical/professional/rights approval -->

# Tamanho amostral para comparar duas proporções

[condições, fontes e permissões](https://elucenia.org/pt-br/ferramentas/tamanho-amostral-duas-proporcoes)

## Como usar

Use a ferramenta no portal ou abra index.html em um servidor HTTP local. Selecione o idioma, preencha os campos e calcule.

## Entradas e unidades

### Proporção esperada no grupo 1 (ex.: controle)

`p1`

% · intervalo: 0,1–99,9

### Proporção esperada no grupo 2 (ex.: intervenção)

`p2`

% · intervalo: 0,1–99,9

### Nível de significância (bicaudal)

`alfa`

- `1` — α = 1%
- `5` — α = 5%

### Poder do teste

`poder`

- `80` — 80%
- `90` — 90%

### Perdas previstas (opcional)

`perdas`

% · opcional · intervalo: 0–50

## Edição do método

Coortes independentes, Charan/Biswas 2013 p. 123, m=1; quantis normais com seis casas decimais; sem correção de continuidade; WHO 1991 não conferido diretamente

## Fórmula documentada

n por grupo = \[zα/2 × √(2 p̄ q̄) + zβ × √(p1q1 + p2q2)\]² / (p1 − p2)², com p̄ = (p1 + p2)/2 e q = 1 − p.

A implementação usa coeficientes com seis casas decimais: zα/2 = 1,959964 (α 5%) ou 2,575829 (α 1%); zβ = 0,841621 (poder 80%) ou 1,281552 (poder 90%). Grupos de mesmo tamanho, sem correção de continuidade.

A equação corresponde à forma para coortes independentes de Charan e Biswas (2013, p. 123), com m = 1; a forma de ensaio com variância inteiramente agrupada da p. 124 é diferente. Os quantis normais foram conferidos matematicamente e arredondados a seis casas decimais; isso não valida a escolha do desenho. A citação WHO 1991 permanece sem conferência direta do manual.

## Limites e população

Esta aproximação calcula o tamanho por grupo para duas proporções binárias independentes, com alocação igual e teste bilateral. Defina diferença clinicamente relevante, proporções esperadas, significância e poder; não trate a diferença desejada como resultado conhecido. O cálculo não incorpora pareamento, conglomerados, medidas repetidas ou alocação desigual, que exigem métodos próprios. O ajuste para perdas aumenta o recrutamento, mas não corrige viés ou um desenho inadequado. A íntegra do manual WHO 1991 não foi conferida. A equação corresponde à forma para coortes independentes de Charan e Biswas (2013, p. 123), com m = 1; a forma de ensaio com variância inteiramente agrupada da p. 124 é diferente. Os quantis normais foram conferidos matematicamente e arredondados a seis casas decimais; isso não valida a escolha do desenho. A citação WHO 1991 permanece sem conferência direta do manual.

## Referências

- [Charan J, Biswas T. How to calculate sample size for different study designs in medical research? Indian J Psychol Med, 2013.](https://doi.org/10.4103/0253-7176.116232)

- [Lwanga SK, Lemeshow S. Sample size determination in health studies: a practical manual. Organização Mundial da Saúde, 1991.](https://iris.who.int/handle/10665/40062)

- [Charan/Biswas2013 original article content reprinted in course PDF](https://www.yoursearchevidence.com/sites/g/files/vrxlpx50391/files/2024-10/M2_ParticularidadesInvestigacion.pdf)

## Reproduzir os testes técnicos

Execute node test.cjs na pasta raiz deste repositório para repetir os casos sintéticos registrados. As entradas, expectativas e tolerâncias originais são preservadas. Testes técnicos não constituem validação clínica.

```sh
node test.cjs
```

tool.json contém fontes, edição e escopo de revisão. examples.json conserva as entradas e expectativas sintéticas; results.json registra os resultados obtidos.

[Ficha e referências](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referência](../examples.json) · [results.json](../results.json)

## Revisão e condições de uso

Revisão clínica independente não realizada.

Esta interface é uma tradução autoral, não uma edição oficial ou certificada. Revisão clínica independente, revisão linguística profissional e autorização de direitos de instrumentos não foram realizadas.

Resultado da fórmula ou classificação. Interpretação, conduta e aplicabilidade dependem da avaliação profissional e da fonte selecionada.

## Licença e atribuição

Apache-2.0 aplica-se somente ao código da ELUCENIA. Os instrumentos, publicações, traduções e dados mantêm os direitos dos respectivos titulares. Preserve LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
