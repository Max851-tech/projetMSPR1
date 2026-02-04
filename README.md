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
