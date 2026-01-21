<p align="center">
  <a href="https://datadrivenconstruction.io">
    <img src="https://datadrivenconstruction.io/wp-content/uploads/2023/07/DataDrivenConstruction-1-1.png" alt="DDC Logo" width="200"/>
  </a>
</p>

<h1 align="center">DDC CWICR: Открытая база данных строительных расценок</h1>

<p align="center">
  <b>55 719 позиций работ | 27 672 ресурса | 9 языков | 85 полей данных</b>
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
  <a href="https://github.com/datadrivenconstruction/OpenConstructionEstimate-DDC-CWICR/blob/main/LICENSE"><img src="https://img.shields.io/badge/База_данных-CC%20BY%204.0-green" alt="License CC BY 4.0"/></a>
  <a href="https://github.com/datadrivenconstruction/OpenConstructionEstimate-DDC-CWICR/blob/main/LICENSE"><img src="https://img.shields.io/badge/Код-MIT-blue" alt="License MIT"/></a>
</p>

---

## Обзор

**DDC CWICR** (Construction Work Items, Components & Resources) — это комплексная открытая база данных для сметного расчёта в строительстве. База данных позволяет автоматизировать расчёт стоимости через AI-воркфлоу и семантический поиск в векторной базе данных.

### Почему DDC CWICR?

| Традиционный подход | Подход DDC CWICR |
|---------------------|------------------|
| Ручной поиск расценок | Семантический AI-поиск |
| Статические прайс-листы | Региональное динамическое ценообразование |
| Один язык | 9 языков, 10+ стран |
| Закрытые форматы | Открытые форматы (Parquet, Excel, Qdrant) |
| Нет интеграции с AI | Нативная поддержка AI/LLM |

---

## Содержание

