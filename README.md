# 🚨 Criminal Data

This project processes, cleans, and analyzes the occurrence records ("Ocorrências") from
October 2021 to August 2026, made publicly available by the Public Security Secretariat
of Rio Grande do Sul (SSP/RS), Brazil. This repository provides a reproducible pipeline
for a comprehensive Exploratory Data Analysis (EDA).

# ✨ Main Features

- **Automated Cleaning**: Parses and unifies multiple yearly CSVs into a single dataset.
- **Memory Optimization**: Drops memory footprint by >80% using optimal pandas
  datatypes.
- **Robust Parsing**: Handles malformed rows, corrects typos, and sanitizes categories.
- **Parquet Export**: Persists the clean dataset as a highly compressed `.parquet` file.

# ✅ Prerequisites

- Python 3.12+ installed on your machine
- Dependency manager `uv` (optional)

# ⚙️ Local Installation

```bash
# Clone the repository
git clone https://github.com/germanocastanho/criminal-data
cd criminal-data/

# Create a venv (optional)
uv venv .venv
source .venv/bin/activate

# Install dependencies
uv pip install -r requirements.txt
```

# 🚀 Getting Started

### `01_clean.ipynb`

Handles data ingestion, type conversions, schema unification, handling of duplicate
records and missing values, and exports the final dataset to `data/clean.parquet`. To
run it, you'll need the raw CSVs from the SSP/RS open data portal placed inside the
`data/` directory.

### `02_eda.ipynb` (Coming Soon)

Will contain the Exploratory Data Analysis (EDA), extracting insights about the types,
locations, and demographics of criminal occurrences in RS.

# 📜 Libre Software

If you have ideas for improvements or new features, please open an issue or submit a
pull request. Make sure to follow the existing code style and include tests for any new
functionality. Licensed under the GNU GPL v3, so you are free to use, modify, and
distribute this software. Please refer to the [LICENSE](LICENSE) for more!
