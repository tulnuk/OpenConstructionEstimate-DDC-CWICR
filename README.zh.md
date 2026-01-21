<p align="center">
  <a href="https://datadrivenconstruction.io">
    <img src="https://datadrivenconstruction.io/wp-content/uploads/2023/07/DataDrivenConstruction-1-1.png" alt="DDC Logo" width="200"/>
  </a>
</p>

<h1 align="center">DDC CWICR: 开放式建筑成本数据库</h1>

<p align="center">
  <b>55,719 工作项目 | 27,672 资源 | 9 种语言 | 85 个数据字段</b>
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
  <a href="https://github.com/datadrivenconstruction/OpenConstructionEstimate-DDC-CWICR/blob/main/LICENSE"><img src="https://img.shields.io/badge/数据库-CC%20BY%204.0-green" alt="License CC BY 4.0"/></a>
  <a href="https://github.com/datadrivenconstruction/OpenConstructionEstimate-DDC-CWICR/blob/main/LICENSE"><img src="https://img.shields.io/badge/代码-MIT-blue" alt="License MIT"/></a>
</p>

---

## 概述

**DDC CWICR**（Construction Work Items, Components & Resources）是一个全面的开源建筑成本估算数据库。该数据库通过AI驱动的工作流程和向量数据库语义搜索实现自动化成本计算。

### 为什么选择 DDC CWICR？

| 传统方法 | DDC CWICR 方法 |
|---------|---------------|
| 手动价格查询 | AI语义搜索 |
| 静态价格表 | 区域动态定价 |
| 单一语言 | 9种语言，10+国家 |
| 封闭格式 | 开放格式（Parquet、Excel、Qdrant） |
| 无AI集成 | 原生AI/LLM支持 |

---

## 目录

