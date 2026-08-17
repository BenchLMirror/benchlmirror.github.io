# BenchLM Mirror

<div align="center">

[🇬🇧 English](README.md) · 🇷🇺 Русский · [🇨🇳 中文](README.zh.md) · [🇪🇸 Español](README.es.md) · [🇩🇪 Deutsch](README.de.md) · [🇫🇷 Français](README.fr.md) · [🇯🇵 日本語](README.ja.md) · [🇰🇷 한국어](README.ko.md)

</div>

> Автоматически обновляемое зеркало публичных данных [BenchLM](https://benchlm.ai/).

[![Обновление](https://img.shields.io/badge/обновление-ежедневно-blue?style=for-the-badge)](https://github.com/seregannj/benchlmirror/actions)
[![Источник](https://img.shields.io/badge/источник-BenchLM-black?style=for-the-badge)](https://benchlm.ai/data)
[![Файлы](https://img.shields.io/badge/данные-6%20JSON-green?style=for-the-badge)](./data/)

---

## 🎯 Зачем это?

BenchLM предоставляет данные об ИИ-моделях: рейтинги, бенчмарки, цены, скорость и результаты сравнений.

Этот репозиторий создан как **простое и удобное зеркало этих данных**, которое можно использовать в сторонних проектах.

### Что можно делать?

- 📥 **Получать актуальные данные** — файлы автоматически обновляются раз в день.
- 🕐 **Отслеживать историю изменений** — GitHub сохраняет предыдущие версии файлов.
- 🔗 **Использовать данные напрямую** — JSON-файлы доступны через GitHub Raw.
- 🚀 **Подключать данные к своим проектам** — для получения JSON не требуется создавать собственный сервер.
- 📊 **Создавать собственные интерфейсы и аналитику** на основе данных BenchLM.

Таким образом, репозиторий может использоваться как простой источник данных BenchLM для сайтов, приложений, ботов, аналитических инструментов и других проектов.

---

## 📊 Данные

| Файл | Описание | Raw |
|:---|:---|:---:|
| [`models.json`](./data/models.json) | Информация об ИИ-моделях | [Открыть](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/models.json) |
| [`leaderboard.json`](./data/leaderboard.json) | Рейтинг моделей | [Открыть](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/leaderboard.json) |
| [`benchmarks.json`](./data/benchmarks.json) | Информация о бенчмарках | [Открыть](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/benchmarks.json) |
| [`pricing.json`](./data/pricing.json) | Цены на модели | [Открыть](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/pricing.json) |
| [`speed.json`](./data/speed.json) | Скорость и производительность моделей | [Открыть](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/speed.json) |
| [`comparisons.json`](./data/comparisons.json) | Сравнения моделей | [Открыть](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/comparisons.json) |

---

## 🔗 Быстрый доступ

Все данные находятся в директории [`data/`](./data/).

### GitHub Raw

Например, [`models.json`](./data/models.json):

```text
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/models.json
```

Другие файлы доступны по аналогичному адресу:

```text
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/leaderboard.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/benchmarks.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/pricing.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/speed.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/comparisons.json
```

### GitHub API

Файлы также можно получать через GitHub Contents API:

```text
https://api.github.com/repos/seregannj/benchlmirror/contents/data/models.json
```

> ⚠️ При использовании GitHub API учитывайте ограничения и условия его использования.

---

## 💻 Использование

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

## 🔄 Автоматическое обновление

Данные автоматически загружаются с BenchLM раз в день с помощью GitHub Actions.

Процесс обновления:

```text
BenchLM
   ↓
Загрузка JSON
   ↓
Проверка файла
   ↓
Проверка JSON
   ↓
data/
   ↓
Git commit
```

Если загрузка файла не удалась, предыдущая версия файла не заменяется.

Обновление также можно запустить вручную через вкладку Actions.

---

## 🕐 История изменений

Все изменения файлов сохраняются в истории Git.

Это позволяет:

- просматривать предыдущие версии данных;
- сравнивать изменения между обновлениями;
- отслеживать изменения рейтингов, цен и других данных;
- восстанавливать предыдущую версию файла при необходимости.

История изменений доступна во вкладке Commits репозитория.

---

## 📁 Структура

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

## 🔗 Источник

Источник данных:

[BenchLM](https://benchlm.ai/)

Этот репозиторий является независимым зеркалом и не связан с BenchLM напрямую.

---

## ⚖️ Лицензия и данные

Код и конфигурация данного репозитория распространяются по лицензии MIT.

Зеркалируемые данные принадлежат их первоначальному источнику.

Лицензия MIT не распространяется автоматически на данные BenchLM.

Перед использованием данных ознакомьтесь с условиями и требованиями их первоначального источника.

---

<div align="center">

Data from BenchLM

[BenchLM](https://benchlm.ai/) · [GitHub](https://github.com/seregannj/benchlmirror) · [Источник данных](https://benchlm.ai/data)

</div>
