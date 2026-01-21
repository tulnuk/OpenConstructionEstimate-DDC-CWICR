<h3 align="center">DDC CWICR - Base de Datos de Partidas de Obra, Componentes y Recursos de Construcción</br>
  + Pipelines n8n para calcular presupuestos basados en descripciones, fotos y CAD (BIM)</h3>

<p align="center">
  <a href="README.md">English</a> •
  <a href="README.zh-CN.md">中文</a> •
  <a href="README.es.md"><b>Español</b></a> •
  <a href="README.pt-BR.md">Português</a> •
  <a href="README.ru.md">Русский</a> •
  <a href="README.ja.md">日本語</a> •
  <a href="README.de.md">Deutsch</a> •
  <a href="README.fr.md">Français</a>
</p>

<p align="center">
  <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/OpenConstructionEstimate.jpg" alt="OpenConstructionEstimate" width="1000">
</p>

<div align="center">
  <img src="https://img.shields.io/badge/Partidas_de_Obra-55.719-2563eb?style=for-the-badge" alt="Work Items">
  <img src="https://img.shields.io/badge/Recursos-27.672-059669?style=for-the-badge" alt="Resources">
  <img src="https://img.shields.io/badge/Idiomas-9-d97706?style=for-the-badge" alt="Languages">
  <img src="https://img.shields.io/badge/Países-10+-dc2626?style=for-the-badge" alt="Countries">
</div>

<div align="center">
  <img src="https://img.shields.io/badge/Licencia-CC_BY_4.0-green?style=flat-square" alt="License">
  <img src="https://img.shields.io/badge/Versión-v0.1.0-blue?style=flat-square" alt="Version">
  <img src="https://img.shields.io/badge/Embeddings-OpenAI_3072d-412991?style=flat-square" alt="Embeddings">
  <img src="https://img.shields.io/badge/Vector_DB-Qdrant-dc382d?style=flat-square" alt="Qdrant">
  <img src="https://img.shields.io/badge/Automatización-n8n-ea4b71?style=flat-square" alt="n8n">
</div>

<p align="center">
  <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/OpenConstructionEstimate_bottom.jpg" alt="OpenConstructionEstimate" width="1000">
</p>

<h3 align="center">⚡ Flujos de Trabajo n8n</h3>
<p align="center"><code>Elige tu entrada → Obtén presupuesto de costos</code></p>

<br>

<table width="100%">
<tr>

<td align="center" valign="top" width="33%">
<br>
<h3>📝 Texto</h3>
<p>Presupuesto rápido desde<br>una breve descripción</p>
<p><b>Entrada:</b> Mensaje de Telegram / chat<br>
<b>Salida:</b> Partidas encontradas + presupuesto</p>
<br>
<a href="#1️⃣-bot-estimador-de-texto">📖 Documentación</a>
<br><br>
<a href="./n8n_1_Telegram_Bot_Cost_Estimates_and_Rate_Finder_TEXT_DDC_CWICR.json">
<img src="https://img.shields.io/badge/Descargar_Workflow-0A84FF?style=for-the-badge&logo=download&logoColor=white" alt="Download"/>
</a>
<br><br>
</td>

<td align="center" valign="top" width="33%">
<br>
<h3>📷 Foto / PDF</h3>
<p>Fotos de obra, presupuestos escaneados,<br>foto-PDF desde campo</p>
<p><b>Entrada:</b> Imagen o páginas PDF<br>
<b>Salida:</b> Alcance extraído → presupuesto</p>
<br>
<a href="#2️⃣-estimador-de-costos-por-foto">📖 Docs Foto</a> · <a href="#3️⃣-bot-estimador-universal-texto--foto--pdf">📖 Bot Universal</a>
<br><br>
<a href="./n8n_2_Photo_Cost_Estimate_DDC_CWICR.json">
<img src="https://img.shields.io/badge/Workflow_Foto-0A84FF?style=for-the-badge&logo=download&logoColor=white" alt="Photo"/>
</a>
&nbsp;
<a href="./n8n_3_Telegram_Bot_Cost_Estimates_and_Rate_Finder_TEXT_PHOTO_PDF_DDC_CWICR.json">
<img src="https://img.shields.io/badge/Bot_Telegram-0A84FF?style=for-the-badge&logo=telegram&logoColor=white" alt="Bot"/>
</a>
<br><br>
</td>

<td align="center" valign="top" width="33%">
<br>
<h3>🧊 CAD / BIM</h3>
<p>Mediciones y presupuestos basados<br>en Revit / IFC / DWG</p>
<p><b>Entrada:</b> Exportación del modelo<br>
<b>Salida:</b> Presupuesto 4D/5D + desglose</p>
<br>
<a href="#4️⃣-pipeline-de-estimación-de-costos-cad-bim">📖 Documentación</a>
<br><br>
<a href="./n8n_4_CAD_(BIM)_Cost_Estimation_Pipeline_4D_5D_with_DDC_CWICR.json">
<img src="https://img.shields.io/badge/Descargar_Workflow-0A84FF?style=for-the-badge&logo=download&logoColor=white" alt="Download"/>
</a>
<br><br>
</td>

</tr>
</table>

<br>
<p align="center">
  <a href="https://openconstructionestimate.com">
    <img src="https://img.shields.io/badge/🌐_DEMO_EN_VIVO_(solo_base_de_datos)-openconstructionestimate.com-2563eb?style=for-the-badge" alt="Live Demo">
  </a>
</p>
<br>
<p align="center">
 Clientes y usuarios de DataDrivenConstruction
  <br>
  <a href="https://datadrivenconstruction.io/">
  <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/Clients_DataDrivenConstruction_logos.png" width="95%"/>
  </a>
  <br></br>
</p>


---

## 📑 Tabla de Contenidos

