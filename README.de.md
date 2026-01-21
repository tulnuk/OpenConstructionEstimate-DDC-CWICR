<p align="center">
  <a href="https://datadrivenconstruction.io">
    <img src="https://datadrivenconstruction.io/wp-content/uploads/2023/07/DataDrivenConstruction-1-1.png" alt="DDC Logo" width="200"/>
  </a>
</p>

<h1 align="center">DDC CWICR: Offene Baukostendatenbank</h1>

<p align="center">
  <b>55.719 Arbeitspositionen | 27.672 Ressourcen | 9 Sprachen | 85 Datenfelder</b>
</p>

<p align="center">
  <a href="README.md">🇬🇧 English</a> •
  <a href="README.ru.md">🇷🇺 Русский</a> •
  <a href="README.de.md">🇩🇪 Deutsch</a> •
  <a href="README.es.md">🇪🇸 Español</a> •
  <a href="README.fr.md">🇫🇷 Français</a> •
  <a href="README.zh.md">🇨🇳 中文</a> •
  <a href="README.ar.md">🇸🇦 العربية</a>
</p>

<p align="center">
  <a href="https://github.com/datadrivenconstruction/OpenConstructionEstimate-DDC-CWICR/stargazers"><img src="https://img.shields.io/github/stars/datadrivenconstruction/OpenConstructionEstimate-DDC-CWICR?style=social" alt="GitHub Stars"/></a>
  <a href="https://github.com/datadrivenconstruction/OpenConstructionEstimate-DDC-CWICR/blob/main/LICENSE"><img src="https://img.shields.io/badge/Datenbank-CC%20BY%204.0-green" alt="License CC BY 4.0"/></a>
  <a href="https://github.com/datadrivenconstruction/OpenConstructionEstimate-DDC-CWICR/blob/main/LICENSE"><img src="https://img.shields.io/badge/Code-MIT-blue" alt="License MIT"/></a>
</p>

---

## Überblick

**DDC CWICR** (Construction Work Items, Components & Resources) ist eine umfassende Open-Source-Datenbank für die Baukostenkalkulation. Die Datenbank ermöglicht automatisierte Kostenberechnungen durch KI-gestützte Workflows und semantische Vektordatenbanksuche.

### Warum DDC CWICR?

| Traditioneller Ansatz | DDC CWICR Ansatz |
|----------------------|------------------|
| Manuelle Preissuche | Semantische KI-Suche |
| Statische Preislisten | Regionale dynamische Preisgestaltung |
| Eine Sprache | 9 Sprachen, 10+ Länder |
| Geschlossene Formate | Offene Formate (Parquet, Excel, Qdrant) |
| Keine KI-Integration | Native KI/LLM-Unterstützung |

---

## Inhaltsverzeichnis

