# BenchLM Mirror

<div align="center">

🇬🇧 English · [🇷🇺 Русский](README.ru.md) · [🇨🇳 中文](README.zh.md) · [🇪🇸 Español](README.es.md) · [🇩🇪 Deutsch](README.de.md) · [🇫🇷 Français](README.fr.md) · [🇯🇵 日本語](README.ja.md) · [🇰🇷 한국어](README.ko.md)

</div>

> An automatically updated mirror of public [BenchLM](https://benchlm.ai/) data.

[![Updates](https://img.shields.io/badge/updates-daily-blue?style=for-the-badge)](https://github.com/seregannj/benchlmirror/actions)
[![Source](https://img.shields.io/badge/source-BenchLM-black?style=for-the-badge)](https://benchlm.ai/data)
[![Files](https://img.shields.io/badge/data-6%20JSON-green?style=for-the-badge)](./data/)

---

## 🎯 Why?

BenchLM provides data about AI models, including rankings, benchmarks, prices, speed, and comparison results.

This repository is designed as a **simple and convenient mirror of this data** for use in third-party projects.

### What can you do?

- 📥 **Get up-to-date data** — files are automatically updated once a day.
- 🕐 **Track changes over time** — GitHub preserves previous file versions.
- 🔗 **Use the data directly** — JSON files are available through GitHub Raw.
- 🚀 **Connect the data to your projects** — no custom server is required to retrieve the JSON files.
- 📊 **Build custom interfaces and analytics** based on BenchLM data.

The repository can therefore be used as a simple source of BenchLM data for websites, applications, bots, analytics tools, and other projects.

---

## 📊 Data

| File | Description | Raw |
|:---|:---|:---:|
| [`models.json`](./data/models.json) | Information about AI models | [Open](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/models.json) |
| [`leaderboard.json`](./data/leaderboard.json) | Model rankings | [Open](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/leaderboard.json) |
| [`benchmarks.json`](./data/benchmarks.json) | Benchmark information | [Open](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/benchmarks.json) |
| [`pricing.json`](./data/pricing.json) | Model pricing | [Open](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/pricing.json) |
| [`speed.json`](./data/speed.json) | Model speed and performance | [Open](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/speed.json) |
| [`comparisons.json`](./data/comparisons.json) | Model comparisons | [Open](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/comparisons.json) |

---

## 🔗 Quick Access

All data is located in the [`data/`](./data/) directory.

### GitHub Raw

For example, [`models.json`](./data/models.json):

```text
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/models.json
```

Other files are available at similar URLs:

```text
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/leaderboard.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/benchmarks.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/pricing.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/speed.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/comparisons.json
```

### GitHub API

Files can also be retrieved through the GitHub Contents API:

```text
https://api.github.com/repos/seregannj/benchlmirror/contents/data/models.json
```

> ⚠️ When using the GitHub API, be aware of its limitations and terms of use.

---

## 💻 Usage

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

## 🔄 Automatic Updates

Data is automatically downloaded from BenchLM once a day using GitHub Actions.

Update process:

```text
BenchLM
   ↓
JSON download
   ↓
File validation
   ↓
JSON validation
   ↓
data/
   ↓
Git commit
```

If a file fails to download, the previous version is not replaced.

Updates can also be triggered manually from the Actions tab.

---

## 🕐 Change History

All file changes are preserved in Git history.

This makes it possible to:

- view previous data versions;
- compare changes between updates;
- track changes in rankings, prices, and other data;
- restore a previous file version when necessary.

The change history is available in the repository's Commits tab.

---

## 📁 Structure

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

## 🔗 Source

Data source:

[BenchLM](https://benchlm.ai/)

This repository is an independent mirror and is not directly affiliated with BenchLM.

---

## ⚖️ License and Data

The code and configuration of this repository are distributed under the MIT License.

The mirrored data belongs to its original source.

The MIT License does not automatically apply to BenchLM data.

Before using the data, review the terms and requirements of its original source.

---

<div align="center">

Data from BenchLM

[BenchLM](https://benchlm.ai/) · [GitHub](https://github.com/seregannj/benchlmirror) · [Data Source](https://benchlm.ai/data)

</div>
