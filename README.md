# Data Retrieval from ChEMBL for Alzheimer's Targets

## Overview
This repository contains a Python script that extracts data from the ChEMBL database to retrieve molecular and activity information for Alzheimer’s disease targets. The script connects to a PostgreSQL database hosting ChEMBL data, retrieves relevant targets, and extracts chemical properties of drug molecules interacting with these targets.

## Features
- Retrieves ChEMBL IDs for specified Alzheimer’s disease targets
- Extracts molecular properties, activity values, and structural information
- Optimized SQL queries for efficient data retrieval
- Uses PostgreSQL with `psycopg2` for database connectivity
- Outputs data in a structured `pandas` DataFrame

## Dependencies
Ensure you have the following installed:
```bash
pip install psycopg2-binary pandas tqdm
```

## Installation
1. Clone this repository:
   ```bash
   git clone git@github.com:maghaeef/LLMs_for_Drug_Discovery.git
   cd LLMs_for_Drug_Discovery
   ```
2. Ensure you have access to a PostgreSQL database with ChEMBL data (e.g., ChEMBL_35).
3. Modify `database_connection_info.py` with your database credentials.

## Usage
Run the script to fetch data:
```bash
python DataRetrievalFromChEMBL.py
```
Alternatively, execute the Jupyter Notebook for step-by-step data retrieval and analysis.

## Data Retrieved
The script fetches:
- Target ChEMBL ID, target type, and organism
- Molecule ChEMBL ID and molecular structure (SMILES, InChI, etc.)
- Activity type and standard values
- Chemical properties (Molecular weight, AlogP, HBA, HBD, PSA, etc.)

## Output
The retrieved data is stored in a `pandas` DataFrame and can be exported as:
```python
df.to_csv("retrieved_data.csv", index=False)
```

## License
This project is licensed under the MIT License.

## Contact
For questions, reach out at your_email@example.com.
