# Car Fuel And Emission 2000-2023
## Table of contents
- [Project Overview](#project-overview)
- [Data Sourcing](#data-sourcing)
- [Tools](#tools)
- [Data CleaningPreparation](#data-cleaningpreparation)
- [Exploratory DataAnalysis](#exploratory-dataanalysis)
- [Data Analysis](#data-analysis)
### Project Overview 
This data analysis project aims to provide insights on Car fuel emmisions over the past years. By analyzing various aspect of the Car manufacturing data we 
seek to identify trends, make data driven recommendations and gain a deeper understanding of the car engine performance.

### Data Sourcing:
The primary dataset used for this analysis is the "Car Fuel Emission 2000-2023.cvs" file,containing detailed
information about company car model and its built features.

### Tools
-PYTHON LANGUAGE(VS CODE/JUPITER NOTEBOOK) /Data Cleaning processes,Data Analysis.

### Data CleaningPreparation
In the initial data prepration phase,we performed the following tasks
1. Data loading and inspection
2. Handling missing values
3. Data Cleaning and formatting

### Exploratory DataAnalysis
EDA involves exploring the Car features to answer key questions such as :
- WHat are the emission categories?
- What is the Cost per mile given fuel cost?
- Checking if the car meet up with the Europe Standard.
- Categorized the car into small,medium and large engine capacity.
- Different kinds of emmision overtime.
- Fuel efficiency,proportion of automatic cars,total Percentage emission.
- Categorized the car into Manual and Automatic
 ### Data Analysis
 Some interesting code features
 import warnings
warnings.filterwarnings("ignore")
category = df.select_dtypes(include=['object','category'])
numerical = df.select_dtypes(include=['int', 'float'])
for x in category:
    df[x].fillna(df[x].mode()[0], inplace=True)
for x in numerical:
    df[x].fillna(df[x].mean(), inplace=True)
import missingno as mns
mns.bar(df, sort='descending', color = 'blue')  
### Limitations
I had to remove all zero values from fuel cost price column because they would have affected the acuracy of my calculations from the analysis
