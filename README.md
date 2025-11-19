# capstone-data-analytics
Final Capstone Projects for Data Analytics Course

PROJECT OVERVIEW: ECONOMIC IMPACT IN MARICOPA COUNTY
This repository contains two interconnected projects examining economic and business development factors within Maricopa County, Arizona, at the ZIP code level. The primary focus is understanding the economic effects of major transit infrastructure (specifically the Phoenix Light Rail) and underlying business density trends.

# PROJECT FOCUS AREAS
## Phoenix Light Rail Study:

### Goal: 
Examines the effect of the Phoenix Light Rail on housing and business density and sector change.

### Methodology: 
Difference-in-Differences (DiD) regression.

#### Note: 
This project is noted for having limitations in its current modeling and data preparation, particularly concerning the definition of control and treatment areas.

## Business Density Analysis:

### Goal: 
Investigates whether business density is primarily driven by historical trends or if current economic conditions play a more significant role.

### Purpose: 
This serves as a foundational analysis to better understand the variables used in the first study.

## REPRODUCTION GUIDE: RECREATING THE ANALYSIS
### Data preparation
The data preparation for these projects was executed using PySpark within the Google Colab environment. To reproduce the final master dataset and run the analysis, follow the steps below in the specified order.

NOTE: Ensure you have access to a PySpark environment (such as Google Colab or a local setup) to run the data preparation scripts.

STEP 1: PREPARE COUNTRY BUSINESS PATTERNS (CBP) DATA
This step combines granular business data into a usable format.

Navigate to the 'master_dataset/CBP_Data_Final' folder.

Access the input data located in the 'CBP_idn_Details' folder and the 'geonames postal code data file'.

Run the appropriate script (.py or .IPYNB) within this folder. This script combines the CBP data with the geonames postal code information.

STEP 2: PREPARE ZILLOW HOUSING DATA
This step cleans and combines raw housing data from multiple sources.

Go to the 'Housing_Data' folder.

Run the first script to clean and pivot the raw Zillow housing data.

Run the second script to combine the cleaned Zillow data with the Housing Index data.

STEP 3: CLEAN LIGHT RAIL DATA
This step processes the light rail station data and proximity features.

Navigate to the 'Light_Rail_Data' folder.

Run the script in this folder to clean and prepare the light rail data.

Output Note: This script produces two intermediate files, but only one, 'houseDataComplete', is needed for the final master dataset creation.

STEP 4: CREATE THE FINAL MASTER DATASET
This final step combines all prepared data sources into the primary analytical dataset.

Go to the main 'master_dataset' folder.

Run the script located here to combine the outputs from the previous steps.

Input Files: Before running the final script, ensure the following processed files are accessible in the environment:

combined_CDPDara_2000-23 (from Step 1)

houseDataComplete (from Step 3)

zip_rail_Proximity_Features (from Step 3)

USA_Zip_Codes

The final analytical dataset, named 'Final_lightRail_dataset', can be found in the 'projects' folder and is used for the regression analysis.

### Phoenix Light Rail Study:
### Business Density Analysis:
