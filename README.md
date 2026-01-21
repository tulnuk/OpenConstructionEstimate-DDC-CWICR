<p align="center">
  <a href="README.md">🇬🇧 English</a> •
  <a href="README.de.md">🇩🇪 Deutsch</a> •
  <a href="README.es.md">🇪🇸 Español</a> •
  <a href="README.fr.md">🇫🇷 Français</a> •
  <a href="README.ru.md">🇷🇺 Русский</a> •
  <a href="README.zh.md">🇨🇳 中文</a> •
  <a href="README.ar.md">🇸🇦 العربية</a>
</p>

<p align="center">
  <img src="https://datadrivenconstruction.io/wp-content/uploads/2025/09/DDC-CWICR-Banner.jpg" alt="DDC CWICR Banner" width="100%"/>
</p>

<p align="center">
  <a href="LICENSE">
    <img src="https://img.shields.io/badge/Database-CC%20BY%204.0-green" alt="Database License: CC BY 4.0">
  </a>
  <a href="LICENSE">
    <img src="https://img.shields.io/badge/Code-MIT-blue" alt="Code License: MIT">
  </a>
  <a href="https://datadrivenconstruction.io">
    <img src="https://img.shields.io/badge/powered%20by-DataDrivenConstruction.io-orange" alt="Powered by DataDrivenConstruction.io">
  </a>
  <br>
  <img src="https://img.shields.io/badge/Work%20Items-55,719-blue" alt="Work Items">
  <img src="https://img.shields.io/badge/Resources-27,672-green" alt="Resources">
  <img src="https://img.shields.io/badge/Languages-9-purple" alt="Languages">
  <img src="https://img.shields.io/badge/Data%20Fields-85-orange" alt="Data Fields">
</p>

<h1 align="center">DDC CWICR: Open Construction Cost Database</h1>

<h3 align="center">Construction Work Items, Components & Resources — Multilingual database with AI-powered cost estimation workflows for Revit, IFC, DWG models and natural language queries</h3>

<p align="center">
  Automate your construction cost estimation using Text Bots, Photo Analysis, PDF parsing, or CAD/BIM pipelines with no vendor lock-in and full control of your project data
</p>

<p align="center">
  <img src="https://datadrivenconstruction.io/wp-content/uploads/2025/09/DDC-CWICR-Overview.gif" alt="DDC CWICR Overview" width="100%"/>
</p>

<p align="center">
  DataDrivenConstruction clients and users
  <br>
  <a href="https://datadrivenconstruction.io/">
    <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/Clients_DataDrivenConstruction_logos.png" width="95%"/>
  </a>
  <br></br>
</p>

---

## Table of Contents

