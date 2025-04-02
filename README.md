# EU Clothing Exports Analysis: A Data Warehousing & Analytics Journey

## Project Overview

This project involves building a small data warehouse and performing exploratory data analysis (EDA) on Eurostat data concerning monthly clothing exports (HS Codes 6101, 6102, 6103 and related 6-digit codes) from selected EU countries (NL, DE, AT, FR, BE) to Russia, Belarus, and Kazakhstan. The analysis covers the period from January 2002 up to the latest available data (targeting up to 2025).

The primary goal is to practice and demonstrate skills in T-SQL, data warehousing concepts (ETL/ELT, Star Schema), data modeling, data cleaning, data profiling, and exploratory data analysis using SQL Server.

## Table of Contents

*   [Project Goals](#project-goals)
*   [Data Source](#data-source)
*   [Technologies Used](#technologies-used)
*   [Setup and Installation](#setup-and-installation)
*   [Workflow / How to Run](#workflow--how-to-run)
*   [Data Model](#data-model)
*   [Data Profiling Highlights](#data-profiling-highlights)
*   [ETL/ELT Process](#etlelt-process)
*   [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
*   [Key Findings](#key-findings)
*   [Challenges and Learnings](#challenges-and-learnings)
*   [Future Work](#future-work)
*   [License](#license)
*   [Author](#author)

## Project Goals

*   Learn and apply ETL/ELT processes using T-SQL.
*   Design and implement a simple Star Schema data warehouse.
*   Practice data cleaning and transformation techniques.
*   Understand and perform data profiling.
*   Conduct Exploratory Data Analysis (EDA) using T-SQL queries.
*   Gain proficiency in T-SQL for data manipulation and analysis.
*   Document the entire process clearly on GitHub.
*   (For the future) Visualize findings using a BI tool like Power BI.

## Data Source

*   **Provider:** Eurostat (Comext Database)
*   **Dataset:** International Trade in Goods Statistics
*   **Parameters:**
    *   **Reporters:** Netherlands (NL), Germany (DE), Austria (AT), France (FR), Belgium (BE)
    *   **Partners:** Russia (RU), Belarus (BY), Kazakhstan (KZ)
    *   **Products (HS Codes):** 6101, 6102, 6103, and associated 6-digit codes within these chapters.
    *   **Flow:** Exports (Code: 2)
    *   **Indicators:** Value in Euro (VALUE_EUR), Quantity in Kilograms (QUANTITY_KG)
    *   **Time Period:** Monthly data from 2002-01 to 2025-1
*   **Format:** CSV (Comma Separated Values)
*   **Raw File Location:** `/data/estat_ds-059341_filtered_en (1)` to `/data/estat_ds-059341_filtered_en (6)`
*   **Data Structure (Raw):**
    ```
    LAST UPDATE,freq,reporter,partner,product,flow,indicators,TIME_PERIOD,OBS_VALUE
    ```

## Technologies Used

*   **Database:** SQL Server
*   **Query Language:** T-SQL (Transact-SQL)
*   **IDE:** SQL Server Management Studio (SSMS), VSCode
*   **Version Control:** Git & GitHub
*   **Visualization:** TBD

## Setup and Installation

1.  **Clone Repository:**
    ```bash
    cd [YourPath]
    git clone https://github.com/bogachev-ei/Eurostat-clothing-export-project
    ```
2.  **Prerequisites:**
    *   Install [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-downloads) (Express Edition is sufficient). During installation, ensure you configure it for SQL Server Authentication or Windows Authentication as needed.
    *   Install [SQL Server Management Studio (SSMS)](https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms).
3.  **Database Setup:**
    *   Connect to your SQL Server instance using SSMS.
    *   Create the staging and data warehouse databases. You can use the scripts in `/sql_scripts/00_setup/` or run these basic commands in SSMS:
        ```sql
        CREATE DATABASE EurostatExports_Staging;
        GO
        CREATE DATABASE EurostatExports_DW;
        GO
        ```
4.  **Prepare Data File:**
    *   Ensure the downloaded CSV data files (`/data/estat_ds-059341_filtered_en (1)` to `/data/estat_ds-059341_filtered_en (6)`) are placed in the `/data/` directory.
    *   **Important:** Update the file path within the staging load script (`/sql_scripts/01_staging/load_staging_table.sql`) to point to the correct location of your CSV file on your machine where SQL Server can access it (e.g., `C:\path\to\your\repo\data\/data/estat_ds-059341_filtered_en (1)`).

## Workflow / How to Run



## Data Model



## Data Profiling Highlights



## ETL/ELT Process



## Exploratory Data Analysis (EDA)



## Key Findings



## Challenges and Learnings



## Future Work



## License


## Author

*   **Name:** `Egor`
*   **GitHub:** 
*   **LinkedIn:** 