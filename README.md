# 🤖 AI Audit Protocol
**Turn any AI into a Ruthless Auditor.**

[![Status](https://img.shields.io/badge/System-Operational-success)]()
[![Type](https://img.shields.io/badge/Type-Prompt_Engineering-blue)]()
[![Logic](https://img.shields.io/badge/Logic-SBCM_Theory-yellow)](https://doi.org/10.5281/zenodo.17762960)

> **「PDF解析はAIに任せろ。我々は『視点（ロジック）』を提供する。」**
>
> 行政文書の複雑なレイアウトや文脈を、ローカルスクリプトで解析するのは非効率です。
> GoogleやOpenAIが数百億円を投じて作った「汎用AI」の能力を、SBCM理論によって**「行政監査」**に一点集中させるための**「指令プロトコル生成ツール」**です。

---

## 🖥️ Generator

**👉 [Launch Protocol Generator](https://sbcm-alliance.github.io/pdf-audit/)**
*(Browser Only / No Server)*

<p align="center">
  <img src="docs/demo_protocol.png" alt="Protocol Generator UI" width="600">
</p>

---

## 📖 Concept: "AI Command Center"

このツールは、PDFファイルそのものを処理しません。
代わりに、**「その自治体の人口規模に合わせた、最適な監査プロンプト」**を動的に生成します。

### The Problem
*   ただPDFをChatGPTに読ませても、「要約」しかしてくれません。
*   AIは「1億円」が高いのか安いのか、基準を持っていません。

### The Solution (SBCM Injection)
*   本ツールは、対象自治体の人口から **「標準ブロック係数 ($S_{factor}$)**」を計算し、プロンプトに埋め込みます。
*   AIに対し、**「感想はいらない。この数式に基づいて $D_{index}$（歪み）を計算し、異常値をリストアップせよ」** という厳格な命令セットを発行します。

---

## 🎮 Workflow

1.  **Configure (設定):**
    *   監査したい自治体名（例：柏市）と人口（例：435,000）を入力します。
    *   システムがバックグラウンドで $S_{factor}$ を計算し、数式を組み立てます。
2.  **Copy Protocol (生成):**
    *   `COPY PROTOCOL` ボタンを押して、生成された指令書をクリップボードにコピーします。
3.  **Inject to AI (注入):**
    *   **ChatGPT / Gemini / Claude** を開きます。
    *   行政の決算書（PDF）をアップロードし、コピーしたプロンプトを貼り付けて送信します。
4.  **Forensics (監査):**
    *   AIがSBCM監査官となり、**「異常な歪み ($D_{index} > 10$)」** を検出したレポートを出力します。

---

## 🧠 Recommended AI Models (2025 Dec. Status)

SBCM監査は「文脈の広さ（Context Window）」が勝負です。
最新の長文読解モデルを使用することで、単年度の決算だけでなく**「過去10年の施策の整合性」**まで監査可能になります。

| Model | 特徴 | 推奨度 |
| :--- | :--- | :---: |
| **Gemini 3.0 Ultra** | **【神の目】** <br>1,000万トークンのコンテキストにより、自治体の「全歴史（議事録・計画書・決算書）」を一度にメモリに展開可能。矛盾を逃さない。 | ⭐⭐⭐⭐⭐ |
| **GPT-5 (Opal)** | **【検察官】** <br>圧倒的な論理推論能力により、数字の裏にある「政治的な隠蔽意図」や「循環取引の疑い」を言語化する能力に長ける。 | ⭐⭐⭐⭐⭐ |
| **Claude 3.5 Opus** | **【書記官】** <br>ハルシネーション（嘘）が最も少なく、堅実な係数計算を行う。報告書のドラフト作成に最適。 | ⭐⭐⭐⭐ |

---

## 📐 The Injected Logic

プロンプトには、以下のSBCM計算ロジックが含まれています。

$$ D_{index} = \frac{\text{Budget Impact}}{\text{Coverage Impact}} = \frac{(\text{Budget} / 30\text{M} \times S_{factor})}{(\text{Users} / 72,000 \times S_{factor})} $$

これにより、AIは単なる「文字起こし」ではなく、**「人口規模に見合わない異常な投資」**を数学的に特定できるようになります。

---

## ⚠️ Disclaimer

*   本ツールはプロンプト（テキスト）を生成するものであり、PDFファイルのアップロード機能はありません。
*   実際の監査精度は、使用するAIモデルの性能に依存します。
*   生成されたレポートは、必ず一次情報（元のPDF）と照らし合わせて確認してください。

---
<p align="center">
  <small>© 2025 SBCM Alliance. Powered by <b>Algorithmic Public Interestism</b>.</small>
</p>
