# Azure Data Factory: Mapping

## SQL Database Types

### Source
When SQL database is used as a source

Example JSON:
```
"source": {
    "name": "column_name",
    "physicalType": "datetime",
    "scale": 3,
    "precision": 23
}
```

| Data Type | physicalType | scale | precision |
| --- | --- | --- |
| Date | date | n/a | n/a |
| DateTime | datetime | 3 | 23 |
| Decimal | decimal | # of decimal places | # of total digits |
| Int32 | int | n/a | 10 |
| Int64 | int | n/a | 19 | 
| String | varchar | n/a | n/a |

### Sink
When SQL database is used as a sink

Example JSON:
```
"sink": {
    "name": "column_name",
    "scale": 3,
    "precision": 10
}
```

| Data Type | scale | precision |
| --- | --- | --- |
| Date | n/a | n/a |
| DateTime | 3 | 23 |
| Double/Decimal | # of decimal places | # of total digits |
| Int32 | n/a | 10 |
| Int64 | n/a | 19 | 
| String | n/a | n/a |
