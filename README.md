Pharmacy Analytics Lakehouse
============================

End-to-End Healthcare Inventory, Sales and Risk Analytics Platform
------------------------------------------------------------------

Project Overview
----------------

Pharmacies operate at the intersection of healthcare responsibility and business efficiency.Lack of proper analytics often leads to medicine stock-outs, expiry-related losses, and inefficient capital usage.

This project builds an end-to-end **Pharmacy Analytics Lakehouse** using Databricks to transform raw pharmacy inventory and sales data into governed analytics, dashboards, and machine learning insights.

The solution follows industry-standard **Medallion Architecture (Bronze, Silver, Gold)** and is fully compatible with **Databricks Community / Serverless compute**.

Problem Statement
-----------------

How can pharmacy transaction and inventory data be transformed into a governed analytics platform to:

*   Improve medicine availability
    
*   Reduce stock-out risks
    
*   Minimize expiry-related losses
    
*   Optimize category and product-level revenue
    

All without using any clinical or patient-sensitive data.

Domain Context
--------------

*   Industry: Retail Pharmacy and Healthcare Supply Chain
    
*   Data Type: Non-clinical transactional and inventory data
    
*   Compliance: No patient or medical records involved
    
*   Business Focus Areas:
    
    *   Inventory management
        
    *   Expiry risk monitoring
        
    *   Demand analysis
        
    *   Revenue optimization
        

This project is inspired by real-world pharmacy operations and a family-run pharmacy business context.

Data Description
----------------

Synthetic pharmacy data was generated to simulate real operational scenarios at scale.

### Data Attributes

*   Medicine brand name
    
*   Medicine combination (drug composition)
    
*   Manufacturing company
    
*   Therapeutic category (BP, Diabetes, Painkillers, etc.)
    
*   Manufacturing date
    
*   Expiry date
    
*   Batch number
    
*   Price including GST
    
*   Medicine form (tablet, syrup, injection, etc.)
    

### Data Scale

*   1,000,000 records
    
*   Generated using Python
    
*   Stored in Delta Lake format
    

Architecture Overview
---------------------

### Lakehouse Architecture

Raw pharmacy data is processed using a Lakehouse architecture:

Raw Data → Bronze Layer → Silver Layer → Gold Layer → Machine Learning → Dashboards

Medallion Layers
----------------

### Bronze Layer (Raw Ingestion)

*   Stores raw pharmacy data
    
*   Minimal transformations
    
*   Adds ingestion timestamp
    
*   Append-friendly and immutable
    

### Silver Layer (Cleaned and Enriched)

*   Data quality checks
    
*   Duplicate removal
    
*   Date normalization
    
*   Expiry risk flags
    
*   Business-ready cleaned dataset
    

### Gold Layer (Business Aggregates)

*   Category-level KPIs
    
*   Product-level metrics
    
*   Expiry risk summaries
    
*   Dashboard-ready analytical tables
    

Analytics and Dashboards
------------------------

An interactive Databricks dashboard was built on Gold tables to provide:

*   Category-wise inventory overview
    
*   Expiry risk percentage by category
    
*   Top medicines by stock presence
    
*   Price distribution across categories
    

### Dashboard Capabilities

*   Interactive filters (category, manufacturer)
    
*   SQL-based visualizations
    
*   Optimized for serverless compute
    

Machine Learning
----------------

### Objectives

*   Regression to predict stock risk score
    
*   Classification to identify high-risk inventory items
    

### Features Used

*   Stock count
    
*   Average price
    
*   Shelf life duration
    
*   Near-expiry indicators
    

### Models Implemented

*   Linear Regression
    
*   Logistic Regression
    

### Experiment Tracking

*   MLflow used for:
    
    *   Parameter logging
        
    *   Metric tracking
        
    *   Model comparison
        
    *   Model versioning
        

Performance Optimization
------------------------

Due to serverless compute constraints:

*   Explicit caching was avoided
    
*   Performance optimization achieved through:
    
    *   Table partitioning
        
    *   Query plan analysis
        
    *   Partition pruning
        
    *   Before and after benchmarking
        

This aligns with Databricks serverless best practices.

Project Structure
-----------------

.
+ pharmacy-analytics-lakehouse/
+ │   ├── 01_data_generation
+ │   ├── 02_bronze_raw_ingestion
+ │   ├── 03_silver_processing
+ │   ├── 04_gold_aggregations
+ │   ├── 05_sql_analytics_dashboards
+ │   ├── 06_machine_learning
+ │   └── 07_performance_optimization
+ ├── data/
+ ├── docs/
+ └── README.md



Pharmacy Analytics Lakehouse
============================

End-to-End Healthcare Inventory, Sales and Risk Analytics Platform
------------------------------------------------------------------

Project Overview
----------------

Pharmacies operate at the intersection of healthcare responsibility and business efficiency.Lack of proper analytics often leads to medicine stock-outs, expiry-related losses, and inefficient capital usage.

This project builds an end-to-end **Pharmacy Analytics Lakehouse** using Databricks to transform raw pharmacy inventory and sales data into governed analytics, dashboards, and machine learning insights.

The solution follows industry-standard **Medallion Architecture (Bronze, Silver, Gold)** and is fully compatible with **Databricks Community / Serverless compute**.

Problem Statement
-----------------

How can pharmacy transaction and inventory data be transformed into a governed analytics platform to:

*   Improve medicine availability
    
*   Reduce stock-out risks
    
*   Minimize expiry-related losses
    
*   Optimize category and product-level revenue
    

