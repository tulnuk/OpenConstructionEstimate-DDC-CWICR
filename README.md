<p align="center">
  <a href="https://datadrivenconstruction.io">
    <img src="https://datadrivenconstruction.io/wp-content/uploads/2023/07/DataDrivenConstruction-1-1.png" alt="DDC Logo" width="200"/>
  </a>
</p>

<h1 align="center">DDC CWICR: Open Construction Cost Database</h1>

<p align="center">
  <b>55,719 Work Items | 27,672 Resources | 9 Languages | 85 Data Fields</b>
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
  <a href="https://github.com/datadrivenconstruction/OpenConstructionEstimate-DDC-CWICR/blob/main/LICENSE"><img src="https://img.shields.io/badge/Database-CC%20BY%204.0-green" alt="License CC BY 4.0"/></a>
  <a href="https://github.com/datadrivenconstruction/OpenConstructionEstimate-DDC-CWICR/blob/main/LICENSE"><img src="https://img.shields.io/badge/Code-MIT-blue" alt="License MIT"/></a>
</p>

---

## Overview

**DDC CWICR** (Construction Work Items, Components & Resources) is a comprehensive open-source database for construction cost estimation. The database enables automated cost calculations through AI-powered workflows and vector database semantic search.

### Why DDC CWICR?

| Traditional Approach | DDC CWICR Approach |
|---------------------|-------------------|
| Manual cost lookups | Semantic AI search |
| Static price lists | Regional dynamic pricing |
| Single language | 9 languages, 10+ countries |
| Closed formats | Open formats (Parquet, Excel, Qdrant) |
| No AI integration | Native AI/LLM support |

---

## Table of Contents

