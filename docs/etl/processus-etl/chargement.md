# Processus de Chargement

## Export des données

### Format CSV
```python
# Export du DataFrame final
final_df.to_csv('merged_data.csv', index=False)
```

### Structure final 

| Colonne   | Type  | Description  |
|-----------|-----------|-----------|
| Country   | text  | Nom du pays  |
| Date   | date  | Date de l'observation  |
| Population   | integer  | Population totale  |
| Cases   | integer  | Nombre total de cas  |
| Active   | integer  | Cas actifs  |
| Recovered   | integer  | Nombre de guérisons  |
| Deaths   | integer  | Nombre de décès  |

### Chargement PostgreSQL

- Création des tables
- Import des données
- Vérification de l'intégrité

### Validation du chargement

- Contrôle des volumes
- Vérification des contraintes
- Tests de cohérence

[Next](../4-points-forts.md)