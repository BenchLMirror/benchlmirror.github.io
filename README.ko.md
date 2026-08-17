


# BenchLM 미러

<div align="center">

[🇬🇧 English](README.md) · [🇷🇺 Русский](README.ru.md) · [🇨🇳 中文](README.zh.md) · [🇪🇸 Español](README.es.md) · [🇩🇪 Deutsch](README.de.md) · [🇫🇷 Français](README.fr.md) · [🇯🇵 日本語](README.ja.md) · 🇰🇷 한국어

</div>

> [BenchLM](https://benchlm.ai/)의 공개 데이터를 자동으로 업데이트하는 미러입니다.

[![업데이트](https://img.shields.io/badge/업데이트-매일-blue?style=for-the-badge)](https://github.com/seregannj/benchlmirror/actions)
[![소스](https://img.shields.io/badge/소스-BenchLM-black?style=for-the-badge)](https://benchlm.ai/data)
[![파일](https://img.shields.io/badge/데이터-6%20JSON-green?style=for-the-badge)](./data/)

---

## 🎯 목적

BenchLM은 AI 모델에 대한 데이터를 제공합니다. 여기에는 순위, 벤치마크, 가격, 속도 및 비교 결과가 포함됩니다.

이 저장소는 **타사 프로젝트에서 사용할 수 있는 이 데이터의 간단하고 편리한 미러**로 설계되었습니다.

### 무엇을 할 수 있나요?

- 📥 **최신 데이터 가져오기** — 파일은 하루에 한 번 자동으로 업데이트됩니다.
- 🕐 **변경 기록 추적** — GitHub는 파일의 이전 버전을 보존합니다.
- 🔗 **데이터 직접 사용** — JSON 파일은 GitHub Raw를 통해 사용할 수 있습니다.
- 🚀 **프로젝트에 데이터 연결** — JSON 파일을 가져오기 위해 자체 서버를 구축할 필요가 없습니다.
- 📊 **BenchLM 데이터를 기반으로 사용자 지정 인터페이스 및 분석 구축**.

따라서 이 저장소는 웹사이트, 애플리케이션, 봇, 분석 도구 및 기타 프로젝트를 위한 BenchLM 데이터의 간단한 소스로 사용할 수 있습니다.

---

## 📊 데이터

| 파일 | 설명 | Raw |
|:---|:---|:---:|
| [`models.json`](./data/models.json) | AI 모델 정보 | [열기](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/models.json) |
| [`leaderboard.json`](./data/leaderboard.json) | 모델 순위 | [열기](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/leaderboard.json) |
| [`benchmarks.json`](./data/benchmarks.json) | 벤치마크 정보 | [열기](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/benchmarks.json) |
| [`pricing.json`](./data/pricing.json) | 모델 가격 | [열기](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/pricing.json) |
| [`speed.json`](./data/speed.json) | 모델 속도 및 성능 | [열기](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/speed.json) |
| [`comparisons.json`](./data/comparisons.json) | 모델 비교 | [열기](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/comparisons.json) |

---

## 🔗 빠른 액세스

모든 데이터는 [`data/`](./data/) 디렉토리에 있습니다.

### GitHub Raw

예를 들어, [`models.json`](./data/models.json):

```text
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/models.json
```

다른 파일도 비슷한 주소로 사용할 수 있습니다:

```text
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/leaderboard.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/benchmarks.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/pricing.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/speed.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/comparisons.json
```

### GitHub API

파일은 GitHub Contents API를 통해서도 가져올 수 있습니다:

```text
https://api.github.com/repos/seregannj/benchlmirror/contents/data/models.json
```

> ⚠️ GitHub API를 사용할 때는 해당 제한 사항과 이용 약관을 숙지하세요.

---

## 💻 사용법

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

## 🔄 자동 업데이트

데이터는 GitHub Actions를 통해 하루에 한 번 BenchLM에서 자동으로 다운로드됩니다.

업데이트 프로세스:

```text
BenchLM
   ↓
JSON 다운로드
   ↓
파일 검증
   ↓
JSON 검증
   ↓
data/
   ↓
Git commit
```

파일 다운로드가 실패하면 이전 버전은 대체되지 않습니다.

Actions 탭에서 수동으로 업데이트를 트리거할 수도 있습니다.

---

## 🕐 변경 기록

모든 파일 변경 사항은 Git 기록에 보존됩니다.

이를 통해 다음이 가능합니다:

- 이전 데이터 버전 확인;
- 업데이트 간의 변경 사항 비교;
- 순위, 가격 및 기타 데이터의 변화 추적;
- 필요한 경우 파일의 이전 버전 복원.

변경 기록은 저장소의 Commits 탭에서 확인할 수 있습니다.

---

## 📁 구조

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

## 🔗 소스

데이터 소스:

[BenchLM](https://benchlm.ai/)

이 저장소는 독립적인 미러이며 BenchLM과 직접적인 관련이 없습니다.

---

## ⚖️ 라이선스 및 데이터

이 저장소의 코드 및 설정은 MIT 라이선스 하에 배포됩니다.

미러링된 데이터는 원본 소스의 소유입니다.

MIT 라이선스는 BenchLM 데이터에 자동으로 적용되지 않습니다.

데이터를 사용하기 전에 원본 소스의 약관 및 요구 사항을 확인하세요.

---

<div align="center">

Data from BenchLM

[BenchLM](https://benchlm.ai/) · [GitHub](https://github.com/seregannj/benchlmirror) · [데이터 소스](https://benchlm.ai/data)

</div>
