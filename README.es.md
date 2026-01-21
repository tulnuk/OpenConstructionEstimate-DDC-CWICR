<p align="center">
  <a href="https://datadrivenconstruction.io">
    <img src="https://datadrivenconstruction.io/wp-content/uploads/2023/07/DataDrivenConstruction-1-1.png" alt="DDC Logo" width="200"/>
  </a>
</p>

<h1 align="center">DDC CWICR: Base de Datos Abierta de Costos de Construccion</h1>

<p align="center">
  <b>55.719 Partidas de Trabajo | 27.672 Recursos | 9 Idiomas | 85 Campos de Datos</b>
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
  <a href="https://github.com/datadrivenconstruction/OpenConstructionEstimate-DDC-CWICR/blob/main/LICENSE"><img src="https://img.shields.io/badge/Base_de_datos-CC%20BY%204.0-green" alt="License CC BY 4.0"/></a>
  <a href="https://github.com/datadrivenconstruction/OpenConstructionEstimate-DDC-CWICR/blob/main/LICENSE"><img src="https://img.shields.io/badge/Codigo-MIT-blue" alt="License MIT"/></a>
</p>

---

## Descripcion General

**DDC CWICR** (Construction Work Items, Components & Resources) es una base de datos integral de codigo abierto para la estimacion de costos de construccion. La base de datos permite calculos de costos automatizados a traves de flujos de trabajo impulsados por IA y busqueda semantica en base de datos vectorial.

### Por que DDC CWICR?

| Enfoque Tradicional | Enfoque DDC CWICR |
|--------------------|-------------------|
| Busqueda manual de precios | Busqueda semantica con IA |
| Listas de precios estaticas | Precios regionales dinamicos |
| Un solo idioma | 9 idiomas, 10+ paises |
| Formatos cerrados | Formatos abiertos (Parquet, Excel, Qdrant) |
| Sin integracion IA | Soporte nativo IA/LLM |

---

## Tabla de Contenidos

