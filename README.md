# Dashboard Analytics - Ferme Verticale AVP

Plateforme analytics professionnelle pour l'analyse des marges, pertes, KPIs et prédictions de demande d'une ferme verticale de micropousses.

## Architecture

- **ETL**: Python/pandas pour le processing et l'algorithme de matching
- **API**: FastAPI avec documentation Swagger automatique  
- **Database**: PostgreSQL avec 3 schemas (staging, processed, analytics)
- **Frontend**: Streamlit + Plotly pour visualisations
- **Deployment**: Docker Compose

## Installation

1. Cloner le repository
2. Créer un environnement virtuel: `python -m venv venv`
3. Activer l'environnement: `source venv/bin/activate` (Linux/Mac) ou `venv\Scripts\activate` (Windows)
4. Installer les dépendances: `pip install -r requirements.txt`
5. Copier `.env.example` vers `.env` et configurer les variables d'environnement

## Utilisation

### Lancer l'API
```bash
uvicorn api.main:app --reload
```

### Lancer le dashboard
```bash
streamlit run dashboard/app.py
```

### Exécuter l'ETL
```bash
python -m etl.pipeline
```

## Tests

```bash
pytest tests/ -v --cov
```

## Licence

Projet personnel - Tous droits réservés
