<h3 align="center">DDC CWICR - Ouvrages de Construction, Composants & Ressources </br>
  + Pipelines n8n pour calculer des estimations basées sur des descriptions, photos et CAO (BIM)</h3>

<p align="center">
  <a href="README.md">English</a> •
  <a href="README.zh-CN.md">中文</a> •
  <a href="README.es.md">Español</a> •
  <a href="README.pt-BR.md">Português</a> •
  <a href="README.ru.md">Русский</a> •
  <a href="README.ja.md">日本語</a> •
  <a href="README.de.md">Deutsch</a> •
  <a href="README.fr.md"><b>Français</b></a>
</p>

<p align="center">
  <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/OpenConstructionEstimate.jpg" alt="OpenConstructionEstimate" width="1000">
</p>

<div align="center">
  <img src="https://img.shields.io/badge/Ouvrages-55,719-2563eb?style=for-the-badge" alt="Ouvrages">
  <img src="https://img.shields.io/badge/Ressources-27,672-059669?style=for-the-badge" alt="Ressources">
  <img src="https://img.shields.io/badge/Langues-9-d97706?style=for-the-badge" alt="Langues">
  <img src="https://img.shields.io/badge/Pays-10+-dc2626?style=for-the-badge" alt="Pays">
</div>

<div align="center">
  <img src="https://img.shields.io/badge/License-CC_BY_4.0-green?style=flat-square" alt="Licence">
  <img src="https://img.shields.io/badge/Version-v0.1.0-blue?style=flat-square" alt="Version">
  <img src="https://img.shields.io/badge/Embeddings-OpenAI_3072d-412991?style=flat-square" alt="Embeddings">
  <img src="https://img.shields.io/badge/Vector_DB-Qdrant-dc382d?style=flat-square" alt="Qdrant">
  <img src="https://img.shields.io/badge/Automation-n8n-ea4b71?style=flat-square" alt="n8n">
</div>

<p align="center">
  <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/OpenConstructionEstimate_bottom.jpg" alt="OpenConstructionEstimate" width="1000">
</p>

<h3 align="center">⚡ Workflows n8n</h3>
<p align="center"><code>Choisissez votre entrée → Obtenez une estimation des coûts</code></p>

<br>

<table width="100%">
<tr>

<td align="center" valign="top" width="33%">
<br>
<h3>📝 Texte</h3>
<p>Estimation rapide à partir<br>d'une courte description</p>
<p><b>Entrée :</b> Message Telegram / chat<br>
<b>Sortie :</b> Ouvrages correspondants + estimation</p>
<br>
<a href="#1️⃣-bot-estimateur-de-texte">📖 Documentation</a>
<br><br>
<a href="./n8n_1_Telegram_Bot_Cost_Estimates_and_Rate_Finder_TEXT_DDC_CWICR.json">
<img src="https://img.shields.io/badge/Télécharger_Workflow-0A84FF?style=for-the-badge&logo=download&logoColor=white" alt="Télécharger"/>
</a>
<br><br>
</td>

<td align="center" valign="top" width="33%">
<br>
<h3>📷 Photo / PDF</h3>
<p>Photos de chantier, devis scannés,<br>PDF-photo du terrain</p>
<p><b>Entrée :</b> Image ou pages PDF<br>
<b>Sortie :</b> Périmètre extrait → estimation</p>
<br>
<a href="#2️⃣-estimateur-de-coûts-par-photo">📖 Docs Photo</a> · <a href="#3️⃣-bot-estimateur-universel-texte--photo--pdf">📖 Bot Universel</a>
<br><br>
<a href="./n8n_2_Photo_Cost_Estimate_DDC_CWICR.json">
<img src="https://img.shields.io/badge/Workflow_Photo-0A84FF?style=for-the-badge&logo=download&logoColor=white" alt="Photo"/>
</a>
&nbsp;
<a href="./n8n_3_Telegram_Bot_Cost_Estimates_and_Rate_Finder_TEXT_PHOTO_PDF_DDC_CWICR.json">
<img src="https://img.shields.io/badge/Bot_Telegram-0A84FF?style=for-the-badge&logo=telegram&logoColor=white" alt="Bot"/>
</a>
<br><br>
</td>

<td align="center" valign="top" width="33%">
<br>
<h3>🧊 CAO / BIM</h3>
<p>Quantification et estimation<br>basées sur Revit / IFC / DWG</p>
<p><b>Entrée :</b> Export de modèle <br>
<b>Sortie :</b> Estimation 4D/5D + décomposition</p>
<br>
<a href="#4️⃣-pipeline-destimation-des-coûts-cao-bim">📖 Documentation</a>
<br><br>
<a href="./n8n_4_CAD_(BIM)_Cost_Estimation_Pipeline_4D_5D_with_DDC_CWICR.json">
<img src="https://img.shields.io/badge/Télécharger_Workflow-0A84FF?style=for-the-badge&logo=download&logoColor=white" alt="Télécharger"/>
</a>
<br><br>
</td>

</tr>
</table>

<br>
<p align="center">
  <a href="https://openconstructionestimate.com">
    <img src="https://img.shields.io/badge/🌐_DÉMO_EN_DIRECT_(base_de_données_uniquement)-openconstructionestimate.com-2563eb?style=for-the-badge" alt="Démo en direct">
  </a>
</p>
<br>
<p align="center">
 Clients et utilisateurs de DataDrivenConstruction
  <br>
  <a href="https://datadrivenconstruction.io/">
  <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/Clients_DataDrivenConstruction_logos.png" width="95%"/>
  </a>
  <br></br>
</p>


---

## 📑 Table des Matières

