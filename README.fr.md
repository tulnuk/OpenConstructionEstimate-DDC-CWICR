<p align="center">
  <a href="https://datadrivenconstruction.io">
    <img src="https://datadrivenconstruction.io/wp-content/uploads/2023/07/DataDrivenConstruction-1-1.png" alt="DDC Logo" width="200"/>
  </a>
</p>

<h1 align="center">DDC CWICR: Base de Donnees Ouverte des Couts de Construction</h1>

<p align="center">
  <b>55 719 Postes de Travail | 27 672 Ressources | 9 Langues | 85 Champs de Donnees</b>
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
  <a href="https://github.com/datadrivenconstruction/OpenConstructionEstimate-DDC-CWICR/blob/main/LICENSE"><img src="https://img.shields.io/badge/Base_de_donnees-CC%20BY%204.0-green" alt="License CC BY 4.0"/></a>
  <a href="https://github.com/datadrivenconstruction/OpenConstructionEstimate-DDC-CWICR/blob/main/LICENSE"><img src="https://img.shields.io/badge/Code-MIT-blue" alt="License MIT"/></a>
</p>

---

## Apercu

**DDC CWICR** (Construction Work Items, Components & Resources) est une base de donnees open-source complete pour l'estimation des couts de construction. La base de donnees permet des calculs de couts automatises grace a des flux de travail alimentes par l'IA et une recherche semantique dans une base de donnees vectorielle.

### Pourquoi DDC CWICR?

| Approche Traditionnelle | Approche DDC CWICR |
|------------------------|-------------------|
| Recherche manuelle des prix | Recherche semantique IA |
| Listes de prix statiques | Tarification regionale dynamique |
| Une seule langue | 9 langues, 10+ pays |
| Formats fermes | Formats ouverts (Parquet, Excel, Qdrant) |
| Pas d'integration IA | Support natif IA/LLM |

---

## Table des Matieres

