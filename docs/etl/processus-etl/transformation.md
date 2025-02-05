# Processus de Transformation

## Étapes de transformation

### 1. Standardisation des noms
```python
def standardize_country_names(df):
    country_mapping = {
        'USA': 'United States',
        'UK': 'United Kingdom',
        # etc.
    }
    if 'Country' in df.columns:
        df['Country'] = df['Country'].replace(country_mapping)
    return df
```

### 2. Nettoyage des données

- Remplacement des valeurs manquantes
- Suppression des doublons
- Correction des formats de date

### 3. Agrégation des données.

- Regroupement par pays
- Calculs des totaux mensuels
- Standardisation des métriques

## Normalisation

### Structure finale des données

- Country (pays)
- Date
- Population
- Cases (cas)
- Active (cas actifs)
- Recovered (guérisons)
- Deaths (décès)

### Validation

- Contrôle des données transformées
- Vérification de la cohérence
- Tests de qualité des données

[Next](chargement.md)