- [Database Content](#database-content)
- [Available Formats](#available-formats)
- [Languages & Regional Pricing](#languages--regional-pricing)
- [n8n Workflows](#n8n-workflows)
  - [1. Text Estimator Bot](#1-text-estimator-bot)
  - [2. Photo Cost Estimator](#2-photo-cost-estimator)
  - [3. Universal Bot](#3-universal-bot)
  - [4. CAD/BIM Pipeline](#4-cadbim-pipeline)
- [Quick Start](#quick-start)
- [AI Integration](#ai-integration)
- [AI Instructions Folder](#ai-instructions-folder)
- [Technical Architecture](#technical-architecture)
- [Database Schema](#database-schema)
- [Use Cases](#use-cases)
- [Integration with CAD2DATA](#integration-with-cad2data)
- [License](#license)
- [Resources](#resources)

---

## Database Content

| Metric | Value |
|--------|-------|
| Work Items | 55,719 |
| Resources | 27,672 |
| Data Fields | 85 |
| Languages | 9 |
| Countries | 10+ |
| Embedding Dimensions | 3,072 (OpenAI text-embedding-3-large) |

### What's Included

- **Work Items**: Complete construction tasks with descriptions, units, and costs
- **Materials**: Quantities, unit costs, weights, specifications
- **Labor**: Worker qualifications, hours, hourly rates
- **Machinery**: Equipment types, hours, fuel consumption, operator wages
- **Cost Aggregates**: Total costs, overheads, profit margins, VAT

---

## Available Formats

| Format | File | Best For |
|--------|------|----------|
| **Parquet** | `DDC_CWICR_{LANG}.parquet` | Python/Pandas, big data processing |
| **Excel** | `DDC_CWICR_{LANG}.xlsx` | Manual analysis, sharing |
| **CSV** | `DDC_CWICR_{LANG}.csv` | Universal compatibility |
| **Qdrant Snapshot** | `qdrant_snapshot_{lang}.snapshot` | Vector search, semantic queries |

---

## Languages & Regional Pricing

| Language | Code | Region | Currency | Qdrant Collection |
|----------|------|--------|----------|-------------------|
| 🇸🇦 Arabic | AR | Dubai | AED | `ddc_cwicr_ar` |
| 🇨🇳 Chinese | ZH | Shanghai | CNY | `ddc_cwicr_zh` |
| 🇩🇪 German | DE | Berlin | EUR | `ddc_cwicr_de` |
| 🇬🇧 English | EN | Toronto | CAD | `ddc_cwicr_en` |
| 🇪🇸 Spanish | ES | Barcelona | EUR | `ddc_cwicr_es` |
| 🇫🇷 French | FR | Paris | EUR | `ddc_cwicr_fr` |
| 🇮🇳 Hindi | HI | Mumbai | INR | `ddc_cwicr_hi` |
| 🇧🇷 Portuguese | PT | São Paulo | BRL | `ddc_cwicr_pt` |
| 🇷🇺 Russian | RU | St. Petersburg | RUB | `ddc_cwicr_ru` |

---

## n8n Workflows

Four production-ready workflows for automated cost estimation.

### 1. Text Estimator Bot

**File**: `n8n_CWICR_Text_Estimator_Bot.json`

Natural language input for quick scope-to-estimate conversions.

```
User: "I need to pour 50 m³ of concrete for a foundation"
Bot: Returns matching work items with costs, materials, labor breakdown
```

**Features:**
- Natural language understanding
- Semantic search via Qdrant
- Multi-language support
- Telegram/WhatsApp integration

---

### 2. Photo Cost Estimator

**File**: `n8n_CWICR_Photo_Estimator_Bot.json`

AI Vision analyzes construction photos and generates estimates.

```
User: [uploads photo of brick wall]
Bot: Identifies brickwork, calculates area, returns cost estimate
```

**Features:**
- GPT-4 Vision / Claude Vision
- Automatic material identification
- Quantity extraction from images
- Before/after comparison

---

### 3. Universal Bot

**File**: `n8n_CWICR_Universal_Bot.json`

Accepts text, photos, and PDFs with intelligent routing.

**Features:**
- Multi-modal input (text, images, documents)
- Smart routing to appropriate estimator
- PDF parsing for specifications
- Combined estimates from multiple sources

---

### 4. CAD/BIM Pipeline

**File**: `n8n_CWICR_CAD_BIM_Pipeline.json`

Processes Revit/IFC/DWG models for 4D/5D estimation.

```
Input: Building.rvt (or .ifc, .dwg)
Output: Complete cost estimate with resource breakdown
```

**Features:**
- Direct integration with [CAD2DATA converters](https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto)
- Element-by-element cost assignment
- Full resource breakdown (materials, labor, equipment)
- 4D scheduling support
- 5D cost visualization

---

## Quick Start

### Python (Pandas)

```python
import pandas as pd

# Load database
df = pd.read_parquet("DDC_CWICR_EN.parquet")
print(f"Total records: {len(df):,}")

# Find concrete work
concrete = df[df['rate_original_name'].str.contains('concrete', case=False, na=False)]
print(concrete[['rate_code', 'rate_original_name', 'rate_unit_of_measure', 'total_cost_per_position']])
```

### Qdrant (Semantic Search)

```python
from qdrant_client import QdrantClient
from openai import OpenAI

# Connect
qdrant = QdrantClient(host="localhost", port=6333)
openai = OpenAI()

# Search
query = "reinforced concrete foundation pouring"
embedding = openai.embeddings.create(input=query, model="text-embedding-3-large").data[0].embedding

results = qdrant.search(
    collection_name="ddc_cwicr_en",
    query_vector=embedding,
    limit=5
)

for r in results:
    print(f"{r.payload['rate_code']}: {r.payload['rate_original_name']}")
    print(f"  Cost: {r.payload['total_cost_per_position']} {r.payload['currency_code']}")
```

### n8n Workflow

1. Install n8n: `npx n8n`
2. Import workflow JSON file
3. Configure credentials (OpenAI, Qdrant, Telegram)
4. Execute workflow

---

## AI Integration

DDC CWICR works seamlessly with modern AI tools:

| Tool | Integration |
|------|-------------|
| **Claude Code** | Full context via AI_INSTRUCTIONS folder |
| **Google Antigravity** | GCP patterns (BigQuery, Vertex AI) |
| **n8n** | Ready-to-use workflow templates |
| **Dify** | LLM application development |
| **LangChain** | RAG pipelines |
| **LlamaIndex** | Knowledge base integration |

### Example: Claude Code

```
You: "Find all painting work items and calculate cost for 500 m²"
Claude: [reads AI_INSTRUCTIONS, queries database, returns formatted result]
```

---

## AI Instructions Folder

The `AI_INSTRUCTIONS/` folder contains documentation for AI coding assistants.

| File | Purpose |
|------|---------|
| `INSTRUCTIONS.md` | Main overview, quick start, data formats |
| `CLAUDE.md` | Claude Code specific patterns and examples |
| `OPENCODE.md` | Concise instructions for Opencode |
| `ANTIGRAVITY.md` | GCP integration (BigQuery, Vertex AI, Qdrant) |
| `DATABASE_SCHEMA.md` | Complete 85-field schema reference |

### Why This Matters

- AI assistants read these files to understand context
- Contains CLI syntax, integration patterns, best practices
- Enables natural language queries to the database
- Accelerates development with AI-assisted coding

### How to Use

```bash
# AI assistants automatically read AI_INSTRUCTIONS
# Or point them directly:
"Read AI_INSTRUCTIONS/CLAUDE.md and help me build a cost estimation query"
```

---

## Technical Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                        INPUT LAYER                          │
├─────────────┬─────────────┬─────────────┬──────────────────┤
│    Text     │   Photo     │    PDF      │    CAD/BIM       │
│  (Telegram) │  (Vision)   │  (Parser)   │ (Revit/IFC/DWG)  │
└──────┬──────┴──────┬──────┴──────┬──────┴────────┬─────────┘
       │             │             │               │
       └─────────────┴──────┬──────┴───────────────┘
                            ▼
┌─────────────────────────────────────────────────────────────┐
│                    AI PROCESSING LAYER                      │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────────────┐ │
│  │   OpenAI    │  │   Claude    │  │      Gemini         │ │
│  │  Embedding  │  │   Vision    │  │      Vision         │ │
│  └──────┬──────┘  └──────┬──────┘  └──────────┬──────────┘ │
└─────────┼────────────────┼────────────────────┼────────────┘
          │                │                    │
          └────────────────┼────────────────────┘
                           ▼
┌─────────────────────────────────────────────────────────────┐
│                    SEARCH & MATCH LAYER                     │
│  ┌─────────────────────────────────────────────────────┐   │
│  │              Qdrant Vector Database                  │   │
│  │         (55,719 items × 3,072 dimensions)           │   │
│  └─────────────────────────────────────────────────────┘   │
└─────────────────────────────┬───────────────────────────────┘
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                    CALCULATION LAYER                        │
│                                                             │
│   Cost = Materials + Labor + Equipment + Overhead + Profit  │
│                                                             │
│   Where:                                                    │
│   • Materials = Σ(quantity × unit_cost)                    │
│   • Labor = hours × hourly_rate                            │
│   • Equipment = machine_hours × equipment_rate             │
└─────────────────────────────┬───────────────────────────────┘
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                      OUTPUT LAYER                           │
├─────────────┬─────────────┬─────────────┬──────────────────┤
│    Excel    │    JSON     │    PDF      │      HTML        │
│   Report    │     API     │   Report    │    Dashboard     │
└─────────────┴─────────────┴─────────────┴──────────────────┘
```

---

## Database Schema

The database contains **85 fields** organized into 10 groups:

| Group | Fields | Key Fields |
|-------|--------|------------|
| Classification | 6 | `category_name`, `department_name`, `section_name` |
| Work Item ID | 8 | `rate_code`, `rate_original_name`, `rate_unit_of_measure` |
| Materials | 12 | `material_name`, `material_quantity`, `material_unit_cost` |
| Labor | 10 | `labor_hours`, `labor_hourly_rate`, `labor_total_cost` |
| Machinery | 12 | `machinery_name`, `machinery_hours`, `machinery_total_cost` |
| Cost Aggregates | 8 | `total_cost_per_position`, `total_material_cost` |
| Price Statistics | 6 | `price_min`, `price_max`, `price_median` |
| Physical Properties | 8 | `mass_total_kg`, `volume_m3`, `area_m2` |
| Regional | 8 | `language_code`, `currency_code`, `region_name` |
| Metadata | 7 | `created_at`, `data_quality_score`, `is_active` |

**Full schema**: See [AI_INSTRUCTIONS/DATABASE_SCHEMA.md](AI_INSTRUCTIONS/DATABASE_SCHEMA.md)

---

## Use Cases

### 1. Quick Estimation
```
Contractor: "How much for 100 m² of ceramic tile flooring?"
System: Returns cost breakdown with materials, labor, timeframe
```

### 2. BIM Cost Integration
```
Architect: Uploads Revit model
System: Extracts quantities, matches work items, generates 5D estimate
```

### 3. Multilingual Projects
```
International firm: Needs estimates in German and Arabic
System: Same work items, localized pricing and descriptions
```

### 4. AI-Assisted Bidding
```
Estimator: "Analyze this specification PDF and create estimate"
System: Parses document, identifies scope, calculates costs
```

---

## Integration with CAD2DATA

DDC CWICR integrates seamlessly with the [CAD2DATA](https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto) converters:

```
Revit/IFC/DWG → CAD2DATA → XLSX/DAE → DDC CWICR → Cost Estimate
```

**Workflow:**
1. Convert BIM model with CAD2DATA
2. Extract element quantities
3. Match elements to CWICR work items
4. Calculate costs with regional pricing
5. Generate reports

---

## License

- **Database**: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — Free commercial use with attribution
- **Code**: [MIT](https://opensource.org/licenses/MIT) — Unrestricted use

---

## Resources

| Resource | Link |
|----------|------|
| Live Demo | [openconstructionestimate.com](https://openconstructionestimate.com) |
| GitHub | [datadrivenconstruction](https://github.com/datadrivenconstruction) |
| CAD2DATA Tools | [cad2data Repository](https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto) |
| Book | [Data-Driven Construction](https://datadrivenconstruction.io/book) |
| Telegram Bot | Test workflows instantly |

---

<p align="center">
  <a href="https://datadrivenconstruction.io">
    <img src="https://datadrivenconstruction.io/wp-content/uploads/2023/07/DataDrivenConstruction-1-1.png" alt="DDC Logo" width="150"/>
  </a>
  <br>
  <b>Unlock the Power of Data in Construction</b>
  <br>
  <sub>Your data is yours</sub>
</p>
