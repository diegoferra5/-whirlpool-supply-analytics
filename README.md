# Bloque Clase - Data Exploratory Analysis

## Overview
This project performs exploratory data analysis (DEA) on customer address, orders, and product data. It processes and analyzes 200K+ records from Excel files to uncover patterns and insights in customer information, order details, and product catalog.

## Project Structure
```
bloque_clase/
├── data/
│   ├── raw/              # Raw data files
│   │   ├── 200K_CustomerAddress.xlsx
│   │   ├── 200K_GeneralOrderDetail.xlsx
│   │   ├── 200K_IndividualCustomer.xlsx
│   │   ├── 200K_OrdersList.xlsx
│   │   ├── 200K_ProductOrderDetail.xlsx
│   │   └── Product_Catalog.xlsx
│   └── processed/                    # processed data files (ignored in git)
├── notebooks/
│   └── DEA.ipynb               # Main exploratory data analysis notebook
├── src/
│   ├── analysis.py             # Analysis functions
│   └── utils.py                # Utility functions
├── environment.yml             # Conda environment configuration
├── .gitignore                  # Git ignore file
└── README.md                   # This file
```

## Dataset Overview
- **customerAddress**: 221,470 records with 25 columns tracking customer location data
- **generalOrder**: Order detail information
- **individualCustomer**: Individual customer profiles
- **ordersList**: Complete orders list
- **productOrderDetail**: Product-level order details
- **productCatalog**: Product information

## Getting Started

### Prerequisites
- Python 3.11+
- Conda or Miniconda

### Installation
1. Clone the repository:
```bash
git clone <repository-url>
cd bloque_clase
```

2. Create the conda environment:
```bash
conda env create -f environment.yml
conda activate bloque_clase
```

3. Launch Jupyter Lab:
```bash
jupyter lab
```

## Usage
Open `notebooks/DEA.ipynb` to explore the data analysis.

## Key Findings
- Address dataset spans January 2021 to November 2022
- 1.93% missing neighborhood data
- 0.02% missing geographic coordinates
- Sparse update tracking (1.27% of records updated)

## Technologies
- Python 3.11
- Pandas
- Jupyter
- NumPy
- Matplotlib/Seaborn
- Openpyxl

## Author
Diego Ferra