- [Содержимое базы данных](#содержимое-базы-данных)
- [Доступные форматы](#доступные-форматы)
- [Языки и региональные цены](#языки-и-региональные-цены)
- [n8n Воркфлоу](#n8n-воркфлоу)
  - [1. Текстовый бот-оценщик](#1-текстовый-бот-оценщик)
  - [2. Фото-оценщик стоимости](#2-фото-оценщик-стоимости)
  - [3. Универсальный бот](#3-универсальный-бот)
  - [4. CAD/BIM Pipeline](#4-cadbim-pipeline)
- [Быстрый старт](#быстрый-старт)
- [Интеграция с AI](#интеграция-с-ai)
- [Папка AI Instructions](#папка-ai-instructions)
- [Техническая архитектура](#техническая-архитектура)
- [Схема базы данных](#схема-базы-данных)
- [Сценарии использования](#сценарии-использования)
- [Интеграция с CAD2DATA](#интеграция-с-cad2data)
- [Лицензия](#лицензия)
- [Ресурсы](#ресурсы)

---

## Содержимое базы данных

| Метрика | Значение |
|---------|----------|
| Позиции работ | 55 719 |
| Ресурсы | 27 672 |
| Полей данных | 85 |
| Языки | 9 |
| Страны | 10+ |
| Размерность эмбеддингов | 3 072 (OpenAI text-embedding-3-large) |

### Что включено

- **Позиции работ**: Полные строительные работы с описаниями, единицами измерения и стоимостью
- **Материалы**: Объёмы, цены за единицу, веса, спецификации
- **Трудозатраты**: Квалификация рабочих, часы, почасовые ставки
- **Механизмы**: Типы оборудования, машино-часы, расход топлива, зарплаты операторов
- **Агрегированные затраты**: Общие затраты, накладные расходы, маржа, НДС

---

## Доступные форматы

| Формат | Файл | Лучше всего для |
|--------|------|-----------------|
| **Parquet** | `DDC_CWICR_{LANG}.parquet` | Python/Pandas, обработка больших данных |
| **Excel** | `DDC_CWICR_{LANG}.xlsx` | Ручной анализ, обмен |
| **CSV** | `DDC_CWICR_{LANG}.csv` | Универсальная совместимость |
| **Qdrant Snapshot** | `qdrant_snapshot_{lang}.snapshot` | Векторный поиск, семантические запросы |

---

## Языки и региональные цены

| Язык | Код | Регион | Валюта | Коллекция Qdrant |
|------|-----|--------|--------|------------------|
| 🇸🇦 Арабский | AR | Дубай | AED | `ddc_cwicr_ar` |
| 🇨🇳 Китайский | ZH | Шанхай | CNY | `ddc_cwicr_zh` |
| 🇩🇪 Немецкий | DE | Берлин | EUR | `ddc_cwicr_de` |
| 🇬🇧 Английский | EN | Торонто | CAD | `ddc_cwicr_en` |
| 🇪🇸 Испанский | ES | Барселона | EUR | `ddc_cwicr_es` |
| 🇫🇷 Французский | FR | Париж | EUR | `ddc_cwicr_fr` |
| 🇮🇳 Хинди | HI | Мумбаи | INR | `ddc_cwicr_hi` |
| 🇧🇷 Португальский | PT | Сан-Паулу | BRL | `ddc_cwicr_pt` |
| 🇷🇺 Русский | RU | Санкт-Петербург | RUB | `ddc_cwicr_ru` |

---

## n8n Воркфлоу

Четыре готовых к использованию воркфлоу для автоматизированной оценки стоимости.

### 1. Текстовый бот-оценщик

**Файл**: `n8n_CWICR_Text_Estimator_Bot.json`

Ввод на естественном языке для быстрого преобразования объёма работ в смету.

```
Пользователь: "Мне нужно залить 50 м³ бетона для фундамента"
Бот: Возвращает подходящие позиции работ со стоимостью, материалами, трудозатратами
```

**Возможности:**
- Понимание естественного языка
- Семантический поиск через Qdrant
- Поддержка нескольких языков
- Интеграция с Telegram/WhatsApp

---

### 2. Фото-оценщик стоимости

**Файл**: `n8n_CWICR_Photo_Estimator_Bot.json`

AI Vision анализирует фото строительных работ и генерирует сметы.

```
Пользователь: [загружает фото кирпичной стены]
Бот: Определяет кладку, рассчитывает площадь, возвращает смету
```

**Возможности:**
- GPT-4 Vision / Claude Vision
- Автоматическое определение материалов
- Извлечение объёмов из изображений
- Сравнение "до/после"

---

### 3. Универсальный бот

**Файл**: `n8n_CWICR_Universal_Bot.json`

Принимает текст, фото и PDF с интеллектуальной маршрутизацией.

**Возможности:**
- Мультимодальный ввод (текст, изображения, документы)
- Умная маршрутизация к нужному оценщику
- Парсинг PDF спецификаций
- Комбинированные сметы из нескольких источников

---

### 4. CAD/BIM Pipeline

**Файл**: `n8n_CWICR_CAD_BIM_Pipeline.json`

Обрабатывает модели Revit/IFC/DWG для 4D/5D оценки.

```
Вход: Building.rvt (или .ifc, .dwg)
Выход: Полная смета с ресурсной раскладкой
```

**Возможности:**
- Прямая интеграция с [конвертерами CAD2DATA](https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto)
- Поэлементное назначение стоимости
- Полная ресурсная раскладка (материалы, труд, оборудование)
- Поддержка 4D планирования
- 5D визуализация затрат

---

## Быстрый старт

### Python (Pandas)

```python
import pandas as pd

# Загрузка базы данных
df = pd.read_parquet("DDC_CWICR_RU.parquet")
print(f"Всего записей: {len(df):,}")

# Поиск бетонных работ
concrete = df[df['rate_original_name'].str.contains('бетон', case=False, na=False)]
print(concrete[['rate_code', 'rate_original_name', 'rate_unit_of_measure', 'total_cost_per_position']])
```

### Qdrant (Семантический поиск)

```python
from qdrant_client import QdrantClient
from openai import OpenAI

# Подключение
qdrant = QdrantClient(host="localhost", port=6333)
openai = OpenAI()

# Поиск
query = "заливка железобетонного фундамента"
embedding = openai.embeddings.create(input=query, model="text-embedding-3-large").data[0].embedding

results = qdrant.search(
    collection_name="ddc_cwicr_ru",
    query_vector=embedding,
    limit=5
)

for r in results:
    print(f"{r.payload['rate_code']}: {r.payload['rate_original_name']}")
    print(f"  Стоимость: {r.payload['total_cost_per_position']} {r.payload['currency_code']}")
```

### n8n Воркфлоу

1. Установите n8n: `npx n8n`
2. Импортируйте JSON файл воркфлоу
3. Настройте credentials (OpenAI, Qdrant, Telegram)
4. Запустите воркфлоу

---

## Интеграция с AI

DDC CWICR легко интегрируется с современными AI-инструментами:

| Инструмент | Интеграция |
|------------|------------|
| **Claude Code** | Полный контекст через папку AI_INSTRUCTIONS |
| **Google Antigravity** | GCP паттерны (BigQuery, Vertex AI) |
| **n8n** | Готовые шаблоны воркфлоу |
| **Dify** | Разработка LLM-приложений |
| **LangChain** | RAG пайплайны |
| **LlamaIndex** | Интеграция базы знаний |

### Пример: Claude Code

```
Вы: "Найди все работы по покраске и рассчитай стоимость на 500 м²"
Claude: [читает AI_INSTRUCTIONS, запрашивает базу данных, возвращает форматированный результат]
```

---

## Папка AI Instructions

Папка `AI_INSTRUCTIONS/` содержит документацию для AI-ассистентов программирования.

| Файл | Назначение |
|------|------------|
| `INSTRUCTIONS.md` | Основной обзор, быстрый старт, форматы данных |
| `CLAUDE.md` | Паттерны и примеры для Claude Code |
| `OPENCODE.md` | Краткие инструкции для Opencode |
| `ANTIGRAVITY.md` | Интеграция с GCP (BigQuery, Vertex AI, Qdrant) |
| `DATABASE_SCHEMA.md` | Полная схема базы данных (85 полей) |

### Почему это важно

- AI-ассистенты читают эти файлы для понимания контекста
- Содержит CLI синтаксис, паттерны интеграции, лучшие практики
- Позволяет делать запросы к базе на естественном языке
- Ускоряет разработку с AI-ассистированным кодированием

### Как использовать

```bash
# AI-ассистенты автоматически читают AI_INSTRUCTIONS
# Или направьте их напрямую:
"Прочитай AI_INSTRUCTIONS/CLAUDE.md и помоги построить запрос для оценки стоимости"
```

---

## Техническая архитектура

```
┌─────────────────────────────────────────────────────────────┐
│                      ВХОДНОЙ СЛОЙ                           │
├─────────────┬─────────────┬─────────────┬──────────────────┤
│   Текст     │    Фото     │    PDF      │    CAD/BIM       │
│ (Telegram)  │  (Vision)   │  (Парсер)   │ (Revit/IFC/DWG)  │
└──────┬──────┴──────┬──────┴──────┬──────┴────────┬─────────┘
       │             │             │               │
       └─────────────┴──────┬──────┴───────────────┘
                            ▼
┌─────────────────────────────────────────────────────────────┐
│                   СЛОЙ AI ОБРАБОТКИ                         │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────────────┐ │
│  │   OpenAI    │  │   Claude    │  │      Gemini         │ │
│  │  Embedding  │  │   Vision    │  │      Vision         │ │
│  └──────┬──────┘  └──────┬──────┘  └──────────┬──────────┘ │
└─────────┼────────────────┼────────────────────┼────────────┘
          │                │                    │
          └────────────────┼────────────────────┘
                           ▼
┌─────────────────────────────────────────────────────────────┐
│                   СЛОЙ ПОИСКА И СОПОСТАВЛЕНИЯ               │
│  ┌─────────────────────────────────────────────────────┐   │
│  │            Векторная база данных Qdrant              │   │
│  │         (55 719 позиций × 3 072 измерения)          │   │
│  └─────────────────────────────────────────────────────┘   │
└─────────────────────────────┬───────────────────────────────┘
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                     СЛОЙ РАСЧЁТОВ                           │
│                                                             │
│  Стоимость = Материалы + Труд + Механизмы + Накладные + СП │
│                                                             │
│   Где:                                                      │
│   • Материалы = Σ(объём × цена_за_единицу)                 │
│   • Труд = часы × почасовая_ставка                         │
│   • Механизмы = машино-часы × ставка_оборудования          │
└─────────────────────────────┬───────────────────────────────┘
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                      ВЫХОДНОЙ СЛОЙ                          │
├─────────────┬─────────────┬─────────────┬──────────────────┤
│    Excel    │    JSON     │    PDF      │      HTML        │
│    Отчёт    │     API     │    Отчёт    │    Дашборд       │
└─────────────┴─────────────┴─────────────┴──────────────────┘
```

---

## Схема базы данных

База данных содержит **85 полей**, организованных в 10 групп:

| Группа | Полей | Ключевые поля |
|--------|-------|---------------|
| Классификация | 6 | `category_name`, `department_name`, `section_name` |
| ID позиции работ | 8 | `rate_code`, `rate_original_name`, `rate_unit_of_measure` |
| Материалы | 12 | `material_name`, `material_quantity`, `material_unit_cost` |
| Трудозатраты | 10 | `labor_hours`, `labor_hourly_rate`, `labor_total_cost` |
| Механизмы | 12 | `machinery_name`, `machinery_hours`, `machinery_total_cost` |
| Агрегированные затраты | 8 | `total_cost_per_position`, `total_material_cost` |
| Ценовая статистика | 6 | `price_min`, `price_max`, `price_median` |
| Физические свойства | 8 | `mass_total_kg`, `volume_m3`, `area_m2` |
| Региональные | 8 | `language_code`, `currency_code`, `region_name` |
| Метаданные | 7 | `created_at`, `data_quality_score`, `is_active` |

**Полная схема**: См. [AI_INSTRUCTIONS/DATABASE_SCHEMA.md](AI_INSTRUCTIONS/DATABASE_SCHEMA.md)

---

## Сценарии использования

### 1. Быстрая оценка
```
Подрядчик: "Сколько стоит 100 м² керамической плитки на пол?"
Система: Возвращает раскладку по материалам, труду, срокам
```

### 2. Интеграция стоимости в BIM
```
Архитектор: Загружает модель Revit
Система: Извлекает объёмы, сопоставляет позиции работ, генерирует 5D смету
```

### 3. Многоязычные проекты
```
Международная компания: Нужны сметы на немецком и арабском
Система: Те же позиции работ, локализованные цены и описания
```

### 4. AI-ассистированные тендеры
```
Сметчик: "Проанализируй этот PDF спецификации и создай смету"
Система: Парсит документ, определяет объём, рассчитывает стоимость
```

---

## Интеграция с CAD2DATA

DDC CWICR легко интегрируется с конвертерами [CAD2DATA](https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto):

```
Revit/IFC/DWG → CAD2DATA → XLSX/DAE → DDC CWICR → Смета
```

**Рабочий процесс:**
1. Конвертируйте BIM модель с CAD2DATA
2. Извлеките объёмы элементов
3. Сопоставьте элементы с позициями CWICR
4. Рассчитайте стоимость с региональными ценами
5. Сгенерируйте отчёты

---

## Лицензия

- **База данных**: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — Бесплатное коммерческое использование с указанием авторства
- **Код**: [MIT](https://opensource.org/licenses/MIT) — Без ограничений

---

## Ресурсы

| Ресурс | Ссылка |
|--------|--------|
| Демо | [openconstructionestimate.com](https://openconstructionestimate.com) |
| GitHub | [datadrivenconstruction](https://github.com/datadrivenconstruction) |
| Инструменты CAD2DATA | [Репозиторий cad2data](https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto) |
| Книга | [Data-Driven Construction](https://datadrivenconstruction.io/book) |
| Telegram бот | Тестируйте воркфлоу мгновенно |

---

<p align="center">
  <a href="https://datadrivenconstruction.io">
    <img src="https://datadrivenconstruction.io/wp-content/uploads/2023/07/DataDrivenConstruction-1-1.png" alt="DDC Logo" width="150"/>
  </a>
  <br>
  <b>Раскройте силу данных в строительстве</b>
  <br>
  <sub>Ваши данные — это ваши данные</sub>
</p>
