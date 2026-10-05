<!-- ELUCENIA technical documentation · tamanho-amostral-duas-proporcoes · zh · no clinical/professional/rights approval -->

# 比较两个比例的样本量

[条件、来源与许可](https://elucenia.org/zh/tools/tamanho-amostral-duas-proporcoes)

## 使用方法

在门户中使用工具，或通过本地 HTTP 服务器打开 index.html。选择语言，填写各字段，然后计算。

## 输入与单位

### 组 1 预期比例（如对照组）

`p1`

% · 范围: 0.1–99.9

### 组 2 预期比例（如干预组）

`p2`

% · 范围: 0.1–99.9

### 显著性水平（双侧）

`alfa`

- `1` — α = 1%
- `5` — α = 5%

### 检验效能

`poder`

- `80` — 80%
- `90` — 90%

### 预期失访（可选）

`perdas`

% · 选填 · 范围: 0–50

## 方法版本

独立队列，Charan/Biswas 2013 第123页，m=1；正态分位数保留六位小数；不作连续性校正；WHO 1991 未直接核实

## 已记录的公式

n 每组 = \[zα/2 × √(2 p̄ q̄) + zβ × √(p1q1 + p2q2)\]² / (p1 − p2)²; p̄ = (p1 + p2)/2; q = 1 − p.

实现使用保留六位小数的系数：zα/2 = 1.959964（α 5%）或 2.575829（α 1%）；zβ = 0.841621（检验效能 80%）或 1.281552（检验效能 90%）。两组样本量相同，不作连续性校正。

该方程对应 Charan 和 Biswas（2013，第123页）的独立队列形式，m = 1；第124页采用完全合并方差的试验形式与之不同。正态分布分位数经过数学核对并四舍五入到六位小数；这不等于确认研究设计选择适当。WHO 1991 引文仍未通过直接查阅手册核实。

## 限制与适用人群

此近似方法计算两个独立二分类比例比较中每组的样本量，采用等量分配和双侧检验。请确定有临床意义的差异、预期比例、显著性水平和检验效能；不要把期望差异当作已知结果。计算不包含配对、整群、重复测量或不等量分配，这些设计需要专门的方法。失访调整会增加招募人数，但不能纠正偏倚或不适当的设计。WHO 1991 手册尚未完整核对。 该方程对应 Charan 和 Biswas（2013，第123页）的独立队列形式，m = 1；第124页采用完全合并方差的试验形式与之不同。正态分布分位数经过数学核对并四舍五入到六位小数；这不等于确认研究设计选择适当。WHO 1991 引文仍未通过直接查阅手册核实。

## 参考文献

- [Charan J, Biswas T. How to calculate sample size for different study designs in medical research? Indian J Psychol Med, 2013.](https://doi.org/10.4103/0253-7176.116232)

- [Lwanga SK, Lemeshow S. Sample size determination in health studies: a practical manual. Organização Mundial da Saúde, 1991.](https://iris.who.int/handle/10665/40062)

- [Charan/Biswas2013 original article content reprinted in course PDF](https://www.yoursearchevidence.com/sites/g/files/vrxlpx50391/files/2024-10/M2_ParticularidadesInvestigacion.pdf)

## 复现技术测试

在此仓库的根目录中运行 node test.cjs，以重复已记录的合成案例。原始输入、预期结果和容差保持不变。技术测试不构成临床验证。

```sh
node test.cjs
```

tool.json 包含来源、版本和审查范围。examples.json 保留合成输入与预期结果；results.json 记录实际得到的结果。

[记录与参考文献](../tool.json) · [JavaScript代码](../calculator.js) · [参考案例](../examples.json) · [results.json](../results.json)

## 审查与使用条件

尚未开展独立临床审查。

此界面为自主编写的翻译，并非官方或认证版本。尚未完成独立临床审查、专业语言审查或工具权利授权。

公式或分类结果。解释、处理及适用性须结合专业评估和所选来源。

## 许可与署名

Apache-2.0 仅适用于 ELUCENIA 代码。工具、出版物、翻译和数据的权利仍归各自权利人所有。请保留 LICENSE 和 NOTICE。

ELUCENIA · Felipe Guedes · Copyright © 2026
