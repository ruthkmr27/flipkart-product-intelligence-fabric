# Flipkart Product Intelligence Platform
## Microsoft Fabric + PySpark + Google Gemini AI + Power BI

## Project Overview
End-to-end data pipeline built on Microsoft Fabric using 
Medallion Architecture to analyse 20,000+ Flipkart product 
listings. Google Gemini AI enriches each product with quality 
scores, target customer classification, and key feature 
extraction.

## Architecture
![Architecture](architecture/medallion_architecture.png)

Bronze → Silver → Gold → Power BI

## Tech Stack
| Tool | Purpose |
|------|---------|
| Microsoft Fabric Lakehouse | Storage and compute |
| PySpark | Data transformation |
| Delta Lake | ACID-compliant storage |
| Google Gemini AI API | Product intelligence |
| Power BI | Dashboard and reporting |

## Pipeline Stages

### Bronze Layer
- Raw ingestion of 20,000+ Flipkart products
- CSV landed as-is — zero transformations
- Schema preserved exactly as received

### Silver Layer
- Column standardisation and data type fixing
- Price cleaning and validation
- Calculated columns: discount_amount, discount_percentage
- Price categorisation: Budget/Mid-Range/Premium/Luxury
- Category extraction from category tree
- Data quality: removed invalid prices and missing products

### Gold Layer (AI-Enriched)
- Google Gemini AI analyses each product description
- AI outputs per product:
  - Quality Score (1-10)
  - Key Features (3 words)
  - Target Customer (Kids/Men/Women/Unisex/Home/Professional)
  - Description Quality (Excellent/Good/Poor)
- 4 aggregated summary tables for Power BI

## Power BI Dashboard
![Dashboard](screenshots/powerbi_dashboard.png)

## Key Findings
- Most products fall in the Mid-Range price category
- [Add your finding after running]
- [Add your finding after running]

## Certifications Demonstrated
- DP-700: Microsoft Fabric Data Engineer Associate
- AI-901: Azure AI Fundamentals  
- Databricks Certified Data Engineer Associate (in progress)

## Author
Ruth Deepti Kumar — Senior Azure Data Engineer