### Intégration IA
- [Carburant Parfait pour l'IA](#-carburant-parfait-pour-vos-produits-ia) — Pourquoi cette base de données est idéale pour l'IA
- [Claude Code](#-claude-code--assistant-de-codage-ia) — Utilisation de l'assistant de codage IA
- [n8n](#-n8n--automatisation-visuelle-des-workflows) — Automatisation des workflows
- [Dify](#-dify--construire-des-applications-llm) — Développement d'applications LLM
- [Sim AI & Autres](#-sim-ai--plateformes-similaires) — Plateformes compatibles
- [Cas d'Utilisation Universels](#-cas-dutilisation-universels) — Ce que vous pouvez construire

### Base de Données & Données
- [À Propos](#à-propos) — Qu'est-ce que DDC CWICR
- [Formats Disponibles](#formats-disponibles) — Excel, Parquet, CSV, Qdrant
- [Schéma de Données](#schéma-de-données) — Structure de 85 champs
- [Groupes de Champs](#groupes-de-champs) — Classification, Ressources, Main-d'œuvre, Machinerie
- [Méthodologie](#méthodologie) — Principes de calcul des coûts basé sur les ressources
- [Contexte Historique](#contexte-historique) — Plus de 100 ans de normes

### Workflows n8n
- [Vue d'Ensemble des Workflows n8n](#-workflows-n8n) — Choisissez votre type d'entrée
- [Essayez Maintenant — Bots de Démonstration en Direct](#-essayez-maintenant--bots-de-démonstration-en-direct) — Testez instantanément sur Telegram
- [Workflow 1 : Bot Estimateur de Texte](#1️⃣-bot-estimateur-de-texte) — Bot Telegram pour entrée texte
- [Workflow 2 : Estimateur de Coûts par Photo](#2️⃣-estimateur-de-coûts-par-photo) — Formulaire web avec Vision IA
- [Workflow 3 : Bot Universel](#3️⃣-bot-estimateur-universel-texte--photo--pdf) — Texte + Photo + PDF
- [Workflow 4 : Pipeline CAO/BIM](#4️⃣-pipeline-destimation-des-coûts-cao-bim) — De Revit/IFC/DWG à l'estimation
- [Démarrage Rapide des Workflows](#démarrage-rapide-des-workflows) — Configuration en 4 étapes
- [⚠️ Configuration n8n 2.0+](#️-configuration-n8n-20-requise) — Activer le nœud Execute Command

### Détails du Pipeline CAO/BIM
- [Prérequis](#-prérequis) — Composants requis
- [Étapes du Pipeline](#-étapes-du-pipeline) — Traitement en 10 étapes
- [Sélection du Modèle LLM](#️-sélection-du-modèle-llm) — OpenAI, Claude, Gemini, Grok
- [Fichiers de Sortie](#-fichiers-de-sortie) — Rapports HTML & Excel
- [Dépannage](#️-dépannage) — Problèmes courants

### Base de Données Vectorielle
- [Base de Données Vectorielle](#base-de-données-vectorielle) — Recherche sémantique avec Qdrant
- [Releases](#releases) — Télécharger les snapshots
- [Collections](#collections) — 9 collections linguistiques
- [Déploiement Docker](#déploiement-docker) — Configuration auto-hébergée

### Pour Commencer
- [Démarrage Rapide - Python](#démarrage-rapide) — Données tabulaires & recherche sémantique
- [Cas d'Utilisation pour l'Intégration](#intégration) — Niveau Débutant à Avancé

### Communauté
- [Ressources & Communauté](#ressources--communauté) — Liens & canaux
- [Conseil & Formation](#conseil--formation) — Services professionnels
- [Contribuer](#contribuer) — Soumettez vos workflows
- [Licence](#licence) — CC BY 4.0 & MIT
- [Soutenir le Projet](#soutenir-le-projet) — Sponsor & don


---

## 🚀 Carburant Parfait pour Vos Produits IA

<p align="center">
  <b>Clonez simplement le dépôt et décrivez ce que vous voulez — l'IA fait le reste</b>
</p>

DDC CWICR n'est pas seulement une base de données — c'est un **carburant prêt à l'emploi pour les applications alimentées par l'IA**. Que vous construisiez des bots d'estimation des coûts, automatisiez des workflows de construction, ou créiez des assistants intelligents — ces données fonctionnent immédiatement avec les outils IA modernes.

### Pourquoi Cette Base de Données est Idéale pour l'IA

| Caractéristique | Avantage |
|-----------------|----------|
| **Embeddings pré-calculés** | Pas besoin de générer des vecteurs — la recherche sémantique fonctionne instantanément |
| **Schéma structuré de 85 champs** | L'IA peut raisonner sur les relations de données et fournir des réponses précises |
| **9 langues incluses** | Construisez des applications multilingues sans surcharge de traduction |
| **55 000+ ouvrages** | Couverture complète pour toute tâche d'estimation de construction |
| **Méthodologie basée sur les ressources** | Données transparentes que l'IA peut expliquer et décomposer |

### 🛠️ Fonctionne Parfaitement Avec

<table>
<tr>
<td align="center" width="25%">
<img src="https://img.shields.io/badge/Claude_Code-000000?style=for-the-badge&logo=anthropic&logoColor=white" alt="Claude Code"/><br/>
<b>Claude Code</b><br/>
<sub>Assistant de codage IA CLI</sub>
</td>
<td align="center" width="25%">
<img src="https://img.shields.io/badge/n8n-EA4B71?style=for-the-badge&logo=n8n&logoColor=white" alt="n8n"/><br/>
<b>n8n</b><br/>
<sub>Automatisation de workflows</sub>
</td>
<td align="center" width="25%">
<img src="https://img.shields.io/badge/Dify-1677FF?style=for-the-badge&logo=openai&logoColor=white" alt="Dify"/><br/>
<b>Dify</b><br/>
<sub>Développement d'applications LLM</sub>
</td>
<td align="center" width="25%">
<img src="https://img.shields.io/badge/Sim_AI-6366F1?style=for-the-badge&logo=simpleicons&logoColor=white" alt="Sim AI"/><br/>
<b>Sim AI & Autres</b><br/>
<sub>Plateformes IA</sub>
</td>
</tr>
<tr>
<td align="center" width="25%">
<img src="https://img.shields.io/badge/Google_Antigravity-4285F4?style=for-the-badge&logo=google&logoColor=white" alt="Google Antigravity"/><br/>
<b>Google Antigravity</b><br/>
<sub>Google Antigravity</sub>
</td>
</tr>
</table>

---

### 💻 Claude Code — Assistant de Codage IA

La façon la plus rapide de travailler avec DDC CWICR. Ouvrez simplement le dépôt dans Claude Code et posez des questions en langage naturel.

**Pour Commencer :**
```bash
# Cloner le dépôt
git clone https://github.com/datadrivenconstruction/OpenConstructionEstimate-DDC-CWICR.git

# Ouvrir avec Claude Code
cd OpenConstructionEstimate-DDC-CWICR
claude
```

**Exemples de Prompts :**

| Tâche | Prompt |
|-------|--------|
| **Explorer les données** | "Montre-moi la structure de cette base de données de construction et explique quelles données sont disponibles" |
| **Trouver des ouvrages** | "Trouve tous les ouvrages liés aux fondations en béton et montre leurs coûts" |
| **Construire des requêtes** | "Écris un script Python pour rechercher des ouvrages de plomberie avec des heures de main-d'œuvre > 100" |
| **Créer des rapports** | "Génère un rapport de décomposition des coûts pour des travaux de rénovation résidentielle" |
| **Analyser les coûts** | "Compare les coûts des matériaux entre différentes méthodes de construction de murs" |
| **Construire des intégrations** | "Crée un script qui se connecte à la base de données Qdrant et effectue une recherche sémantique" |

**Conseils Pro :**
- Pointez Claude vers des fichiers spécifiques : *"Analyse le fichier Parquet et résume la distribution des coûts"*
- Demandez des explications : *"Explique comment la méthodologie de calcul des coûts basée sur les ressources fonctionne dans cette base de données"*
- Demandez des modifications : *"Modifie le workflow n8n pour ajouter des notifications par email"*

---

### ⚡ n8n — Automatisation Visuelle des Workflows

Construisez des pipelines d'automatisation puissants sans coder. Connectez DDC CWICR à plus de 400 applications et services.

**Cas d'Utilisation :**

| Workflow | Description |
|----------|-------------|
| **Bot Telegram** | Les utilisateurs envoient texte/photo → L'IA extrait les ouvrages → Retourne l'estimation des coûts |
| **Automatisation Email** | Recevoir un devis par email → Traiter avec l'IA → Envoyer une estimation formatée |
| **Intégration CRM** | Nouveau projet dans le CRM → Générer automatiquement une estimation préliminaire → Mettre à jour la valeur du contrat |
| **Pipeline BIM** | Export depuis Revit → Extraire les quantités → Correspondre avec les tarifs DDC → Générer un rapport 5D |
| **Bot Slack** | L'équipe pose des questions → L'IA recherche dans la base → Retourne les ouvrages pertinents |

**Démarrage Rapide :**
1. Téléchargez le JSON du workflow depuis ce dépôt
2. Importez dans n8n : `Workflows → Import → From File`
3. Configurez les identifiants (OpenAI, Qdrant, Telegram)
4. Activez et testez

Voir la section [Workflows n8n](#workflows-n8n--description-détaillée) pour la configuration détaillée.

---

### 🤖 Dify — Construire des Applications LLM

Créez des applications IA personnalisées avec DDC CWICR comme base de connaissances.

**Configuration :**
1. Créez une nouvelle application Dify
2. Ajoutez une Base de Connaissances → Téléchargez les fichiers Parquet/CSV ou connectez-vous à Qdrant
3. Configurez le pipeline RAG avec les embeddings
4. Construisez votre interface de chat ou API

**Idées d'Applications :**

| Type d'App | Description |
|------------|-------------|
| **Chatbot Estimateur de Construction** | Interface conversationnelle pour les requêtes de coûts |
| **Recherche d'Ouvrages** | Recherche en langage naturel parmi 55 000+ éléments |
| **Conseiller en Coûts** | IA qui explique les décompositions de coûts et suggère des optimisations |
| **Assistant Multilingue** | Détection automatique de la langue et réponse dans la langue de l'utilisateur |
| **Point de Terminaison API** | API REST pour l'intégration avec d'autres systèmes |

**Exemple de Template de Prompt Dify :**
```
Vous êtes un assistant d'estimation des coûts de construction avec accès à la base de données DDC CWICR.

Contexte : {{context}}

Question de l'utilisateur : {{query}}

Fournissez des informations de coûts précises basées sur la base de données. Incluez :
- Les ouvrages pertinents avec leurs codes
- Les coûts unitaires et quantités
- La décomposition des ressources (main-d'œuvre, matériaux, équipement)
- Le calcul du coût total
```

---

### 🔮 Sim AI & Plateformes Similaires

DDC CWICR s'intègre avec toute plateforme IA qui supporte :
- **Bases de données vectorielles** (Qdrant, Pinecone, Weaviate, Milvus)
- **Données structurées** (CSV, Parquet, Excel)
- **Embeddings OpenAI** (text-embedding-3-large, 3072 dimensions)

**Plateformes Compatibles :**
- **Sim AI** — Simulation et modélisation IA
- **LangChain / LlamaIndex** — Frameworks d'applications LLM
- **Flowise** — Constructeur d'applications LLM low-code
- **Botpress** — Plateforme d'IA conversationnelle
- **Voiceflow** — Conception vocale et chat
- **Stack AI** — Workflows IA no-code
- **Relevance AI** — Plateforme de main-d'œuvre IA

**Pattern d'Intégration Universel :**

```python
# Fonctionne avec toute plateforme supportant Qdrant
from qdrant_client import QdrantClient

# Se connecter à DDC CWICR
client = QdrantClient("your-qdrant-instance", port=6333)

# Recherche sémantique
results = client.search(
    collection_name="ddc_cwicr_en",  # ou de, ru, zh, etc.
    query_vector=your_embedding,
    limit=10
)

# Utiliser les résultats dans votre application IA
for item in results:
    print(f"{item.payload['rate_code']}: {item.payload['rate_original_name']}")
```

---

### 📋 Cas d'Utilisation Universels

Quel que soit l'outil IA que vous choisissez, DDC CWICR permet :

| Cas d'Utilisation | Description |
|-------------------|-------------|
| **Estimation Instantanée des Coûts** | Obtenez les coûts de construction à partir de descriptions textuelles ou de photos |
| **Génération de Devis Quantitatifs** | Générez automatiquement des devis quantitatifs à partir de descriptions de projets |
| **Benchmarking des Prix** | Comparez les coûts entre régions et langues |
| **Planification des Ressources** | Calculez les heures de main-d'œuvre, matériaux et besoins en équipement |
| **Analyse d'Investissement** | Audits approfondis des coûts avec transparence totale des ressources |
| **Support Multilingue** | Servez les utilisateurs dans 9 langues avec des prix localisés |
| **Intégration BIM** | Connectez-vous à Revit/IFC pour l'estimation 4D/5D automatisée |
| **Entraînement de Modèles IA** | Utilisez des données structurées pour l'ajustement fin de l'IA de construction |

---

## À Propos

**DDC CWICR** (Construction Work Items, Components & Resources - Ouvrages de Construction, Composants & Ressources) est une base de données ouverte pour l'estimation des coûts de construction, couvrant l'ensemble des activités de construction - des terrassements et du coulage de béton aux travaux d'installation spécialisés.

La base de données s'appuie sur des sources décrivant les pratiques de construction modernes à travers l'Eurasie et la région Asie-Pacifique, où un écosystème de normalisation technique unifié sert de langage d'ingénierie commun pour plus de dix économies en développement dynamique. DDC CWICR représente un effort d'harmonisation des normes ouvertes en établissant un cadre réglementaire unique pour la gestion de projets d'investissement dans plusieurs langues.

<p align="center">
  <br>
  <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/DDC%20CWICR%20GEOGRAPHIC%20COVERAGE.jpg" width="100%"/>
  <br></br>
</p>

Les données structurées peuvent être accessibles via des formats tabulaires (XLSX, CSV, Parquet) ou interrogées de manière conversationnelle via LLM, permettant aux spécialistes d'intégrer les descriptions d'ouvrages de construction (base de données vectorielle QDRANT) dans des pipelines et workflows automatisés en utilisant un langage simple ou des requêtes concises.

### Formats Disponibles

| Format      | Extension   | Taille       | Idéal Pour                            | Caractéristiques                     |
|-------------|-------------|--------------|---------------------------------------|--------------------------------------|
| **Excel**   | `.xlsx`     | ~150–400 Mo  | Analyse manuelle, filtrage, tableaux croisés | Lisible par l'homme, formatage complet |
| **Parquet** | `.parquet`  | ~55 Mo       | Pipelines ETL, entraînement ML, Big Data | Colonaire, excellente compression    |
| **CSV**     | `.csv`      | ~1,3 Go      | Import base de données, systèmes hérités | Compatibilité universelle            |
| **Qdrant**  | `.snapshot` | ~1 Go        | Recherche sémantique, RAG, assistants IA | Embeddings OpenAI pré-calculés       |


Une démonstration en direct est disponible sur [openconstructionestimate.com](https://openconstructionestimate.com/), où vous pouvez explorer les données et voir la base de données vectorielle en action pour la recherche sémantique.

<p align="center">
  <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/DDC%20CWICR%20Resource-based%20Work%20Cost%20Norms.jpg" alt="OpenConstructionEstimate" width="1000">
</p>

---

## Schéma de Données

La base de données contient **85 champs** organisés en groupes logiques. Chaque enregistrement représente soit un ouvrage (tarif) soit une ressource avec une décomposition complète des coûts.

```mermaid
erDiagram
    TARIF ||--o{ RESSOURCE : contient
    TARIF ||--o{ MAIN_DOEUVRE : requiert
    TARIF ||--o{ MACHINERIE : utilise
    TARIF ||--o{ VARIANTE_PRIX : possède

    TARIF {
        string rate_code PK "MEKA_KASA_KAKATO_KAME"
        string rate_original_name "Installation de cloisons..."
        string rate_unit "100 m2"
        string category_type "TRAVAUX DE CONSTRUCTION"
        string collection_name "Constructions en bois"
        string department_name "CLOISONS..."
        string section_name "Installation de cloisons..."
        text work_composition_text
    }

    RESSOURCE {
        string resource_code PK "KAME-NE-KAME-KARI"
        string resource_name "Plaques de plâtre"
        string resource_unit "m2"
        float resource_quantity "632.0"
        float resource_price_per_unit_eur "5.02"
        float resource_cost_eur "3170.73"
        boolean is_material
        boolean is_abstract
    }

    MAIN_DOEUVRE {
        string resource_code FK
        float labor_hours_workers "172"
        float labor_hours_machinists "1.67"
        int count_workers_per_unit "172"
        int count_machinists_per_unit "2"
        float cost_of_working_hours "3088.11"
    }

    MACHINERIE {
        string machine_class2_name "Grues"
        string machine_class3_name "Grues sur châssis"
        float electricity_consumption_kwh "0.23"
        float price_machinist_wages "13.56"
        float total_value_machinery "64.18"
    }

    VARIANTE_PRIX {
        float price_est_median "5.02"
        float price_est_min "3.03"
        float price_est_max "7.99"
        int position_count "24"
        string variable_parts "renforcé de fibres de verre..."
    }
```

### Groupes de Champs
Les 85 champs de la base de données sont organisés en groupes logiques qui reflètent la méthodologie d'estimation des coûts basée sur les ressources. Chaque groupe remplit une fonction spécifique dans la structure de décomposition des coûts : de la classification hiérarchique et l'identification des ouvrages à la consommation détaillée des ressources, aux exigences de main-d'œuvre, aux coûts de machinerie et aux totaux agrégés. Cette structure modulaire permet aux utilisateurs de ne requêter que les champs pertinents pour leur tâche - qu'il s'agisse de générer une nomenclature des matériaux, d'analyser la productivité de la main-d'œuvre ou de construire une estimation complète des coûts.

<p align="center">
  <br>
  <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/Resource-based%20Work%20Cost%20Norms%20table2.jpg" width="100%"/>
  <br></br>
</p>

**Classification** - `category_type`, `collection_code`, `collection_name`, `department_code`, `department_name`, `department_type`, `section_name`, `section_type`, `subsection_code`, `subsection_name`

**Ouvrage (Tarif)** - `rate_code`, `rate_original_name`, `rate_final_name`, `rate_unit`, `row_type`, `is_scope`, `is_abstract`, `is_machine`, `is_labor`, `is_material`, `work_composition_text`

**Ressources** - `resource_code`, `resource_name`, `resource_unit`, `resource_quantity`, `parameter_resource_quantity`, `resource_price_per_unit_eur_current`, `resource_cost_eur`

**Main-d'œuvre** - `count_workers_per_unit`, `count_engineers_per_unit`, `count_machinists_per_unit`, `count_total_people_per_unit`, `labor_hours_construction_workers`, `labor_hours_machinists`, `labor_hours_engineers`, `total_labor_hours_workers_machinists`, `total_labor_hours_all_personnel`, `cost_of_working_hours`, `count_people_per_day`

**Machinerie** - `machine_class2_name`, `machine_class3_name`, `personnel_machinist_code`, `personnel_machinist_grade`, `price_machinist_wages`, `price_relocation_included`, `price_cost_without_wages`, `electricity_consumption_kwh_per_machine_hour`, `electricity_cost_per_unit`, `electricity_cost_total_sum`, `cost_machinist_sum`, `total_value_machinery_equipment`

**Variantes de Prix** - `price_code_prefix`, `price_abstract_resource_common_start`, `price_abstract_resource_variable_parts`, `price_abstract_resource_position_count`, `price_abstract_resource_est_price_min`, `price_abstract_resource_est_price_max`, `price_abstract_resource_est_price_mean`, `price_abstract_resource_est_price_median`, `price_abstract_resource_unit`, `abstract_resource_tech_group`

**Agrégats** - `total_cost_per_position`, `total_material_cost_per_position`, `total_resource_cost_per_position`, `total_value_abstract_resources`, `materials_resource_cost_eur`

**Masse & Services** - `mass_name`, `mass_value`, `mass_unit`, `service_category`, `service_type`, `parameter_service_code`, `parameter_service_unit`, `parameter_service_name`, `parameter_service_quantity`, `service_cost_sum`

### Formule de Calcul des Coûts

| Composant         | Norme Technologique | ×   | Prix Régional   | =   | Coût                    |
|-------------------|---------------------|-----|-----------------|-----|-------------------------|
| 👷 **Main-d'œuvre** | 172 h/100m²        | ×   | 17,95 €/h       | =   | 3 088,11 €              |
| 🧱 **Matériaux**   | 632 m²/100m²       | ×   | 5,02 €/m²       | =   | 3 170,73 €              |
| 🚜 **Équipement**  | 1,67 h/100m²       | ×   | 38,42 €/h       | =   | 64,18 €                 |
|                   |                     |     | **Total**       | =   | **7 725,91 € par 100m²**|

---

## Méthodologie

La valeur clé du **Calcul des Coûts Basé sur les Ressources** est la séparation de la technologie de production immuable de la composante financière volatile. Elle est basée sur les "premiers principes" physiques de la construction :
- Les heures de main-d'œuvre requises pour un travail spécifique
- Les quantités de matériaux par unité de travail
- Le temps d'équipement nécessaire

**Pourquoi c'est important :**

- **Transparence** - Tarification sans majorations cachées, décomposition complète des ressources
- **Vérifiabilité** - Capacité d'analyse approfondie pour l'analyse d'investissement et la vérification
- **Portabilité** - Normes indépendantes de la région applicables à travers les marchés
- **Éprouvée** - Méthodologie standard de l'industrie établie depuis plus de 100 ans

```mermaid
flowchart TB
    subgraph Source["📦 Source de Données"]
        CWICR[(DDC CWICR<br/>────────────<br/>55 719 Ouvrages<br/>27 672 Ressources<br/>85 Champs par Enregistrement)]
    end

    subgraph Processing["⚙️ Pipeline de Traitement"]
        direction LR
        ETL[["🔄 ETL<br/>Extraction &<br/>Transformation"]]
        TRANS[["🌐 Traduction<br/>9 Langues"]]
        EMBED[["🧠 Vectorisation<br/>OpenAI 3072d"]]
        ETL --> TRANS --> EMBED
    end

    subgraph Outputs["📤 Formats de Sortie"]
        XLSX[("📊 Excel<br/>.xlsx")]
        PARQUET[("⚡ Parquet<br/>.parquet")]
        CSV[("📄 CSV<br/>.csv")]
        QDRANT[("🔍 Qdrant<br/>.snapshot")]
    end

    subgraph Apps["🎯 Applications"]
        SEARCH["🔎 Recherche<br/>Sémantique"]
        BIM["🏗️ BIM 5D<br/>Intégration"]
        RAG["🤖 Systèmes<br/>RAG"]
        BI["📈 Analytique<br/>BI"]
    end

    Source --> Processing
    Processing --> XLSX & PARQUET & CSV & QDRANT
    XLSX & PARQUET & CSV --> BI & BIM
    QDRANT --> SEARCH & RAG & BIM

    style Source fill:#dbeafe,stroke:#2563eb,stroke-width:2px
    style Processing fill:#fef3c7,stroke:#d97706,stroke-width:2px
    style Outputs fill:#d1fae5,stroke:#059669,stroke-width:2px
    style Apps fill:#fce7f3,stroke:#db2777,stroke-width:2px
```


### Contexte Historique

Les descriptions d'ouvrages de construction de cette base de données sont fondées sur une méthodologie de normalisation basée sur les ressources dont les racines s'étendent des normes de production du début du XXe siècle aux systèmes de référence numériques d'aujourd'hui. Développée et affinée continuellement depuis les années 1920, cette approche a connu une évolution particulièrement robuste à travers la région eurasienne.

Tout au long d'un siècle de développement, le système est passé des calculs manuels aux formats lisibles par machine - pourtant son principe fondamental reste intact : la mesure précise des ressources physiques requises par unité de production de construction. Les implémentations modernes relient les données normatives historiques aux prix du marché en temps réel.

Les adaptations régionales de cette méthodologie fonctionnent sous diverses désignations nationales : ENIR, GESN, FER, NRR, ESN, AzDTN, ShNQK, MKS ChT, SNT, BNbD, Dinh Muc, Ding'e.

<p align="center">
  <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/DDC%20CWICR%20SPREAD%20OF%20METHODOLOGY%20FROM%20THE%201920s.jpg" alt="OpenConstructionEstimate" width="1000">
</p>

⭐ <b>Si vous souhaitez voir de nouvelles mises à jour et versions de la base de données et si vous trouvez nos outils utiles, veuillez donner une étoile à nos dépôts pour voir plus d'applications similaires pour l'industrie de la construction.</b>
Donnez une étoile au workflow DDC sur GitHub et soyez instantanément notifié des nouvelles versions.
<p align="center">
  <br>
  <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/OCE%20star%20GitHub.gif" width="100%"/>
  <br></br>
</p>


---


## Intégration

### Cas d'Utilisation

- **Niveau Débutant** - Benchmarking des Coûts, Indexation des Prix, Estimation d'Appel d'Offres

- **Niveau Intermédiaire** - Localisation, Pipelines ETL/BI, Calcul CO₂

- **Niveau Avancé** - Entraînement IA/ML, CAO (BIM) 5D, Audit d'Investissement Approfondi

---

## Workflows n8n — Description Détaillée

Quatre workflows prêts pour la production pour l'estimation automatisée des coûts de construction. Chaque workflow se connecte à la base de données vectorielle DDC CWICR via Qdrant et utilise des modèles d'IA pour l'analyse et la correspondance intelligentes.

| #   | Workflow                                                        | Entrée      | Idéal Pour                      | Télécharger                                                                                         |
|-----|-----------------------------------------------------------------|-------------|---------------------------------|-----------------------------------------------------------------------------------------------------|
| 1   | [Bot Estimateur de Texte](#1️⃣-bot-estimateur-de-texte)          | 💬 Texte    | Estimations rapides à partir de texte | [JSON](./n8n_1_Telegram_Bot_Cost_Estimates_and_Rate_Finder_TEXT_DDC_CWICR.json)                      |
| 2   | [Estimateur Photo](#2️⃣-estimateur-de-coûts-par-photo)           | 📷 Photo    | Visites de chantier, inspections visuelles | [JSON](./n8n_2_Photo_Cost_Estimate_DDC_CWICR.json)                                                  |
| 3   | [Bot Universel](#3️⃣-bot-estimateur-universel-texte--photo--pdf) | 💬📷📄 Tous | Utilisation en production complète | [JSON](./n8n_3_Telegram_Bot_Cost_Estimates_and_Rate_Finder_TEXT_PHOTO_PDF_DDC_CWICR.json)            |
| 4   | [Pipeline CAO/BIM](#4️⃣-pipeline-destimation-des-coûts-cao-bim)  | 🏗️ Revit   | Estimation 4D/5D basée sur BIM  | [JSON](./n8n_4_CAD_(BIM)_Cost_Estimation_Pipeline_4D_5D_with_DDC_CWICR.json)                         |

---

### 1️⃣ Bot Estimateur de Texte

**Fichier :** `n8n_1_Telegram_Bot_Cost_Estimates_and_Rate_Finder_TEXT_DDC_CWICR.json`

Bot Telegram pour l'estimation des coûts basée sur le texte. Décrivez les travaux de construction en langage naturel — le bot analyse l'entrée, recherche dans la base de données vectorielle et retourne des décompositions détaillées des coûts.

<p align="center">
  <br>
  <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/Text_Estimator_Bot.jpg" width="100%"/>
  <br></br>
</p>

<h3 align="left">🤖 Essayez Maintenant — Bots de Démonstration en Direct</h3>
<p align="left"><i>Testez les workflows d'estimation instantanément sur Telegram</i></p>
<p><b>@TextOpenConstructionEstimate_bot</b></p>
<p>Créez des estimations de coûts complètes<br>à partir de descriptions textuelles</p>
<a href="https://t.me/TextOpenConstructionEstimate_bot">
<img src="https://img.shields.io/badge/Ouvrir_Bot-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" alt="Bot Texte"/>
</a>

```mermaid
flowchart LR
    subgraph Input["💬 ENTRÉE"]
        A[Message Telegram]
    end

    subgraph AI["🤖 TRAITEMENT IA"]
        B[Analyser le Texte]
        C[Extraire les Ouvrages]
    end

    subgraph Search["🔍 RECHERCHE VECTORIELLE"]
        D[Générer Embeddings]
        E[Recherche Qdrant]
        F[Reranking IA]
    end

    subgraph Output["📊 SORTIE"]
        G[Calculer les Coûts]
        H[Rapport HTML]
        I[Export Excel]
    end

    A --> B --> C --> D --> E --> F --> G --> H
    G --> I

    style Input fill:#e0f2fe,stroke:#0284c7
    style AI fill:#fef3c7,stroke:#d97706
    style Search fill:#dcfce7,stroke:#16a34a
    style Output fill:#f3e8ff,stroke:#9333ea
```



**Comment ça fonctionne :**

| Étape | Action                                 | Technologie                            |
|-------|----------------------------------------|----------------------------------------|
| 1     | L'utilisateur envoie une description textuelle | API Bot Telegram                       |
| 2     | L'IA analyse et extrait les ouvrages   | OpenAI / Claude / Gemini               |
| 3     | Génération d'embeddings pour chaque élément | OpenAI `text-embedding-3-large`        |
| 4     | Recherche des tarifs correspondants dans la base | Recherche vectorielle Qdrant           |
| 5     | Reranking IA des résultats pour la précision | Scoring LLM                            |
| 6     | Calcul des coûts et génération du rapport | HTML / Excel / PDF                     |

**Fonctionnalités :**

| Fonctionnalité             | Description                                                          |
|----------------------------|----------------------------------------------------------------------|
| 💬 Entrée en langage naturel | Accepte tout format de texte — listes, phrases, descriptions structurées |
| 🤖 Support multi-LLM       | Fonctionne avec OpenAI, Claude ou Gemini (interchangeable)           |
| 🔍 Recherche sémantique    | Trouve les meilleures correspondances même avec une formulation différente |
| 🌍 9 langues               | DE, EN, RU, ES, FR, PT, ZH, AR, HI                                   |
| 📊 Exports multiples       | Rapport HTML, tableur Excel, document PDF                            |
| ✏️ Édition interactive     | Modifier les quantités avant le calcul final                         |

**Identifiants requis :**
- Token de Bot Telegram (depuis @BotFather)
- Clé API OpenAI (pour embeddings + LLM optionnel)
- URL Qdrant + Clé API

---

### 2️⃣ Estimateur de Coûts par Photo

**Fichier :** `n8n_2_Photo_Cost_Estimate_DDC_CWICR.json`

Interface de formulaire web pour l'estimation basée sur les photos. Téléchargez une photo de construction — l'IA Vision identifie les éléments, estime les dimensions et calcule automatiquement les coûts.

<p align="center">
  <br>
  <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/n8n%20pipeline%20photo%20estimator.jpg" width="100%"/>
  <br></br>
</p>

```mermaid
flowchart TB
    subgraph Upload["📷 TÉLÉCHARGEMENT PHOTO"]
        A[Formulaire Web]
        B[Sélectionner la Région]
        C[Choisir le Type de Travaux]
    end

    subgraph Vision["👁️ VISION IA"]
        D[Analyse GPT-4 Vision]
        E[Identifier les Éléments]
        F[Estimer les Dimensions]
        G[Détecter le Type de Pièce]
    end

    subgraph Decompose["🔧 DÉCOMPOSITION"]
        H[Éléments → Ouvrages]
        I[Calculer les Quantités]
    end

    subgraph Price["💰 TARIFICATION"]
        J[Recherche Vectorielle]
        K[Correspondance Tarifs DDC]
        L[Appliquer les Prix Régionaux]
    end

    subgraph Report["📄 RAPPORT"]
        M[Générer HTML]
        N[Décomposition des Coûts]
    end

    A --> B --> C --> D
    D --> E --> F --> G
    G --> H --> I
    I --> J --> K --> L
    L --> M --> N

    style Upload fill:#dbeafe,stroke:#2563eb
    style Vision fill:#fef3c7,stroke:#d97706
    style Decompose fill:#dcfce7,stroke:#16a34a
    style Price fill:#fee2e2,stroke:#dc2626
    style Report fill:#f3e8ff,stroke:#9333ea
```



**Comment ça fonctionne :**

| Étape | Action                                        | Technologie                          |
|-------|-----------------------------------------------|--------------------------------------|
| 1     | L'utilisateur télécharge une photo via formulaire web | Déclencheur de Formulaire n8n        |
| 2     | L'IA Vision analyse l'image                   | GPT-4 Vision                         |
| 3     | Identifier le type de pièce, éléments, matériaux | Extraction JSON structurée           |
| 4     | Estimer les dimensions à partir d'objets de référence | Raisonnement IA (portes, carrelages, etc.) |
| 5     | Décomposer les éléments en ouvrages           | Traitement LLM                       |
| 6     | Tarifer chaque travail via recherche vectorielle | Qdrant + embeddings OpenAI           |
| 7     | Générer un rapport HTML professionnel         | Sortie stylisée                      |

**Fonctionnalités :**

| Fonctionnalité         | Description                                             |
|------------------------|---------------------------------------------------------|
| 📷 Analyse photo       | GPT-4 Vision identifie les éléments de construction     |
| 📐 Dimensionnement auto| Estime les tailles à partir d'objets de référence (portes, carrelages) |
| 🏠 Détection de pièce  | Salle de bain, cuisine, chambre, extérieur, etc.        |
| 🔨 Types de travaux    | Construction neuve / Rénovation / Réparation            |
| 🌍 9 bases régionales  | Prix localisés pour Berlin, Toronto, Paris, etc.        |
| 📄 Rapports professionnels | Sortie HTML propre prête pour les clients            |

**Identifiants requis :**
- Clé API OpenAI (GPT-4 Vision + embeddings)
- URL Qdrant + Clé API

---

### 3️⃣ Bot Estimateur Universel (Texte + Photo + PDF)

**Fichier :** `n8n_3_Telegram_Bot_Cost_Estimates_and_Rate_Finder_TEXT_PHOTO_PDF_DDC_CWICR.json`

Bot Telegram complet supportant tous les types d'entrée : descriptions textuelles, photos de construction et plans PDF. Le workflow le plus complet pour une utilisation en production.


<p align="center">
  <br>
  <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/Universal%20Estimator%20Bot%20Text%20%20Photo%20PDF.jpg" width="100%"/>
  <br></br>
</p>

<h3 align="left">🤖 Essayez Maintenant — Bots de Démonstration en Direct</h3>
<p align="left"><i>Testez les workflows d'estimation instantanément sur Telegram</i></p>
<h3>📷 Bot Universel</h3>
<p><b>@OpenConstructionEstimate_bot</b></p>
<p>Bot complet pour texte, photos et PDF</p>
<a href="https://t.me/OpenConstructionEstimate_bot">
<img src="https://img.shields.io/badge/Ouvrir_Bot-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" alt="Bot Universel"/>
</a>
<br><br>


```mermaid
flowchart TB
    subgraph Input["📥 MULTI-ENTRÉE"]
        A[💬 Message Texte]
        B[📷 Photo]
        C[📄 Document PDF]
    end

    subgraph Router["🔀 ROUTEUR INTELLIGENT"]
        D{Détecter le Type}
    end

    subgraph TextPath["💬 CHEMIN TEXTE"]
        E[Analyse IA du Texte]
        F[Extraire les Travaux]
    end

    subgraph PhotoPath["📷 CHEMIN PHOTO"]
        G[Vision IA]
        H[Identifier les Éléments]
        I[Décomposer]
    end

    subgraph PDFPath["📄 CHEMIN PDF"]
        J[Extraire les Pages]
        K[Analyse Vision]
        L[Analyser le Contenu]
    end

    subgraph Common["🔍 PIPELINE COMMUN"]
        M[Générer Embeddings]
        N[Recherche Qdrant]
        O[Reranking IA]
        P[Calculer les Coûts]
    end

    subgraph Export["📤 EXPORT"]
        Q[Rapport HTML]
        R[Excel CSV]
        S[Document PDF]
    end

    A --> D
    B --> D
    C --> D
    D -->|Texte| E --> F --> M
    D -->|Photo| G --> H --> I --> M
    D -->|PDF| J --> K --> L --> M
    M --> N --> O --> P
    P --> Q
    P --> R
    P --> S

    style Input fill:#e0f2fe,stroke:#0284c7
    style Router fill:#fef3c7,stroke:#d97706
    style TextPath fill:#dcfce7,stroke:#16a34a
    style PhotoPath fill:#fce7f3,stroke:#db2777
    style PDFPath fill:#f3e8ff,stroke:#9333ea
    style Common fill:#fee2e2,stroke:#dc2626
    style Export fill:#d1fae5,stroke:#059669
```



**Comment ça fonctionne :**

| Étape | Action                                    | Technologie                    |
|-------|-------------------------------------------|--------------------------------|
| 1     | L'utilisateur envoie texte, photo ou PDF  | API Bot Telegram               |
| 2     | Le routeur détecte le type d'entrée       | Analyse du content-type        |
| 3a    | **Texte :** L'IA analyse les ouvrages     | OpenAI / Gemini                |
| 3b    | **Photo :** Vision IA extrait les éléments| GPT-4 Vision / Gemini 2.0      |
| 3c    | **PDF :** Extraire et analyser les pages  | Traitement PDF + Vision        |
| 4     | Recherche sémantique dans DDC CWICR       | Base vectorielle Qdrant        |
| 5     | Reranking IA pour les meilleures correspondances | Scoring LLM                    |
| 6     | Édition interactive via menu du bot       | Claviers inline Telegram       |
| 7     | Exporter les résultats                    | HTML / Excel / PDF             |

**17 Actions du Bot :**

| Action           | Description                         |
|------------------|-------------------------------------|
| `/start`         | Menu de sélection de langue         |
| Téléchargement photo | Déclencher l'analyse vision IA    |
| Message texte    | Analyser et extraire les ouvrages   |
| Téléchargement PDF | Traiter les plans                  |
| Éditer quantités | Modifier avant le calcul            |
| Ajouter travaux  | Entrée manuelle d'ouvrage           |
| Calculer         | Lancer l'estimation complète        |
| Voir détails     | Afficher les ressources de chaque élément |
| Exporter Excel   | Télécharger le tableur CSV          |
| Exporter PDF     | Générer le rapport PDF              |
| Aide             | Afficher les instructions d'utilisation |
| Affiner          | Ré-analyser avec corrections        |

**Fonctionnalités :**

| Fonctionnalité        | Description                                        |
|-----------------------|----------------------------------------------------|
| 📷 Double Vision IA   | Gemini 2.0 Flash ou GPT-4 Vision (configurable)    |
| 📄 Traitement PDF     | Plans, devis scannés, documents                    |
| 💬 Analyse texte intelligente | Gère listes, tableaux, texte libre          |
| 🔍 Reranking IA       | Améliore la précision des correspondances          |
| ✏️ Édition complète   | Ajouter, supprimer, modifier les ouvrages          |
| 📊 Export multi-format| HTML, Excel, PDF                                   |
| 🌍 9 langues          | Localisation complète                              |

**Identifiants requis :**
- Token de Bot Telegram
- Clé API OpenAI (embeddings)
- Clé API Gemini (Vision) ou GPT-4 Vision OpenAI
- URL Qdrant + Clé API

---

### 4️⃣ Pipeline d'Estimation des Coûts CAO (BIM)

**Fichier :** `n8n_4_CAD_(BIM)_Cost_Estimation_Pipeline_4D_5D_with_DDC_CWICR.json`

Estimation automatisée des coûts à partir de modèles Revit/IFC/DWG. Extrait les données BIM, classe les éléments, décompose en ouvrages et génère des estimations 4D/5D avec décomposition complète des ressources.

<p align="left">
  <a href="https://datadrivenconstruction.io">
    <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/CAD%20(Revit)%20to%205D-4D%20Cost%20and%20Time%20Estimate.jpg" alt="DataDrivenConstruction">
  </a>
</p>

```mermaid
flowchart TB
    subgraph INPUT["📁 ENTRÉE<br/><i>CAO • photos • description textuelle</i>"]
        CAD["📐 Entrée Projet<br/>(texte • photos • RVT / IFC / DWG)"]
    end

    subgraph EXTRACT["⚙️ EXTRACTION"]
        CONV["RvtExporter.exe / Export CAO / ETL"]
        XLSX["📊 .XLSX<br/>(Éléments Bruts)"]
    end

    subgraph PREP["🔧 PRÉPARATION DES DONNÉES"]
        PREP_AI["🤖 IA : Nettoyer & Classifier<br/><i>en-têtes • types • catégories</i>"]
    end

    subgraph STAGE_PLAN["📋 ÉTAPES 1–3 : Planification"]
        PLAN["🤖 Détecter Projet & Phases<br/><i>neuf / rénovation / démolition</i><br/><i>petit / moyen / grand</i><br/><i>éléments → phases de construction</i>"]
    end

    subgraph STAGE4["🔨 ÉTAPE 4 : Décomposition"]
        S4["🤖 Décomposer Types en Travaux<br/><i>'Mur Brique 240mm' → maçonnerie, mortier, enduit</i>"]
    end

    subgraph STAGE5["💰 ÉTAPE 5 : Tarification"]
        S5["🤖 Tarifer via Base Vectorielle<br/><i>Embeddings OpenAI + Qdrant</i><br/><i>rate_code, unit_cost, ressources</i>"]
    end

    subgraph STAGE75["✅ ÉTAPE 7.5 : Validation"]
        S75["🤖 Revue CTO<br/><i>complétude • doublons • travaux manquants</i>"]
    end

    subgraph OUTPUT["📤 SORTIE"]
        HTML["📄 Rapport HTML"]
        XLS["📊 Rapport XLS"]
    end

    CAD --> CONV --> XLSX
    XLSX --> PREP_AI --> PLAN --> S4 --> S5 --> S75
    S75 --> HTML & XLS

    style INPUT fill:#f4f4f5,stroke:#d4d4d8,color:#18181b
    style EXTRACT fill:#e0f2fe,stroke:#bae6fd,color:#0f172a
    style PREP fill:#ede9fe,stroke:#ddd6fe,color:#1e1b4b
    style STAGE_PLAN fill:#ecfdf5,stroke:#bbf7d0,color:#064e3b
    style STAGE4 fill:#fef9c3,stroke:#fef3c7,color:#78350f
    style STAGE5 fill:#fee2e2,stroke:#fecaca,color:#7f1d1d
    style STAGE75 fill:#e0f2f1,stroke:#bae5e1,color:#134e4a
    style OUTPUT fill:#eef2ff,stroke:#e0e7ff,color:#111827
```


**n8n fournit plus de 400 intégrations natives** avec des plateformes comme Google Sheets, Notion, Slack, Airtable, des bases de données (PostgreSQL, MongoDB), le stockage cloud, et plus encore. Chaque nœud de ce workflow est modulaire — vous pouvez :

- 🔄 **Changer de fournisseur LLM** (OpenAI ↔ Claude ↔ Gemini ↔ Grok)
- 📊 **Connecter à votre ERP ou système de gestion de projet**
- 📁 **Exporter les résultats vers n'importe quelle destination** (stockage cloud, email, tableaux de bord)
- 🔧 **Modifier n'importe quelle étape** pour correspondre à votre méthodologie d'estimation

Le workflow vous appartient pour l'adapter. Aucune restriction. Aucun frais de licence. Contrôle total.

---

## 📋 Prérequis

| Composant                                          | Exigence                               | Description                                                           |
|----------------------------------------------------|----------------------------------------|-----------------------------------------------------------------------|
| **[n8n](https://n8n.io/)**                         | v1.0+ (v2.0+ requiert [configuration](#️-configuration-n8n-20-requise)) | Plateforme d'automatisation de workflows pour orchestrer le pipeline d'estimation |
| **[Qdrant](https://qdrant.tech/)**                 | Instance Cloud ou auto-hébergée        | Base de données vectorielle pour la recherche sémantique parmi les ouvrages de construction |
| **[API OpenAI](https://platform.openai.com/)**     | Pour embeddings (`text-embedding-3-large`) | Génère des embeddings vectoriels pour les éléments BIM et la correspondance avec la base de coûts |
| **API LLM**                                        | OpenAI / Claude / Gemini / xAI Grok    | Modèles IA pour la classification des ouvrages et la génération d'estimations |
| **[DDC Converter](https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto)** | `RvtExporter.exe` | Extrait les données BIM des modèles Revit vers Excel/JSON pour traitement |

---

## Démarrage Rapide des Workflows

### Étape 1 : Importer le Workflow

```
n8n → Nouveau workflow → Importer depuis un Fichier → Sélectionner JSON
```

### Étape 2 : Configurer les Identifiants

Dans le nœud **🔑 TOKEN**, définissez vos clés API :

```json
{
  "bot_token": "VOTRE_TOKEN_BOT_TELEGRAM",
  "OPENAI_API_KEY": "VOTRE_CLÉ_OPENAI",
  "GEMINI_API_KEY": "VOTRE_CLÉ_GEMINI",
  "QDRANT_URL": "http://localhost:6333",
  "QDRANT_API_KEY": ""
}
```

### Étape 3 : Charger DDC CWICR dans Qdrant

Téléchargez le snapshot depuis [Releases](#releases) et importez :

```bash
curl -X POST "http://localhost:6333/collections/ddc_cwicr_en/snapshots/upload" \
  -H "Content-Type: multipart/form-data" \
  -F "snapshot=@EN_TORONTO_workitems_EMBEDDINGS_3072_DDC.snapshot"
```

### Étape 4 : Activer & Tester

- Activez le workflow dans n8n
- Pour les bots Telegram : envoyez `/start` à votre bot
- Pour les formulaires web : ouvrez l'URL du formulaire fournie par n8n

---

## ⚠️ Configuration n8n 2.0+ Requise

> **À partir de la version 2.0 de n8n, le nœud Execute Command est désactivé par défaut pour des raisons de sécurité.**
>
> Sans la configuration ci-dessous, les workflows utilisant Execute Command (notamment le Pipeline CAO/BIM) **ne fonctionneront pas** — les nœuds s'afficheront avec un point d'interrogation ou ne seront pas reconnus.

### Correction Rapide

**Windows (CMD) — exécuter à chaque fois :**
```cmd
set NODES_EXCLUDE=[] && npx n8n
```

**Solution permanente — créer une fois :**

Créez le fichier `C:\Users\VOTRE_UTILISATEUR\.n8n\.env` avec :
```
NODES_EXCLUDE=[]
```
Puis lancez simplement `npx n8n` comme d'habitude.

**Docker :**
```yaml
environment:
  - NODES_EXCLUDE=[]
```

### Vérifier la Configuration

1. Démarrez n8n
2. Cliquez sur **+** → recherchez **"Execute Command"**
3. Si le nœud apparaît → ✅ vous êtes prêt !

> 📚 Plus de détails : [Changements Majeurs n8n 2.0](https://docs.n8n.io/2-0-breaking-changes/)

---

## 🌍 Langues Supportées & Niveaux de Prix

| Code  | Langue      | Niveau de Prix  | Devise | Collection Qdrant   |
|-------|-------------|-----------------|--------|---------------------|
| `AR`  | Arabe       | Dubaï           | AED    | `ddc_cwicr_ar`      |
| `DE`  | Allemand    | Berlin          | EUR    | `ddc_cwicr_de`      |
| `EN`  | Anglais     | Toronto         | CAD    | `ddc_cwicr_en`      |
| `ES`  | Espagnol    | Barcelone       | EUR    | `ddc_cwicr_es`      |
| `FR`  | Français    | Paris           | EUR    | `ddc_cwicr_fr`      |
| `HI`  | Hindi       | Mumbai          | INR    | `ddc_cwicr_hi`      |
| `PT`  | Portugais   | São Paulo       | BRL    | `ddc_cwicr_pt`      |
| `RU`  | Russe       | Saint-Pétersbourg | RUB  | `ddc_cwicr_ru`      |
| `ZH`  | Chinois     | Shanghai        | CNY    | `ddc_cwicr_zh`      |

---

## 📊 Étapes du Pipeline

Le workflow CAO/BIM traite les données en 10 étapes :

| Étape   | Nom                  | Description                                                       |
|---------|----------------------|-------------------------------------------------------------------|
| **0**   | Collecter Données BIM| Extraire les éléments de Revit via DDC Converter                  |
| **1**   | Détection du Projet  | L'IA identifie le type de projet (Résidentiel, Commercial, etc.)  |
| **2**   | Génération des Phases| L'IA crée les phases de construction                              |
| **3**   | Affectation des Éléments | L'IA mappe les types BIM aux phases                           |
| **4**   | Décomposition des Travaux | L'IA décompose les types en ouvrages ("Mur Brique" → maçonnerie, mortier) |
| **5**   | Recherche Vectorielle| Trouver les tarifs correspondants dans DDC CWICR via Qdrant       |
| **6**   | Correspondance des Unités | Convertir les unités BIM en unités de tarif                   |
| **7**   | Calcul des Coûts     | Qté × Prix Unitaire pour chaque ouvrage                           |
| **7.5** | Validation           | Revue CTO pour complétude et doublons                             |
| **8**   | Agrégation           | Somme par phases et catégories                                    |
| **9**   | Génération du Rapport| Créer les sorties HTML et Excel                                   |

---

## ⚙️ Sélection du Modèle LLM

Le workflow supporte plusieurs fournisseurs d'IA. Activez votre modèle préféré dans la section **Modèles LLM** :

| Modèle           | Nom du Nœud                  | Statut       |
|------------------|------------------------------|--------------|
| OpenAI GPT-4o    | `OpenAI LLM`                 | ✅ Par défaut |
| Claude Opus 4    | `Anthropic Chat Model2`      | Désactivé    |
| Gemini 2.5 Pro   | `Google Gemini Chat Model`   | Désactivé    |
| xAI Grok         | `xAI Grok Chat Model1`       | Désactivé    |
| DeepSeek         | `DeepSeek Chat Model`        | Désactivé    |

Pour changer de modèle : **Activez** le nœud de modèle souhaité et **Désactivez** les autres.

---

## 📁 Fichiers de Sortie

Les rapports sont sauvegardés dans le dossier du projet :
```
projet_AAAA-MM-JJ.html   ← Rapport interactif (s'ouvre dans le navigateur)
projet_AAAA-MM-JJ.xls    ← Tableur compatible Excel
```
<p align="center">
  <br>
  <img src="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto/blob/main/DDC_in_additon/DDC_readme_content/The%20generated%20report%20includes.jpg" width="100%"/>
  <br></br>
</p>

---

## 🔗 Collections Qdrant

Le workflow sélectionne automatiquement la collection correcte basée sur `language_code` :

```
{LANG}_{CITY}_workitems_costs_resources_EMBEDDINGS_3072_DDC_CWICR
```

Exemple : `DE_BERLIN_workitems_costs_resources_EMBEDDINGS_3072_DDC_CWICR`

---

## ⚠️ Dépannage

| Problème                     | Solution                                                    |
|------------------------------|-------------------------------------------------------------|
| "Execute Command manquant" (n8n 2.0+) | Définir la variable d'environnement `NODES_EXCLUDE=[]`. Voir [Configuration n8n 2.0+](#️-configuration-n8n-20-requise) |
| "Fichier Excel non trouvé"   | Vérifier les chemins `path_to_converter` et `project_file`  |
| "Connexion Qdrant échouée"   | Vérifier l'URL Qdrant et la clé API dans les identifiants   |
| "Limite de débit dépassée"   | Réduire la taille des lots ou ajouter des délais entre les appels API |
| "Tarif non trouvé"           | Vérifier si la collection de langue correcte existe dans Qdrant |
| "Erreur webhook Telegram"    | S'assurer que le workflow est actif et que l'URL webhook est accessible |
| "Échec API Vision"           | Vérifier que la clé API Gemini ou OpenAI Vision est valide  |

---

## Base de Données Vectorielle

Collections Qdrant prêtes à l'emploi avec embeddings OpenAI `text-embedding-3-large` pour la recherche sémantique parmi les ouvrages de construction.

Les bases de données vectorielles vous permettent de "parler" à vos données en langage naturel – en utilisant des phrases simples ou de courtes expressions au lieu de code ou de filtres complexes. Cela accélère considérablement la recherche du bon ouvrage ou de la ligne de coût, même dans de très grands ensembles de données.

Ces collections Qdrant peuvent être connectées à des applications via des workflows d'automatisation et d'intégration modernes (par exemple, des outils de Workflow et Pipeline low-code/no-code). Vous pouvez construire des assistants qui recherchent, filtrent et expliquent les ouvrages de construction, ou intégrer la recherche sémantique directement dans vos outils d'estimation et de contrôle de projet existants.

---

### Releases

Téléchargez les ensembles de données QDRANT et CSV (fichiers de plus de 1 gigaoctet) depuis [GitHub Releases](https://github.com/datadrivenconstruction/OpenConstructionEstimate-DDC-CWICR/releases).

| Langue          | Région         | Fichiers CSV          | Snapshot Qdrant                            |
|-----------------|----------------|-----------------------|--------------------------------------------|
| 🇸🇦 Arabe       | Dubaï          | `AR_DUBAI_*.csv`      | `AR_DUBAI_*_EMBEDDINGS_3072_DDC.snapshot`   |
| 🇨🇳 Chinois     | Shanghai       | `ZH_SHANGHAI_*.csv`   | `ZH_SHANGHAI_*_EMBEDDINGS_3072_DDC.snapshot`|
| 🇩🇪 Allemand    | Berlin         | `DE_BERLIN_*.csv`     | `DE_BERLIN_*_EMBEDDINGS_3072_DDC.snapshot`  |
| 🇬🇧 Anglais     | Toronto        | `EN_TORONTO_*.csv`    | `EN_TORONTO_*_EMBEDDINGS_3072_DDC.snapshot` |
| 🇪🇸 Espagnol    | Barcelone      | `ES_BARCELONA_*.csv`  | `ES_BARCELONA_*_EMBEDDINGS_3072_DDC.snapshot`|
| 🇫🇷 Français    | Paris          | `FR_PARIS_*.csv`      | `FR_PARIS_*_EMBEDDINGS_3072_DDC.snapshot`   |
| 🇮🇳 Hindi       | Mumbai         | `HI_MUMBAI_*.csv`     | `HI_MUMBAI_*_EMBEDDINGS_3072_DDC.snapshot`  |
| 🇧🇷 Portugais   | São Paulo      | `PT_SAOPAULO_*.csv`   | `PT_SAOPAULO_*_EMBEDDINGS_3072_DDC.snapshot`|
| 🇷🇺 Russe       | Saint-Pétersbourg | `RU_SPB_*.csv`     | `RU_SPB_*_EMBEDDINGS_3072_DDC.snapshot`     |

<a href="https://github.com/datadrivenconstruction/OpenConstructionEstimate-DDC-CWICR/releases/tag/v0.1.0">
  <img src="https://img.shields.io/badge/📥_Télécharger_v0.1.0-GitHub_Releases-181717?style=for-the-badge&logo=github" alt="Télécharger v0.1.0">
</a>

### Collections

🇸🇦 `ddc_cwicr_ar` (Arabe) · 🇨🇳 `ddc_cwicr_zh` (Chinois) · 🇩🇪 `ddc_cwicr_de` (Allemand) · 🇬🇧 `ddc_cwicr_en` (Anglais) · 🇪🇸 `ddc_cwicr_es` (Espagnol) · 🇫🇷 `ddc_cwicr_fr` (Français) · 🇮🇳 `ddc_cwicr_hi` (Hindi) · 🇧🇷 `ddc_cwicr_pt` (Portugais) · 🇷🇺 `ddc_cwicr_ru` (Russe)

Chaque collection contient **55 719 vecteurs** avec métadonnées complètes.

### Déploiement Docker

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
# Démarrer
docker-compose up -d

# Importer le snapshot
curl -X POST "http://localhost:6333/collections/ddc_cwicr_en/snapshots/upload" \
  -H "Content-Type: multipart/form-data" \
  -F "snapshot=@ddc_cwicr_en.snapshot"

# Tableau de bord : http://localhost:6333/dashboard
```
---

## Démarrage Rapide

### Python - Données Tabulaires

```python
import pandas as pd

# Parquet (recommandé)
df = pd.read_parquet("DDC_CWICR_EN.parquet")

# Excel
df = pd.read_excel("DDC_CWICR_EN.xlsx")

print(f"Enregistrements : {len(df):,} | Champs : {len(df.columns)}")
print(df[['rate_code', 'rate_original_name', 'rate_unit', 'total_cost_per_position']].head())
```

### Python - Recherche Sémantique

```python
from qdrant_client import QdrantClient
from openai import OpenAI

client = QdrantClient("localhost", port=6333)
openai = OpenAI()

# Recherche en langage naturel
query = "coulage de fondation en béton armé"
embedding = openai.embeddings.create(
    input=query,
    model="text-embedding-3-large"
).data[0].embedding

results = client.search(
    collection_name="ddc_cwicr_en",
    query_vector=embedding,
    limit=5
)

for r in results:
    print(f"[{r.score:.3f}] {r.payload['rate_code']}: {r.payload['rate_original_name']}")
```

### Recherche Filtrée

```python
from qdrant_client.models import Filter, FieldCondition, MatchValue, Range

# Par département
results = client.search(
    collection_name="ddc_cwicr_en",
    query_vector=embedding,
    query_filter=Filter(must=[
        FieldCondition(key="department_name", match=MatchValue(value="Concrete and Reinforced Concrete"))
    ]),
    limit=10
)

# Par plage de prix
results = client.search(
    collection_name="ddc_cwicr_en",
    query_vector=embedding,
    query_filter=Filter(must=[
        FieldCondition(key="price_est_median", range=Range(gte=1000, lte=50000))
    ]),
    limit=10
)
```


---

## Ressources & Communauté

[![Site Web](https://img.shields.io/badge/🌐_Site_Web-datadrivenconstruction.io-2563eb?style=for-the-badge)](https://datadrivenconstruction.io)
[![Démo](https://img.shields.io/badge/🎯_Démo-openconstructionestimate.com-059669?style=for-the-badge)](https://openconstructionestimate.com)
[![GitHub](https://img.shields.io/badge/💻_GitHub-datadrivenconstruction-181717?style=for-the-badge&logo=github)](https://github.com/datadrivenconstruction)
[![YouTube](https://img.shields.io/badge/📺_YouTube-@datadrivenconstruction-FF0000?style=for-the-badge&logo=youtube)](https://youtube.com/@datadrivenconstruction)
[![LinkedIn](https://img.shields.io/badge/💼_LinkedIn-datadrivenconstruction-0A66C2?style=for-the-badge&logo=linkedin)](https://linkedin.com/company/datadrivenconstruction)
[![Telegram](https://img.shields.io/badge/💬_Telegram-datadrivenconstruction-26A5E4?style=for-the-badge&logo=telegram)](https://t.me/datadrivenconstruction)

### Conseil & Formation

Nous travaillons avec des entreprises de construction, d'ingénierie, de conseil et de technologie leaders dans le monde entier pour les aider à mettre en œuvre les principes de données ouvertes, automatiser le traitement CAO/BIM et construire des pipelines ETL robustes. Nous soutenons activement les organisations recherchant des solutions pratiques pour la transformation numérique et l'interopérabilité, en nous concentrant sur la qualité des données et les défis de classification tout en favorisant l'adoption de workflows ouverts et automatisés.

Si vous souhaitez tester cette solution avec vos propres données ou si vous êtes intéressé par l'adaptation du workflow à des tâches de projet réelles, n'hésitez pas à nous contacter. Notre équipe propose des ateliers pratiques, fournit du conseil stratégique et développe des prototypes adaptés aux processus de projet réels.

<a href="mailto:info@datadrivenconstruction.io">
  <img src="https://img.shields.io/badge/📧_Contactez_Nous-info@datadrivenconstruction.io-2563eb?style=for-the-badge" alt="Contact">
</a>

### Contribuer

DDC CWICR est un projet gratuit et ouvert dédié à rendre l'industrie de la construction plus efficace, transparente et technologiquement avancée. Nous recherchons activement des enthousiastes partageant cette mission. Si vous créez des solutions utiles et êtes prêt à les partager avec la communauté, nous sommes là pour vous aider à être entendu.

Nous vous invitons à soumettre vos workflows, pipelines et intégrations open source basés sur DDC CWICR - des outils que tout le monde peut utiliser librement dans son travail. Les meilleures solutions seront publiées avec l'attribution complète de l'auteur sur GitHub et annoncées via notre newsletter et nos réseaux sociaux, atteignant des dizaines de milliers d'abonnés professionnels. Cela place votre nom directement devant une communauté internationale d'estimateurs, de spécialistes BIM et de chefs de projet.

Ensemble, nous changeons l'industrie. Vous pouvez envoyer votre solution à info@datadrivenconstruction.io avec le sujet "DDC Open Workflow" ou soumettre une Pull Request directement à nos dépôts GitHub.

Automatisez le traitement des données de construction avec des workflows n8n CAO-BIM prêts à l'emploi :

<a href="https://github.com/datadrivenconstruction/cad2data-Revit-IFC-DWG-DGN-pipeline-with-conversion-validation-qto">
  <img src="https://img.shields.io/badge/Pipeline_cad2data-GitHub-181717?style=for-the-badge&logo=github" alt="Pipeline cad2data">
</a>


## Licence

**Base de données** (DDC CWICR) - [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Libre d'utilisation, de partage et d'adaptation commerciale. Attribution : "DDC CWICR par DataDrivenConstruction"

**Code** (workflows, scripts) - [MIT](https://opensource.org/licenses/MIT). Libre d'utilisation, de modification et de distribution sans restrictions.

## Soutenir le Projet

Si vous trouvez cela utile, veuillez envisager de nous soutenir :

[![GitHub Sponsors](https://img.shields.io/badge/Sponsoriser_sur-GitHub-ea4aaa?style=for-the-badge&logo=github)](https://github.com/sponsors/datadrivenconstruction)
[![Buy Me A Coffee](https://img.shields.io/badge/Buy_Me_A_Coffee-ffdd00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/boikoartem)


<p align="left">
  <br/>
  <b>Libérez la Puissance des Données dans la Construction</b><br/>
  <sub>Passez à une gestion de données complète où seules les données et processus structurés et unifiés demeurent</sub>
</p>

<p align="left">
  <a href="https://datadrivenconstruction.io">
    <img src="https://datadrivenconstruction.io/wp-content/uploads/2023/07/DataDrivenConstruction-1-1.png.webp" alt="DataDrivenConstruction" width="180">
  </a>
</p>

<p align="left">
  <sub>© 2025 Artem Boiko · <a href="https://datadrivenconstruction.io">datadrivenconstruction.io</a></sub>
</p>