- [Tutorial Videos](#tutorial-videos)
- [Overview](#overview)
- [Database Content](#database-content)
- [Available Formats](#available-formats)
- [Languages & Regional Pricing](#languages--regional-pricing)
- [n8n Workflows](#n8n-workflows-for-cost-estimation)
  - [⚡️ 1. Text Estimator Bot](#️-1-text-estimator-bot)
  - [⚡️ 2. Photo Cost Estimator](#️-2-photo-cost-estimator)
  - [⚡️ 3. Universal Bot](#️-3-universal-bot)
  - [⚡️ 4. CAD/BIM Cost Pipeline](#️-4-cadbim-cost-pipeline)
- [Quick Start](#quick-start)
  - [Python (Pandas)](#python-pandas)
  - [Qdrant (Semantic Search)](#qdrant-semantic-search)
  - [n8n Workflow](#n8n-workflow-setup)
- [🚀 AI Integration](#-ai-integration--perfect-fuel-for-ai-products)
- [📂 AI_INSTRUCTIONS Folder](#-ai_instructions-folder--ready-context-for-ai-assistants)
- [Technical Architecture](#technical-architecture)
- [Database Schema](#database-schema)
- [Use Cases](#use-cases)
- [Integration with CAD2DATA](#integration-with-cad2data)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [🆘 Support](#support)
- [🎓 Consulting and Training](#consulting-and-training)

---

## Tutorial Videos

<table style="border: none; border-collapse: collapse;">
  <tr>
    <td style="border: none; padding-right: 12px; vertical-align: top;">
      <a href="https://www.youtube.com/watch?v=CWICR_DEMO" target="_blank">
        <img src="https://datadrivenconstruction.io/wp-content/uploads/2025/09/DDC-CWICR-Tutorial.png" alt="DDC CWICR Tutorial" width="460" height="315">
      </a>
    </td>
    <td style="border: none; vertical-align: top;">
      <b>DDC CWICR Cost Estimation Overview</b>
      <br>
      Introduction to the <strong>DDC CWICR</strong> construction cost database — text bots, photo estimation, and CAD/BIM integration workflows.<br>
      <a href="https://www.youtube.com/watch?v=CWICR_DEMO" target="_blank">Watch CWICR Overview on YouTube</a>
    </td>
  </tr>
  <tr>
    <td style="border: none; padding-right: 12px; vertical-align: top;">
      <a href="https://www.youtube.com/watch?v=TEXT_BOT_DEMO" target="_blank">
        <img src="https://datadrivenconstruction.io/wp-content/uploads/2025/09/Text-Estimator-Bot.png" alt="Text Estimator Bot" width="460" height="315">
      </a>
    </td>
    <td style="border: none; vertical-align: top;">
      <b>Text Estimator Bot Tutorial</b>
      <br>
      Step-by-step guide on using <strong>natural language</strong> to get instant construction cost estimates via Telegram or WhatsApp.<br>
      <a href="https://www.youtube.com/watch?v=TEXT_BOT_DEMO" target="_blank">Watch Text Bot Tutorial on YouTube</a>
    </td>
  </tr>
  <tr>
    <td style="border: none; padding-right: 12px; vertical-align: top;">
      <a href="https://www.youtube.com/watch?v=PHOTO_BOT_DEMO" target="_blank">
        <img src="https://datadrivenconstruction.io/wp-content/uploads/2025/09/Photo-Cost-Estimator.png" alt="Photo Cost Estimator" width="460" height="315">
      </a>
    </td>
    <td style="border: none; vertical-align: top;">
      <b>Photo Cost Estimator with AI Vision</b>
      <br>
      Learn how <strong>GPT-4 Vision</strong> and <strong>Claude Vision</strong> analyze construction photos and automatically generate cost estimates.<br>
      <a href="https://www.youtube.com/watch?v=PHOTO_BOT_DEMO" target="_blank">Watch Photo Estimator Tutorial on YouTube</a>
    </td>
  </tr>
  <tr>
    <td style="border: none; padding-right: 12px; vertical-align: top;">
      <a href="https://www.youtube.com/watch?v=CAD_BIM_DEMO" target="_blank">
        <img src="https://datadrivenconstruction.io/wp-content/uploads/2025/09/CAD-BIM-Cost-Pipeline.png" alt="CAD/BIM Cost Pipeline" width="460" height="315">
      </a>
    </td>
    <td style="border: none; vertical-align: top;">
      <b>CAD/BIM 4D/5D Cost Estimation Pipeline</b>
      <br>
      Full walkthrough: automate <strong>Revit/IFC/DWG</strong> model processing with element-by-element cost assignment and resource breakdown.<br>
      <a href="https://www.youtube.com/watch?v=CAD_BIM_DEMO" target="_blank">Watch CAD/BIM Pipeline Tutorial on YouTube</a>
    </td>
  </tr>
</table>

<p align="center">
  <img src="https://datadrivenconstruction.io/wp-content/uploads/2025/09/DDC-CWICR-Workflows.jpg" alt="DDC CWICR Workflows" width="100%"/>
</p>

---

## Overview

**DDC CWICR** (Construction Work Items, Components & Resources) is a comprehensive open-source database for construction cost estimation. The database enables automated cost calculations through AI-powered workflows and vector database semantic search.

### Why DDC CWICR?

| Traditional Approach | DDC CWICR Approach |
|---------------------|-------------------|
| Manual cost lookups in price books | Semantic AI search in natural language |
| Static price lists that expire | Regional dynamic pricing with updates |
| Single language databases | 9 languages, 10+ countries |
| Closed proprietary formats | Open formats (Parquet, Excel, Qdrant) |
| No AI integration | Native AI/LLM support with RAG |
| Manual BIM quantity takeoff | Automated CAD/BIM cost pipelines |

<p align="center">
  <img src="https://datadrivenconstruction.io/wp-content/uploads/2025/09/Traditional-vs-CWICR.jpg" alt="Traditional vs CWICR" width="100%"/>
</p>

---

⭐ <b>If you find our tools useful and would like to see more similar applications for the construction industry, please give our repositories a star.</b>
Star DDC CWICR on GitHub and be instantly notified of new releases.

<p align="center">
  <br>
  <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/GitHub%20Star%20DDC.gif" width="100%"/>
  <br></br>
</p>

---

## Database Content

| Metric | Value |
|--------|-------|
| **Work Items** | 55,719 |
| **Resources** | 27,672 |
| **Data Fields** | 85 |
| **Languages** | 9 |
| **Countries** | 10+ |
| **Embedding Dimensions** | 3,072 (OpenAI text-embedding-3-large) |

### What's Included

| Category | Description | Examples |
|----------|-------------|----------|
| **Work Items** | Complete construction tasks with descriptions, units, and costs | Concrete pouring, wall painting, roofing |
| **Materials** | Quantities, unit costs, weights, specifications | Cement, rebar, tiles, paint |
| **Labor** | Worker qualifications, hours, hourly rates | Mason, electrician, welder |
| **Machinery** | Equipment types, hours, fuel consumption, operator wages | Excavator, crane, concrete mixer |
| **Cost Aggregates** | Total costs, overheads, profit margins, VAT | Direct costs, indirect costs, final price |

<p align="center">
  <img src="https://datadrivenconstruction.io/wp-content/uploads/2025/09/CWICR-Database-Structure.jpg" alt="Database Structure" width="100%"/>
</p>

---

## Available Formats

| Format | File | Best For | Download |
|--------|------|----------|----------|
| **Parquet** | `DDC_CWICR_{LANG}.parquet` | Python/Pandas, big data processing | [Download](https://github.com/datadrivenconstruction/OpenConstructionEstimate-DDC-CWICR/releases) |
| **Excel** | `DDC_CWICR_{LANG}.xlsx` | Manual analysis, sharing | [Download](https://github.com/datadrivenconstruction/OpenConstructionEstimate-DDC-CWICR/releases) |
| **CSV** | `DDC_CWICR_{LANG}.csv` | Universal compatibility | [Download](https://github.com/datadrivenconstruction/OpenConstructionEstimate-DDC-CWICR/releases) |
| **Qdrant Snapshot** | `qdrant_snapshot_{lang}.snapshot` | Vector search, semantic queries | [Download](https://github.com/datadrivenconstruction/OpenConstructionEstimate-DDC-CWICR/releases) |

---

## Languages & Regional Pricing

| Flag | Language | Code | Region | Currency | Qdrant Collection |
|------|----------|------|--------|----------|-------------------|
| 🇸🇦 | Arabic | AR | Dubai | AED | `ddc_cwicr_ar` |
| 🇨🇳 | Chinese | ZH | Shanghai | CNY | `ddc_cwicr_zh` |
| 🇩🇪 | German | DE | Berlin | EUR | `ddc_cwicr_de` |
| 🇬🇧 | English | EN | Toronto | CAD | `ddc_cwicr_en` |
| 🇪🇸 | Spanish | ES | Barcelona | EUR | `ddc_cwicr_es` |
| 🇫🇷 | French | FR | Paris | EUR | `ddc_cwicr_fr` |
| 🇮🇳 | Hindi | HI | Mumbai | INR | `ddc_cwicr_hi` |
| 🇧🇷 | Portuguese | PT | São Paulo | BRL | `ddc_cwicr_pt` |
| 🇷🇺 | Russian | RU | St. Petersburg | RUB | `ddc_cwicr_ru` |

<p align="center">
  <img src="https://datadrivenconstruction.io/wp-content/uploads/2025/09/CWICR-Regional-Coverage.jpg" alt="Regional Coverage" width="100%"/>
</p>

---

## n8n Workflows for Cost Estimation

Four production-ready workflows for automated cost estimation. Import the JSON files into n8n and start estimating immediately.

<p align="center">
  <img src="https://datadrivenconstruction.io/wp-content/uploads/2025/09/n8n-CWICR-Workflows.jpg" alt="n8n Workflows" width="100%"/>
</p>

---

### ⚡️ 1. Text Estimator Bot

**File**: `n8n_CWICR_Text_Estimator_Bot.json`

Natural language input for quick scope-to-estimate conversions via Telegram or WhatsApp.

<p align="center">
  <img src="https://datadrivenconstruction.io/wp-content/uploads/2025/09/Text-Estimator-Workflow.jpg" alt="Text Estimator Workflow" width="100%"/>
</p>

**How it works:**
```
User: "I need to pour 50 m³ of concrete for a foundation"

Bot Response:
┌─────────────────────────────────────────────────────┐
│ 🏗️ Cost Estimate for Concrete Foundation           │
├─────────────────────────────────────────────────────┤
│ Work Item: E2-02-03-01 Concrete C25/30             │
│ Quantity: 50 m³                                     │
│                                                     │
│ 📦 Materials:                                       │
│   • Concrete C25/30: 50 m³ × $125 = $6,250        │
│   • Rebar: 2,500 kg × $1.20 = $3,000              │
│   • Formwork: 120 m² × $15 = $1,800               │
│                                                     │
│ 👷 Labor:                                           │
│   • Concrete workers: 80 hours × $35 = $2,800     │
│   • Rebar workers: 40 hours × $40 = $1,600        │
│                                                     │
│ 🚜 Equipment:                                       │
│   • Concrete pump: 8 hours × $150 = $1,200        │
│   • Vibrator: 16 hours × $25 = $400               │
│                                                     │
│ 💰 TOTAL: $17,050 CAD                              │
└─────────────────────────────────────────────────────┘
```

**Features:**
- ✅ Natural language understanding
- ✅ Semantic search via Qdrant
- ✅ Multi-language support (9 languages)
- ✅ Telegram/WhatsApp integration
- ✅ Full resource breakdown

---

### ⚡️ 2. Photo Cost Estimator

**File**: `n8n_CWICR_Photo_Estimator_Bot.json`

AI Vision analyzes construction photos and generates estimates automatically.

<p align="center">
  <img src="https://datadrivenconstruction.io/wp-content/uploads/2025/09/Photo-Estimator-Workflow.jpg" alt="Photo Estimator Workflow" width="100%"/>
</p>

**How it works:**
```
User: [uploads photo of brick wall]

AI Vision Analysis:
┌─────────────────────────────────────────────────────┐
│ 🖼️ Image Analysis Results                          │
├─────────────────────────────────────────────────────┤
│ Detected: Brick masonry wall                        │
│ Estimated dimensions: 4m × 3m = 12 m²              │
│ Brick type: Standard ceramic brick                  │
│ Mortar joints: ~10mm                               │
│                                                     │
│ 🏗️ Matched Work Item: E3-01-02-05                  │
│ "Brick masonry 250mm with ceramic bricks"          │
│                                                     │
│ 💰 Cost Estimate:                                   │
│   • Materials: $480                                 │
│   • Labor: $360                                     │
│   • Total: $840 for 12 m²                          │
│   • Unit price: $70/m²                             │
└─────────────────────────────────────────────────────┘
```

**Features:**
- ✅ GPT-4 Vision / Claude Vision / Gemini Vision
- ✅ Automatic material identification
- ✅ Quantity extraction from images
- ✅ Before/after comparison
- ✅ Multiple photos in one request

---

### ⚡️ 3. Universal Bot

**File**: `n8n_CWICR_Universal_Bot.json`

Accepts text, photos, and PDFs with intelligent routing to the appropriate estimator.

<p align="center">
  <img src="https://datadrivenconstruction.io/wp-content/uploads/2025/09/Universal-Bot-Workflow.jpg" alt="Universal Bot Workflow" width="100%"/>
</p>

**Features:**
- ✅ Multi-modal input (text, images, documents)
- ✅ Smart routing to appropriate estimator
- ✅ PDF specification parsing
- ✅ Combined estimates from multiple sources
- ✅ Conversation memory

---

### ⚡️ 4. CAD/BIM Cost Pipeline

**File**: `n8n_CWICR_CAD_BIM_Pipeline.json`

Processes Revit/IFC/DWG models for 4D/5D estimation with full resource breakdown.

<p align="center">
  <img src="https://datadrivenconstruction.io/wp-content/uploads/2025/09/CAD-BIM-Pipeline-Workflow.jpg" alt="CAD/BIM Pipeline Workflow" width="100%"/>
</p>

**How it works:**
```
Input: Building.rvt (or .ifc, .dwg)
         ↓
   CAD2DATA Conversion
         ↓
   XLSX with quantities
         ↓
   AI Classification
         ↓
   CWICR Matching
         ↓
Output: Complete 5D Estimate
```

**Pipeline Steps:**
1. **Convert** BIM model with [CAD2DATA](https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto)
2. **Extract** element quantities (walls, floors, doors, etc.)
3. **Classify** elements using AI (LLM + RAG)
4. **Match** to CWICR work items via semantic search
5. **Calculate** costs with regional pricing
6. **Generate** reports (Excel, PDF, HTML)

**Features:**
- ✅ Direct integration with CAD2DATA converters
- ✅ Element-by-element cost assignment
- ✅ Full resource breakdown (materials, labor, equipment)
- ✅ 4D scheduling support
- ✅ 5D cost visualization
- ✅ Multi-format output

<p align="center">
  <img src="https://datadrivenconstruction.io/wp-content/uploads/2025/09/5D-Cost-Visualization.jpg" alt="5D Cost Visualization" width="100%"/>
</p>

---

## Quick Start

### Python (Pandas)

```python
import pandas as pd

# Load database
df = pd.read_parquet("DDC_CWICR_EN.parquet")
print(f"Total records: {len(df):,}")  # 55,719

# Find concrete work items
concrete = df[df['rate_original_name'].str.contains('concrete', case=False, na=False)]
print(concrete[['rate_code', 'rate_original_name', 'rate_unit_of_measure', 'total_cost_per_position']].head(10))

# Filter by category
foundations = df[df['category_name'].str.contains('foundation', case=False, na=False)]

# Calculate total cost for 100 m³
quantity = 100
unit_price = foundations.iloc[0]['total_cost_per_position']
total = quantity * unit_price
print(f"Total cost for {quantity} m³: ${total:,.2f}")
```

### Qdrant (Semantic Search)

```python
from qdrant_client import QdrantClient
from openai import OpenAI

# Connect to Qdrant
qdrant = QdrantClient(host="localhost", port=6333)
openai = OpenAI()

# Semantic search
query = "reinforced concrete foundation pouring with formwork"
embedding = openai.embeddings.create(
    input=query,
    model="text-embedding-3-large"
).data[0].embedding

results = qdrant.search(
    collection_name="ddc_cwicr_en",
    query_vector=embedding,
    limit=5
)

# Display results
for i, r in enumerate(results, 1):
    print(f"\n{i}. {r.payload['rate_code']}: {r.payload['rate_original_name']}")
    print(f"   Unit: {r.payload['rate_unit_of_measure']}")
    print(f"   Cost: {r.payload['total_cost_per_position']} {r.payload['currency_code']}")
    print(f"   Score: {r.score:.4f}")
```

### n8n Workflow Setup

1. **Install n8n**:
   ```bash
   npx n8n
   ```

2. **Import workflow**:
   - Open n8n at `http://localhost:5678`
   - Click **Import** and select JSON file

3. **Configure credentials**:
   - OpenAI API key (for embeddings)
   - Qdrant connection (host, port)
   - Telegram Bot token (optional)

4. **Execute workflow**: Click **Execute Workflow**

<p align="center">
  <img src="https://datadrivenconstruction.io/wp-content/uploads/2025/07/Install-Nodejs-and-n8n.png" alt="n8n Installation" width="100%"/>
</p>

---

## 🚀 AI Integration — Perfect Fuel for AI Products

DDC CWICR is designed to work seamlessly with modern AI tools and platforms:

| Platform | Integration | Use Case |
|----------|-------------|----------|
| **Claude Code** | Full context via AI_INSTRUCTIONS folder | Code generation, data queries |
| **Cursor / Windsurf** | Project context awareness | Automated pipeline building |
| **n8n** | Ready-to-use workflow templates | Visual automation |
| **Dify** | Knowledge base integration | LLM applications |
| **LangChain** | RAG pipelines | Semantic search apps |
| **LlamaIndex** | Vector store integration | Q&A systems |
| **Flowise** | Visual LLM chains | No-code AI apps |

### 🤖 Why AI Integration Matters

**Modern AI coding assistants can use DDC CWICR directly:**

1. **Copy the AI_INSTRUCTIONS** folder to your project
2. **Describe your task** in natural language
3. **AI reads the context**, writes code, and executes queries

**Example with Claude Code:**
```
You: "Find all painting work items and calculate the cost for painting 500 m² of interior walls"

Claude: [reads AI_INSTRUCTIONS, queries Qdrant, calculates costs]

Result:
- Work Item: E4-03-02-01 "Interior wall painting, 2 coats"
- Unit price: $12.50/m²
- Quantity: 500 m²
- Materials: $2,800 (paint, primer, tape)
- Labor: $2,450 (40 hours × $61.25/hr)
- Equipment: $500 (sprayer rental)
- Total: $6,250
```

---

## 📂 AI_INSTRUCTIONS Folder — Ready Context for AI Assistants

The repository includes a dedicated **[AI_INSTRUCTIONS](AI_INSTRUCTIONS/)** folder that contains everything AI coding assistants need to work effectively with the database.

**What's included:**

| File | Purpose |
|------|---------|
| **INSTRUCTIONS.md** | Main overview: philosophy, data formats, quick start |
| **CLAUDE.md** | Claude Code specific instructions with detailed patterns |
| **OPENCODE.md** | Instructions for Opencode |
| **ANTIGRAVITY.md** | Google Antigravity instructions with GCP integration examples |
| **DATABASE_SCHEMA.md** | Complete 85-field schema reference |
| **DATA_DRIVEN_CONSTRUCTION_BOOK.txt** | The "Data-Driven Construction" book — guiding philosophy |

**Why this matters:**
- AI assistants can read these files to understand full context
- Contains data access patterns, query examples, and best practices
- The book serves as "compass" for construction automation decisions
- Enables natural language queries to the database

**How to use:**
```bash
# AI assistants automatically read AI_INSTRUCTIONS when working with the repo
# Or point them directly:
"Read AI_INSTRUCTIONS/CLAUDE.md and help me build a cost estimation query"
```

---

## Technical Architecture

```
┌─────────────────────────────────────────────────────────────────────────┐
│                            INPUT LAYER                                  │
├────────────────┬────────────────┬────────────────┬─────────────────────┤
│     Text       │     Photo      │      PDF       │      CAD/BIM        │
│   (Telegram)   │   (Vision AI)  │   (Parser)     │  (Revit/IFC/DWG)    │
│                │                │                │                     │
│  "50m³ of      │  [brick wall   │  [spec.pdf]    │  Building.rvt       │
│   concrete"    │   image]       │                │                     │
└───────┬────────┴───────┬────────┴───────┬────────┴──────────┬──────────┘
        │                │                │                   │
        └────────────────┴────────┬───────┴───────────────────┘
                                  ▼
┌─────────────────────────────────────────────────────────────────────────┐
│                         AI PROCESSING LAYER                             │
│  ┌─────────────────┐  ┌─────────────────┐  ┌─────────────────────────┐ │
│  │     OpenAI      │  │     Claude      │  │        Gemini           │ │
│  │   Embeddings    │  │     Vision      │  │        Vision           │ │
│  │  (3072-dim)     │  │   (Analysis)    │  │      (Analysis)         │ │
│  └────────┬────────┘  └────────┬────────┘  └────────────┬────────────┘ │
└───────────┼────────────────────┼────────────────────────┼──────────────┘
            │                    │                        │
            └────────────────────┼────────────────────────┘
                                 ▼
┌─────────────────────────────────────────────────────────────────────────┐
│                      SEARCH & MATCH LAYER                               │
│  ┌─────────────────────────────────────────────────────────────────┐   │
│  │                  Qdrant Vector Database                          │   │
│  │             55,719 work items × 3,072 dimensions                 │   │
│  │                                                                  │   │
│  │  Query: "concrete foundation" → Top 5 matches with scores       │   │
│  └─────────────────────────────────────────────────────────────────┘   │
└─────────────────────────────────┬───────────────────────────────────────┘
                                  ▼
┌─────────────────────────────────────────────────────────────────────────┐
│                        CALCULATION LAYER                                │
│                                                                         │
│   Total Cost = Materials + Labor + Equipment + Overhead + Profit + VAT │
│                                                                         │
│   Where:                                                                │
│   • Materials = Σ(material_quantity × material_unit_cost)              │
│   • Labor = labor_hours × labor_hourly_rate                            │
│   • Equipment = machinery_hours × machinery_hourly_rate                │
│   • Overhead = (Materials + Labor + Equipment) × overhead_rate         │
│   • Profit = Subtotal × profit_margin                                  │
│   • VAT = (Subtotal + Profit) × vat_rate                              │
└─────────────────────────────────┬───────────────────────────────────────┘
                                  ▼
┌─────────────────────────────────────────────────────────────────────────┐
│                          OUTPUT LAYER                                   │
├────────────────┬────────────────┬────────────────┬─────────────────────┤
│     Excel      │      JSON      │      PDF       │       HTML          │
│    Report      │      API       │    Report      │    Dashboard        │
│                │                │                │                     │
│  [Detailed     │  {"items":[],  │  [Formatted    │  [Interactive       │
│   breakdown]   │   "total":...} │   document]    │   charts]           │
└────────────────┴────────────────┴────────────────┴─────────────────────┘
```

---

## Database Schema

The database contains **85 fields** organized into 10 logical groups:

| Group | Fields | Key Fields | Description |
|-------|--------|------------|-------------|
| **Classification** | 6 | `category_name`, `department_name`, `section_name` | Hierarchical categorization |
| **Work Item ID** | 8 | `rate_code`, `rate_original_name`, `rate_unit_of_measure` | Unique identification |
| **Materials** | 12 | `material_name`, `material_quantity`, `material_unit_cost` | Material resources |
| **Labor** | 10 | `labor_hours`, `labor_hourly_rate`, `labor_total_cost` | Labor resources |
| **Machinery** | 12 | `machinery_name`, `machinery_hours`, `machinery_total_cost` | Equipment resources |
| **Cost Aggregates** | 8 | `total_cost_per_position`, `total_material_cost` | Calculated totals |
| **Price Statistics** | 6 | `price_min`, `price_max`, `price_median` | Market price data |
| **Physical Properties** | 8 | `mass_total_kg`, `volume_m3`, `area_m2` | Physical measurements |
| **Regional** | 8 | `language_code`, `currency_code`, `region_name` | Localization |
| **Metadata** | 7 | `created_at`, `data_quality_score`, `is_active` | Record information |

**Full schema reference**: See [AI_INSTRUCTIONS/DATABASE_SCHEMA.md](AI_INSTRUCTIONS/DATABASE_SCHEMA.md)

---

## Use Cases

### 1. Quick Estimation for Contractors
```
Contractor: "How much for 100 m² of ceramic tile flooring?"
System: Returns detailed breakdown with materials ($1,200), labor ($800),
        equipment ($150), timeline (2 days), and total ($2,150)
```

### 2. BIM Cost Integration for Architects
```
Architect: Uploads Revit model with 500 elements
System: Extracts quantities → Classifies elements → Matches work items
        → Generates 5D estimate with element-by-element costs
        → Creates visual cost heatmap
```

### 3. Multilingual Projects for International Firms
```
International firm: Needs estimates in German for Berlin site
                   and Arabic for Dubai site
System: Same work items, localized descriptions and pricing
        DE: "Stahlbetonarbeiten" → €125/m³
        AR: "أعمال الخرسانة المسلحة" → AED 580/m³
```

### 4. AI-Assisted Bidding for Estimators
```
Estimator: "Analyze this 50-page specification PDF and create estimate"
System: Parses document → Extracts scope items → Identifies quantities
        → Matches to CWICR database → Calculates regional costs
        → Generates professional bid document
```

### 5. Photo-Based Field Estimation
```
Site manager: [Uploads photo of partially completed wall]
System: AI Vision analyzes → Identifies brick masonry, 25m² complete
        → Calculates remaining work: 15m² × $85/m² = $1,275
        → Estimates 1.5 days to completion
```

---

## Integration with CAD2DATA

DDC CWICR integrates seamlessly with the [CAD2DATA](https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto) converters for complete BIM-to-cost automation:

```
┌─────────────┐     ┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│   Revit     │     │  CAD2DATA   │     │    AI       │     │    DDC      │
│   IFC       │ ──▶ │  Converter  │ ──▶ │ Classifier  │ ──▶ │   CWICR     │
│   DWG       │     │             │     │             │     │             │
└─────────────┘     └─────────────┘     └─────────────┘     └─────────────┘
     Input              XLSX/DAE           Matching           Cost Estimate
```

**Combined workflow:**
1. **Convert** BIM model with CAD2DATA → XLSX with quantities
2. **Classify** elements using LLM (GPT-4, Claude, Gemini)
3. **Match** to CWICR work items via Qdrant semantic search
4. **Calculate** costs with regional pricing
5. **Generate** reports (Excel, PDF, HTML dashboard)

**Get CAD2DATA**: [github.com/datadrivenconstruction/cad2data](https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto)

---

## Troubleshooting

### Common Issues

| Issue | Solution |
|-------|----------|
| Qdrant connection refused | Ensure Qdrant is running: `docker run -p 6333:6333 qdrant/qdrant` |
| OpenAI API errors | Check API key and rate limits |
| Empty search results | Verify collection exists and has data |
| Encoding errors in CSV | Use UTF-8 encoding: `pd.read_csv(file, encoding='utf-8')` |
| Parquet read errors | Update pyarrow: `pip install --upgrade pyarrow` |

### Getting Help

1. Check [existing issues](https://github.com/datadrivenconstruction/OpenConstructionEstimate-DDC-CWICR/issues)
2. Join our [Telegram community](https://t.me/datadrivenconstruction)
3. Contact support: info@datadrivenconstruction.io

---

## Contributing

We welcome contributions! Here's how you can help:

1. **Report bugs**: Open an issue with reproduction steps
2. **Suggest features**: Describe your use case
3. **Submit PRs**: Fork, branch, commit, and open a pull request
4. **Improve docs**: Fix typos, add examples, clarify instructions
5. **Share workflows**: Submit your n8n workflows for others to use
6. **Add translations**: Help translate to new languages

---

## 🆘 Support

| Channel | Link |
|---------|------|
| **Issues** | [GitHub Issues](https://github.com/datadrivenconstruction/OpenConstructionEstimate-DDC-CWICR/issues) |
| **Email** | info@datadrivenconstruction.io |
| **Telegram** | [@datadrivenconstruction](https://t.me/datadrivenconstruction) |
| **Website** | [datadrivenconstruction.io](https://datadrivenconstruction.io) |

---

## 🎓 Consulting and Training

Need help implementing DDC CWICR in your organization?

- **Custom integrations** with your existing systems
- **Training workshops** for your team
- **Custom database** tailored to your regional pricing
- **Enterprise support** with SLA

Contact: consulting@datadrivenconstruction.io

---

## License

- **Database**: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — Free commercial use with attribution
- **Code**: [MIT](https://opensource.org/licenses/MIT) — Unrestricted use

---

## Resources

| Resource | Link |
|----------|------|
| **Live Demo** | [openconstructionestimate.com](https://openconstructionestimate.com) |
| **GitHub** | [datadrivenconstruction](https://github.com/datadrivenconstruction) |
| **CAD2DATA Tools** | [cad2data Repository](https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto) |
| **Book** | [Data-Driven Construction](https://datadrivenconstruction.io/book) |
| **Telegram Bot** | Test workflows instantly |
| **API Documentation** | [docs.datadrivenconstruction.io](https://docs.datadrivenconstruction.io) |

---

<p align="center">
  <a href="https://datadrivenconstruction.io">
    <img src="https://datadrivenconstruction.io/wp-content/uploads/2023/07/DataDrivenConstruction-1-1.png" alt="DDC Logo" width="200"/>
  </a>
  <br>
  <b>Unlock the Power of Data in Construction</b>
  <br>
  🚀 Move to full-cycle data management where only unified <br/> structured data & processes remain and where 🔓 your data is yours
</p>
