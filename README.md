# Data Project
Data Analysis on Duke University Wetland Center Duke Gardens 2019

## Summary
Water Quality Data is sourced from the Duke University Wetland Center, 2019. Data was collected as part of the long term analysis of water quality being contributed from Duke Univeristy's central campus to Sandy Creek and down to the Cape Fear River. Additional water quality data is being collected in the Duke Forest as part of a long term analysis on wetland and stream restoration sites.

Precipitation Data was sourced from NOAA.This dataset includes daily precipitation for one station, "Durham 1.2 NW, NC US" from January 1, 2019 to December 31, 2019. This is part of a large database within NOAA of past weather pattern data.  <https://www.ncdc.noaa.gov/cdo-web/datasets>

I am curious of the water quality over the months of 2019. I will analyze the general trends in parameters of particular interest, as well as relationships between fecal coliform and oxygen concentration, and precipitation levels and concentrations of nutrients (TN and TP). Looking into a potential relationship between fecal coliform and oxygen concentration goes into the deeper biogeochemistry of the ponds. Duck Pond has access water foul visiting and living pondside. This analysis may allude to their impact on the water quality of the pond. Precipitation and nutriet concentrations are a relevant research question because of the geographic location of the ponds. The ponds, are down slope from a large parking lot used for the hospital. If precipitation causes runoff, and specifically runoff of these nutrients, Upper Pond is the first to recieve it. The water then runs down to Duck Pond, and South Pond before exiting Duke Gardens. 

Analysis of trends of main parameters like phosphorus, nitrogen, and fecal coliform are analyzed over time to see general trends between the ponds. Line plots are used to show these trends between the ponds. Plots comparing fecal coliform and oxygen concentration are constructed to see if there is a relevant relationship. Statistical anaylsis are also performed. Statistical analysis is also performed on precipitation and total phosphorus. These relationships are plotted over the year of 2019 with monthly data points.


## Database Information
The qater quality data was collected, processed, and compiled by the Duke University Wetland Center. It contains data from 3 ponds in Duke Gardens: South, Upper, and Duke Pond, Durham, NC, over the year 2019. Certain water quality parameters are reported from the use of a YSI instrument, while others are from grab samples processed in a lab under various protocols. 

Precipitation data is stored by NOAA under the National Center for Environmental Information's Climate Data Online platform. "Data Summaries" was chosen as the dataset as it provides daily precipitation levels at a gage station the nearest to Duke Gardens. This station's identification name is "Durham 1.2 NW, NC US." Because the Duke Gardens water quality data is sampled monthly in 2019, precipitation data was obtained for the 2019 year, following the data range of January 1, 2019 to December 31, 2019. Data from this source is downloaded as a .csv file.


## Investigators
**Duke University Wetland Center**

*Curt Richardson, Director

*Neal Flanagan, Assistant Director

*Belen De La Berrera, Lab Administrator, Main Data Source Contact, belen.de.la.barrera@duke.edu

*Bryan Stokes Cawley, Lab Assistant

*Autumn Dunn, Lab Graduate Assistant

*Kathleen Mason, Lab Graduate Assistant, Main Data Analysis Contact, kathleen.f.mason@duke.edu


**NOAA National Center for Environmental Information**

Climate Data Online (CDO)




## Keywords
Duke University, Duke Gardens, water quality, water testing, watershed restoration, reducing nutrients, nutrient pollution, water supply, monitoring, management, data summary, precipitation, runoff, nutrient runoff, biogeochemistry


## Folder Structure, File Formats, and Naming Conventions 
**Folder Structure:**
*Code-R markdown code for data wrangling, data exploration/analysis, and data visualization

*Output-This contains any .pdf documents of maps, as well as .jpg or .png exported files of graphs.

*Processed-Exported .csv files of wrangled datasets, so particular formatted datasets can be accessed again or shared.

*Raw- Original .xlsx sheets of the data, which are also saved as .csv files for use in R.There is one .xlsx and .csv for each of the three ponds.



**Naming Convention:**

Files are named according to the following naming convention: `databasename_datatype_details_stage.format`, where: 

**databasename** refers to the database from where the data originated, all files in this folder include DG2019, or Duke Gardens 2019

**datatype** is a description of data 

**details** are additional descriptive details, particularly important for processed data or outputs

**stage**refers to the stage in data management pipelines (raw, wrangled, or processed)

**format** is a non-proprietary file format (.csv, .txt, .pdf, .png, .jpg, .xlsx)


## Metadata
Description of the data contained in each of the below data sets.


**Water Quality Data**
*DG2019_UpperPond_raw.csv

*DG2019_SouthPond_raw.csv

*DG2019_DuckPond_raw.csv


Column name | Data Description | Class | Associated Units
--------|-----|--------|-------
Month | name of the month the data was collected in | character
Rep | the number of the replicate sample those data belong to | character
FOP| orthophosphorus concentration | numeric | µg/L
TP| total phosphorus concentrations | numeric | µg/L
NOx | total nitrates | numeric | µg/L
NHx | total ammonium | numeric | µg/L
TN | total nitrogen | numeric | µg/L
TSS | total suspended solids | numeric | mg/L
Fecal Coliform | total concentration of the bacteria fecal coliform | numeric | CFU/100mL
T | temperature | numeric | degrees Celcius
Oxygen Saturdation | total oxygen saturation | numeric | %
Oxygen Concentration | total oxygen concentration | numeric | mg/L
Specific Conductivity | how well water can conduct an electric current | numeric | uS/cm
Electrical Conductivity|   | numeric | uS/cm
Dissolved Solid TDS | total dissolved solids within the water | numeric | mg/L
Salinity | a measure of the contents of salts | numeric | %
pH | a measure of how acidic or basic the water is| numeric |


**Precipitation Data**

*NCEI_DurhamRainStation_raw.csv


Column name | Data Description | Class | Associated Units
--------|-----|--------|-------
Station | ID number of the precipitation gage | factor | 
Name | Name of the precipitation gage station |factor |
Date | Month, day, year the data was recorded |Date |
PRCP| Daily precipitation data | numeric | milimeters



## Scripts and Code
**DataWrangling.Rmd**

This includes the steps required to create a tidy dataset with variables in their own columns, and observations in their own cells, with no blank cells so proper analysis and visualization can be performed. Class of columns are specified, and column headers edited. My data comes in three different datasets so these steps are performed for each dataset

**DataExploration.Rmd**

Exploration of the three datasets to see if there are any outliers, missing data, or out of range data. This led to realization of needing precipitation data, so in this markdown document I wrangle precipitation data as well. Wrangled precipitation data and wrangled pond data are then added together. In addition, edited datasets are saved as processed files, and initial visualizations are performed to find trends, outliers, and potential relationships.

**DataVisualization.Rmd**

Simple histograms are created to show trends of single variables over time, as well as more complex histograms, scatter plots, and line plots comparing various numeric variables across time nad the three different ponds. These visuals aim to show trends and relationships between variables and ponds. 


## Quality Assurance/Quality Control
*Protocol has been set by the Duke University Wetland Center for data collection and processing. These procesdures have been happening for many years as part of an ongoing study, and are therefore performed consistently besides any human error.

*All values are checked to see if they are within an expected range of data.

*Notes are made by the Lab Administrator of data gaps, unexpected values, or error in processing. These notes are taken into account within analysis.

*Boxplots and visualization techniques are used to discover any outliers within data, and these are flagged accordingly. 

*Data wrangling, exploration, and visualization steps within R are properly annotated for reproducible analysis.

*Naming conventions are used for reproducible files and datasets. 

