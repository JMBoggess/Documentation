# Azure Data Factory: Mapping

## SQL Database Types

### Source
When SQL database is used, specify the physcialType to indicate the type of database field.
- Decimal
  - Scale: refers to the number of digits after the decimal place
  - Precision: the total number of digits

Example 1: DateTime
```
"source": {
    "name": "column_name",
    "physicalType": "datetime"
}
```

Example 2: String
```
"sink": {
    "name": "column_name",
    "physicalType": "varchar"
}
```

Example 3: Decimal
```
"sink": {
    "name": "column_name",
    "physicalType": "decimal",
    "scale": 2,
    "precision": 8
}
```
