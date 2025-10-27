# Data Analysis - RIWI Sport

## Description
Analysis of customer behavior and sales for RIWI Sport, a sports retail store in Colombia. This project fulfills the requirements of the Data Analytics Performance Test.

## Prerequisites
- PostgreSQL installed and running
- Python 3.8 or higher
- `RiwiSport.sql` file restored in PostgreSQL

## Installation and Configuration

### 1. Restore the Database
```bash
psql -U your_username -d RiwiSport -f RiwiSport.sql
```

### 2. Install Python Dependencies
```bash
pip install -r requirements.txt
```

### 3. Configure Environment Variables
- Copy the `.env.example` file to `.env`
- Edit the `.env` file with your credentials:

```env
DB_HOST=localhost
DB_PORT=5432
DB_NAME=RiwiSport
DB_USER=your_postgres_user
DB_PASSWORD=your_postgres_password
```

### 4. Run the Analysis
```bash
jupyter notebook analisis_RIWI_Sport.ipynb
```

## Project Structure

```
proyecto_riwisport/
├── analisis_RIWI_Sport.ipynb      # Main notebook with complete analysis
├── analysis_RIWI_Sport.ipynb      # Main notebook with complete analysis (English)
├── requirements.txt               # Python dependencies
├── .env                           # Database configuration (do not share)
├── README.md                      # This file (Spanish)
├── README_En.md                   # This file (English)
├── informe_RIWI_Sport.md          # Executive summary of the analysis (Spanish)
└── En_informe_RIWI_Sport.md       # Executive summary of the analysis (English)
```

## Main Dependencies

- **pandas, numpy** - Data analysis and manipulation
- **sqlalchemy, psycopg2-binary** - PostgreSQL connection
- **matplotlib, seaborn** - Visualizations and charts
- **python-dotenv** - Environment variables management

## Implemented Features

### ✅ Database Connection
- Secure connection to PostgreSQL using SQLAlchemy
- Successful connection verification

### ✅ SQL Queries
- Queries to tables: customer, order, order_item, product, category
- Data integration into a unified sales table

### ✅ Pandas/NumPy Analysis
- **Central tendency:** Mean, median, mode of spending
- **Dispersion:** Variance, standard deviation
- **Business KPIs:** Average ticket, top categories, top products

### ✅ Visualizations
- Histogram of customer spending
- Boxplot of sales by category
- Bar charts for top categories and products

### ✅ Actionable Insights
- Analysis of commercial opportunities
- Specific recommendations for RIWI Sport

## Troubleshooting

### Database Connection Error
- Verify that PostgreSQL is running
- Confirm credentials in the `.env` file
- Ensure the `RiwiSport` database exists

### Dependencies Not Found
```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### Issues with Jupyter
```bash
pip install jupyter
jupyter notebook
```