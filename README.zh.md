# BenchLM 镜像

<div align="center">

[🇬🇧 English](README.md) · [🇺 Русский](README.ru.md) · 🇨🇳 中文 · [🇪🇸 Español](README.es.md) · [🇩🇪 Deutsch](README.de.md) · [🇫🇷 Français](README.fr.md) · [🇯🇵 日本語](README.ja.md) · [🇰🇷 한국어](README.ko.md)

</div>

> [BenchLM](https://benchlm.ai/) 公开数据的自动更新镜像。

[![更新](https://img.shields.io/badge/更新-每日-blue?style=for-the-badge)](https://github.com/seregannj/benchlmirror/actions)
[![来源](https://img.shields.io/badge/来源-BenchLM-black?style=for-the-badge)](https://benchlm.ai/data)
[![文件](https://img.shields.io/badge/数据-6%20JSON-green?style=for-the-badge)](./data/)

---

## 🎯 用途

BenchLM 提供有关 AI 模型的数据,包括排名、基准测试、价格、速度和对比结果。

本仓库是这些数据的**简单便捷的镜像**,可用于第三方项目。

### 您可以做什么?

- 📥 **获取最新数据** — 文件每日自动更新一次。
- 🕐 **追踪变更历史** — GitHub 会保留文件的旧版本。
- 🔗 **直接使用数据** — JSON 文件可通过 GitHub Raw 获取。
- 🚀 **将数据接入您的项目** — 无需自行搭建服务器即可获取 JSON 文件。
- 📊 **基于 BenchLM 数据构建自定义界面和分析工具**。

因此,该仓库可用作网站、应用程序、机器人、分析工具及其他项目的 BenchLM 数据来源。

---

## 📊 数据

| 文件 | 说明 | Raw |
|:---|:---|:---:|
| [`models.json`](./data/models.json) | AI 模型信息 | [打开](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/models.json) |
| [`leaderboard.json`](./data/leaderboard.json) | 模型排行榜 | [打开](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/leaderboard.json) |
| [`benchmarks.json`](./data/benchmarks.json) | 基准测试信息 | [打开](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/benchmarks.json) |
| [`pricing.json`](./data/pricing.json) | 模型价格 | [打开](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/pricing.json) |
| [`speed.json`](./data/speed.json) | 模型速度与性能 | [打开](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/speed.json) |
| [`comparisons.json`](./data/comparisons.json) | 模型对比 | [打开](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/comparisons.json) |

---

## 🔗 快速访问

所有数据位于 [`data/`](./data/) 目录。

### GitHub Raw

例如,[`models.json`](./data/models.json):

```text
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/models.json
```

其他文件可通过类似地址访问:

```text
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/leaderboard.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/benchmarks.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/pricing.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/speed.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/comparisons.json
```

### GitHub API

也可通过 GitHub Contents API 获取文件:

```text
https://api.github.com/repos/seregannj/benchlmirror/contents/data/models.json
```

> ⚠️ 使用 GitHub API 时,请注意其限制和使用条款。

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

## 🔄 自动更新

数据通过 GitHub Actions 每天自动从 BenchLM 下载一次。

更新流程:

```text
BenchLM
   ↓
下载 JSON
   ↓
文件校验
   ↓
JSON 校验
   ↓
data/
   ↓
Git commit
```

如果文件下载失败,旧版本文件不会被替换。

也可通过 Actions 选项卡手动触发更新。

---

## 🕐 变更历史

所有文件变更均保存在 Git 历史记录中。

这使得以下操作成为可能:

- 查看历史数据版本;
- 对比不同更新之间的变化;
- 追踪排名、价格及其他数据的变化;
- 在需要时恢复文件的旧版本。

变更历史可在仓库的 Commits 选项卡中查看。

---

## 📁 目录结构

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

## 🔗 数据来源

数据来源:

[BenchLM](https://benchlm.ai/)

本仓库是独立的镜像项目,与 BenchLM 没有直接关联。

---

## ⚖️ 许可证与数据

本仓库的代码和配置采用 MIT 许可证发布。

镜像数据的版权归其原始来源所有。

MIT 许可证不自动适用于 BenchLM 的数据。

使用数据前,请阅读其原始来源的条款和要求。

---

<div align="center">

Data from BenchLM

[BenchLM](https://benchlm.ai/) · [GitHub](https://github.com/seregannj/benchlmirror) · [数据来源](https://benchlm.ai/data)

</div>
