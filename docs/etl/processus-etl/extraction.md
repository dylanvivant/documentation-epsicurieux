# Processus d'Extraction

## Sources de données

Le processus d'extraction gère plusieurs fichiers CSV contenant des données COVID-19 :

```python
csv_files = [
    'country_wise_latest.csv',
    'covid_19_clean_complete.csv',
    'full_grouped.csv',
    'usa_county_wise.csv',
    'worldometer_coronavirus_daily_data.csv',
    'worldometer_coronavirus_summary_data.csv',
    'worldometer_data.csv'
] 
```

## Méthode d'extraction

### Chargement initial

``` python
def load_csv_files(file_list):
    dataframes = {}
    for file in file_list:
        df_name = file.replace('.csv', '')
        dataframes[df_name] = pd.read_csv(file)
    return dataframes
```

### Validation des données

- Vérification des colonnes requises
- Contrôle des types de données
- Détection des valeurs manquantes

### Gestion des erreurs

- Validation des fichiers sources
- Gestion des encodages
- Traitement des données manquantes

[Next](transformation.md)