### Integración con IA
- [Combustible Perfecto para IA](#-combustible-perfecto-para-tus-productos-de-ia) — Por qué esta base de datos es ideal para IA
- [Claude Code](#-claude-code--asistente-de-codificación-ia) — Uso del asistente de codificación IA
- [n8n](#-n8n--automatización-visual-de-flujos-de-trabajo) — Automatización de flujos de trabajo
- [Dify](#-dify--construir-aplicaciones-llm) — Desarrollo de aplicaciones LLM
- [Sim AI y Otros](#-sim-ai-y-plataformas-similares) — Plataformas compatibles
- [Casos de Uso Universales](#-casos-de-uso-universales) — Qué puedes construir

### Base de Datos y Datos
- [Acerca de](#acerca-de) — Qué es DDC CWICR
- [Formatos Disponibles](#formatos-disponibles) — Excel, Parquet, CSV, Qdrant
- [Esquema de Datos](#esquema-de-datos) — Estructura de 85 campos
- [Grupos de Campos](#grupos-de-campos) — Clasificación, Recursos, Mano de Obra, Maquinaria
- [Metodología](#metodología) — Principios de costeo basado en recursos
- [Contexto Histórico](#contexto-histórico) — Más de 100 años de estándares

### Flujos de Trabajo n8n
- [Resumen de Flujos n8n](#-flujos-de-trabajo-n8n) — Elige tu tipo de entrada
- [Pruébalo Ahora — Bots Demo en Vivo](#-pruébalo-ahora--bots-demo-en-vivo) — Prueba instantánea en Telegram
- [Workflow 1: Bot Estimador de Texto](#1️⃣-bot-estimador-de-texto) — Bot de Telegram para entrada de texto
- [Workflow 2: Estimador de Costos por Foto](#2️⃣-estimador-de-costos-por-foto) — Formulario web con IA Vision
- [Workflow 3: Bot Universal](#3️⃣-bot-estimador-universal-texto--foto--pdf) — Texto + Foto + PDF
- [Workflow 4: Pipeline CAD/BIM](#4️⃣-pipeline-de-estimación-de-costos-cad-bim) — De Revit/IFC/DWG a presupuesto
- [Inicio Rápido de Workflows](#inicio-rápido-de-workflows) — Configuración en 4 pasos
- [⚠️ Configuración n8n 2.0+](#️-configuración-requerida-para-n8n-20) — Habilitar nodo Execute Command

### Detalles del Pipeline CAD/BIM
- [Requisitos Previos](#-requisitos-previos) — Componentes requeridos
- [Etapas del Pipeline](#-etapas-del-pipeline) — Procesamiento en 10 etapas
- [Selección de Modelo LLM](#️-selección-de-modelo-llm) — OpenAI, Claude, Gemini, Grok
- [Archivos de Salida](#-archivos-de-salida) — Informes HTML y Excel
- [Solución de Problemas](#️-solución-de-problemas) — Problemas comunes

### Base de Datos Vectorial
- [Base de Datos Vectorial](#base-de-datos-vectorial) — Búsqueda semántica con Qdrant
- [Releases](#releases) — Descargar snapshots
- [Colecciones](#colecciones) — 9 colecciones por idioma
- [Despliegue con Docker](#despliegue-con-docker) — Configuración auto-alojada

### Comenzando
- [Inicio Rápido - Python](#inicio-rápido) — Datos tabulares y búsqueda semántica
- [Casos de Uso de Integración](#integración) — Nivel inicial a avanzado

### Comunidad
- [Recursos y Comunidad](#recursos-y-comunidad) — Enlaces y canales
- [Consultoría y Formación](#consultoría-y-formación) — Servicios profesionales
- [Contribuir](#contribuir) — Envía tus workflows
- [Licencia](#licencia) — CC BY 4.0 y MIT
- [Apoya el Proyecto](#apoya-el-proyecto) — Patrocinar y donar


---

## 🚀 Combustible Perfecto para Tus Productos de IA

<p align="center">
  <b>Solo clona el repositorio y describe lo que quieres — la IA hace el resto</b>
</p>

DDC CWICR no es solo una base de datos — es **combustible listo para usar en aplicaciones impulsadas por IA**. Ya sea que estés construyendo bots de estimación de costos, automatizando flujos de trabajo de construcción o creando asistentes inteligentes — estos datos funcionan directamente con herramientas modernas de IA.

### Por Qué Esta Base de Datos es Ideal para IA

| Característica | Beneficio |
|----------------|-----------|
| **Embeddings pre-calculados** | No necesitas generar vectores — la búsqueda semántica funciona instantáneamente |
| **Esquema estructurado de 85 campos** | La IA puede razonar sobre relaciones de datos y proporcionar respuestas precisas |
| **9 idiomas incluidos** | Construye aplicaciones multilingües sin sobrecarga de traducción |
| **55.000+ partidas de obra** | Cobertura completa para cualquier tarea de estimación de construcción |
| **Metodología basada en recursos** | Datos transparentes que la IA puede explicar y desglosar |

### 🛠️ Funciona Perfectamente Con

<table>
<tr>
<td align="center" width="20%">
<img src="https://img.shields.io/badge/Claude_Code-000000?style=for-the-badge&logo=anthropic&logoColor=white" alt="Claude Code"/><br/>
<b>Claude Code</b><br/>
<sub>CLI de asistente de codificación IA</sub>
</td>
<td align="center" width="20%">
<img src="https://img.shields.io/badge/Google_Antigravity-4285F4?style=for-the-badge&logo=google&logoColor=white" alt="Google Antigravity"/><br/>
<b>Google Antigravity</b><br/>
<sub>Google Antigravity</sub>
</td>
<td align="center" width="20%">
<img src="https://img.shields.io/badge/n8n-EA4B71?style=for-the-badge&logo=n8n&logoColor=white" alt="n8n"/><br/>
<b>n8n</b><br/>
<sub>Automatización de flujos de trabajo</sub>
</td>
<td align="center" width="20%">
<img src="https://img.shields.io/badge/Dify-1677FF?style=for-the-badge&logo=openai&logoColor=white" alt="Dify"/><br/>
<b>Dify</b><br/>
<sub>Desarrollo de apps LLM</sub>
</td>
<td align="center" width="20%">
<img src="https://img.shields.io/badge/Sim_AI-6366F1?style=for-the-badge&logo=simpleicons&logoColor=white" alt="Sim AI"/><br/>
<b>Sim AI y Otros</b><br/>
<sub>Plataformas de IA</sub>
</td>
</tr>
</table>

---

### 💻 Claude Code & Google Antigravity — Asistentes de Codificación IA

La forma más rápida de trabajar con DDC CWICR. Solo abre el repositorio en Claude Code o Google Antigravity y haz preguntas en lenguaje natural.

**Comenzando:**
```bash
# Clonar el repositorio
git clone https://github.com/datadrivenconstruction/OpenConstructionEstimate-DDC-CWICR.git

# Abrir con Claude Code
cd OpenConstructionEstimate-DDC-CWICR
claude
```

**Ejemplos de Prompts:**

| Tarea | Prompt |
|-------|--------|
| **Explorar datos** | "Muéstrame la estructura de esta base de datos de construcción y explica qué datos están disponibles" |
| **Buscar partidas** | "Encuentra todas las partidas relacionadas con cimentaciones de hormigón y muestra sus costos" |
| **Crear consultas** | "Escribe un script Python para buscar partidas de fontanería con horas de trabajo > 100" |
| **Crear informes** | "Genera un informe de desglose de costos para obras de renovación residencial" |
| **Analizar costos** | "Compara los costos de materiales entre diferentes métodos de construcción de muros" |
| **Crear integraciones** | "Crea un script que se conecte a la base de datos Qdrant y realice búsqueda semántica" |

**Consejos Pro:**
- Apunta a Claude a archivos específicos: *"Analiza el archivo Parquet y resume la distribución de costos"*
- Pide explicaciones: *"Explica cómo funciona la metodología de costeo basada en recursos en esta base de datos"*
- Solicita modificaciones: *"Modifica el workflow n8n para agregar notificaciones por email"*

---

### ⚡ n8n — Automatización Visual de Flujos de Trabajo

Construye potentes pipelines de automatización sin programar. Conecta DDC CWICR a más de 400 apps y servicios.

**Casos de Uso:**

| Workflow | Descripción |
|----------|-------------|
| **Bot de Telegram** | Los usuarios envían texto/foto → IA extrae partidas → Devuelve presupuesto |
| **Automatización de Email** | Recibir presupuesto por email → Procesar con IA → Enviar estimación formateada |
| **Integración CRM** | Nuevo proyecto en CRM → Auto-generar estimación preliminar → Actualizar valor del negocio |
| **Pipeline BIM** | Exportar desde Revit → Extraer cantidades → Emparejar con tarifas DDC → Generar informe 5D |
| **Bot de Slack** | El equipo hace preguntas → IA busca en la base de datos → Devuelve partidas relevantes |

**Inicio Rápido:**
1. Descarga el workflow JSON de este repositorio
2. Importar en n8n: `Workflows → Importar → Desde Archivo`
3. Configurar credenciales (OpenAI, Qdrant, Telegram)
4. Activar y probar

Consulta la sección [Flujos de Trabajo n8n](#flujos-de-trabajo-n8n--descripción-detallada) para configuración detallada.

---

### 🤖 Dify — Construir Aplicaciones LLM

Crea aplicaciones de IA personalizadas con DDC CWICR como base de conocimiento.

**Configuración:**
1. Crear nueva aplicación Dify
2. Agregar Base de Conocimiento → Cargar archivos Parquet/CSV o conectar a Qdrant
3. Configurar pipeline RAG con embeddings
4. Construir tu interfaz de chat o API

**Ideas de Aplicaciones:**

| Tipo de App | Descripción |
|-------------|-------------|
| **Chatbot Estimador de Construcción** | Interfaz conversacional para consultas de costos |
| **Búsqueda de Partidas** | Búsqueda en lenguaje natural entre 55.000+ partidas |
| **Asesor de Costos** | IA que explica desgloses de costos y sugiere optimizaciones |
| **Asistente Multilingüe** | Detecta automáticamente el idioma y responde en el idioma del usuario |
| **Endpoint API** | API REST para integración con otros sistemas |

**Plantilla de Prompt para Dify:**
```
Eres un asistente de estimación de costos de construcción con acceso a la base de datos DDC CWICR.

Contexto: {{context}}

Pregunta del usuario: {{query}}

Proporciona información de costos precisa basada en la base de datos. Incluye:
- Partidas relevantes con códigos
- Costos unitarios y cantidades
- Desglose de recursos (mano de obra, materiales, equipos)
- Cálculo del costo total
```

---

### 🔮 Sim AI y Plataformas Similares

DDC CWICR se integra con cualquier plataforma de IA que soporte:
- **Bases de datos vectoriales** (Qdrant, Pinecone, Weaviate, Milvus)
- **Datos estructurados** (CSV, Parquet, Excel)
- **Embeddings de OpenAI** (text-embedding-3-large, 3072 dimensiones)

**Plataformas Compatibles:**
- **Sim AI** — Simulación y modelado de IA
- **LangChain / LlamaIndex** — Frameworks para aplicaciones LLM
- **Flowise** — Constructor de apps LLM low-code
- **Botpress** — Plataforma de IA conversacional
- **Voiceflow** — Diseño de voz y chat
- **Stack AI** — Workflows de IA sin código
- **Relevance AI** — Plataforma de fuerza laboral IA

**Patrón de Integración Universal:**

```python
# Funciona con cualquier plataforma que soporte Qdrant
from qdrant_client import QdrantClient

# Conectar a DDC CWICR
client = QdrantClient("tu-instancia-qdrant", port=6333)

# Búsqueda semántica
results = client.search(
    collection_name="ddc_cwicr_es",  # o de, ru, zh, etc.
    query_vector=tu_embedding,
    limit=10
)

# Usar resultados en tu aplicación de IA
for item in results:
    print(f"{item.payload['rate_code']}: {item.payload['rate_original_name']}")
```

---

### 📋 Casos de Uso Universales

Sin importar qué herramienta de IA elijas, DDC CWICR permite:

| Caso de Uso | Descripción |
|-------------|-------------|
| **Estimación Instantánea de Costos** | Obtener costos de construcción desde descripciones de texto o fotos |
| **Generación de Presupuestos** | Auto-generar mediciones y presupuestos desde descripciones de proyecto |
| **Benchmarking de Precios** | Comparar costos entre regiones e idiomas |
| **Planificación de Recursos** | Calcular horas de trabajo, materiales y necesidades de equipo |
| **Análisis de Inversión** | Auditorías profundas de costos con total transparencia de recursos |
| **Soporte Multilingüe** | Servir a usuarios en 9 idiomas con precios localizados |
| **Integración BIM** | Conectar a Revit/IFC para estimación automatizada 4D/5D |
| **Entrenamiento de Modelos IA** | Usar datos estructurados para fine-tuning de IA de construcción |

---

## Acerca de

**DDC CWICR** (Construction Work Items, Components & Resources - Partidas de Obra, Componentes y Recursos de Construcción) es una base de datos abierta para la estimación de costos de construcción, que cubre el espectro completo de actividades de construcción - desde movimientos de tierra y colocación de hormigón hasta trabajos de instalación especializados.

La base de datos se nutre de fuentes que describen las prácticas modernas de construcción en Eurasia y la región de Asia-Pacífico, donde un ecosistema unificado de estandarización técnica sirve como lenguaje común de ingeniería para más de diez economías en desarrollo dinámico. DDC CWICR representa un esfuerzo por armonizar estándares abiertos estableciendo un marco regulatorio único para la gestión de proyectos de capital en múltiples idiomas.

<p align="center">
  <br>
  <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/DDC%20CWICR%20GEOGRAPHIC%20COVERAGE.jpg" width="100%"/>
  <br></br>
</p>

Los datos estructurados se pueden acceder a través de formatos tabulares (XLSX, CSV, Parquet) o consultar conversacionalmente vía LLM, permitiendo a los especialistas integrar descripciones de trabajos de construcción (base de datos vectorial QDRANT) en pipelines y flujos de trabajo automatizados usando lenguaje natural o consultas concisas.

### Formatos Disponibles

| Formato     | Extensión   | Tamaño       | Mejor Para                              | Características                        |
|-------------|-------------|--------------|-----------------------------------------|----------------------------------------|
| **Excel**   | `.xlsx`     | ~150–400 MB  | Análisis manual, filtros, tablas dinámicas | Legible, formato completo            |
| **Parquet** | `.parquet`  | ~55 MB       | Pipelines ETL, entrenamiento ML, Big Data | Columnar, excelente compresión       |
| **CSV**     | `.csv`      | ~1.3 GB      | Importación a bases de datos, sistemas legacy | Compatibilidad universal           |
| **Qdrant**  | `.snapshot` | ~1 GB        | Búsqueda semántica, RAG, asistentes IA  | Embeddings OpenAI pre-calculados      |


Una demo en vivo está disponible en [openconstructionestimate.com](https://openconstructionestimate.com/), donde puedes explorar los datos y ver la base de datos vectorial en acción para búsqueda semántica.

<p align="center">
  <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/DDC%20CWICR%20Resource-based%20Work%20Cost%20Norms.jpg" alt="OpenConstructionEstimate" width="1000">
</p>

---

## Esquema de Datos

La base de datos contiene **85 campos** organizados en grupos lógicos. Cada registro representa ya sea una partida de obra (tarifa) o un recurso con desglose completo de costos.

```mermaid
erDiagram
    PARTIDA ||--o{ RECURSO : contiene
    PARTIDA ||--o{ MANO_DE_OBRA : requiere
    PARTIDA ||--o{ MAQUINARIA : usa
    PARTIDA ||--o{ VARIANTE_PRECIO : tiene

    PARTIDA {
        string rate_code PK "MEKA_KASA_KAKATO_KAME"
        string rate_original_name "Instalación de tabiques..."
        string rate_unit "100 m2"
        string category_type "OBRAS_DE_CONSTRUCCION"
        string collection_name "Estructuras de madera"
        string department_name "TABIQUES..."
        string section_name "Instalación de tabiques..."
        text work_composition_text
    }

    RECURSO {
        string resource_code PK "KAME-NE-KAME-KARI"
        string resource_name "Placas de yeso"
        string resource_unit "m2"
        float resource_quantity "632.0"
        float resource_price_per_unit_eur "5.02"
        float resource_cost_eur "3170.73"
        boolean is_material
        boolean is_abstract
    }

    MANO_DE_OBRA {
        string resource_code FK
        float labor_hours_workers "172"
        float labor_hours_machinists "1.67"
        int count_workers_per_unit "172"
        int count_machinists_per_unit "2"
        float cost_of_working_hours "3088.11"
    }

    MAQUINARIA {
        string machine_class2_name "Grúas"
        string machine_class3_name "Grúas sobre chasis"
        float electricity_consumption_kwh "0.23"
        float price_machinist_wages "13.56"
        float total_value_machinery "64.18"
    }

    VARIANTE_PRECIO {
        float price_est_median "5.02"
        float price_est_min "3.03"
        float price_est_max "7.99"
        int position_count "24"
        string variable_parts "reforzado con fibra de vidrio..."
    }
```

### Grupos de Campos
Los 85 campos de la base de datos están organizados en grupos lógicos que reflejan la metodología de estimación de costos basada en recursos. Cada grupo cumple una función específica en la estructura de desglose de costos: desde clasificación jerárquica e identificación de partidas hasta consumo detallado de recursos, requisitos de mano de obra, costos de maquinaria y totales agregados. Esta estructura modular permite a los usuarios consultar solo los campos relevantes para su tarea - ya sea generando una lista de materiales, analizando productividad laboral o construyendo un presupuesto completo.

<p align="center">
  <br>
  <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/Resource-based%20Work%20Cost%20Norms%20table2.jpg" width="100%"/>
  <br></br>
</p>

**Clasificación** - `category_type`, `collection_code`, `collection_name`, `department_code`, `department_name`, `department_type`, `section_name`, `section_type`, `subsection_code`, `subsection_name`

**Partida de Obra (Tarifa)** - `rate_code`, `rate_original_name`, `rate_final_name`, `rate_unit`, `row_type`, `is_scope`, `is_abstract`, `is_machine`, `is_labor`, `is_material`, `work_composition_text`

**Recursos** - `resource_code`, `resource_name`, `resource_unit`, `resource_quantity`, `parameter_resource_quantity`, `resource_price_per_unit_eur_current`, `resource_cost_eur`

**Mano de Obra** - `count_workers_per_unit`, `count_engineers_per_unit`, `count_machinists_per_unit`, `count_total_people_per_unit`, `labor_hours_construction_workers`, `labor_hours_machinists`, `labor_hours_engineers`, `total_labor_hours_workers_machinists`, `total_labor_hours_all_personnel`, `cost_of_working_hours`, `count_people_per_day`

**Maquinaria** - `machine_class2_name`, `machine_class3_name`, `personnel_machinist_code`, `personnel_machinist_grade`, `price_machinist_wages`, `price_relocation_included`, `price_cost_without_wages`, `electricity_consumption_kwh_per_machine_hour`, `electricity_cost_per_unit`, `electricity_cost_total_sum`, `cost_machinist_sum`, `total_value_machinery_equipment`

**Variantes de Precio** - `price_code_prefix`, `price_abstract_resource_common_start`, `price_abstract_resource_variable_parts`, `price_abstract_resource_position_count`, `price_abstract_resource_est_price_min`, `price_abstract_resource_est_price_max`, `price_abstract_resource_est_price_mean`, `price_abstract_resource_est_price_median`, `price_abstract_resource_unit`, `abstract_resource_tech_group`

**Agregados** - `total_cost_per_position`, `total_material_cost_per_position`, `total_resource_cost_per_position`, `total_value_abstract_resources`, `materials_resource_cost_eur`

**Masa y Servicios** - `mass_name`, `mass_value`, `mass_unit`, `service_category`, `service_type`, `parameter_service_code`, `parameter_service_unit`, `parameter_service_name`, `parameter_service_quantity`, `service_cost_sum`

### Fórmula de Cálculo de Costos

| Componente        | Norma Tecnológica | ×   | Precio Regional  | =   | Costo                    |
|-------------------|-------------------|-----|------------------|-----|--------------------------|
| 👷 **Mano de Obra** | 172 hrs/100m²    | ×   | €17,95/hr        | =   | €3.088,11                |
| 🧱 **Materiales** | 632 m²/100m²      | ×   | €5,02/m²         | =   | €3.170,73                |
| 🚜 **Equipos**    | 1,67 hrs/100m²    | ×   | €38,42/hr        | =   | €64,18                   |
|                   |                   |     | **Total**        | =   | **€7.725,91 por 100m²**  |

---

## Metodología

El valor clave del **Costeo Basado en Recursos** es la separación de la tecnología de producción inmutable del componente financiero volátil. Se basa en los "primeros principios" físicos de la construcción:
- Horas de trabajo requeridas para trabajos específicos
- Cantidades de material por unidad de obra
- Tiempo de equipo necesario

**Por qué es importante:**

- **Transparencia** - Precios sin márgenes ocultos, desglose completo de recursos
- **Auditabilidad** - Capacidad de análisis profundo para verificación y análisis de inversiones
- **Portabilidad** - Normas independientes de la región aplicables en diferentes mercados
- **Probado** - Metodología estándar de la industria establecida durante más de 100 años

```mermaid
flowchart TB
    subgraph Fuente["📦 Fuente de Datos"]
        CWICR[(DDC CWICR<br/>────────────<br/>55.719 Partidas de Obra<br/>27.672 Recursos<br/>85 Campos por Registro)]
    end

    subgraph Procesamiento["⚙️ Pipeline de Procesamiento"]
        direction LR
        ETL[["🔄 ETL<br/>Extracción y<br/>Transformación"]]
        TRANS[["🌐 Traducción<br/>9 Idiomas"]]
        EMBED[["🧠 Vectorización<br/>OpenAI 3072d"]]
        ETL --> TRANS --> EMBED
    end

    subgraph Salidas["📤 Formatos de Salida"]
        XLSX[("📊 Excel<br/>.xlsx")]
        PARQUET[("⚡ Parquet<br/>.parquet")]
        CSV[("📄 CSV<br/>.csv")]
        QDRANT[("🔍 Qdrant<br/>.snapshot")]
    end

    subgraph Apps["🎯 Aplicaciones"]
        SEARCH["🔎 Búsqueda<br/>Semántica"]
        BIM["🏗️ BIM 5D<br/>Integración"]
        RAG["🤖 Sistemas<br/>RAG"]
        BI["📈 BI<br/>Analíticas"]
    end

    Fuente --> Procesamiento
    Procesamiento --> XLSX & PARQUET & CSV & QDRANT
    XLSX & PARQUET & CSV --> BI & BIM
    QDRANT --> SEARCH & RAG & BIM

    style Fuente fill:#dbeafe,stroke:#2563eb,stroke-width:2px
    style Procesamiento fill:#fef3c7,stroke:#d97706,stroke-width:2px
    style Salidas fill:#d1fae5,stroke:#059669,stroke-width:2px
    style Apps fill:#fce7f3,stroke:#db2777,stroke-width:2px
```


### Contexto Histórico

Las descripciones de trabajos de construcción en esta base de datos están fundamentadas en una metodología de estandarización basada en recursos con raíces que se extienden desde las normas de producción de principios del siglo XX hasta los sistemas de referencia digitales actuales. Desarrollado y refinado continuamente desde la década de 1920, este enfoque ha experimentado una evolución especialmente robusta en la región euroasiática.

A lo largo de cien años de desarrollo, el sistema ha pasado de cálculos manuales a formatos legibles por máquinas - sin embargo, su principio fundamental permanece intacto: la medición precisa de los recursos físicos requeridos por unidad de producción de construcción. Las implementaciones modernas conectan datos normativos históricos con precios de mercado en tiempo real.

Las adaptaciones regionales de esta metodología operan bajo diversas denominaciones nacionales: ENIR, GESN, FER, NRR, ESN, AzDTN, ShNQK, MKS ChT, SNT, BNbD, Dinh Muc, Ding'e.

<p align="center">
  <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/DDC%20CWICR%20SPREAD%20OF%20METHODOLOGY%20FROM%20THE%201920s.jpg" alt="OpenConstructionEstimate" width="1000">
</p>

⭐ <b>Si quieres ver nuevas actualizaciones y versiones de la base de datos y si encuentras útiles nuestras herramientas, por favor dale una estrella a nuestros repositorios para ver más aplicaciones similares para la industria de la construcción.</b>
Dale estrella al workflow DDC en GitHub y recibe notificaciones instantáneas de nuevos lanzamientos.
<p align="center">
  <br>
  <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/OCE%20star%20GitHub.gif" width="100%"/>
  <br></br>
</p>


---


## Integración

### Casos de Uso

- **Nivel Inicial** - Benchmarking de Costos, Indexación de Precios, Estimación de Licitaciones

- **Intermedio** - Localización, Pipelines ETL/BI, Cálculo de CO₂

- **Avanzado** - Entrenamiento IA/ML, CAD (BIM) 5D, Auditoría Profunda de Inversiones

---

## Flujos de Trabajo n8n — Descripción Detallada

Cuatro flujos de trabajo listos para producción para estimación automatizada de costos de construcción. Cada workflow se conecta a la base de datos vectorial DDC CWICR vía Qdrant y usa modelos de IA para análisis y emparejamiento inteligente.

| #   | Workflow                                                          | Entrada     | Mejor Para                        | Descargar                                                                                         |
|-----|-------------------------------------------------------------------|-------------|-----------------------------------|---------------------------------------------------------------------------------------------------|
| 1   | [Bot Estimador de Texto](#1️⃣-bot-estimador-de-texto)              | 💬 Texto    | Estimaciones rápidas desde texto  | [JSON](./n8n_1_Telegram_Bot_Cost_Estimates_and_Rate_Finder_TEXT_DDC_CWICR.json)                   |
| 2   | [Estimador por Foto](#2️⃣-estimador-de-costos-por-foto)            | 📷 Foto     | Visitas de obra, inspecciones     | [JSON](./n8n_2_Photo_Cost_Estimate_DDC_CWICR.json)                                               |
| 3   | [Bot Universal](#3️⃣-bot-estimador-universal-texto--foto--pdf)     | 💬📷📄 Todo | Uso completo en producción        | [JSON](./n8n_3_Telegram_Bot_Cost_Estimates_and_Rate_Finder_TEXT_PHOTO_PDF_DDC_CWICR.json)         |
| 4   | [Pipeline CAD/BIM](#4️⃣-pipeline-de-estimación-de-costos-cad-bim)  | 🏗️ Revit   | Estimación 4D/5D basada en BIM    | [JSON](./n8n_4_CAD_(BIM)_Cost_Estimation_Pipeline_4D_5D_with_DDC_CWICR.json)                      |

---

### 1️⃣ Bot Estimador de Texto

**Archivo:** `n8n_1_Telegram_Bot_Cost_Estimates_and_Rate_Finder_TEXT_DDC_CWICR.json`

Bot de Telegram para estimación de costos basada en texto. Describe trabajos de construcción en lenguaje natural — el bot analiza la entrada, busca en la base de datos vectorial y devuelve desgloses de costos detallados.

<p align="center">
  <br>
  <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/Text_Estimator_Bot.jpg" width="100%"/>
  <br></br>
</p>

<h3 align="left">🤖 Pruébalo Ahora — Bots Demo en Vivo</h3>
<p align="left"><i>Prueba los flujos de estimación instantáneamente en Telegram</i></p>
<p><b>@TextOpenConstructionEstimate_bot</b></p>
<p>Crea presupuestos completos<br>desde descripciones de texto</p>
<a href="https://t.me/TextOpenConstructionEstimate_bot">
<img src="https://img.shields.io/badge/Abrir_Bot-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" alt="Text Bot"/>
</a>

```mermaid
flowchart LR
    subgraph Entrada["💬 ENTRADA"]
        A[Mensaje de Telegram]
    end

    subgraph IA["🤖 PROCESAMIENTO IA"]
        B[Analizar Texto]
        C[Extraer Partidas]
    end

    subgraph Busqueda["🔍 BÚSQUEDA VECTORIAL"]
        D[Generar Embeddings]
        E[Buscar en Qdrant]
        F[Reordenar con IA]
    end

    subgraph Salida["📊 SALIDA"]
        G[Calcular Costos]
        H[Informe HTML]
        I[Exportar Excel]
    end

    A --> B --> C --> D --> E --> F --> G --> H
    G --> I

    style Entrada fill:#e0f2fe,stroke:#0284c7
    style IA fill:#fef3c7,stroke:#d97706
    style Busqueda fill:#dcfce7,stroke:#16a34a
    style Salida fill:#f3e8ff,stroke:#9333ea
```



**Cómo funciona:**

| Paso  | Acción                                  | Tecnología                            |
|-------|-----------------------------------------|---------------------------------------|
| 1     | Usuario envía descripción de texto      | API de Bot de Telegram                |
| 2     | IA analiza y extrae partidas de obra    | OpenAI / Claude / Gemini              |
| 3     | Generar embeddings para cada partida    | OpenAI `text-embedding-3-large`       |
| 4     | Buscar tarifas coincidentes en BD       | Búsqueda vectorial Qdrant             |
| 5     | IA reordena resultados por precisión    | Puntuación LLM                        |
| 6     | Calcular costos y generar informe       | HTML / Excel / PDF                    |

**Características:**

| Característica               | Descripción                                                         |
|------------------------------|---------------------------------------------------------------------|
| 💬 Entrada en lenguaje natural | Acepta cualquier formato de texto — listas, frases, descripciones estructuradas |
| 🤖 Soporte multi-LLM         | Funciona con OpenAI, Claude o Gemini (intercambiable)               |
| 🔍 Búsqueda semántica        | Encuentra mejores coincidencias incluso con diferente redacción     |
| 🌍 9 idiomas                 | DE, EN, RU, ES, FR, PT, ZH, AR, HI                                  |
| 📊 Múltiples exportaciones   | Informe HTML, hoja de cálculo Excel, documento PDF                  |
| ✏️ Edición interactiva       | Modificar cantidades antes del cálculo final                        |

**Credenciales requeridas:**
- Token de Bot de Telegram (de @BotFather)
- API Key de OpenAI (para embeddings + LLM opcional)
- URL de Qdrant + API Key

---

### 2️⃣ Estimador de Costos por Foto

**Archivo:** `n8n_2_Photo_Cost_Estimate_DDC_CWICR.json`

Interfaz de formulario web para estimación basada en fotos. Sube una foto de construcción — AI Vision identifica elementos, estima dimensiones y calcula costos automáticamente.

<p align="center">
  <br>
  <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/n8n%20pipeline%20photo%20estimator.jpg" width="100%"/>
  <br></br>
</p>

```mermaid
flowchart TB
    subgraph Subida["📷 SUBIDA DE FOTO"]
        A[Formulario Web]
        B[Seleccionar Región]
        C[Elegir Tipo de Obra]
    end

    subgraph Vision["👁️ IA VISION"]
        D[Análisis GPT-4 Vision]
        E[Identificar Elementos]
        F[Estimar Dimensiones]
        G[Detectar Tipo de Habitación]
    end

    subgraph Descomponer["🔧 DESCOMPOSICIÓN"]
        H[Elementos → Partidas]
        I[Calcular Cantidades]
    end

    subgraph Precio["💰 PRECIOS"]
        J[Búsqueda Vectorial]
        K[Emparejar Tarifas DDC]
        L[Aplicar Precios Regionales]
    end

    subgraph Informe["📄 INFORME"]
        M[Generar HTML]
        N[Desglose de Costos]
    end

    A --> B --> C --> D
    D --> E --> F --> G
    G --> H --> I
    I --> J --> K --> L
    L --> M --> N

    style Subida fill:#dbeafe,stroke:#2563eb
    style Vision fill:#fef3c7,stroke:#d97706
    style Descomponer fill:#dcfce7,stroke:#16a34a
    style Precio fill:#fee2e2,stroke:#dc2626
    style Informe fill:#f3e8ff,stroke:#9333ea
```



**Cómo funciona:**

| Paso  | Acción                                        | Tecnología                           |
|-------|-----------------------------------------------|--------------------------------------|
| 1     | Usuario sube foto vía formulario web          | n8n Form Trigger                     |
| 2     | AI Vision analiza la imagen                   | GPT-4 Vision                         |
| 3     | Identificar tipo de habitación, elementos, materiales | Extracción JSON estructurada   |
| 4     | Estimar dimensiones desde objetos de referencia | Razonamiento IA (puertas, azulejos) |
| 5     | Descomponer elementos en partidas de obra     | Procesamiento LLM                    |
| 6     | Presupuestar cada trabajo vía búsqueda vectorial | Qdrant + embeddings OpenAI        |
| 7     | Generar informe HTML profesional              | Salida estilizada                    |

**Características:**

| Característica          | Descripción                                             |
|-------------------------|---------------------------------------------------------|
| 📷 Análisis de fotos    | GPT-4 Vision identifica elementos de construcción       |
| 📐 Auto-dimensionamiento | Estima tamaños usando objetos de referencia (puertas, azulejos) |
| 🏠 Detección de habitación | Baño, cocina, dormitorio, exterior, etc.             |
| 🔨 Soporte tipo de obra | Construcción nueva / Renovación / Reparación            |
| 🌍 9 bases de datos regionales | Precios localizados para Berlín, Toronto, París, etc. |
| 📄 Informes profesionales | Salida HTML limpia lista para clientes                |

**Credenciales requeridas:**
- API Key de OpenAI (GPT-4 Vision + embeddings)
- URL de Qdrant + API Key

---

### 3️⃣ Bot Estimador Universal (Texto + Foto + PDF)

**Archivo:** `n8n_3_Telegram_Bot_Cost_Estimates_and_Rate_Finder_TEXT_PHOTO_PDF_DDC_CWICR.json`

Bot de Telegram con todas las funciones que soporta todos los tipos de entrada: descripciones de texto, fotos de construcción y planos PDF. El flujo de trabajo más completo para uso en producción.


<p align="center">
  <br>
  <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/Universal%20Estimator%20Bot%20Text%20%20Photo%20PDF.jpg" width="100%"/>
  <br></br>
</p>

<h3 align="left">🤖 Pruébalo Ahora — Bots Demo en Vivo</h3>
<p align="left"><i>Prueba los flujos de estimación instantáneamente en Telegram</i></p>
<h3>📷 Bot Universal</h3>
<p><b>@OpenConstructionEstimate_bot</b></p>
<p>Bot completo para texto, fotos y PDF</p>
<a href="https://t.me/OpenConstructionEstimate_bot">
<img src="https://img.shields.io/badge/Abrir_Bot-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" alt="Universal Bot"/>
</a>
<br><br>


```mermaid
flowchart TB
    subgraph Entrada["📥 MULTI-ENTRADA"]
        A[💬 Mensaje de Texto]
        B[📷 Foto]
        C[📄 Documento PDF]
    end

    subgraph Router["🔀 ENRUTADOR INTELIGENTE"]
        D{Detectar Tipo}
    end

    subgraph RutaTexto["💬 RUTA TEXTO"]
        E[IA Analiza Texto]
        F[Extraer Trabajos]
    end

    subgraph RutaFoto["📷 RUTA FOTO"]
        G[Vision IA]
        H[Identificar Elementos]
        I[Descomponer]
    end

    subgraph RutaPDF["📄 RUTA PDF"]
        J[Extraer Páginas]
        K[Análisis Vision]
        L[Procesar Contenido]
    end

    subgraph Comun["🔍 PIPELINE COMÚN"]
        M[Generar Embeddings]
        N[Buscar en Qdrant]
        O[Reordenar con IA]
        P[Calcular Costos]
    end

    subgraph Exportar["📤 EXPORTAR"]
        Q[Informe HTML]
        R[Excel CSV]
        S[Documento PDF]
    end

    A --> D
    B --> D
    C --> D
    D -->|Texto| E --> F --> M
    D -->|Foto| G --> H --> I --> M
    D -->|PDF| J --> K --> L --> M
    M --> N --> O --> P
    P --> Q
    P --> R
    P --> S

    style Entrada fill:#e0f2fe,stroke:#0284c7
    style Router fill:#fef3c7,stroke:#d97706
    style RutaTexto fill:#dcfce7,stroke:#16a34a
    style RutaFoto fill:#fce7f3,stroke:#db2777
    style RutaPDF fill:#f3e8ff,stroke:#9333ea
    style Comun fill:#fee2e2,stroke:#dc2626
    style Exportar fill:#d1fae5,stroke:#059669
```



**Cómo funciona:**

| Paso  | Acción                                    | Tecnología                     |
|-------|-------------------------------------------|--------------------------------|
| 1     | Usuario envía texto, foto o PDF           | API de Bot de Telegram         |
| 2     | Enrutador detecta tipo de entrada         | Análisis de tipo de contenido  |
| 3a    | **Texto:** IA analiza partidas            | OpenAI / Gemini                |
| 3b    | **Foto:** Vision IA extrae elementos      | GPT-4 Vision / Gemini 2.0      |
| 3c    | **PDF:** Extraer y analizar páginas       | Procesamiento PDF + Vision     |
| 4     | Búsqueda semántica en DDC CWICR           | Base de datos vectorial Qdrant |
| 5     | Reordenamiento IA para mejores coincidencias | Puntuación LLM              |
| 6     | Edición interactiva vía menú del bot      | Teclados inline de Telegram    |
| 7     | Exportar resultados                       | HTML / Excel / PDF             |

**17 Acciones del Bot:**

| Acción           | Descripción                         |
|------------------|-------------------------------------|
| `/start`         | Menú de selección de idioma         |
| Subir foto       | Activar análisis AI vision          |
| Mensaje de texto | Analizar y extraer partidas         |
| Subir PDF        | Procesar planos                     |
| Editar cantidades| Modificar antes del cálculo         |
| Agregar trabajo  | Entrada manual de partida           |
| Calcular         | Ejecutar estimación completa        |
| Ver detalles     | Mostrar recursos de cada partida    |
| Exportar Excel   | Descargar hoja CSV                  |
| Exportar PDF     | Generar informe PDF                 |
| Ayuda            | Mostrar instrucciones de uso        |
| Refinar          | Re-analizar con correcciones        |

**Características:**

| Característica           | Descripción                                        |
|--------------------------|----------------------------------------------------|
| 📷 Dual Vision IA        | Gemini 2.0 Flash o GPT-4 Vision (configurable)     |
| 📄 Procesamiento PDF     | Planos, presupuestos escaneados, documentos        |
| 💬 Análisis inteligente de texto | Maneja listas, tablas, texto libre          |
| 🔍 Reordenamiento IA     | Mejora precisión de coincidencias                  |
| ✏️ Edición completa      | Agregar, eliminar, modificar partidas              |
| 📊 Exportación multi-formato | HTML, Excel, PDF                                |
| 🌍 9 idiomas             | Localización completa                              |

**Credenciales requeridas:**
- Token de Bot de Telegram
- API Key de OpenAI (embeddings)
- API Key de Gemini (Vision) u OpenAI GPT-4 Vision
- URL de Qdrant + API Key

---

### 4️⃣ Pipeline de Estimación de Costos CAD (BIM)

**Archivo:** `n8n_4_CAD_(BIM)_Cost_Estimation_Pipeline_4D_5D_with_DDC_CWICR.json`

Estimación automatizada de costos desde modelos Revit/IFC/DWG. Extrae datos BIM, clasifica elementos, descompone en partidas de obra y genera estimaciones 4D/5D con desglose completo de recursos.

<p align="left">
  <a href="https://datadrivenconstruction.io">
    <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/CAD%20(Revit)%20to%205D-4D%20Cost%20and%20Time%20Estimate.jpg" alt="DataDrivenConstruction">
  </a>
</p>

```mermaid
flowchart TB
    subgraph ENTRADA["📁 ENTRADA<br/><i>CAD • fotos • descripción de texto</i>"]
        CAD["📐 Entrada de Proyecto<br/>(texto • fotos • RVT / IFC / DWG)"]
    end

    subgraph EXTRAER["⚙️ EXTRACCIÓN"]
        CONV["RvtExporter.exe / Exportación CAD / ETL"]
        XLSX["📊 .XLSX<br/>(Elementos Crudos)"]
    end

    subgraph PREP["🔧 PREPARACIÓN DE DATOS"]
        PREP_AI["🤖 IA: Limpiar y Clasificar<br/><i>encabezados • tipos • categorías</i>"]
    end

    subgraph STAGE_PLAN["📋 ETAPAS 1–3: Planificación"]
        PLAN["🤖 Detectar Proyecto y Fases<br/><i>nuevo / renovación / demolición</i><br/><i>pequeño / mediano / grande</i><br/><i>elementos → fases de construcción</i>"]
    end

    subgraph STAGE4["🔨 ETAPA 4: Descomposición"]
        S4["🤖 Descomponer Tipos en Trabajos<br/><i>'Muro de Ladrillo 240mm' → mampostería, mortero, enlucido</i>"]
    end

    subgraph STAGE5["💰 ETAPA 5: Precios"]
        S5["🤖 Presupuestar vía BD Vectorial<br/><i>Embeddings OpenAI + Qdrant</i><br/><i>rate_code, costo_unitario, recursos</i>"]
    end

    subgraph STAGE75["✅ ETAPA 7.5: Validación"]
        S75["🤖 Revisión CTO<br/><i>completitud • duplicados • trabajos faltantes</i>"]
    end

    subgraph SALIDA["📤 SALIDA"]
        HTML["📄 Informe HTML"]
        XLS["📊 Informe XLS"]
    end

    CAD --> CONV --> XLSX
    XLSX --> PREP_AI --> PLAN --> S4 --> S5 --> S75
    S75 --> HTML & XLS

    style ENTRADA fill:#f4f4f5,stroke:#d4d4d8,color:#18181b
    style EXTRAER fill:#e0f2fe,stroke:#bae6fd,color:#0f172a
    style PREP fill:#ede9fe,stroke:#ddd6fe,color:#1e1b4b
    style STAGE_PLAN fill:#ecfdf5,stroke:#bbf7d0,color:#064e3b
    style STAGE4 fill:#fef9c3,stroke:#fef3c7,color:#78350f
    style STAGE5 fill:#fee2e2,stroke:#fecaca,color:#7f1d1d
    style STAGE75 fill:#e0f2f1,stroke:#bae5e1,color:#134e4a
    style SALIDA fill:#eef2ff,stroke:#e0e7ff,color:#111827
```


**n8n proporciona más de 400 integraciones nativas** con plataformas como Google Sheets, Notion, Slack, Airtable, bases de datos (PostgreSQL, MongoDB), almacenamiento en la nube y más. Cada nodo en este workflow es modular — puedes:

- 🔄 **Cambiar proveedores de LLM** (OpenAI ↔ Claude ↔ Gemini ↔ Grok)
- 📊 **Conectar a tu ERP o sistema de gestión de proyectos**
- 📁 **Exportar resultados a cualquier destino** (almacenamiento en la nube, email, dashboards)
- 🔧 **Modificar cualquier etapa** para coincidir con tu metodología de estimación

El workflow es tuyo para adaptar. Sin restricciones. Sin tarifas de licencia. Control total.

---

## 📋 Requisitos Previos

| Componente                                         | Requisito                            | Descripción                                                           |
|----------------------------------------------------|--------------------------------------|-----------------------------------------------------------------------|
| **[n8n](https://n8n.io/)**                         | v1.0+ (v2.0+ requiere [configuración](#️-configuración-requerida-para-n8n-20)) | Plataforma de automatización de workflows para orquestar el pipeline de estimación |
| **[Qdrant](https://qdrant.tech/)**                 | Instancia en la nube o auto-alojada  | Base de datos vectorial para búsqueda semántica de partidas de construcción |
| **[API OpenAI](https://platform.openai.com/)**     | Para embeddings (`text-embedding-3-large`) | Genera embeddings vectoriales para elementos BIM y emparejamiento con BD de costos |
| **API LLM**                                        | OpenAI / Claude / Gemini / xAI Grok  | Modelos de IA para clasificación de partidas y generación de estimaciones |
| **[Conversor DDC](https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto)** | `RvtExporter.exe` | Extrae datos BIM de modelos Revit a Excel/JSON para procesamiento |

---

## Inicio Rápido de Workflows

### Paso 1: Importar Workflow

```
n8n → Nuevo workflow → Importar desde Archivo → Seleccionar JSON
```

### Paso 2: Configurar Credenciales

En el nodo **🔑 TOKEN**, configura tus API keys:

```json
{
  "bot_token": "TU_TOKEN_BOT_TELEGRAM",
  "OPENAI_API_KEY": "TU_KEY_OPENAI",
  "GEMINI_API_KEY": "TU_KEY_GEMINI",
  "QDRANT_URL": "http://localhost:6333",
  "QDRANT_API_KEY": ""
}
```

### Paso 3: Cargar DDC CWICR en Qdrant

Descarga el snapshot de [Releases](#releases) e importa:

```bash
curl -X POST "http://localhost:6333/collections/ddc_cwicr_es/snapshots/upload" \
  -H "Content-Type: multipart/form-data" \
  -F "snapshot=@ES_BARCELONA_workitems_EMBEDDINGS_3072_DDC.snapshot"
```

### Paso 4: Activar y Probar

- Habilita el workflow en n8n
- Para bots de Telegram: envía `/start` a tu bot
- Para formularios web: abre la URL del formulario proporcionada por n8n

---

## ⚠️ Configuración Requerida para n8n 2.0+

> **A partir de la versión 2.0 de n8n, el nodo Execute Command está deshabilitado por defecto por razones de seguridad.**
>
> Sin la configuración a continuación, los workflows que usan Execute Command (especialmente el Pipeline CAD/BIM) **no funcionarán** — los nodos aparecerán con un signo de interrogación o no serán reconocidos.

### Solución Rápida

**Windows (CMD) — ejecutar cada vez:**
```cmd
set NODES_EXCLUDE=[] && npx n8n
```

**Solución permanente — crear una vez:**

Crea el archivo `C:\Users\TU_USUARIO\.n8n\.env` con:
```
NODES_EXCLUDE=[]
```
Luego simplemente ejecuta `npx n8n` como siempre.

**Docker:**
```yaml
environment:
  - NODES_EXCLUDE=[]
```

### Verificar Configuración

1. Inicia n8n
2. Haz clic en **+** → busca **"Execute Command"**
3. Si el nodo aparece → ✅ ¡todo listo!

> 📚 Más detalles: [Cambios Importantes n8n 2.0](https://docs.n8n.io/2-0-breaking-changes/)

---

## 🌍 Idiomas y Niveles de Precios Soportados

| Código | Idioma      | Nivel de Precios   | Moneda | Colección Qdrant     |
|--------|-------------|--------------------|--------|----------------------|
| `AR`   | Árabe       | Dubái              | AED    | `ddc_cwicr_ar`       |
| `DE`   | Alemán      | Berlín             | EUR    | `ddc_cwicr_de`       |
| `EN`   | Inglés      | Toronto            | CAD    | `ddc_cwicr_en`       |
| `ES`   | Español     | Barcelona          | EUR    | `ddc_cwicr_es`       |
| `FR`   | Francés     | París              | EUR    | `ddc_cwicr_fr`       |
| `HI`   | Hindi       | Bombay             | INR    | `ddc_cwicr_hi`       |
| `PT`   | Portugués   | São Paulo          | BRL    | `ddc_cwicr_pt`       |
| `RU`   | Ruso        | San Petersburgo    | RUB    | `ddc_cwicr_ru`       |
| `ZH`   | Chino       | Shanghái           | CNY    | `ddc_cwicr_zh`       |

---

## 📊 Etapas del Pipeline

El workflow CAD/BIM procesa datos a través de 10 etapas:

| Etapa   | Nombre               | Descripción                                                       |
|---------|----------------------|-------------------------------------------------------------------|
| **0**   | Recopilar Datos BIM  | Extraer elementos de Revit vía Conversor DDC                      |
| **1**   | Detección de Proyecto| IA identifica tipo de proyecto (Residencial, Comercial, etc.)     |
| **2**   | Generación de Fases  | IA crea fases de construcción                                     |
| **3**   | Asignación de Elementos | IA mapea tipos BIM a fases                                     |
| **4**   | Descomposición de Trabajos | IA desglosa tipos en partidas ("Muro de Ladrillo" → mampostería, mortero) |
| **5**   | Búsqueda Vectorial   | Encontrar tarifas coincidentes en DDC CWICR vía Qdrant            |
| **6**   | Mapeo de Unidades    | Convertir unidades BIM a unidades de tarifa                       |
| **7**   | Cálculo de Costos    | Cantidad × Precio Unitario para cada partida                      |
| **7.5** | Validación           | Revisión CTO para completitud y duplicados                        |
| **8**   | Agregación           | Sumar por fases y categorías                                      |
| **9**   | Generación de Informe| Crear salidas HTML y Excel                                        |

---

## ⚙️ Selección de Modelo LLM

El workflow soporta múltiples proveedores de IA. Habilita tu modelo preferido en la sección **Modelos LLM**:

| Modelo           | Nombre del Nodo                | Estado       |
|------------------|--------------------------------|--------------|
| OpenAI GPT-4o    | `OpenAI LLM`                   | ✅ Predeterminado |
| Claude Opus 4    | `Anthropic Chat Model2`        | Deshabilitado |
| Gemini 2.5 Pro   | `Google Gemini Chat Model`     | Deshabilitado |
| xAI Grok         | `xAI Grok Chat Model1`         | Deshabilitado |
| DeepSeek         | `DeepSeek Chat Model`          | Deshabilitado |

Para cambiar modelos: **Habilita** el nodo del modelo deseado y **Deshabilita** los demás.

---

## 📁 Archivos de Salida

Los informes se guardan en la carpeta del proyecto:
```
proyecto_YYYY-MM-DD.html   ← Informe interactivo (se abre en navegador)
proyecto_YYYY-MM-DD.xls    ← Hoja de cálculo compatible con Excel
```
<p align="center">
  <br>
  <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/The%20generated%20report%20includes.jpg" width="100%"/>
  <br></br>
</p>

---

## 🔗 Colecciones Qdrant

El workflow selecciona automáticamente la colección correcta basándose en `language_code`:

```
{IDIOMA}_{CIUDAD}_workitems_costs_resources_EMBEDDINGS_3072_DDC_CWICR
```

Ejemplo: `ES_BARCELONA_workitems_costs_resources_EMBEDDINGS_3072_DDC_CWICR`

---

## ⚠️ Solución de Problemas

| Problema                      | Solución                                                    |
|-------------------------------|-------------------------------------------------------------|
| "Execute Command falta" (n8n 2.0+) | Configura la variable de entorno `NODES_EXCLUDE=[]`. Ver [Configuración n8n 2.0+](#️-configuración-requerida-para-n8n-20) |
| "No se encontró archivo Excel" | Verifica las rutas `path_to_converter` y `project_file`    |
| "Conexión a Qdrant falló"     | Verifica URL de Qdrant y API key en credenciales           |
| "Límite de tasa excedido"     | Reduce el tamaño del lote o agrega retrasos entre llamadas API |
| "No se encontraron precios"   | Verifica si la colección de idioma correcta existe en Qdrant |
| "Error de webhook de Telegram"| Asegúrate de que el workflow esté activo y la URL del webhook sea accesible |
| "API Vision falló"            | Verifica que la API key de Gemini u OpenAI Vision sea válida |

---

## Base de Datos Vectorial

Colecciones Qdrant listas para usar con embeddings OpenAI `text-embedding-3-large` para búsqueda semántica de partidas de construcción.

Las bases de datos vectoriales te permiten "hablar" con tus datos en lenguaje natural – usando frases simples o palabras cortas en lugar de código o filtros complejos. Esto acelera dramáticamente la búsqueda de la partida o línea de costo correcta, incluso en conjuntos de datos muy grandes.

Estas colecciones Qdrant se pueden conectar a aplicaciones a través de flujos de trabajo modernos de automatización e integración (por ejemplo, herramientas de Workflow y Pipeline low-code/no-code). Puedes construir asistentes que busquen, filtren y expliquen partidas de construcción, o integrar búsqueda semántica directamente en tus herramientas de estimación y control de proyectos existentes.

---

### Releases

Descarga conjuntos de datos QDRANT y CSV (archivos mayores a 1 gigabyte) desde [GitHub Releases](https://github.com/datadrivenconstruction/OpenConstructionEstimate-DDC-CWICR/releases).

| Idioma          | Región         | Archivos CSV          | Snapshot Qdrant                            |
|-----------------|----------------|-----------------------|--------------------------------------------|
| 🇸🇦 Árabe       | Dubái          | `AR_DUBAI_*.csv`      | `AR_DUBAI_*_EMBEDDINGS_3072_DDC.snapshot`   |
| 🇨🇳 Chino       | Shanghái       | `ZH_SHANGHAI_*.csv`   | `ZH_SHANGHAI_*_EMBEDDINGS_3072_DDC.snapshot`|
| 🇩🇪 Alemán      | Berlín         | `DE_BERLIN_*.csv`     | `DE_BERLIN_*_EMBEDDINGS_3072_DDC.snapshot`  |
| 🇬🇧 Inglés      | Toronto        | `EN_TORONTO_*.csv`    | `EN_TORONTO_*_EMBEDDINGS_3072_DDC.snapshot` |
| 🇪🇸 Español     | Barcelona      | `ES_BARCELONA_*.csv`  | `ES_BARCELONA_*_EMBEDDINGS_3072_DDC.snapshot`|
| 🇫🇷 Francés     | París          | `FR_PARIS_*.csv`      | `FR_PARIS_*_EMBEDDINGS_3072_DDC.snapshot`   |
| 🇮🇳 Hindi       | Bombay         | `HI_MUMBAI_*.csv`     | `HI_MUMBAI_*_EMBEDDINGS_3072_DDC.snapshot`  |
| 🇧🇷 Portugués   | São Paulo      | `PT_SAOPAULO_*.csv`   | `PT_SAOPAULO_*_EMBEDDINGS_3072_DDC.snapshot`|
| 🇷🇺 Ruso        | San Petersburgo| `RU_SPB_*.csv`        | `RU_SPB_*_EMBEDDINGS_3072_DDC.snapshot`     |

<a href="https://github.com/datadrivenconstruction/OpenConstructionEstimate-DDC-CWICR/releases/tag/v0.1.0">
  <img src="https://img.shields.io/badge/📥_Descargar_v0.1.0-GitHub_Releases-181717?style=for-the-badge&logo=github" alt="Download v0.1.0">
</a>

### Colecciones

🇸🇦 `ddc_cwicr_ar` (Árabe) · 🇨🇳 `ddc_cwicr_zh` (Chino) · 🇩🇪 `ddc_cwicr_de` (Alemán) · 🇬🇧 `ddc_cwicr_en` (Inglés) · 🇪🇸 `ddc_cwicr_es` (Español) · 🇫🇷 `ddc_cwicr_fr` (Francés) · 🇮🇳 `ddc_cwicr_hi` (Hindi) · 🇧🇷 `ddc_cwicr_pt` (Portugués) · 🇷🇺 `ddc_cwicr_ru` (Ruso)

Cada colección contiene **55.719 vectores** con metadatos de payload completos.

### Despliegue con Docker

```yaml
# docker-compose.yml
services:
  qdrant:
    image: qdrant/qdrant:latest
    container_name: ddc-cwicr-qdrant
    ports:
      - "6333:6333"
      - "6334:6334"
    volumes:
      - qdrant_storage:/qdrant/storage
      - ./snapshots:/qdrant/snapshots
    environment:
      - QDRANT__LOG_LEVEL=INFO
    restart: unless-stopped

volumes:
  qdrant_storage:
```

```bash
# Iniciar
docker-compose up -d

# Importar snapshot
curl -X POST "http://localhost:6333/collections/ddc_cwicr_es/snapshots/upload" \
  -H "Content-Type: multipart/form-data" \
  -F "snapshot=@ddc_cwicr_es.snapshot"

# Dashboard: http://localhost:6333/dashboard
```
---

## Inicio Rápido

### Python - Datos Tabulares

```python
import pandas as pd

# Parquet (recomendado)
df = pd.read_parquet("DDC_CWICR_ES.parquet")

# Excel
df = pd.read_excel("DDC_CWICR_ES.xlsx")

print(f"Registros: {len(df):,} | Campos: {len(df.columns)}")
print(df[['rate_code', 'rate_original_name', 'rate_unit', 'total_cost_per_position']].head())
```

### Python - Búsqueda Semántica

```python
from qdrant_client import QdrantClient
from openai import OpenAI

client = QdrantClient("localhost", port=6333)
openai = OpenAI()

# Buscar en lenguaje natural
query = "vertido de cimentación de hormigón armado"
embedding = openai.embeddings.create(
    input=query,
    model="text-embedding-3-large"
).data[0].embedding

results = client.search(
    collection_name="ddc_cwicr_es",
    query_vector=embedding,
    limit=5
)

for r in results:
    print(f"[{r.score:.3f}] {r.payload['rate_code']}: {r.payload['rate_original_name']}")
```

### Búsqueda Filtrada

```python
from qdrant_client.models import Filter, FieldCondition, MatchValue, Range

# Por departamento
results = client.search(
    collection_name="ddc_cwicr_es",
    query_vector=embedding,
    query_filter=Filter(must=[
        FieldCondition(key="department_name", match=MatchValue(value="Hormigón y Hormigón Armado"))
    ]),
    limit=10
)

# Por rango de precio
results = client.search(
    collection_name="ddc_cwicr_es",
    query_vector=embedding,
    query_filter=Filter(must=[
        FieldCondition(key="price_est_median", range=Range(gte=1000, lte=50000))
    ]),
    limit=10
)
```


---

## Recursos y Comunidad

[![Sitio Web](https://img.shields.io/badge/🌐_Sitio_Web-datadrivenconstruction.io-2563eb?style=for-the-badge)](https://datadrivenconstruction.io)
[![Demo](https://img.shields.io/badge/🎯_Demo-openconstructionestimate.com-059669?style=for-the-badge)](https://openconstructionestimate.com)
[![GitHub](https://img.shields.io/badge/💻_GitHub-datadrivenconstruction-181717?style=for-the-badge&logo=github)](https://github.com/datadrivenconstruction)
[![YouTube](https://img.shields.io/badge/📺_YouTube-@datadrivenconstruction-FF0000?style=for-the-badge&logo=youtube)](https://youtube.com/@datadrivenconstruction)
[![LinkedIn](https://img.shields.io/badge/💼_LinkedIn-datadrivenconstruction-0A66C2?style=for-the-badge&logo=linkedin)](https://linkedin.com/company/datadrivenconstruction)
[![Telegram](https://img.shields.io/badge/💬_Telegram-datadrivenconstruction-26A5E4?style=for-the-badge&logo=telegram)](https://t.me/datadrivenconstruction)

### Consultoría y Formación

Trabajamos con empresas líderes de construcción, ingeniería, agencias de consultoría y firmas de tecnología de todo el mundo para ayudarles a implementar principios de datos abiertos, automatizar el procesamiento CAD/BIM y construir pipelines ETL robustos. Apoyamos activamente a organizaciones que buscan soluciones prácticas para la transformación digital e interoperabilidad, enfocándonos en desafíos de calidad de datos y clasificación mientras impulsamos la adopción de flujos de trabajo abiertos y automatizados.

Si deseas probar esta solución con tus propios datos o estás interesado en adaptar el workflow a tareas reales de proyecto, no dudes en contactarnos. Nuestro equipo ofrece talleres prácticos, consultoría estratégica y desarrolla prototipos adaptados a procesos reales de proyectos.

<a href="mailto:info@datadrivenconstruction.io">
  <img src="https://img.shields.io/badge/📧_Contáctanos-info@datadrivenconstruction.io-2563eb?style=for-the-badge" alt="Contact">
</a>

### Contribuir

DDC CWICR es un proyecto gratuito y abierto dedicado a hacer que la industria de la construcción sea más eficiente, transparente y tecnológicamente avanzada. Estamos buscando activamente entusiastas con ideas afines que compartan esta misión. Si creas soluciones útiles y estás listo para compartirlas con la comunidad, estamos aquí para ayudarte a ser escuchado.

Te invitamos a enviar tus workflows de código abierto, pipelines e integraciones basadas en herramientas DDC CWICR que cualquiera pueda usar libremente en su trabajo. Las mejores soluciones se publicarán con atribución completa del autor en GitHub y se anunciarán a través de nuestro newsletter y canales de redes sociales, llegando a decenas de miles de suscriptores profesionales. Esto coloca tu nombre directamente frente a una comunidad internacional de estimadores, especialistas BIM y gerentes de proyecto.

Juntos estamos cambiando la industria. Puedes enviar tu solución a info@datadrivenconstruction.io con el asunto "DDC Open Workflow" o enviar un Pull Request directamente a nuestros repositorios de GitHub.

Automatiza el procesamiento de datos de construcción con workflows n8n CAD-BIM listos para usar:

<a href="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto">
  <img src="https://img.shields.io/badge/Pipeline_cad2data-GitHub-181717?style=for-the-badge&logo=github" alt="cad2data Pipeline">
</a>


## Licencia

**Base de Datos** (DDC CWICR) - [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Libre para usar, compartir y adaptar comercialmente. Atribución: "DDC CWICR by DataDrivenConstruction"

**Código** (workflows, scripts) - [MIT](https://opensource.org/licenses/MIT). Libre para usar, modificar y distribuir sin restricciones.

## Apoya el Proyecto

Si encuentras esto útil, por favor considera apoyar:

[![GitHub Sponsors](https://img.shields.io/badge/Patrocinar_en-GitHub-ea4aaa?style=for-the-badge&logo=github)](https://github.com/sponsors/datadrivenconstruction)
[![Buy Me A Coffee](https://img.shields.io/badge/Invítame_Un_Café-ffdd00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/boikoartem)


<p align="left">
  <br/>
  <b>Desbloquea el Poder de los Datos en la Construcción</b><br/>
  <sub>Pasa a la gestión de datos de ciclo completo donde solo permanecen datos y procesos estructurados unificados</sub>
</p>

<p align="left">
  <a href="https://datadrivenconstruction.io">
    <img src="https://datadrivenconstruction.io/wp-content/uploads/2023/07/DataDrivenConstruction-1-1.png.webp" alt="DataDrivenConstruction" width="180">
  </a>
</p>

<p align="left">
  <sub>© 2025 Artem Boiko · <a href="https://datadrivenconstruction.io">datadrivenconstruction.io</a></sub>
</p>