- [Datenbankinhalt](#datenbankinhalt)
- [Verfügbare Formate](#verfügbare-formate)
- [Sprachen & Regionale Preise](#sprachen--regionale-preise)
- [n8n Workflows](#n8n-workflows)
  - [1. Text-Schätzer-Bot](#1-text-schätzer-bot)
  - [2. Foto-Kostenschätzer](#2-foto-kostenschätzer)
  - [3. Universal-Bot](#3-universal-bot)
  - [4. CAD/BIM Pipeline](#4-cadbim-pipeline)
- [Schnellstart](#schnellstart)
- [KI-Integration](#ki-integration)
- [AI Instructions Ordner](#ai-instructions-ordner)
- [Technische Architektur](#technische-architektur)
- [Datenbankschema](#datenbankschema)
- [Anwendungsfälle](#anwendungsfälle)
- [Integration mit CAD2DATA](#integration-mit-cad2data)
- [Lizenz](#lizenz)
- [Ressourcen](#ressourcen)

---

## Datenbankinhalt

| Metrik | Wert |
|--------|------|
| Arbeitspositionen | 55.719 |
| Ressourcen | 27.672 |
| Datenfelder | 85 |
| Sprachen | 9 |
| Länder | 10+ |
| Embedding-Dimensionen | 3.072 (OpenAI text-embedding-3-large) |

### Was enthalten ist

- **Arbeitspositionen**: Vollständige Bauarbeiten mit Beschreibungen, Einheiten und Kosten
- **Materialien**: Mengen, Einheitskosten, Gewichte, Spezifikationen
- **Arbeitskräfte**: Qualifikationen, Stunden, Stundensätze
- **Maschinen**: Gerätetypen, Maschinenstunden, Kraftstoffverbrauch, Bedienerlöhne
- **Kostenaggregate**: Gesamtkosten, Gemeinkosten, Gewinnmargen, MwSt.

---

## Verfügbare Formate

| Format | Datei | Ideal für |
|--------|-------|-----------|
| **Parquet** | `DDC_CWICR_{LANG}.parquet` | Python/Pandas, Big Data Verarbeitung |
| **Excel** | `DDC_CWICR_{LANG}.xlsx` | Manuelle Analyse, Teilen |
| **CSV** | `DDC_CWICR_{LANG}.csv` | Universelle Kompatibilität |
| **Qdrant Snapshot** | `qdrant_snapshot_{lang}.snapshot` | Vektorsuche, semantische Abfragen |

---

## Sprachen & Regionale Preise

| Sprache | Code | Region | Währung | Qdrant Collection |
|---------|------|--------|---------|-------------------|
| 🇸🇦 Arabisch | AR | Dubai | AED | `ddc_cwicr_ar` |
| 🇨🇳 Chinesisch | ZH | Shanghai | CNY | `ddc_cwicr_zh` |
| 🇩🇪 Deutsch | DE | Berlin | EUR | `ddc_cwicr_de` |
| 🇬🇧 Englisch | EN | Toronto | CAD | `ddc_cwicr_en` |
| 🇪🇸 Spanisch | ES | Barcelona | EUR | `ddc_cwicr_es` |
| 🇫🇷 Französisch | FR | Paris | EUR | `ddc_cwicr_fr` |
| 🇮🇳 Hindi | HI | Mumbai | INR | `ddc_cwicr_hi` |
| 🇧🇷 Portugiesisch | PT | São Paulo | BRL | `ddc_cwicr_pt` |
| 🇷🇺 Russisch | RU | St. Petersburg | RUB | `ddc_cwicr_ru` |

---

## n8n Workflows

Vier produktionsreife Workflows für automatisierte Kostenschätzung.

### 1. Text-Schätzer-Bot

**Datei**: `n8n_CWICR_Text_Estimator_Bot.json`

Natürliche Spracheingabe für schnelle Umwandlung von Leistungsumfang zu Kostenvoranschlag.

```
Benutzer: "Ich brauche 50 m³ Beton für ein Fundament"
Bot: Liefert passende Arbeitspositionen mit Kosten, Materialien, Arbeitsaufschlüsselung
```

**Funktionen:**
- Verständnis natürlicher Sprache
- Semantische Suche über Qdrant
- Mehrsprachige Unterstützung
- Telegram/WhatsApp Integration

---

### 2. Foto-Kostenschätzer

**Datei**: `n8n_CWICR_Photo_Estimator_Bot.json`

KI Vision analysiert Baufotos und erstellt Kostenvoranschläge.

```
Benutzer: [lädt Foto einer Ziegelwand hoch]
Bot: Identifiziert Mauerwerk, berechnet Fläche, liefert Kostenvoranschlag
```

**Funktionen:**
- GPT-4 Vision / Claude Vision
- Automatische Materialerkennung
- Mengenextraktion aus Bildern
- Vorher/Nachher-Vergleich

---

### 3. Universal-Bot

**Datei**: `n8n_CWICR_Universal_Bot.json`

Akzeptiert Text, Fotos und PDFs mit intelligenter Weiterleitung.

**Funktionen:**
- Multimodale Eingabe (Text, Bilder, Dokumente)
- Intelligente Weiterleitung zum passenden Schätzer
- PDF-Parsing für Spezifikationen
- Kombinierte Schätzungen aus mehreren Quellen

---

### 4. CAD/BIM Pipeline

**Datei**: `n8n_CWICR_CAD_BIM_Pipeline.json`

Verarbeitet Revit/IFC/DWG-Modelle für 4D/5D-Schätzung.

```
Eingabe: Building.rvt (oder .ifc, .dwg)
Ausgabe: Vollständiger Kostenvoranschlag mit Ressourcenaufschlüsselung
```

**Funktionen:**
- Direkte Integration mit [CAD2DATA Konvertern](https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto)
- Element-für-Element Kostenzuweisung
- Vollständige Ressourcenaufschlüsselung (Material, Arbeit, Ausrüstung)
- 4D Zeitplanungsunterstützung
- 5D Kostenvisualisierung

---

## Schnellstart

### Python (Pandas)

```python
import pandas as pd

# Datenbank laden
df = pd.read_parquet("DDC_CWICR_DE.parquet")
print(f"Gesamtdatensätze: {len(df):,}")

# Betonarbeiten finden
concrete = df[df['rate_original_name'].str.contains('Beton', case=False, na=False)]
print(concrete[['rate_code', 'rate_original_name', 'rate_unit_of_measure', 'total_cost_per_position']])
```

### Qdrant (Semantische Suche)

```python
from qdrant_client import QdrantClient
from openai import OpenAI

# Verbinden
qdrant = QdrantClient(host="localhost", port=6333)
openai = OpenAI()

# Suchen
query = "Stahlbetonfundament gießen"
embedding = openai.embeddings.create(input=query, model="text-embedding-3-large").data[0].embedding

results = qdrant.search(
    collection_name="ddc_cwicr_de",
    query_vector=embedding,
    limit=5
)

for r in results:
    print(f"{r.payload['rate_code']}: {r.payload['rate_original_name']}")
    print(f"  Kosten: {r.payload['total_cost_per_position']} {r.payload['currency_code']}")
```

### n8n Workflow

1. n8n installieren: `npx n8n`
2. Workflow-JSON-Datei importieren
3. Credentials konfigurieren (OpenAI, Qdrant, Telegram)
4. Workflow ausführen

---

## KI-Integration

DDC CWICR arbeitet nahtlos mit modernen KI-Tools:

| Tool | Integration |
|------|-------------|
| **Claude Code** | Vollständiger Kontext über AI_INSTRUCTIONS Ordner |
| **Google Antigravity** | GCP-Muster (BigQuery, Vertex AI) |
| **n8n** | Fertige Workflow-Vorlagen |
| **Dify** | LLM-Anwendungsentwicklung |
| **LangChain** | RAG-Pipelines |
| **LlamaIndex** | Wissensbasis-Integration |

### Beispiel: Claude Code

```
Sie: "Finde alle Malerarbeiten und berechne Kosten für 500 m²"
Claude: [liest AI_INSTRUCTIONS, fragt Datenbank ab, liefert formatiertes Ergebnis]
```

---

## AI Instructions Ordner

Der `AI_INSTRUCTIONS/` Ordner enthält Dokumentation für KI-Programmierassistenten.

| Datei | Zweck |
|-------|-------|
| `INSTRUCTIONS.md` | Hauptübersicht, Schnellstart, Datenformate |
| `CLAUDE.md` | Claude Code spezifische Muster und Beispiele |
| `OPENCODE.md` | Kurzanleitungen für Opencode |
| `ANTIGRAVITY.md` | GCP-Integration (BigQuery, Vertex AI, Qdrant) |
| `DATABASE_SCHEMA.md` | Vollständige 85-Felder-Schemareferenz |

### Warum das wichtig ist

- KI-Assistenten lesen diese Dateien um Kontext zu verstehen
- Enthält CLI-Syntax, Integrationsmuster, Best Practices
- Ermöglicht natürlichsprachliche Abfragen an die Datenbank
- Beschleunigt Entwicklung mit KI-assistierter Programmierung

### Verwendung

```bash
# KI-Assistenten lesen automatisch AI_INSTRUCTIONS
# Oder direkt verweisen:
"Lies AI_INSTRUCTIONS/CLAUDE.md und hilf mir eine Kostenschätzungsabfrage zu erstellen"
```

---

## Technische Architektur

```
┌─────────────────────────────────────────────────────────────┐
│                      EINGABESCHICHT                         │
├─────────────┬─────────────┬─────────────┬──────────────────┤
│    Text     │    Foto     │    PDF      │    CAD/BIM       │
│ (Telegram)  │  (Vision)   │  (Parser)   │ (Revit/IFC/DWG)  │
└──────┬──────┴──────┬──────┴──────┬──────┴────────┬─────────┘
       │             │             │               │
       └─────────────┴──────┬──────┴───────────────┘
                            ▼
┌─────────────────────────────────────────────────────────────┐
│                   KI-VERARBEITUNGSSCHICHT                   │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────────────┐ │
│  │   OpenAI    │  │   Claude    │  │      Gemini         │ │
│  │  Embedding  │  │   Vision    │  │      Vision         │ │
│  └──────┬──────┘  └──────┬──────┘  └──────────┬──────────┘ │
└─────────┼────────────────┼────────────────────┼────────────┘
          │                │                    │
          └────────────────┼────────────────────┘
                           ▼
┌─────────────────────────────────────────────────────────────┐
│                   SUCH- & ABGLEICHSCHICHT                   │
│  ┌─────────────────────────────────────────────────────┐   │
│  │            Qdrant Vektordatenbank                    │   │
│  │         (55.719 Positionen × 3.072 Dimensionen)     │   │
│  └─────────────────────────────────────────────────────┘   │
└─────────────────────────────┬───────────────────────────────┘
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                    BERECHNUNGSSCHICHT                       │
│                                                             │
│   Kosten = Material + Arbeit + Maschinen + Gemeinkosten +  │
│            Gewinn                                           │
│   Wo:                                                       │
│   • Material = Σ(Menge × Einheitskosten)                   │
│   • Arbeit = Stunden × Stundensatz                         │
│   • Maschinen = Maschinenstunden × Gerätesatz              │
└─────────────────────────────┬───────────────────────────────┘
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                      AUSGABESCHICHT                         │
├─────────────┬─────────────┬─────────────┬──────────────────┤
│    Excel    │    JSON     │    PDF      │      HTML        │
│   Bericht   │     API     │   Bericht   │   Dashboard      │
└─────────────┴─────────────┴─────────────┴──────────────────┘
```

---

## Datenbankschema

Die Datenbank enthält **85 Felder**, organisiert in 10 Gruppen:

| Gruppe | Felder | Schlüsselfelder |
|--------|--------|-----------------|
| Klassifikation | 6 | `category_name`, `department_name`, `section_name` |
| Arbeitspositions-ID | 8 | `rate_code`, `rate_original_name`, `rate_unit_of_measure` |
| Materialien | 12 | `material_name`, `material_quantity`, `material_unit_cost` |
| Arbeitskräfte | 10 | `labor_hours`, `labor_hourly_rate`, `labor_total_cost` |
| Maschinen | 12 | `machinery_name`, `machinery_hours`, `machinery_total_cost` |
| Kostenaggregate | 8 | `total_cost_per_position`, `total_material_cost` |
| Preisstatistik | 6 | `price_min`, `price_max`, `price_median` |
| Physische Eigenschaften | 8 | `mass_total_kg`, `volume_m3`, `area_m2` |
| Regional | 8 | `language_code`, `currency_code`, `region_name` |
| Metadaten | 7 | `created_at`, `data_quality_score`, `is_active` |

**Vollständiges Schema**: Siehe [AI_INSTRUCTIONS/DATABASE_SCHEMA.md](AI_INSTRUCTIONS/DATABASE_SCHEMA.md)

---

## Anwendungsfälle

### 1. Schnelle Schätzung
```
Auftragnehmer: "Was kostet 100 m² Keramikfliesenboden?"
System: Liefert Kostenaufschlüsselung mit Materialien, Arbeit, Zeitrahmen
```

### 2. BIM-Kostenintegration
```
Architekt: Lädt Revit-Modell hoch
System: Extrahiert Mengen, gleicht Arbeitspositionen ab, erstellt 5D-Schätzung
```

### 3. Mehrsprachige Projekte
```
Internationales Unternehmen: Braucht Schätzungen auf Deutsch und Arabisch
System: Gleiche Arbeitspositionen, lokalisierte Preise und Beschreibungen
```

### 4. KI-gestützte Ausschreibungen
```
Kalkulator: "Analysiere dieses PDF-Leistungsverzeichnis und erstelle Kostenvoranschlag"
System: Parst Dokument, identifiziert Umfang, berechnet Kosten
```

---

## Integration mit CAD2DATA

DDC CWICR integriert sich nahtlos mit den [CAD2DATA](https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto) Konvertern:

```
Revit/IFC/DWG → CAD2DATA → XLSX/DAE → DDC CWICR → Kostenvoranschlag
```

**Workflow:**
1. BIM-Modell mit CAD2DATA konvertieren
2. Elementmengen extrahieren
3. Elemente mit CWICR-Positionen abgleichen
4. Kosten mit regionalen Preisen berechnen
5. Berichte generieren

---

## Lizenz

- **Datenbank**: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — Kostenlose kommerzielle Nutzung mit Namensnennung
- **Code**: [MIT](https://opensource.org/licenses/MIT) — Uneingeschränkte Nutzung

---

## Ressourcen

| Ressource | Link |
|-----------|------|
| Live-Demo | [openconstructionestimate.com](https://openconstructionestimate.com) |
| GitHub | [datadrivenconstruction](https://github.com/datadrivenconstruction) |
| CAD2DATA Tools | [cad2data Repository](https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto) |
| Buch | [Data-Driven Construction](https://datadrivenconstruction.io/book) |
| Telegram Bot | Workflows sofort testen |

---

<p align="center">
  <a href="https://datadrivenconstruction.io">
    <img src="https://datadrivenconstruction.io/wp-content/uploads/2023/07/DataDrivenConstruction-1-1.png" alt="DDC Logo" width="150"/>
  </a>
  <br>
  <b>Entfesseln Sie die Kraft der Daten im Bauwesen</b>
  <br>
  <sub>Ihre Daten gehören Ihnen</sub>
</p>
