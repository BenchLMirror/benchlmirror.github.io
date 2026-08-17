


# Espejo de BenchLM

<div align="center">

[🇬🇧 English](README.md) · [🇷🇺 Русский](README.ru.md) · [🇨🇳 中文](README.zh.md) · 🇪🇸 Español · [🇩🇪 Deutsch](README.de.md) · [🇫🇷 Français](README.fr.md) · [🇯🇵 日本語](README.ja.md) · [🇰🇷 한국어](README.ko.md)

</div>

> Un espejo de datos públicos de [BenchLM](https://benchlm.ai/) actualizado automáticamente.

[![Actualización](https://img.shields.io/badge/actualización-diaria-blue?style=for-the-badge)](https://github.com/seregannj/benchlmirror/actions)
[![Fuente](https://img.shields.io/badge/fuente-BenchLM-black?style=for-the-badge)](https://benchlm.ai/data)
[![Archivos](https://img.shields.io/badge/datos-6%20JSON-green?style=for-the-badge)](./data/)

---

## 🎯 ¿Por qué?

BenchLM proporciona datos sobre modelos de IA, incluyendo clasificaciones, pruebas comparativas, precios, velocidad y resultados de comparaciones.

Este repositorio está diseñado como un **espejo simple y conveniente de estos datos** para su uso en proyectos de terceros.

### ¿Qué puedes hacer?

- 📥 **Obtener datos actualizados** — los archivos se actualizan automáticamente una vez al día.
- 🕐 **Seguir el historial de cambios** — GitHub conserva las versiones anteriores de los archivos.
- 🔗 **Usar los datos directamente** — los archivos JSON están disponibles a través de GitHub Raw.
- 🚀 **Conectar los datos a tus proyectos** — no se necesita un servidor personalizado para obtener los archivos JSON.
- 📊 **Crear interfaces y análisis personalizados** basados en los datos de BenchLM.

Por lo tanto, el repositorio puede usarse como una fuente simple de datos de BenchLM para sitios web, aplicaciones, bots, herramientas de análisis y otros proyectos.

---

## 📊 Datos

| Archivo | Descripción | Raw |
|:---|:---|:---:|
| [`models.json`](./data/models.json) | Información sobre modelos de IA | [Abrir](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/models.json) |
| [`leaderboard.json`](./data/leaderboard.json) | Clasificación de modelos | [Abrir](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/leaderboard.json) |
| [`benchmarks.json`](./data/benchmarks.json) | Información de pruebas comparativas | [Abrir](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/benchmarks.json) |
| [`pricing.json`](./data/pricing.json) | Precios de los modelos | [Abrir](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/pricing.json) |
| [`speed.json`](./data/speed.json) | Velocidad y rendimiento de los modelos | [Abrir](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/speed.json) |
| [`comparisons.json`](./data/comparisons.json) | Comparaciones de modelos | [Abrir](https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/comparisons.json) |

---

## 🔗 Acceso rápido

Todos los datos se encuentran en el directorio [`data/`](./data/).

### GitHub Raw

Por ejemplo, [`models.json`](./data/models.json):

```text
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/models.json
```

Los demás archivos están disponibles en direcciones similares:

```text
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/leaderboard.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/benchmarks.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/pricing.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/speed.json
https://raw.githubusercontent.com/seregannj/benchlmirror/main/data/comparisons.json
```

### GitHub API

Los archivos también se pueden obtener a través de la API de contenidos de GitHub:

```text
https://api.github.com/repos/seregannj/benchlmirror/contents/data/models.json
```

> ⚠️ Al usar la API de GitHub, ten en cuenta sus limitaciones y condiciones de uso.

---

## 💻 Uso

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

## 🔄 Actualización automática

Los datos se descargan automáticamente desde BenchLM una vez al día mediante GitHub Actions.

Proceso de actualización:

```text
BenchLM
   ↓
Descarga de JSON
   ↓
Validación del archivo
   ↓
Validación de JSON
   ↓
data/
   ↓
Git commit
```

Si falla la descarga de un archivo, no se reemplaza la versión anterior.

Las actualizaciones también se pueden activar manualmente desde la pestaña Actions.

---

## 🕐 Historial de cambios

Todos los cambios en los archivos se conservan en el historial de Git.

Esto permite:

- ver versiones anteriores de los datos;
- comparar cambios entre actualizaciones;
- seguir los cambios en las clasificaciones, precios y otros datos;
- restaurar una versión anterior del archivo cuando sea necesario.

El historial de cambios está disponible en la pestaña Commits del repositorio.

---

## 📁 Estructura

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

## 🔗 Fuente

Fuente de datos:

[BenchLM](https://benchlm.ai/)

Este repositorio es un espejo independiente y no está afiliado directamente con BenchLM.

---

## ⚖️ Licencia y datos

El código y la configuración de este repositorio se distribuyen bajo la Licencia MIT.

Los datos reflejados pertenecen a su fuente original.

La Licencia MIT no se aplica automáticamente a los datos de BenchLM.

Antes de usar los datos, consulta los términos y requisitos de su fuente original.

---

<div align="center">

Data from BenchLM

[BenchLM](https://benchlm.ai/) · [GitHub](https://github.com/seregannj/benchlmirror) · [Fuente de datos](https://benchlm.ai/data)

</div>
