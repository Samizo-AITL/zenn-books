
---
title: "Weff という考え方：幅 W は構造パラメータになった"
emoji: "📏"
type: "tech"
topics: ["Weff", "FinFET", "回路設計", "デバイスモデル"]
published: false
---

## Planar 時代の W

Planar MOSFET では、  
チャネル幅 W は単なるレイアウト寸法でした。

回路設計者は W/L を電気パラメータとして扱えました。

---

## FinFET における Weff

FinFET では、有効チャネル幅は構造から決まります。

概念的には以下で表されます。

Weff ≒ 2 × Hfin + Wfin


つまり、**電流能力は形状そのものに依存**します。

---

## Weff が意味するもの

- 回路設計とレイアウトが直結
- 構造が電気特性を支配
- BSIM-CMG などのモデルが必須

Weff は、  
**回路とデバイスをつなぐ翻訳点**になりました。
