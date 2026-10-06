<!-- ELUCENIA technical documentation · tamanho-amostral-duas-proporcoes · es · no clinical/professional/rights approval -->

# Tamaño de muestra para comparar dos proporciones

[condiciones, fuentes y permisos](https://elucenia.org/es/herramientas/tamanho-amostral-duas-proporcoes)

## Cómo usar

Utilice la herramienta en el portal o abra index.html mediante un servidor HTTP local. Seleccione el idioma, complete los campos y calcule.

## Entradas y unidades

### Proporción esperada en el grupo 1 (p. ej., control)

`p1`

% · intervalo: 0,1–99,9

### Proporción esperada en el grupo 2 (p. ej., intervención)

`p2`

% · intervalo: 0,1–99,9

### Nivel de significación (bilateral)

`alfa`

- `1` — α = 1%
- `5` — α = 5%

### Potencia estadística

`poder`

- `80` — 80%
- `90` — 90%

### Pérdidas previstas (opcional)

`perdas`

% · opcional · intervalo: 0–50

## Edición del método

Cohortes independientes, Charan/Biswas 2013 p. 123, m=1; cuantiles normales con seis decimales; sin corrección de continuidad; WHO 1991 no comprobado directamente

## Fórmula documentada

n por grupo = \[zα/2 × √(2 p̄ q̄) + zβ × √(p1q1 + p2q2)\]² / (p1 − p2)²; p̄ = (p1 + p2)/2; q = 1 − p.

La implementación utiliza coeficientes con seis decimales: zα/2 = 1,959964 (α 5%) o 2,575829 (α 1%); zβ = 0,841621 (potencia 80%) o 1,281552 (potencia 90%). Grupos del mismo tamaño, sin corrección de continuidad.

La ecuación corresponde a la forma para cohortes independientes de Charan y Biswas (2013, p. 123), con m = 1; la forma para ensayos con varianza totalmente agrupada de la p. 124 es diferente. Los cuantiles normales se comprobaron matemáticamente y se redondearon a seis decimales; esto no valida la elección del diseño. La cita WHO 1991 sigue sin comprobación directa del manual.

## Límites y población

Esta aproximación calcula el tamaño por grupo para dos proporciones binarias independientes, con asignación igual y prueba bilateral. Defina diferencia clínicamente relevante, proporciones esperadas, significación y potencia; no trate la diferencia deseada como resultado conocido. No incorpora emparejamiento, conglomerados, medidas repetidas ni asignación desigual, que requieren métodos propios. El ajuste por pérdidas aumenta el reclutamiento, pero no corrige sesgo ni diseño inadecuado. No se ha comprobado el manual WHO 1991 íntegro. La ecuación corresponde a la forma para cohortes independientes de Charan y Biswas (2013, p. 123), con m = 1; la forma para ensayos con varianza totalmente agrupada de la p. 124 es diferente. Los cuantiles normales se comprobaron matemáticamente y se redondearon a seis decimales; esto no valida la elección del diseño. La cita WHO 1991 sigue sin comprobación directa del manual.

## Referencias

- [Charan J, Biswas T. How to calculate sample size for different study designs in medical research? Indian J Psychol Med, 2013.](https://doi.org/10.4103/0253-7176.116232)

- [Lwanga SK, Lemeshow S. Sample size determination in health studies: a practical manual. Organização Mundial da Saúde, 1991.](https://iris.who.int/handle/10665/40062)

- [Charan/Biswas2013 original article content reprinted in course PDF](https://www.yoursearchevidence.com/sites/g/files/vrxlpx50391/files/2024-10/M2_ParticularidadesInvestigacion.pdf)

## Reproducir las pruebas técnicas

Ejecute node test.cjs en el directorio raíz de este repositorio para repetir los casos sintéticos registrados. Se conservan las entradas, los resultados esperados y las tolerancias originales. Las pruebas técnicas no constituyen validación clínica.

```sh
node test.cjs
```

tool.json contiene las fuentes, la edición y el alcance de la revisión. examples.json conserva las entradas y los resultados esperados de los casos sintéticos; results.json registra los resultados obtenidos.

[Ficha y referencias](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referencia](../examples.json) · [results.json](../results.json)

## Revisión y condiciones de uso

No se ha realizado una revisión clínica independiente.

Esta interfaz es una traducción de elaboración propia, no una edición oficial o certificada. No se han realizado la revisión clínica independiente, la revisión lingüística profesional ni la autorización de derechos de los instrumentos.

Resultado de la fórmula o clasificación. La interpretación, la conducta y la aplicabilidad dependen de la evaluación profesional y de la fuente seleccionada.

## Licencia y atribución

Apache-2.0 se aplica únicamente al código de ELUCENIA. Los derechos de los instrumentos, publicaciones, traducciones y datos permanecen en manos de sus respectivos titulares. Conserve LICENSE y NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Resultados documentados

La información siguiente conserva las salidas del método para ejemplos sintéticos. No constituye una validación clínica independiente.

### 1

Detectar 20,0% frente a 10,0% con α = 5% (bilateral) y poder de 80%

| Detalles del resultado | |
| --- | --- |
| Por grupo (sin pérdidas) | 199 |
| Total (dos grupos) | 398 |


### 2

Detectar 20,0% frente a 10,0% con α = 5% (bilateral) y poder de 90%

| Detalles del resultado | |
| --- | --- |
| Por grupo (sin pérdidas) | 266 |
| Total (dos grupos) | 532 |

