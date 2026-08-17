# BenchLM-Spiegel

<div align="center">

[🇬🇧 English](README.md) · [🇷🇺 Русский](README.ru.md) · [🇨🇳 中文](README.zh.md) · [🇪🇸 Español](README.es.md) · 🇩🇪 Deutsch · [🇫🇷 Français](README.fr.md) · [🇯🇵 日本語](README.ja.md) · [🇰🇷 한국어](README.ko.md)

</div>

> Ein automatisch aktualisierter Spiegel öffentlicher [BenchLM](https://benchlm.ai/)-Daten.

[![Aktualisierung](https://img.shields.io/badge/aktualisierung-täglich-blue?style=for-the-badge)](https://github.com/seregannj/benchlmirror/actions)
[![Quelle](https://img.shields.io/badge/quelle-BenchLM-black?style=for-the-badge)](https://benchlm.ai/data)
[![Dateien](https://img.shields.io/badge/daten-6%20JSON-green?style=for-the-badge)](./data/)

---

## 🎯 Wozu?

BenchLM liefert Daten zu KI-Modellen, einschließlich Ranglisten, Benchmarks, Preisen, Geschwindigkeit und Vergleichsergebnissen.

Dieses Repository ist als **einfacher und praktischer Spiegel dieser Daten** für die Nutzung in Drittanbieterprojekten gedacht.

### Was kann man damit machen?

- 📥 **Aktuelle Daten abrufen** — Dateien werden automatisch einmal täglich aktualisiert.
- 🕐 **Änderungsverlauf verfolgen** — GitHub bewahrt frühere Dateiversionen auf.
- 🔗 **Daten direkt verwenden** — JSON-Dateien sind über GitHub Raw verfügbar.
- 🚀 **Daten in eigene Projekte einbinden** — Es ist kein eigener Server erforderlich, um die JSON-Dateien abzurufen.
- 📊 **Eigene Oberflächen und Analysen** auf Basis von BenchLM-Daten erstellen.

Das Repository kann daher als einfache Datenquelle für BenchLM-Daten für Websites, Anwendungen, Bots, Analysetools und andere Projekte genutzt werden.

---

## 📊 Daten

| Datei | Beschreibung | Raw |
|:---|:---|:---:|
| [`models.json`](./data/models.json) | Informationen zu KI-Modellen | [Öffnen](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/models.json) |
| [`leaderboard.json`](./data/leaderboard.json) | Modell-Rangliste | [Öffnen](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/leaderboard.json) |
| [`benchmarks.json`](./data/benchmarks.json) | Benchmark-Informationen | [Öffnen](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/benchmarks.json) |
| [`pricing.json`](./data/pricing.json) | Modellpreise | [Öffnen](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/pricing.json) |
| [`speed.json`](./data/speed.json) | Geschwindigkeit und Leistung der Modelle | [Öffnen](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/speed.json) |
| [`comparisons.json`](./data/comparisons.json) | Modellvergleiche | [Öffnen](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/comparisons.json) |

---

## 🔗 Schnellzugriff

Alle Daten befinden sich im Verzeichnis [`data/`](./data/).

### GitHub Raw

Zum Beispiel [`models.json`](./data/models.json):

```text
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/models.json
```

Weitere Dateien sind unter ähnlichen Adressen verfügbar:

```text
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/leaderboard.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/benchmarks.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/pricing.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/speed.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/comparisons.json
```

### GitHub-API

Dateien können auch über die GitHub-Contents-API abgerufen werden:

```text
https://api.github.com/repos/seregannj/benchlmirror/contents/data/models.json
```

> ⚠️ Beachte bei der Nutzung der GitHub-API deren Einschränkungen und Nutzungsbedingungen.

---

## 💻 Verwendung

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

## 🔄 Automatische Aktualisierung

Die Daten werden einmal täglich über GitHub Actions automatisch von BenchLM heruntergeladen.

Aktualisierungsprozess:

```text
BenchLM
   ↓
JSON-Download
   ↓
Dateiprüfung
   ↓
JSON-Prüfung
   ↓
data/
   ↓
Git commit
```

Schlägt der Download einer Datei fehl, wird die vorherige Version nicht ersetzt.

Aktualisierungen können auch manuell über den Tab Actions ausgelöst werden.

---

## 🕐 Änderungsverlauf

Alle Dateiänderungen werden in der Git-Historie aufbewahrt.

Dadurch ist es möglich:

- frühere Datenversionen einzusehen;
- Änderungen zwischen Aktualisierungen zu vergleichen;
- Veränderungen bei Ranglisten, Preisen und anderen Daten zu verfolgen;
- bei Bedarf eine frühere Dateiversion wiederherzustellen.

Der Änderungsverlauf ist im Tab Commits des Repositories verfügbar.

---

## 📁 Struktur

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

## 🔗 Quelle

Datenquelle:

[BenchLM](https://benchlm.ai/)

Dieses Repository ist ein unabhängiger Spiegel und steht in keiner direkten Verbindung zu BenchLM.

---

## ⚖️ Lizenz und Daten

Der Code und die Konfiguration dieses Repositories werden unter der MIT-Lizenz veröffentlicht.

Die gespiegelten Daten gehören ihrer ursprünglichen Quelle.

Die MIT-Lizenz gilt nicht automatisch für BenchLM-Daten.

Lies vor der Nutzung der Daten die Bedingungen und Anforderungen der ursprünglichen Quelle.

---

<div align="center">

Data from BenchLM

[BenchLM](https://benchlm.ai/) · [GitHub](https://github.com/seregannj/benchlmirror) · [Datenquelle](https://benchlm.ai/data)

</div>
