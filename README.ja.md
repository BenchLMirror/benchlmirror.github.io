# BenchLM ミラー

<div align="center">

[🇬🇧 English](README.md) · [🇷🇺 Русский](README.ru.md) · [🇨🇳 中文](README.zh.md) · [🇪🇸 Español](README.es.md) · [🇩🇪 Deutsch](README.de.md) · [🇫🇷 Français](README.fr.md) · 🇯🇵 日本語 · [🇰🇷 한국어](README.ko.md)

</div>

> [BenchLM](https://benchlm.ai/) の公開データを自動更新するミラーです。

[![更新](https://img.shields.io/badge/更新-毎日-blue?style=for-the-badge)](https://github.com/seregannj/benchlmirror/actions)
[![ソース](https://img.shields.io/badge/ソース-BenchLM-black?style=for-the-badge)](https://benchlm.ai/data)
[![ファイル](https://img.shields.io/badge/データ-6%20JSON-green?style=for-the-badge)](./data/)

---

## 🎯 目的

BenchLM は、ランキング、ベンチマーク、価格、速度、比較結果など、AI モデルに関するデータを提供しています。

このリポジトリは、サードパーティプロジェクトで利用するための、**シンプルで便利なこのデータのミラー**として作成されています。

### 何ができる?

- 📥 **最新データを取得** — ファイルは1日1回自動的に更新されます。
- 🕐 **変更履歴を追跡** — GitHub はファイルの過去バージョンを保存します。
- 🔗 **データを直接利用** — JSON ファイルは GitHub Raw 経由で取得できます。
- 🚀 **プロジェクトにデータを取り込み** — JSON ファイルを取得するために独自のサーバーを立てる必要はありません。
- 📊 **BenchLM のデータに基づく独自のインターフェースや分析を構築**。

そのため、このリポジトリはウェブサイト、アプリケーション、ボット、分析ツール、その他のプロジェクトのための BenchLM データのシンプルなソースとして利用できます。

---

## 📊 データ

| ファイル | 説明 | Raw |
|:---|:---|:---:|
| [`models.json`](./data/models.json) | AI モデルに関する情報 | [開く](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/models.json) |
| [`leaderboard.json`](./data/leaderboard.json) | モデルランキング | [開く](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/leaderboard.json) |
| [`benchmarks.json`](./data/benchmarks.json) | ベンチマーク情報 | [開く](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/benchmarks.json) |
| [`pricing.json`](./data/pricing.json) | モデル料金 | [開く](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/pricing.json) |
| [`speed.json`](./data/speed.json) | モデルの速度とパフォーマンス | [開く](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/speed.json) |
| [`comparisons.json`](./data/comparisons.json) | モデル比較 | [開く](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/comparisons.json) |

---

## 🔗 クイックアクセス

すべてのデータは [`data/`](./data/) ディレクトリにあります。

### GitHub Raw

例えば、[`models.json`](./data/models.json):

```text
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/models.json
```

他のファイルも同様のアドレスで利用できます:

```text
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/leaderboard.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/benchmarks.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/pricing.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/speed.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/comparisons.json
```

### GitHub API

ファイルは GitHub Contents API 経由でも取得できます:

```text
https://api.github.com/repos/seregannj/benchlmirror/contents/data/models.json
```

> ⚠️ GitHub API を利用する際は、その制限と利用規約に注意してください。

---

## 💻 使用方法

### Python

```python
import requests

url = "https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/models.json"

response = requests.get(url)
response.raise_for_status()

data = response.json()

print(data)
```

### JavaScript

```javascript
const response = await fetch(
  "https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/models.json"
);

if (!response.ok) {
  throw new Error(`HTTP ${response.status}`);
}

const data = await response.json();

console.log(data);
```

### cURL

```bash
curl -L https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/models.json
```

---

## 🔄 自動更新

データは GitHub Actions により、BenchLM から1日1回自動的にダウンロードされます。

更新プロセス:

```text
BenchLM
   ↓
JSON ダウンロード
   ↓
ファイル検証
   ↓
JSON 検証
   ↓
data/
   ↓
Git commit
```

ファイルのダウンロードに失敗した場合、旧バージョンは置き換えられません。

Actions タブから手動で更新をトリガーすることもできます。

---

## 🕐 変更履歴

すべてのファイル変更は Git の履歴に保存されます。

これにより、以下のことが可能になります:

- 過去のデータバージョンを確認;
- 更新間の変更を比較;
- ランキング、料金、その他のデータの変化を追跡;
- 必要に応じてファイルの旧バージョンを復元。

変更履歴はリポジトリの Commits タブで確認できます。

---

## 📁 構成

```text
benchlmirror/
│
├── data/
│   ├── models.json
│   ├── leaderboard.json
│   ├── benchmarks.json
│   ├── pricing.json
│   ├── speed.json
│   └── comparisons.json
│
├── .github/
│   └── workflows/
│
├── LICENSE
├── README.md
└── README.ru.md
```

---

## 🔗 ソース

データソース:

[BenchLM](https://benchlm.ai/)

このリポジトリは独立したミラーであり、BenchLM と直接の関連はありません。

---

## ⚖️ ライセンスとデータ

このリポジトリのコードと設定は MIT ライセンスの下で配布されています。

ミラーされているデータはそれぞれのオリジナルソースに帰属します。

MIT ライセンスは BenchLM のデータには自動的に適用されません。

データを使用する前に、オリジナルソースの規約と要件を確認してください。

---

<div align="center">

Data from BenchLM

[BenchLM](https://benchlm.ai/) · [GitHub](https://github.com/seregannj/benchlmirror) · [データソース](https://benchlm.ai/data)

</div>