- [数据库内容](#数据库内容)
- [可用格式](#可用格式)
- [语言和区域定价](#语言和区域定价)
- [n8n 工作流程](#n8n-工作流程)
  - [1. 文本估算机器人](#1-文本估算机器人)
  - [2. 照片成本估算器](#2-照片成本估算器)
  - [3. 通用机器人](#3-通用机器人)
  - [4. CAD/BIM 管道](#4-cadbim-管道)
- [快速开始](#快速开始)
- [AI 集成](#ai-集成)
- [AI 指南文件夹](#ai-指南文件夹)
- [技术架构](#技术架构)
- [数据库架构](#数据库架构)
- [使用场景](#使用场景)
- [与 CAD2DATA 集成](#与-cad2data-集成)
- [许可证](#许可证)
- [资源](#资源)

---

## 数据库内容

| 指标 | 值 |
|------|-----|
| 工作项目 | 55,719 |
| 资源 | 27,672 |
| 数据字段 | 85 |
| 语言 | 9 |
| 国家 | 10+ |
| 嵌入维度 | 3,072（OpenAI text-embedding-3-large） |

### 包含内容

- **工作项目**: 完整的建筑工作，包括描述、单位和成本
- **材料**: 数量、单位成本、重量、规格
- **人工**: 工人资质、工时、小时费率
- **机械**: 设备类型、机器工时、燃料消耗、操作员工资
- **成本汇总**: 总成本、管理费用、利润率、增值税

---

## 可用格式

| 格式 | 文件 | 最适合 |
|------|------|--------|
| **Parquet** | `DDC_CWICR_{LANG}.parquet` | Python/Pandas，大数据处理 |
| **Excel** | `DDC_CWICR_{LANG}.xlsx` | 手动分析，共享 |
| **CSV** | `DDC_CWICR_{LANG}.csv` | 通用兼容性 |
| **Qdrant 快照** | `qdrant_snapshot_{lang}.snapshot` | 向量搜索，语义查询 |

---

## 语言和区域定价

| 语言 | 代码 | 地区 | 货币 | Qdrant 集合 |
|------|------|------|------|-------------|
| 🇸🇦 阿拉伯语 | AR | 迪拜 | AED | `ddc_cwicr_ar` |
| 🇨🇳 中文 | ZH | 上海 | CNY | `ddc_cwicr_zh` |
| 🇩🇪 德语 | DE | 柏林 | EUR | `ddc_cwicr_de` |
| 🇬🇧 英语 | EN | 多伦多 | CAD | `ddc_cwicr_en` |
| 🇪🇸 西班牙语 | ES | 巴塞罗那 | EUR | `ddc_cwicr_es` |
| 🇫🇷 法语 | FR | 巴黎 | EUR | `ddc_cwicr_fr` |
| 🇮🇳 印地语 | HI | 孟买 | INR | `ddc_cwicr_hi` |
| 🇧🇷 葡萄牙语 | PT | 圣保罗 | BRL | `ddc_cwicr_pt` |
| 🇷🇺 俄语 | RU | 圣彼得堡 | RUB | `ddc_cwicr_ru` |

---

## n8n 工作流程

四个可用于生产的自动化成本估算工作流程。

### 1. 文本估算机器人

**文件**: `n8n_CWICR_Text_Estimator_Bot.json`

自然语言输入，快速将范围转换为估算。

```
用户: "我需要浇筑50立方米的基础混凝土"
机器人: 返回匹配的工作项目，包括成本、材料、人工分解
```

**功能:**
- 自然语言理解
- 通过Qdrant进行语义搜索
- 多语言支持
- Telegram/WhatsApp 集成

---

### 2. 照片成本估算器

**文件**: `n8n_CWICR_Photo_Estimator_Bot.json`

AI Vision 分析建筑照片并生成估算。

```
用户: [上传砖墙照片]
机器人: 识别砌体，计算面积，返回成本估算
```

**功能:**
- GPT-4 Vision / Claude Vision
- 自动材料识别
- 从图像中提取数量
- 前后对比

---

### 3. 通用机器人

**文件**: `n8n_CWICR_Universal_Bot.json`

接受文本、照片和PDF，智能路由。

**功能:**
- 多模态输入（文本、图像、文档）
- 智能路由到适当的估算器
- PDF规格解析
- 多来源组合估算

---

### 4. CAD/BIM 管道

**文件**: `n8n_CWICR_CAD_BIM_Pipeline.json`

处理Revit/IFC/DWG模型进行4D/5D估算。

```
输入: Building.rvt（或 .ifc, .dwg）
输出: 带资源分解的完整成本估算
```

**功能:**
- 与[CAD2DATA转换器](https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto)直接集成
- 逐元素成本分配
- 完整资源分解（材料、人工、设备）
- 4D进度支持
- 5D成本可视化

---

## 快速开始

### Python (Pandas)

```python
import pandas as pd

# 加载数据库
df = pd.read_parquet("DDC_CWICR_ZH.parquet")
print(f"总记录数: {len(df):,}")

# 查找混凝土工作
concrete = df[df['rate_original_name'].str.contains('混凝土', case=False, na=False)]
print(concrete[['rate_code', 'rate_original_name', 'rate_unit_of_measure', 'total_cost_per_position']])
```

### Qdrant (语义搜索)

```python
from qdrant_client import QdrantClient
from openai import OpenAI

# 连接
qdrant = QdrantClient(host="localhost", port=6333)
openai = OpenAI()

# 搜索
query = "钢筋混凝土基础浇筑"
embedding = openai.embeddings.create(input=query, model="text-embedding-3-large").data[0].embedding

results = qdrant.search(
    collection_name="ddc_cwicr_zh",
    query_vector=embedding,
    limit=5
)

for r in results:
    print(f"{r.payload['rate_code']}: {r.payload['rate_original_name']}")
    print(f"  成本: {r.payload['total_cost_per_position']} {r.payload['currency_code']}")
```

### n8n 工作流程

1. 安装 n8n: `npx n8n`
2. 导入工作流程 JSON 文件
3. 配置凭证（OpenAI, Qdrant, Telegram）
4. 执行工作流程

---

## AI 集成

DDC CWICR 与现代 AI 工具无缝协作：

| 工具 | 集成 |
|------|------|
| **Claude Code** | 通过 AI_INSTRUCTIONS 文件夹提供完整上下文 |
| **Google Antigravity** | GCP 模式（BigQuery, Vertex AI） |
| **n8n** | 即用型工作流程模板 |
| **Dify** | LLM 应用开发 |
| **LangChain** | RAG 管道 |
| **LlamaIndex** | 知识库集成 |

### 示例: Claude Code

```
你: "找到所有油漆工作项目并计算500平方米的成本"
Claude: [读取 AI_INSTRUCTIONS，查询数据库，返回格式化结果]
```

---

## AI 指南文件夹

`AI_INSTRUCTIONS/` 文件夹包含 AI 编程助手的文档。

| 文件 | 用途 |
|------|------|
| `INSTRUCTIONS.md` | 主要概述、快速入门、数据格式 |
| `CLAUDE.md` | Claude Code 特定模式和示例 |
| `OPENCODE.md` | Opencode 简明指南 |
| `ANTIGRAVITY.md` | GCP 集成（BigQuery, Vertex AI, Qdrant） |
| `DATABASE_SCHEMA.md` | 完整的 85 字段架构参考 |

### 为什么重要

- AI 助手读取这些文件以理解上下文
- 包含 CLI 语法、集成模式、最佳实践
- 支持对数据库的自然语言查询
- 通过 AI 辅助编码加速开发

### 如何使用

```bash
# AI 助手自动读取 AI_INSTRUCTIONS
# 或直接指向它们:
"读取 AI_INSTRUCTIONS/CLAUDE.md 并帮我构建成本估算查询"
```

---

## 技术架构

```
┌─────────────────────────────────────────────────────────────┐
│                        输入层                               │
├─────────────┬─────────────┬─────────────┬──────────────────┤
│    文本     │    照片     │    PDF      │    CAD/BIM       │
│ (Telegram)  │  (Vision)   │  (解析器)   │ (Revit/IFC/DWG)  │
└──────┬──────┴──────┬──────┴──────┬──────┴────────┬─────────┘
       │             │             │               │
       └─────────────┴──────┬──────┴───────────────┘
                            ▼
┌─────────────────────────────────────────────────────────────┐
│                      AI 处理层                              │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────────────┐ │
│  │   OpenAI    │  │   Claude    │  │      Gemini         │ │
│  │  Embedding  │  │   Vision    │  │      Vision         │ │
│  └──────┬──────┘  └──────┬──────┘  └──────────┬──────────┘ │
└─────────┼────────────────┼────────────────────┼────────────┘
          │                │                    │
          └────────────────┼────────────────────┘
                           ▼
┌─────────────────────────────────────────────────────────────┐
│                      搜索与匹配层                           │
│  ┌─────────────────────────────────────────────────────┐   │
│  │              Qdrant 向量数据库                       │   │
│  │         (55,719 项目 × 3,072 维度)                  │   │
│  └─────────────────────────────────────────────────────┘   │
└─────────────────────────────┬───────────────────────────────┘
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                        计算层                               │
│                                                             │
│   成本 = 材料 + 人工 + 设备 + 管理费 + 利润                │
│                                                             │
│   其中:                                                     │
│   • 材料 = Σ(数量 × 单位成本)                              │
│   • 人工 = 工时 × 小时费率                                 │
│   • 设备 = 机器工时 × 设备费率                             │
└─────────────────────────────┬───────────────────────────────┘
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                        输出层                               │
├─────────────┬─────────────┬─────────────┬──────────────────┤
│    Excel    │    JSON     │    PDF      │      HTML        │
│    报告     │     API     │    报告     │     仪表板       │
└─────────────┴─────────────┴─────────────┴──────────────────┘
```

---

## 数据库架构

数据库包含 **85 个字段**，分为 10 组：

| 组 | 字段 | 关键字段 |
|----|------|----------|
| 分类 | 6 | `category_name`, `department_name`, `section_name` |
| 工作项目 ID | 8 | `rate_code`, `rate_original_name`, `rate_unit_of_measure` |
| 材料 | 12 | `material_name`, `material_quantity`, `material_unit_cost` |
| 人工 | 10 | `labor_hours`, `labor_hourly_rate`, `labor_total_cost` |
| 机械 | 12 | `machinery_name`, `machinery_hours`, `machinery_total_cost` |
| 成本汇总 | 8 | `total_cost_per_position`, `total_material_cost` |
| 价格统计 | 6 | `price_min`, `price_max`, `price_median` |
| 物理属性 | 8 | `mass_total_kg`, `volume_m3`, `area_m2` |
| 区域 | 8 | `language_code`, `currency_code`, `region_name` |
| 元数据 | 7 | `created_at`, `data_quality_score`, `is_active` |

**完整架构**: 参见 [AI_INSTRUCTIONS/DATABASE_SCHEMA.md](AI_INSTRUCTIONS/DATABASE_SCHEMA.md)

---

## 使用场景

### 1. 快速估算
```
承包商: "100平方米瓷砖地板多少钱？"
系统: 返回成本分解，包括材料、人工、时间框架
```

### 2. BIM 成本集成
```
建筑师: 上传 Revit 模型
系统: 提取工程量，匹配工作项目，生成 5D 估算
```

### 3. 多语言项目
```
国际公司: 需要德语和阿拉伯语的估算
系统: 相同的工作项目，本地化的价格和描述
```

### 4. AI 辅助投标
```
造价师: "分析这个 PDF 规格并创建估算"
系统: 解析文档，识别范围，计算成本
```

---

## 与 CAD2DATA 集成

DDC CWICR 与 [CAD2DATA](https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto) 转换器无缝集成：

```
Revit/IFC/DWG → CAD2DATA → XLSX/DAE → DDC CWICR → 成本估算
```

**工作流程:**
1. 使用 CAD2DATA 转换 BIM 模型
2. 提取元素工程量
3. 将元素与 CWICR 工作项目匹配
4. 使用区域价格计算成本
5. 生成报告

---

## 许可证

- **数据库**: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — 免费商业使用，需注明出处
- **代码**: [MIT](https://opensource.org/licenses/MIT) — 无限制使用

---

## 资源

| 资源 | 链接 |
|------|------|
| 在线演示 | [openconstructionestimate.com](https://openconstructionestimate.com) |
| GitHub | [datadrivenconstruction](https://github.com/datadrivenconstruction) |
| CAD2DATA 工具 | [cad2data 仓库](https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto) |
| 书籍 | [Data-Driven Construction](https://datadrivenconstruction.io/book) |
| Telegram 机器人 | 即时测试工作流程 |

---

<p align="center">
  <a href="https://datadrivenconstruction.io">
    <img src="https://datadrivenconstruction.io/wp-content/uploads/2023/07/DataDrivenConstruction-1-1.png" alt="DDC Logo" width="150"/>
  </a>
  <br>
  <b>释放建筑数据的力量</b>
  <br>
  <sub>您的数据属于您</sub>
</p>
