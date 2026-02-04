# Security Policy

## Reporting a Vulnerability
Si vous découvrez une vulnérabilité de sécurité dans ce projet, merci de l'envoyer par email à [ton email ou celui du groupe].

## Security Measures
- Utilisation de variables d'environnement (.env)
- Secrets jamais commités (exclus via .gitignore)
- JWT pour l'authentification API
- CORS configuré
- Rate limiting sur les endpoints
- Logs structurés et niveaux d'erreur

## Docker Security
- Images officielles (postgres, metabase, etc.)
- Pas de root user par défaut
