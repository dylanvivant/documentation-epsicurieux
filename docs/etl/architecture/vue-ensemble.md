# Vue d'Ensemble de l'Architecture

## Structure générale

```mermaid
graph LR
    subgraph Sources
        A1[Country Wise Latest]
        A2[Covid Clean Complete]
        A3[Full Grouped]
        A4[USA County Wise]
        A5[Worldometer Data]
    end

    subgraph ETL Python
        B1[Extraction]
        B2[Transformation]
        B3[Loading]
        B1 --> B2
        B2 --> B3
    end

    subgraph Output
        C1[Données Nettoyées]
        D1[(PostgreSQL)]
    end

    A1 & A2 & A3 & A4 & A5 --> B1
    B3 --> C1
    C1 --> D1

    style Sources fill:#e6f3ff,stroke:#4d94ff
    style ETL Python fill:#f0fff0,stroke:#66b266
    style Output fill:#fff0f0,stroke:#ff8080
```

## Composants principaux

### 1. Sources de données

- Multiples fichiers CSV
- Données sur les cas COVID-19
- Informations démographiques
- Statistiques par pays

### 2. Processus ETL

- Scripts Python
- Notebooks Jupyter
- Bibliothèques de traitement de données

### 3. Stockage

- Fichiers CSV intermédiaires
- Base de données PostgreSQL

## Flux de données

### Extraction

- Lecture des fichiers sources
- Validation initiale des données

### Transformation

- Nettoyage
- Standardisation
- Agrégation

### Chargement

- Export CSV
- Insertion en base de données

[Next](choix-techniques.md)