- [Contenido de la Base de Datos](#contenido-de-la-base-de-datos)
- [Formatos Disponibles](#formatos-disponibles)
- [Idiomas y Precios Regionales](#idiomas-y-precios-regionales)
- [Flujos de Trabajo n8n](#flujos-de-trabajo-n8n)
  - [1. Bot Estimador de Texto](#1-bot-estimador-de-texto)
  - [2. Estimador de Costos por Foto](#2-estimador-de-costos-por-foto)
  - [3. Bot Universal](#3-bot-universal)
  - [4. Pipeline CAD/BIM](#4-pipeline-cadbim)
- [Inicio Rapido](#inicio-rapido)
- [Integracion con IA](#integracion-con-ia)
- [Carpeta AI Instructions](#carpeta-ai-instructions)
- [Arquitectura Tecnica](#arquitectura-tecnica)
- [Esquema de Base de Datos](#esquema-de-base-de-datos)
- [Casos de Uso](#casos-de-uso)
- [Integracion con CAD2DATA](#integracion-con-cad2data)
- [Licencia](#licencia)
- [Recursos](#recursos)

---

## Contenido de la Base de Datos

| Metrica | Valor |
|---------|-------|
| Partidas de Trabajo | 55.719 |
| Recursos | 27.672 |
| Campos de Datos | 85 |
| Idiomas | 9 |
| Paises | 10+ |
| Dimensiones de Embedding | 3.072 (OpenAI text-embedding-3-large) |

### Que Incluye

- **Partidas de Trabajo**: Trabajos de construccion completos con descripciones, unidades y costos
- **Materiales**: Cantidades, costos unitarios, pesos, especificaciones
- **Mano de Obra**: Cualificaciones, horas, tarifas por hora
- **Maquinaria**: Tipos de equipo, horas-maquina, consumo de combustible, salarios de operadores
- **Agregados de Costos**: Costos totales, gastos generales, margenes de beneficio, IVA

---

## Formatos Disponibles

| Formato | Archivo | Ideal Para |
|---------|---------|------------|
| **Parquet** | `DDC_CWICR_{LANG}.parquet` | Python/Pandas, procesamiento big data |
| **Excel** | `DDC_CWICR_{LANG}.xlsx` | Analisis manual, compartir |
| **CSV** | `DDC_CWICR_{LANG}.csv` | Compatibilidad universal |
| **Qdrant Snapshot** | `qdrant_snapshot_{lang}.snapshot` | Busqueda vectorial, consultas semanticas |

---

## Idiomas y Precios Regionales

| Idioma | Codigo | Region | Moneda | Coleccion Qdrant |
|--------|--------|--------|--------|------------------|
| 🇸🇦 Arabe | AR | Dubai | AED | `ddc_cwicr_ar` |
| 🇨🇳 Chino | ZH | Shanghai | CNY | `ddc_cwicr_zh` |
| 🇩🇪 Aleman | DE | Berlin | EUR | `ddc_cwicr_de` |
| 🇬🇧 Ingles | EN | Toronto | CAD | `ddc_cwicr_en` |
| 🇪🇸 Espanol | ES | Barcelona | EUR | `ddc_cwicr_es` |
| 🇫🇷 Frances | FR | Paris | EUR | `ddc_cwicr_fr` |
| 🇮🇳 Hindi | HI | Mumbai | INR | `ddc_cwicr_hi` |
| 🇧🇷 Portugues | PT | Sao Paulo | BRL | `ddc_cwicr_pt` |
| 🇷🇺 Ruso | RU | San Petersburgo | RUB | `ddc_cwicr_ru` |

---

## Flujos de Trabajo n8n

Cuatro flujos de trabajo listos para produccion para estimacion automatizada de costos.

### 1. Bot Estimador de Texto

**Archivo**: `n8n_CWICR_Text_Estimator_Bot.json`

Entrada en lenguaje natural para conversiones rapidas de alcance a presupuesto.

```
Usuario: "Necesito verter 50 m³ de hormigon para una cimentacion"
Bot: Devuelve partidas coincidentes con costos, materiales, desglose de mano de obra
```

**Caracteristicas:**
- Comprension de lenguaje natural
- Busqueda semantica via Qdrant
- Soporte multiidioma
- Integracion Telegram/WhatsApp

---

### 2. Estimador de Costos por Foto

**Archivo**: `n8n_CWICR_Photo_Estimator_Bot.json`

IA Vision analiza fotos de construccion y genera presupuestos.

```
Usuario: [sube foto de muro de ladrillo]
Bot: Identifica albanileria, calcula area, devuelve estimacion de costos
```

**Caracteristicas:**
- GPT-4 Vision / Claude Vision
- Identificacion automatica de materiales
- Extraccion de cantidades de imagenes
- Comparacion antes/despues

---

### 3. Bot Universal

**Archivo**: `n8n_CWICR_Universal_Bot.json`

Acepta texto, fotos y PDFs con enrutamiento inteligente.

**Caracteristicas:**
- Entrada multimodal (texto, imagenes, documentos)
- Enrutamiento inteligente al estimador apropiado
- Analisis de PDF para especificaciones
- Estimaciones combinadas de multiples fuentes

---

### 4. Pipeline CAD/BIM

**Archivo**: `n8n_CWICR_CAD_BIM_Pipeline.json`

Procesa modelos Revit/IFC/DWG para estimacion 4D/5D.

```
Entrada: Building.rvt (o .ifc, .dwg)
Salida: Presupuesto completo con desglose de recursos
```

**Caracteristicas:**
- Integracion directa con [convertidores CAD2DATA](https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto)
- Asignacion de costos elemento por elemento
- Desglose completo de recursos (materiales, mano de obra, equipo)
- Soporte de planificacion 4D
- Visualizacion de costos 5D

---

## Inicio Rapido

### Python (Pandas)

```python
import pandas as pd

# Cargar base de datos
df = pd.read_parquet("DDC_CWICR_ES.parquet")
print(f"Registros totales: {len(df):,}")

# Buscar trabajos de hormigon
concrete = df[df['rate_original_name'].str.contains('hormigon', case=False, na=False)]
print(concrete[['rate_code', 'rate_original_name', 'rate_unit_of_measure', 'total_cost_per_position']])
```

### Qdrant (Busqueda Semantica)

```python
from qdrant_client import QdrantClient
from openai import OpenAI

# Conectar
qdrant = QdrantClient(host="localhost", port=6333)
openai = OpenAI()

# Buscar
query = "vertido de cimentacion de hormigon armado"
embedding = openai.embeddings.create(input=query, model="text-embedding-3-large").data[0].embedding

results = qdrant.search(
    collection_name="ddc_cwicr_es",
    query_vector=embedding,
    limit=5
)

for r in results:
    print(f"{r.payload['rate_code']}: {r.payload['rate_original_name']}")
    print(f"  Costo: {r.payload['total_cost_per_position']} {r.payload['currency_code']}")
```

### Flujo de Trabajo n8n

1. Instalar n8n: `npx n8n`
2. Importar archivo JSON del flujo de trabajo
3. Configurar credenciales (OpenAI, Qdrant, Telegram)
4. Ejecutar flujo de trabajo

---

## Integracion con IA

DDC CWICR funciona perfectamente con herramientas modernas de IA:

| Herramienta | Integracion |
|-------------|-------------|
| **Claude Code** | Contexto completo via carpeta AI_INSTRUCTIONS |
| **Google Antigravity** | Patrones GCP (BigQuery, Vertex AI) |
| **n8n** | Plantillas de flujo de trabajo listas |
| **Dify** | Desarrollo de aplicaciones LLM |
| **LangChain** | Pipelines RAG |
| **LlamaIndex** | Integracion de base de conocimiento |

### Ejemplo: Claude Code

```
Tu: "Encuentra todas las partidas de pintura y calcula el costo para 500 m²"
Claude: [lee AI_INSTRUCTIONS, consulta base de datos, devuelve resultado formateado]
```

---

## Carpeta AI Instructions

La carpeta `AI_INSTRUCTIONS/` contiene documentacion para asistentes de programacion IA.

| Archivo | Proposito |
|---------|-----------|
| `INSTRUCTIONS.md` | Vision general principal, inicio rapido, formatos de datos |
| `CLAUDE.md` | Patrones y ejemplos especificos de Claude Code |
| `OPENCODE.md` | Instrucciones concisas para Opencode |
| `ANTIGRAVITY.md` | Integracion GCP (BigQuery, Vertex AI, Qdrant) |
| `DATABASE_SCHEMA.md` | Referencia completa del esquema de 85 campos |

### Por Que Esto Importa

- Los asistentes IA leen estos archivos para entender el contexto
- Contiene sintaxis CLI, patrones de integracion, mejores practicas
- Permite consultas en lenguaje natural a la base de datos
- Acelera el desarrollo con codificacion asistida por IA

### Como Usar

```bash
# Los asistentes IA leen automaticamente AI_INSTRUCTIONS
# O dirigelos directamente:
"Lee AI_INSTRUCTIONS/CLAUDE.md y ayudame a construir una consulta de estimacion de costos"
```

---

## Arquitectura Tecnica

```
┌─────────────────────────────────────────────────────────────┐
│                      CAPA DE ENTRADA                        │
├─────────────┬─────────────┬─────────────┬──────────────────┤
│   Texto     │    Foto     │    PDF      │    CAD/BIM       │
│ (Telegram)  │  (Vision)   │  (Parser)   │ (Revit/IFC/DWG)  │
└──────┬──────┴──────┬──────┴──────┬──────┴────────┬─────────┘
       │             │             │               │
       └─────────────┴──────┬──────┴───────────────┘
                            ▼
┌─────────────────────────────────────────────────────────────┐
│                   CAPA DE PROCESAMIENTO IA                  │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────────────┐ │
│  │   OpenAI    │  │   Claude    │  │      Gemini         │ │
│  │  Embedding  │  │   Vision    │  │      Vision         │ │
│  └──────┬──────┘  └──────┬──────┘  └──────────┬──────────┘ │
└─────────┼────────────────┼────────────────────┼────────────┘
          │                │                    │
          └────────────────┼────────────────────┘
                           ▼
┌─────────────────────────────────────────────────────────────┐
│                   CAPA DE BUSQUEDA Y COINCIDENCIA           │
│  ┌─────────────────────────────────────────────────────┐   │
│  │            Base de Datos Vectorial Qdrant            │   │
│  │         (55.719 partidas × 3.072 dimensiones)       │   │
│  └─────────────────────────────────────────────────────┘   │
└─────────────────────────────┬───────────────────────────────┘
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                     CAPA DE CALCULO                         │
│                                                             │
│   Costo = Materiales + Mano de Obra + Equipo + Gastos +    │
│           Beneficio                                         │
│   Donde:                                                    │
│   • Materiales = Σ(cantidad × costo_unitario)              │
│   • Mano de Obra = horas × tarifa_hora                     │
│   • Equipo = horas_maquina × tarifa_equipo                 │
└─────────────────────────────┬───────────────────────────────┘
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                      CAPA DE SALIDA                         │
├─────────────┬─────────────┬─────────────┬──────────────────┤
│    Excel    │    JSON     │    PDF      │      HTML        │
│   Informe   │     API     │   Informe   │   Dashboard      │
└─────────────┴─────────────┴─────────────┴──────────────────┘
```

---

## Esquema de Base de Datos

La base de datos contiene **85 campos** organizados en 10 grupos:

| Grupo | Campos | Campos Clave |
|-------|--------|--------------|
| Clasificacion | 6 | `category_name`, `department_name`, `section_name` |
| ID de Partida | 8 | `rate_code`, `rate_original_name`, `rate_unit_of_measure` |
| Materiales | 12 | `material_name`, `material_quantity`, `material_unit_cost` |
| Mano de Obra | 10 | `labor_hours`, `labor_hourly_rate`, `labor_total_cost` |
| Maquinaria | 12 | `machinery_name`, `machinery_hours`, `machinery_total_cost` |
| Agregados de Costos | 8 | `total_cost_per_position`, `total_material_cost` |
| Estadisticas de Precios | 6 | `price_min`, `price_max`, `price_median` |
| Propiedades Fisicas | 8 | `mass_total_kg`, `volume_m3`, `area_m2` |
| Regional | 8 | `language_code`, `currency_code`, `region_name` |
| Metadatos | 7 | `created_at`, `data_quality_score`, `is_active` |

**Esquema completo**: Ver [AI_INSTRUCTIONS/DATABASE_SCHEMA.md](AI_INSTRUCTIONS/DATABASE_SCHEMA.md)

---

## Casos de Uso

### 1. Estimacion Rapida
```
Contratista: "Cuanto cuesta 100 m² de suelo ceramico?"
Sistema: Devuelve desglose de costos con materiales, mano de obra, plazos
```

### 2. Integracion de Costos BIM
```
Arquitecto: Sube modelo Revit
Sistema: Extrae cantidades, coincide partidas, genera estimacion 5D
```

### 3. Proyectos Multilingues
```
Empresa internacional: Necesita estimaciones en aleman y arabe
Sistema: Mismas partidas, precios y descripciones localizados
```

### 4. Licitaciones Asistidas por IA
```
Estimador: "Analiza este PDF de especificaciones y crea presupuesto"
Sistema: Parsea documento, identifica alcance, calcula costos
```

---

## Integracion con CAD2DATA

DDC CWICR se integra perfectamente con los convertidores [CAD2DATA](https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto):

```
Revit/IFC/DWG → CAD2DATA → XLSX/DAE → DDC CWICR → Presupuesto
```

**Flujo de trabajo:**
1. Convertir modelo BIM con CAD2DATA
2. Extraer cantidades de elementos
3. Coincidir elementos con partidas CWICR
4. Calcular costos con precios regionales
5. Generar informes

---

## Licencia

- **Base de datos**: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — Uso comercial gratuito con atribucion
- **Codigo**: [MIT](https://opensource.org/licenses/MIT) — Uso sin restricciones

---

## Recursos

| Recurso | Enlace |
|---------|--------|
| Demo en Vivo | [openconstructionestimate.com](https://openconstructionestimate.com) |
| GitHub | [datadrivenconstruction](https://github.com/datadrivenconstruction) |
| Herramientas CAD2DATA | [Repositorio cad2data](https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto) |
| Libro | [Data-Driven Construction](https://datadrivenconstruction.io/book) |
| Telegram Bot | Prueba flujos de trabajo al instante |

---

<p align="center">
  <a href="https://datadrivenconstruction.io">
    <img src="https://datadrivenconstruction.io/wp-content/uploads/2023/07/DataDrivenConstruction-1-1.png" alt="DDC Logo" width="150"/>
  </a>
  <br>
  <b>Libera el Poder de los Datos en la Construccion</b>
  <br>
  <sub>Tus datos son tuyos</sub>
</p>
