<!-- ELUCENIA technical documentation · tamanho-amostral-duas-proporcoes · ja · no clinical/professional/rights approval -->

# 2つの比率を比較する標本サイズ

[条件・出典・許諾](https://elucenia.org/ja/tools/tamanho-amostral-duas-proporcoes)

## 使い方

ポータルでツールを使用するか、ローカルHTTPサーバー経由でindex.htmlを開いてください。言語を選択し、項目を入力して計算してください。

## 入力項目と単位

### 群1の予想割合（例：対照群）

`p1`

% · 範囲: 0.1–99.9

### 群2の予想割合（例：介入群）

`p2`

% · 範囲: 0.1–99.9

### 有意水準（両側）

`alfa`

- `1` — α = 1%
- `5` — α = 5%

### 検出力

`poder`

- `80` — 80%
- `90` — 90%

### 予想脱落率（任意）

`perdas`

% · 任意 · 範囲: 0–50

## 方法の版

独立コホート、Charan/Biswas 2013、123頁、m=1；正規分布の分位点は小数点以下6桁；連続性補正なし；WHO 1991は直接未確認

## 記載された計算式

n 群ごと = \[zα/2 × √(2 p̄ q̄) + zβ × √(p1q1 + p2q2)\]² / (p1 − p2)²; p̄ = (p1 + p2)/2; q = 1 − p.

実装では小数点以下6桁の係数を使用します：zα/2 = 1.959964（α 5%）または 2.575829（α 1%）、zβ = 0.841621（検出力80%）または 1.281552（検出力90%）。両群の人数は同じで、連続性補正は行いません。

この式は Charan と Biswas（2013、123頁）の独立コホートの形式に対応し、m = 1です。124頁の分散を完全にプールする試験用の形式とは異なります。正規分布の分位点を数学的に確認し、小数点以下6桁に丸めていますが、研究デザインの選択が妥当であることを示すものではありません。WHO 1991の引用は、手引きの直接確認が行われていません。

## 限界・対象集団

この近似は、二つの独立した二値割合を等数割付・両側検定で比較する場合の各群の標本数を計算します。臨床的に意味のある差、予想割合、有意水準、検出力を設定し、目標の差を既知の結果と扱わないでください。対応付け、クラスター、反復測定、不均等割付は含まず、それぞれ専用の方法が必要です。脱落調整は募集人数を増やしますが、バイアスや不適切なデザインを修正しません。WHO 1991 手引き全体は確認されていません。 この式は Charan と Biswas（2013、123頁）の独立コホートの形式に対応し、m = 1です。124頁の分散を完全にプールする試験用の形式とは異なります。正規分布の分位点を数学的に確認し、小数点以下6桁に丸めていますが、研究デザインの選択が妥当であることを示すものではありません。WHO 1991の引用は、手引きの直接確認が行われていません。

## 参考文献

- [Charan J, Biswas T. How to calculate sample size for different study designs in medical research? Indian J Psychol Med, 2013.](https://doi.org/10.4103/0253-7176.116232)

- [Lwanga SK, Lemeshow S. Sample size determination in health studies: a practical manual. Organização Mundial da Saúde, 1991.](https://iris.who.int/handle/10665/40062)

- [Charan/Biswas2013 original article content reprinted in course PDF](https://www.yoursearchevidence.com/sites/g/files/vrxlpx50391/files/2024-10/M2_ParticularidadesInvestigacion.pdf)

## 技術テストの再現

このリポジトリのルートディレクトリでnode test.cjsを実行すると、記録された合成ケースを再実行できます。元の入力、期待結果、許容誤差は保持されています。技術テストは臨床的検証を意味しません。

```sh
node test.cjs
```

tool.jsonには出典、版、確認範囲が記録されています。examples.jsonには合成入力と期待結果が保持され、results.jsonには実際に得られた結果が記録されています。

[記録・参考文献](../tool.json) · [JavaScriptコード](../calculator.js) · [参照ケース](../examples.json) · [results.json](../results.json)

## 確認状況と使用条件

独立した臨床レビューは実施されていません。

このインターフェースは独自に作成した翻訳であり、公式版や認証済みの版ではありません。独立した臨床レビュー、専門家による言語レビュー、評価尺度等の権利許諾の確認は実施されていません。

式または分類の結果です。解釈、対応、適用可能性は専門家による評価と選択した出典に依存します。

## ライセンスと帰属表示

Apache-2.0はELUCENIAのコードにのみ適用されます。評価尺度等、出版物、翻訳、データの権利は、それぞれの権利者に帰属します。LICENSEとNOTICEを保持してください。

ELUCENIA · Felipe Guedes · Copyright © 2026
