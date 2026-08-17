



 same structure and fixing errors similar to what I did before.
</think>

# Miroir de BenchLM

<div align="center">

[🇬🇧 English](README.md) · [🇷🇺 Русский](README.ru.md) · [🇨🇳 中文](README.zh.md) · [🇪🇸 Español](README.es.md) · [🇩🇪 Deutsch](README.de.md) · 🇫🇷 Français · [🇯🇵 日本語](README.ja.md) · [🇰🇷 한국어](README.ko.md)

</div>

> Un miroir des données publiques de [BenchLM](https://benchlm.ai/) mis à jour automatiquement.

[![Mise à jour](https://img.shields.io/badge/mise%20à%20jour-quotidienne-blue?style=for-the-badge)](https://github.com/seregannj/benchlmirror/actions)
[![Source](https://img.shields.io/badge/source-BenchLM-black?style=for-the-badge)](https://benchlm.ai/data)
[![Fichiers](https://img.shields.io/badge/données-6%20JSON-green?style=for-the-badge)](./data/)

---

## 🎯 Pourquoi ?

BenchLM fournit des données sur les modèles d'IA, notamment les classements, les benchmarks, les prix, la vitesse et les résultats de comparaisons.

Ce dépôt est conçu comme un **miroir simple et pratique de ces données**, destiné à être utilisé dans des projets tiers.

### Que pouvez-vous faire ?

- 📥 **Obtenir des données à jour** — les fichiers sont mis à jour automatiquement une fois par jour.
- 🕐 **Suivre l'historique des modifications** — GitHub conserve les versions précédentes des fichiers.
- 🔗 **Utiliser les données directement** — les fichiers JSON sont accessibles via GitHub Raw.
- 🚀 **Connecter les données à vos projets** — aucun serveur personnalisé n'est nécessaire pour récupérer les fichiers JSON.
- 📊 **Créer vos propres interfaces et analyses** à partir des données de BenchLM.

Le dépôt peut ainsi servir de source simple de données BenchLM pour des sites web, applications, bots, outils d'analyse et autres projets.

---

## 📊 Données

| Fichier | Description | Raw |
|:---|:---|:---:|
| [`models.json`](./data/models.json) | Informations sur les modèles d'IA | [Ouvrir](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/models.json) |
| [`leaderboard.json`](./data/leaderboard.json) | Classement des modèles | [Ouvrir](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/leaderboard.json) |
| [`benchmarks.json`](./data/benchmarks.json) | Informations sur les benchmarks | [Ouvrir](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/benchmarks.json) |
| [`pricing.json`](./data/pricing.json) | Tarification des modèles | [Ouvrir](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/pricing.json) |
| [`speed.json`](./data/speed.json) | Vitesse et performance des modèles | [Ouvrir](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/speed.json) |
| [`comparisons.json`](./data/comparisons.json) | Comparaisons de modèles | [Ouvrir](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/comparisons.json) |

---

## 🔗 Accès rapide

Toutes les données se trouvent dans le répertoire [`data/`](./data/).

### GitHub Raw

Par exemple, [`models.json`](./data/models.json) :

```text
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/models.json
```

Les autres fichiers sont disponibles à des adresses similaires :

```text
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/leaderboard.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/benchmarks.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/pricing.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/speed.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/comparisons.json
```

### API GitHub

Les fichiers peuvent également être récupérés via l'API Contents de GitHub :

```text
https://api.github.com/repos/seregannj/benchlmirror/contents/data/models.json
```

> ⚠️ Lors de l'utilisation de l'API GitHub, tenez compte de ses limites et de ses conditions d'utilisation.

---

##  Utilisation

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

## 🔄 Mise à jour automatique

Les données sont téléchargées automatiquement depuis BenchLM une fois par jour via GitHub Actions.

Processus de mise à jour :

```text
BenchLM
   ↓
Téléchargement du JSON
   ↓
Validation du fichier
   ↓
Validation du JSON
   ↓
data/
   ↓
Git commit
```

En cas d'échec du téléchargement d'un fichier, la version précédente n'est pas remplacée.

Les mises à jour peuvent également être déclenchées manuellement depuis l'onglet Actions.

---

## 🕐 Historique des modifications

Toutes les modifications des fichiers sont conservées dans l'historique Git.

Cela permet de :

- consulter les versions précédentes des données ;
- comparer les modifications entre les mises à jour ;
- suivre les évolutions des classements, prix et autres données ;
- restaurer une version antérieure du fichier si nécessaire.

L'historique des modifications est disponible dans l'onglet Commits du dépôt.

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

Source des données :

[BenchLM](https://benchlm.ai/)

Ce dépôt est un miroir indépendant et n'est pas directement affilié à BenchLM.

---

## ⚖️ Licence et données

Le code et la configuration de ce dépôt sont distribués sous la licence MIT.

Les données mises en miroir appartiennent à leur source d'origine.

La licence MIT ne s'applique pas automatiquement aux données de BenchLM.

Avant d'utiliser les données, veuillez consulter les conditions et exigences de leur source d'origine.

---

<div align="center">

Data from BenchLM

[BenchLM](https://benchlm.ai/) · [GitHub](https://github.com/seregannj/benchlmirror) · [Source des données](https://benchlm.ai/data)

</div>
