# Guide d'installation et de lancement local

## Prérequis
- Docker & Docker Compose
- Git

## Étapes
1. Clone le repo
   ```bash
   git clone https://github.com/Max851-tech/projetMSP1.git
   cd projetMSP1


 2. Copie les variables d'environnementBash
    cp .env.example .env

3. Lance l'environnement
   docker-compose up -d

4. Accès :
PostgreSQL : localhost:5432
Metabase : http://localhost:3000
API (placeholder) : http://localhost:8000/docs


Arrêt
docker-compose down
