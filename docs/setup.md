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

## Accès aux services après docker compose up -d

- **PostgreSQL** :  
  Host : localhost  
  Port : 5432  
  User : ${POSTGRES_USER} (ex. healthai)  
  Password : ${POSTGRES_PASSWORD} (ex. secret123)  
  DB : ${POSTGRES_DB} (ex. mspr_fitness)

- **Metabase (Dashboard)** :  
  URL : http://localhost:3000  
  Premier login :  
  - Email : ${MB_ADMIN_EMAIL} (ex. admin@healthai.coach)  
  - Password : ${MB_ADMIN_PASSWORD} (ex. admin123)  
  Une fois connecté, ajoute la datasource PostgreSQL (host=postgres, port=5432, user/password comme ci-dessus).

- **API placeholder** : http://localhost:8000/docs (Swagger) – à remplacer par la vraie FastAPI quand Hichem l’aura implémentée.

- **ETL placeholder** :  
  Lance manuellement pour test :  
  docker compose run --rm etl  
  → Tu devrais voir "ETL placeholder ready - [date]"


Arrêt
docker-compose down
