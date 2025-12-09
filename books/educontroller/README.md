# 📘 EduController — 統合制御工学テキスト

本フォルダは Zenn 上で公開する書籍 **「EduController」** のソースです。  
古典制御から AI 制御まで、制御工学を体系的に整理した教材として構成しています。

---

# 📂 構成

```

books/educontroller/
├ config.yaml
├ cover.png
├ 01_classical.md
├ 02_modern.md
├ 03_digital.md
├ 04_adaptive.md
├ 05_practical.md
├ 06_nn_control.md
├ 07_rl_control.md
├ 08_data_driven.md
├ 09_llm_hybrid.md
├ 10_pendulum.md
├ 11_matlab_tools.md
└ 12_soc_designkit.md

```

---

# 📝 config.yaml の役割

Zenn における書籍のメタ情報と、章の順序を定義します。

```yaml
title: "EduController"
summary: "古典・現代・デジタル・適応・AI制御まで体系的に学べる統合教材"
topics:
  - control
  - pid
  - robotics
  - engineering
published: false

chapters:
  - 01_classical
  - 02_modern
  - 03_digital
  - 04_adaptive
  - 05_practical
  - 06_nn_control
  - 07_rl_control
  - 08_data_driven
  - 09_llm_hybrid
  - 10_pendulum
  - 11_matlab_tools
  - 12_soc_designkit

```

---

# 📖 EduController — 各章の概要

本書「EduController」は、古典制御から AI 制御までを体系的に整理した統合制御工学テキストです。  
以下に各章の要点をまとめます。

---

## 01. Classical — PID 制御 / 周波数応答 / 安定性理論

- 比例・積分・微分（PID）制御の基礎とチューニング法  
- ボード線図・ナイキスト線図による周波数応答解析  
- 安定判別（Routh-Hurwitz、極配置など）  
- 古典制御の実務的な適用範囲と限界  

---

## 02. Modern — 状態空間 / LQR / 可制御性・可観測性

- 状態空間モデルの導入  
- 可制御性・可観測性の判定  
- LQR/LQG 制御系設計  
- 極配置法と現代制御の設計体系  

---

## 03. Digital — 離散時間制御 / Z変換 / サンプル値制御

- 連続系と離散系の関係  
- サンプリングとZ変換  
- デジタルPID制御  
- 状態空間の離散化（ゼロ次ホールドなど）  

---

## 04. Adaptive — MRAC / L1 / 適応ゲイン制御

- モデル参照適応制御（MRAC）  
- L1 適応制御  
- ゲイン更新則の導出  
- 適応制御の安定性と実装注意点  

---

## 05. Practical — ノイズ / 飽和 / 遅れの扱い

- ノイズと外乱への実務対応  
- アクチュエータ飽和の影響とアンチワインドアップ  
- 時間遅れシステムの扱い  
- 実際の制御器設計で考慮すべき要素  

---

## 06. NN Control — ニューラルネット制御 / 深層制御

- ニューラルネットワークによる非線形制御  
- DNN コントローラ設計  
- NN + PID ハイブリッド制御  
- 安定性保証の課題  

---

## 07. RL Control — 強化学習による制御

- Q学習・Deep Q-Network (DQN)  
- 連続制御のための Actor-Critic 系 (DDPG, SAC, TD3)  
- RL制御の安定性と安全性  
- 実機適用への課題  

---

## 08. Data-Driven — 識別 / サブスペース法 / 非線形モデル

- システム同定の基礎  
- サブスペース同定  
- 非線形モデル（NARX, Koopman など）  
- Data-driven 制御の設計プロセス  

---

## 09. LLM Hybrid — LLM + 制御のハイブリッド系

- LLM による制御パラメータ自動調整  
- LLM + PID / LLM + MPC  
- 制御器自動生成、異常検知への応用  
- LLM 活用の限界と安全性  

---

## 10. Pendulum — 倒立振子モデル

- 倒立振子の力学モデル  
- 線形化、平衡点まわりの安定化  
- LQR / MPC による制御  
- 実験系での課題  

---

## 11. MATLAB Tools — MATLAB/Simulink による制御設計

- Control System Toolbox の使い方  
- Simulink による制御器設計とシミュレーション  
- 周波数応答解析、過渡応答解析  
- 実務での MATLAB 活用例  

---

## 12. SoC Design Kit — SoC 設計用制御キット

- SoC（System-on-Chip）設計と制御の関係  
- 制御アルゴリズムのハードウェア実装  
- FPGA/ASIC フローとの接続  
- SoC + 制御の実装例  

---

# 🚀 Zenn への反映方法

本フォルダを含むリポジトリを Zenn と GitHub 連携すると、  
`config.yaml` に基づいて自動的に書籍として認識されます。

- `.md` を編集して GitHub に push  
- Zenn 側で自動ビルド  
- 本の管理画面に即反映される  

サブフォルダ構造は使用できません。  
章ファイルは **書籍フォルダ直下に置く必要があります**。

---

# 👤 Author

**Samizo-AITL**

