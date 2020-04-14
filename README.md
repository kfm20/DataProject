# DataProject
Data Analysis on Duke University Wetland Center Duke Gardens 2019

## Summary
Data is sourced from the Duke University Wetland Center, 2019. Data was collected as part of the long term analysis of water quality being contributed from Duke Univeristy's central campus to Sandy Creek and down to the Cape Fear River. Additional water quality data is being collected in the Duke Forest as part of a long term analysis on wetland and stream restoration sites.

Analysis of trends of main parameters like phosphorus, nitrogen, and fecal coliform over time are analyzed to see if there is significance using a time series analysis test. Trends of different parameters over time are analyzed across time using histograms and line plots, and these are compared across ponds. I am interested in seeing if there is a relationship of flow from Upper to Duck then to South Pond of high levels of any parameter. This can be accomplished by visualizing one parameter over time for each pond, and stacking these figures on top of each other. I hope to identify a particular parameter or time frame where high levels move from one pond to another in accordance with the flow of water. This will help indicate potential trends in data over time due to the flow of water, or aid in new restoration or management strategies to reduce the downflow of these nutrients, or by increasing their retention.


## Database Information
This data was collected, processed, and compiled by the Duke University Wetland Center. It contains data from 3 ponds in Duke Gardens: South, Upper, and Duke Pond, Durham, NC, over the year 2019. Certain water quality parameters are reported from the use of a YSI instrument, while others are from grab samples processed in a lab under various protocols. 


## Investigators
**Duke University Wetland Center**

*Curt Richardson, Director

*Neal Flanagan, Assistant Director

*Belen De La Berrera, Lab Administrator, Main Data Source Contact, belen.de.la.barrera@duke.edu

*Bryan Stokes Cawley, Lab Assistant

*Autumn Dunn, Lab Graduate Assistant

*Kathleen Mason, Lab Graduate Assistant, Main Data Analysis Contact, kathleen.f.mason@duke.edu


## Keywords
Duke University, Duke Gardens, water quality, water testing, watershed restoration, reducing nutrients, nutrient pollution, water supply, monitoring, management, data summary


## Folder structure, file formats, and naming conventions 
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

*DG2019_UpperPond_raw.csv

*DG2019_SouthPond_raw.csv

*DG2019_DuckPond_raw.csv


Column name | Data Description | Class | Associated Units
--------|-----|--------|-------
Month | name of the month the data was collected in | character
Rep | the number of the replicate sample those data belong to | character
FOP| x | numeric | µg/L
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
Electrical Conductivity|  x | numeric | uS/cm
Dissolved Solid TDS | total dissolved solids within the water | numeric | mg/L
Salinity | a measure of the contents of salts | numeric | %
pH | a measure of how acidic or basic the water is| numeric |


## Scripts and code
**DataWrangling.Rmd**

This includes the steps required to create a tidy dataset with variables in their own columns, and observations in their own cells, with no blank cells so proper analysis and visualization can be performed. Class of columns are specified, nad column headers edited. My data comes in three different datasets so these steps are performed for each dataset

**DataExploration.Rmd**

Exploration of the three datasets to see if there are any outliers, missing data, or out of range data. In addition, edited datasets are saved as processed files, and initial visualizations are performed to find trends and ouliers. 

**DataVisualization.Rmd**

Simple histograms are created to show trends of single variables over time, as well as more complex histograms, scatter plots, and line plots comparing various numeric variables across time nad the three different ponds. These visuals aim to show trends and relationships between variables and ponds. 


## Quality assurance/quality control
*Protocol has been set by the Duke University Wetland Center for data collection and processing. These procesdures have been happening for many years as part of an ongoing study, and are therefore performed consistently besides any human error.

*All values are checked to see if they are within an expected range of data.

*Notes are made by the Lab Administrator of data gaps, unexpected values, or error in processing. These notes are taken into account within analysis.

*Boxplots and visualization techniques are used to discover any outliers within data, and these are flagged accordingly. 

*Data wrangling, exploration, and visualization steps within R are properly annotated for reproducible analysis.

*Naming conventions are used for reproducible files and datasets. 

