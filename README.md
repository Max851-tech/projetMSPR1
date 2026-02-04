# projetMSPR1

# HealthAI Coach - MSPR Bloc 1 (2025-2026)

**Développement et déploiement d'une application dans le respect du cahier des charges Client**  
**Création d'un backend métier permettant le nettoyage et la visualisation des données**

Projet réalisé dans le cadre du **Bloc E6.1** : Créer un modèle de données d'une solution IA en utilisant des méthodes de Data Science  
Certification RNCP36581 – Concepteur Développeur d'Applications / Développeur en Intelligence Artificielle et Data Science

## Contexte du projet
HealthAI Coach est une plateforme de coaching santé personnalisé (nutrition, sport, sommeil, bien-être) utilisant l'IA pour des recommandations et un suivi holistique.  
Le backend centralise des données hétérogènes (open data Kaggle), les nettoie, les stocke en base relationnelle, les expose via API REST et les visualise via dashboard accessible.

**Compétences évaluées** (Bloc E6.1) :
- Collecte sécurisée depuis sources hétérogènes (open data, APIs simulées)
- Nettoyage, validation et qualité des données (Data Science)
- Modélisation et stockage relationnel (MCD / MLD / MPD)
- Visualisation interactive accessible (RGAA)
- Automatisation (ETL, requêtage, déploiement)

## Équipe
- **Maxime** (Tech Lead / DevOps)  
- Hichem (Backend API)  
- Aedh (Data Engineer / ETL)  
- Zeinab (Frontend Admin)  
- Christiana (BI / Data Analyst + QA)

## Stack technique
- **Backend** : FastAPI (Python)  
- **Base de données** : PostgreSQL  
- **ETL** : Python + Pandas (nettoyage, validation, logs)  
- **Dashboard** : Metabase / Superset  
- **Conteneurisation** : Docker + Docker Compose  
- **CI** : GitHub Actions (lint, tests)  
- **Sécurité** : JWT, CORS, rate limiting

## Structure du projet

```text
projetMSP1/
├── docs/                              # Documentation & livrables
│   ├── models/                        # Modèle Merise
│   │   ├── mcd.png                    # Diagramme MCD (Eraser.io)
│   │   ├── mld.png                    # Diagramme MLD
│   │   ├── mpd.sql                    # Script SQL physique (MPD)
│   │   └── data-dictionary.md         # Dictionnaire de données (tables/colonnes/description/contraintes)
│   └── architecture/                  # Diagrammes d'architecture
│       └── architecture-flux.png      # Diagramme flux global
├── data/                              # Datasets bruts et intermédiaires (nouveau dossier !)
│   ├── raw/                           # Datasets téléchargés de Kaggle (non versionnés)
│   │   ├── gym_members_exercise.csv
│   │   ├── daily_food_nutrition.csv
│   │   ├── sleep_health_lifestyle.csv
│   │   └── fitness_exercises.csv
│   └── processed/                     # Données nettoyées/exportées par l'ETL
├── backend/                           # Couche API (FastAPI)
│   └── app/                           # Application principale
│       ├── main.py                    # Point d'entrée FastAPI
│       └── ...                        # routes, models, services, etc.
├── etl/                               # Couche ETL (Data Engineer)
│   ├── ingest.py                      # Scripts ingestion, nettoyage, validation
│   └── quality_report.py              # Génération rapports qualité ETL
├── dashboard/                         # Couche visualisation
│   └── metabase-config/               # Configuration Metabase/Superset (dashboards)
├── migrations/                        # Alembic (si migrations DB utilisées)
├── .github/
│   └── workflows/                     # CI/CD GitHub Actions
│       └── lint.yml                   # CI basique (lint + tests)
├── docker-compose.yml                 # Environnement Docker complet
├── .env.example                       # Variables d'environnement exemple
├── README.md                          # Cette page
└── .gitignore                         # Fichiers à ignorer


## Installation et lancement local (avec Docker)
Prérequis : Docker & Docker Compose installés.

1. Clone le repo
   ```bash
   git clone https://github.com/Max851-tech/projetMSP1.git
   cd projetMSP1
