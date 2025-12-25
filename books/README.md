---
title: "Zenn Books Directory"
---

# 📚 Zenn Books Directory

このディレクトリ `books/` は、**Zenn で公開・更新する「執筆中の書籍のみ」**を管理するための場所です。  
Zenn の GitHub 連携では、`books/` 配下に存在する各フォルダが **1 冊の書籍**として自動認識されます。

> ✅ **完成済み・凍結済みの書籍は `done-books/` に移動します**  
> ❌ `books/` に置かれた書籍のみが Zenn のデプロイ対象になります

---

## 🚦 運用方針（重要）

- `books/`  
  → **執筆中 / 更新中（Active）** の書籍のみを配置  
- `done-books/`  
  → **完成済み / 凍結（Frozen）** 書籍のアーカイブ  
- 原則として  
  **`books/` には 0〜1 冊のみを置く** ことで、  
  Zenn の投稿数制限・誤更新を防止します。

---

## 📘 現在の状態

現在、`books/` には **執筆中の書籍は存在しません**。

```text
books/
├ .gitkeep
└ README.md
```

- `.gitkeep` は、空ディレクトリを Git 管理下に保つためのものです
- 新しい書籍を開始する場合のみ、ここにフォルダを追加します

---

## ✍ 新しい書籍を追加する場合

以下の構造で `books/` 配下に新しいフォルダを作成してください。

```text
books/
└ my-new-book/
  ├ config.yaml
  ├ cover.png        # 任意
  ├ 01_intro.md
  ├ 02_theory.md
  └ 03_application.md
```

---

## 📌 Zenn 書籍の構築ルール

### ✔ 書籍フォルダ直下に `.md` を配置
- サブディレクトリ（`chapters/` など）は使用不可

### ✔ `config.yaml` の `chapters:` で章順を指定
```yaml
chapters:
  - 01_intro
  - 02_theory
  - 03_application
```

### ✔ `cover.png` は任意
- 設定すると Zenn 上で表紙として表示されます

### ✔ GitHub → Zenn の連携はリポジトリ単位
- `zenn-books` を 1 回連携すれば  
  `books/` 配下の書籍は自動的に検出・反映されます

---

## 🧊 完成書籍について

完成した書籍は、以下のコマンドで **必ず `done-books/` に移動**してください。

```powershell
git mv books/書籍名 done-books/
```

これにより：

- Zenn デプロイ対象から除外
- 意図しない更新・再ビルドを防止
- 教材アーカイブとして長期保存

が可能になります。

---

## 👤 Author

**Samizo-AITL**  
AI × 制御 × 半導体 技術教育プロジェクト  

GitHub / Zenn / 教材アーカイブを統合した  
長期運用前提の技術教育基盤を構築中。