- [Contenu de la Base de Donnees](#contenu-de-la-base-de-donnees)
- [Formats Disponibles](#formats-disponibles)
- [Langues et Prix Regionaux](#langues-et-prix-regionaux)
- [Flux de Travail n8n](#flux-de-travail-n8n)
  - [1. Bot Estimateur de Texte](#1-bot-estimateur-de-texte)
  - [2. Estimateur de Couts par Photo](#2-estimateur-de-couts-par-photo)
  - [3. Bot Universel](#3-bot-universel)
  - [4. Pipeline CAD/BIM](#4-pipeline-cadbim)
- [Demarrage Rapide](#demarrage-rapide)
- [Integration IA](#integration-ia)
- [Dossier AI Instructions](#dossier-ai-instructions)
- [Architecture Technique](#architecture-technique)
- [Schema de Base de Donnees](#schema-de-base-de-donnees)
- [Cas d'Utilisation](#cas-dutilisation)
- [Integration avec CAD2DATA](#integration-avec-cad2data)
- [Licence](#licence)
- [Ressources](#ressources)

---

## Contenu de la Base de Donnees

| Metrique | Valeur |
|----------|--------|
| Postes de Travail | 55 719 |
| Ressources | 27 672 |
| Champs de Donnees | 85 |
| Langues | 9 |
| Pays | 10+ |
| Dimensions d'Embedding | 3 072 (OpenAI text-embedding-3-large) |

### Ce qui est Inclus

- **Postes de Travail**: Travaux de construction complets avec descriptions, unites et couts
- **Materiaux**: Quantites, couts unitaires, poids, specifications
- **Main d'Oeuvre**: Qualifications, heures, taux horaires
- **Machines**: Types d'equipement, heures-machine, consommation de carburant, salaires des operateurs
- **Agregats de Couts**: Couts totaux, frais generaux, marges beneficiaires, TVA

---

## Formats Disponibles

| Format | Fichier | Ideal Pour |
|--------|---------|------------|
| **Parquet** | `DDC_CWICR_{LANG}.parquet` | Python/Pandas, traitement big data |
| **Excel** | `DDC_CWICR_{LANG}.xlsx` | Analyse manuelle, partage |
| **CSV** | `DDC_CWICR_{LANG}.csv` | Compatibilite universelle |
| **Qdrant Snapshot** | `qdrant_snapshot_{lang}.snapshot` | Recherche vectorielle, requetes semantiques |

---

## Langues et Prix Regionaux

| Langue | Code | Region | Devise | Collection Qdrant |
|--------|------|--------|--------|-------------------|
| 🇸🇦 Arabe | AR | Dubai | AED | `ddc_cwicr_ar` |
| 🇨🇳 Chinois | ZH | Shanghai | CNY | `ddc_cwicr_zh` |
| 🇩🇪 Allemand | DE | Berlin | EUR | `ddc_cwicr_de` |
| 🇬🇧 Anglais | EN | Toronto | CAD | `ddc_cwicr_en` |
| 🇪🇸 Espagnol | ES | Barcelone | EUR | `ddc_cwicr_es` |
| 🇫🇷 Francais | FR | Paris | EUR | `ddc_cwicr_fr` |
| 🇮🇳 Hindi | HI | Mumbai | INR | `ddc_cwicr_hi` |
| 🇧🇷 Portugais | PT | Sao Paulo | BRL | `ddc_cwicr_pt` |
| 🇷🇺 Russe | RU | Saint-Petersbourg | RUB | `ddc_cwicr_ru` |

---

## Flux de Travail n8n

Quatre flux de travail prets pour la production pour l'estimation automatisee des couts.

### 1. Bot Estimateur de Texte

**Fichier**: `n8n_CWICR_Text_Estimator_Bot.json`

Entree en langage naturel pour des conversions rapides de perimetre en devis.

```
Utilisateur: "J'ai besoin de couler 50 m³ de beton pour une fondation"
Bot: Retourne les postes correspondants avec couts, materiaux, ventilation main d'oeuvre
```

**Fonctionnalites:**
- Comprehension du langage naturel
- Recherche semantique via Qdrant
- Support multilingue
- Integration Telegram/WhatsApp

---

### 2. Estimateur de Couts par Photo

**Fichier**: `n8n_CWICR_Photo_Estimator_Bot.json`

L'IA Vision analyse les photos de construction et genere des devis.

```
Utilisateur: [telecharge photo d'un mur en briques]
Bot: Identifie la maconnerie, calcule la surface, retourne l'estimation des couts
```

**Fonctionnalites:**
- GPT-4 Vision / Claude Vision
- Identification automatique des materiaux
- Extraction des quantites depuis les images
- Comparaison avant/apres

---

### 3. Bot Universel

**Fichier**: `n8n_CWICR_Universal_Bot.json`

Accepte texte, photos et PDFs avec routage intelligent.

**Fonctionnalites:**
- Entree multimodale (texte, images, documents)
- Routage intelligent vers l'estimateur approprie
- Analyse PDF pour specifications
- Estimations combinees de sources multiples

---

### 4. Pipeline CAD/BIM

**Fichier**: `n8n_CWICR_CAD_BIM_Pipeline.json`

Traite les modeles Revit/IFC/DWG pour l'estimation 4D/5D.

```
Entree: Building.rvt (ou .ifc, .dwg)
Sortie: Devis complet avec ventilation des ressources
```

**Fonctionnalites:**
- Integration directe avec [convertisseurs CAD2DATA](https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto)
- Attribution des couts element par element
- Ventilation complete des ressources (materiaux, main d'oeuvre, equipement)
- Support de planification 4D
- Visualisation des couts 5D

---

## Demarrage Rapide

### Python (Pandas)

```python
import pandas as pd

# Charger la base de donnees
df = pd.read_parquet("DDC_CWICR_FR.parquet")
print(f"Total des enregistrements: {len(df):,}")

# Trouver les travaux de beton
concrete = df[df['rate_original_name'].str.contains('beton', case=False, na=False)]
print(concrete[['rate_code', 'rate_original_name', 'rate_unit_of_measure', 'total_cost_per_position']])
```

### Qdrant (Recherche Semantique)

```python
from qdrant_client import QdrantClient
from openai import OpenAI

# Connecter
qdrant = QdrantClient(host="localhost", port=6333)
openai = OpenAI()

# Rechercher
query = "coulage de fondation en beton arme"
embedding = openai.embeddings.create(input=query, model="text-embedding-3-large").data[0].embedding

results = qdrant.search(
    collection_name="ddc_cwicr_fr",
    query_vector=embedding,
    limit=5
)

for r in results:
    print(f"{r.payload['rate_code']}: {r.payload['rate_original_name']}")
    print(f"  Cout: {r.payload['total_cost_per_position']} {r.payload['currency_code']}")
```

### Flux de Travail n8n

1. Installer n8n: `npx n8n`
2. Importer le fichier JSON du flux de travail
3. Configurer les credentials (OpenAI, Qdrant, Telegram)
4. Executer le flux de travail

---

## Integration IA

DDC CWICR fonctionne parfaitement avec les outils d'IA modernes:

| Outil | Integration |
|-------|-------------|
| **Claude Code** | Contexte complet via dossier AI_INSTRUCTIONS |
| **Google Antigravity** | Patterns GCP (BigQuery, Vertex AI) |
| **n8n** | Modeles de flux de travail prets a l'emploi |
| **Dify** | Developpement d'applications LLM |
| **LangChain** | Pipelines RAG |
| **LlamaIndex** | Integration de base de connaissances |

### Exemple: Claude Code

```
Vous: "Trouve tous les postes de peinture et calcule le cout pour 500 m²"
Claude: [lit AI_INSTRUCTIONS, interroge la base de donnees, retourne resultat formate]
```

---

## Dossier AI Instructions

Le dossier `AI_INSTRUCTIONS/` contient la documentation pour les assistants de programmation IA.

| Fichier | Objectif |
|---------|----------|
| `INSTRUCTIONS.md` | Apercu principal, demarrage rapide, formats de donnees |
| `CLAUDE.md` | Patterns et exemples specifiques a Claude Code |
| `OPENCODE.md` | Instructions concises pour Opencode |
| `ANTIGRAVITY.md` | Integration GCP (BigQuery, Vertex AI, Qdrant) |
| `DATABASE_SCHEMA.md` | Reference complete du schema 85 champs |

### Pourquoi C'est Important

- Les assistants IA lisent ces fichiers pour comprendre le contexte
- Contient la syntaxe CLI, les patterns d'integration, les meilleures pratiques
- Permet des requetes en langage naturel vers la base de donnees
- Accelere le developpement avec la programmation assistee par IA

### Comment Utiliser

```bash
# Les assistants IA lisent automatiquement AI_INSTRUCTIONS
# Ou les diriger directement:
"Lis AI_INSTRUCTIONS/CLAUDE.md et aide-moi a construire une requete d'estimation des couts"
```

---

## Architecture Technique

```
┌─────────────────────────────────────────────────────────────┐
│                      COUCHE D'ENTREE                        │
├─────────────┬─────────────┬─────────────┬──────────────────┤
│   Texte     │    Photo    │    PDF      │    CAD/BIM       │
│ (Telegram)  │  (Vision)   │ (Analyseur) │ (Revit/IFC/DWG)  │
└──────┬──────┴──────┬──────┴──────┬──────┴────────┬─────────┘
       │             │             │               │
       └─────────────┴──────┬──────┴───────────────┘
                            ▼
┌─────────────────────────────────────────────────────────────┐
│                   COUCHE DE TRAITEMENT IA                   │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────────────┐ │
│  │   OpenAI    │  │   Claude    │  │      Gemini         │ │
│  │  Embedding  │  │   Vision    │  │      Vision         │ │
│  └──────┬──────┘  └──────┬──────┘  └──────────┬──────────┘ │
└─────────┼────────────────┼────────────────────┼────────────┘
          │                │                    │
          └────────────────┼────────────────────┘
                           ▼
┌─────────────────────────────────────────────────────────────┐
│                   COUCHE DE RECHERCHE ET CORRESPONDANCE     │
│  ┌─────────────────────────────────────────────────────┐   │
│  │            Base de Donnees Vectorielle Qdrant        │   │
│  │         (55 719 postes × 3 072 dimensions)          │   │
│  └─────────────────────────────────────────────────────┘   │
└─────────────────────────────┬───────────────────────────────┘
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                     COUCHE DE CALCUL                        │
│                                                             │
│   Cout = Materiaux + Main d'Oeuvre + Equipement +          │
│          Frais Generaux + Benefice                          │
│   Ou:                                                       │
│   • Materiaux = Σ(quantite × cout_unitaire)                │
│   • Main d'Oeuvre = heures × taux_horaire                  │
│   • Equipement = heures_machine × taux_equipement          │
└─────────────────────────────┬───────────────────────────────┘
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                      COUCHE DE SORTIE                       │
├─────────────┬─────────────┬─────────────┬──────────────────┤
│    Excel    │    JSON     │    PDF      │      HTML        │
│   Rapport   │     API     │   Rapport   │   Tableau de Bord│
└─────────────┴─────────────┴─────────────┴──────────────────┘
```

---

## Schema de Base de Donnees

La base de donnees contient **85 champs** organises en 10 groupes:

| Groupe | Champs | Champs Cles |
|--------|--------|-------------|
| Classification | 6 | `category_name`, `department_name`, `section_name` |
| ID de Poste | 8 | `rate_code`, `rate_original_name`, `rate_unit_of_measure` |
| Materiaux | 12 | `material_name`, `material_quantity`, `material_unit_cost` |
| Main d'Oeuvre | 10 | `labor_hours`, `labor_hourly_rate`, `labor_total_cost` |
| Machines | 12 | `machinery_name`, `machinery_hours`, `machinery_total_cost` |
| Agregats de Couts | 8 | `total_cost_per_position`, `total_material_cost` |
| Statistiques de Prix | 6 | `price_min`, `price_max`, `price_median` |
| Proprietes Physiques | 8 | `mass_total_kg`, `volume_m3`, `area_m2` |
| Regional | 8 | `language_code`, `currency_code`, `region_name` |
| Metadonnees | 7 | `created_at`, `data_quality_score`, `is_active` |

**Schema complet**: Voir [AI_INSTRUCTIONS/DATABASE_SCHEMA.md](AI_INSTRUCTIONS/DATABASE_SCHEMA.md)

---

## Cas d'Utilisation

### 1. Estimation Rapide
```
Entrepreneur: "Combien coute 100 m² de carrelage ceramique?"
Systeme: Retourne ventilation des couts avec materiaux, main d'oeuvre, delais
```

### 2. Integration des Couts BIM
```
Architecte: Telecharge modele Revit
Systeme: Extrait quantites, fait correspondre les postes, genere estimation 5D
```

### 3. Projets Multilingues
```
Entreprise internationale: Besoin d'estimations en allemand et arabe
Systeme: Memes postes, prix et descriptions localises
```

### 4. Appels d'Offres Assistes par IA
```
Metreur: "Analyse ce PDF de specifications et cree un devis"
Systeme: Analyse document, identifie perimetre, calcule couts
```

---

## Integration avec CAD2DATA

DDC CWICR s'integre parfaitement avec les convertisseurs [CAD2DATA](https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto):

```
Revit/IFC/DWG → CAD2DATA → XLSX/DAE → DDC CWICR → Devis
```

**Flux de travail:**
1. Convertir modele BIM avec CAD2DATA
2. Extraire quantites d'elements
3. Faire correspondre elements avec postes CWICR
4. Calculer couts avec prix regionaux
5. Generer rapports

---

## Licence

- **Base de donnees**: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — Utilisation commerciale gratuite avec attribution
- **Code**: [MIT](https://opensource.org/licenses/MIT) — Utilisation sans restriction

---

## Ressources

| Ressource | Lien |
|-----------|------|
| Demo en Direct | [openconstructionestimate.com](https://openconstructionestimate.com) |
| GitHub | [datadrivenconstruction](https://github.com/datadrivenconstruction) |
| Outils CAD2DATA | [Repository cad2data](https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto) |
| Livre | [Data-Driven Construction](https://datadrivenconstruction.io/book) |
| Telegram Bot | Testez les flux de travail instantanement |

---

<p align="center">
  <a href="https://datadrivenconstruction.io">
    <img src="https://datadrivenconstruction.io/wp-content/uploads/2023/07/DataDrivenConstruction-1-1.png" alt="DDC Logo" width="150"/>
  </a>
  <br>
  <b>Liberez la Puissance des Donnees dans la Construction</b>
  <br>
  <sub>Vos donnees vous appartiennent</sub>
</p>
