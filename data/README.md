# Data Folder

This folder contains synthetic datasets used for the Microsoft Fabric POC.

## Structure
- bronze/  : Raw source-aligned datasets (as received)
- silver/  : Cleansed and conformed datasets
- gold/    : Curated dimensional and fact tables for analytics

## Notes
- All data is synthetic and anonymized
- Data volumes are intentionally small (POC-scale)
- Structure mirrors OneLake / Lakehouse medallion architecture