All without using any clinical or patient-sensitive data.

Domain Context
--------------

*   Industry: Retail Pharmacy and Healthcare Supply Chain
    
*   Data Type: Non-clinical transactional and inventory data
    
*   Compliance: No patient or medical records involved
    
*   Business Focus Areas:
    
    *   Inventory management
        
    *   Expiry risk monitoring
        
    *   Demand analysis
        
    *   Revenue optimization
        

This project is inspired by real-world pharmacy operations and a family-run pharmacy business context.

Data Description
----------------

Synthetic pharmacy data was generated to simulate real operational scenarios at scale.

### Data Attributes

*   Medicine brand name
    
*   Medicine combination (drug composition)
    
*   Manufacturing company
    
*   Therapeutic category (BP, Diabetes, Painkillers, etc.)
    
*   Manufacturing date
    
*   Expiry date
    
*   Batch number
    
*   Price including GST
    
*   Medicine form (tablet, syrup, injection, etc.)
    

### Data Scale

*   1,000,000 records
    
*   Generated using Python
    
*   Stored in Delta Lake format
    

Architecture Overview
---------------------

### Lakehouse Architecture

Raw pharmacy data is processed using a Lakehouse architecture:

Raw Data → Bronze Layer → Silver Layer → Gold Layer → Machine Learning → Dashboards

Medallion Layers
----------------

### Bronze Layer (Raw Ingestion)

*   Stores raw pharmacy data
    
*   Minimal transformations
    
*   Adds ingestion timestamp
    
*   Append-friendly and immutable
    

### Silver Layer (Cleaned and Enriched)

*   Data quality checks
    
*   Duplicate removal
    
*   Date normalization
    
*   Expiry risk flags
    
*   Business-ready cleaned dataset
    

### Gold Layer (Business Aggregates)

*   Category-level KPIs
    
*   Product-level metrics
    
*   Expiry risk summaries
    
*   Dashboard-ready analytical tables
    

Analytics and Dashboards
------------------------

An interactive Databricks dashboard was built on Gold tables to provide:

*   Category-wise inventory overview
    
*   Expiry risk percentage by category
    
*   Top medicines by stock presence
    
*   Price distribution across categories
    

### Dashboard Capabilities

*   Interactive filters (category, manufacturer)
    
*   SQL-based visualizations
    
*   Optimized for serverless compute
    

Machine Learning
----------------

### Objectives

*   Regression to predict stock risk score
    
*   Classification to identify high-risk inventory items
    

### Features Used

*   Stock count
    
*   Average price
    
*   Shelf life duration
    
*   Near-expiry indicators
    

### Models Implemented

*   Linear Regression
    
*   Logistic Regression
    

### Experiment Tracking

*   MLflow used for:
    
    *   Parameter logging
        
    *   Metric tracking
        
    *   Model comparison
        
    *   Model versioning
        

Performance Optimization
------------------------

Due to serverless compute constraints:

*   Explicit caching was avoided
    
*   Performance optimization achieved through:
    
    *   Table partitioning
        
    *   Query plan analysis
        
    *   Partition pruning
        
    *   Before and after benchmarking
        

This aligns with Databricks serverless best practices.

Project Structure
-----------------

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   pharmacy-analytics-lakehouse/  ├── notebooks/  │   ├── 01_data_generation  │   ├── 02_bronze_raw_ingestion  │   ├── 03_silver_processing  │   ├── 04_gold_aggregations  │   ├── 05_sql_analytics_dashboards  │   ├── 06_machine_learning  │   └── 07_performance_optimization  ├── data/  ├── docs/  └── README.md   `

Technologies Used
-----------------

### Languages

*   Python
    
*   SQL
    

### Platforms and Tools

*   Databricks (Community / Serverless)
    
*   Apache Spark
    
*   Delta Lake
    
*   Spark SQL
    
*   Spark ML
    
*   MLflow
    
*   Databricks Dashboards
    
*   GitHub
    

Business Impact
---------------

*   Improved visibility into pharmacy inventory
    
*   Early identification of expiry risks
    
*   Data-driven stock planning
    
*   Reduced wastage and improved capital efficiency
    
*   Scalable analytics foundation for healthcare use cases
    

Future Enhancements
-------------------

*   QR code–based batch traceability
    
*   Time-series sales forecasting
    
*   Supplier lead-time optimization
    
*   Real-time ingestion using streaming
    
*   POS system integration
    

Author
------

Guru Saran Satsangi PeddintiBS in Data Science and Applications, IIT MadrasFocus Areas: Data Engineering, Analytics, Healthcare AI
Technologies Used
-----------------

### Languages

*   Python
    
*   SQL
    

### Platforms and Tools

*   Databricks (Community / Serverless)
    
*   Apache Spark
    
*   Delta Lake
    
*   Spark SQL
    
*   Spark ML
    
*   MLflow
    
*   Databricks Dashboards
    
*   GitHub
    

Business Impact
---------------

*   Improved visibility into pharmacy inventory
    
*   Early identification of expiry risks
    
*   Data-driven stock planning
    
*   Reduced wastage and improved capital efficiency
    
*   Scalable analytics foundation for healthcare use cases
    

Future Enhancements
-------------------

*   QR code–based batch traceability
    
*   Time-series sales forecasting
    
*   Supplier lead-time optimization
    
*   Real-time ingestion using streaming
    
*   POS system integration
    

Author
------

Guru Saran Satsangi PeddintiBS in Data Science and Applications, IIT MadrasFocus Areas: Data Engineering, Analytics, Healthcare AI
