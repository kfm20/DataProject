# Data Project
Data Analysis on Duke University Wetland Center Duke Gardens 2019

## Summary
Water Quality Data is sourced from the Duke University Wetland Center, 2019. Data was collected as part of the long term analysis of water quality being contributed from Duke Univeristy's central campus to Sandy Creek and down to the Cape Fear River. Additional water quality data is being collected in the Duke Forest as part of a long term analysis on wetland and stream restoration sites.


I am curious of the water quality over the months of 2019. I will analyze the general trends in parameters of particular interest, as well as relationships between total suspended solids and concentrations of nutrients (TN and TP), as well as fecal coliform and concentrations of nutrients. These analyses go into the deeper biogeochemistry of the ponds. Duck Pond has excess water foul visiting and living pondside, contributing fecal coliform and potentially excess dust particles. This analysis may allude to their impact on the water quality of the pond. Nutriet concentrations are a relevant research question because of the geographic location of the ponds. The ponds, are down slope from a large parking lot used for the hospital. If precipitation causes runoff, and specifically runoff of these nutrients, Upper Pond is the first to recieve it. The water then runs down to Duck Pond, and South Pond before exiting Duke Gardens. 

Analysis of trends of main parameters like phosphorus, nitrogen, fecal coliform, pH, and total suspended solids are analyzed over time to see general trends between the ponds. Line plots are used to show these trends between the ponds. Statistical analysis is also performed between TSS and TP, and TN, and fecal coliform and TP, and TN. These relationships are plotted over the year of 2019 with monthly data points.


## Database Information
The water quality data was collected, processed, and compiled by the Duke University Wetland Center. It contains data from 3 ponds in Duke Gardens: South, Upper, and Duke Pond, Durham, NC, over the year 2019. Certain water quality parameters are reported from the use of a YSI instrument, while others are from grab samples processed in a lab under various protocols. 



## Investigators
**Duke University Wetland Center**

*Curt Richardson, Director

*Neal Flanagan

*Belen De La Berrera, Lab Administrator, Main Data Source Contact, belen.de.la.barrera@duke.edu

*Bryan Stokes Cawley, Lab Assistant

*Autumn Dunn, Lab Graduate Assistant

*Kathleen Mason, Lab Graduate Assistant, Main Data Analysis Contact, kathleen.f.mason@duke.edu






## Keywords
Duke University, Duke Gardens, water quality, water testing, watershed restoration, reducing nutrients, nutrient pollution, water supply, monitoring, management, data summary, nutrient runoff, biogeochemistry


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
*DG2019_UpperPond_RAW.csv

*DG2019_SouthPond_RAW.csv

*DG2019_DuckPond_RAW.csv


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





## Scripts and Code
**DataWrangling.Rmd**

This includes the steps required to create a tidy dataset. My data comes in three different datasets so these steps are performed for each dataset, and then work to combine them. Visualization of general trends over time are also worked out within their own chunks, as well as calculations of mean, minimum, and maximums for particular parameters. Finally, statisticall analysis and graphics of these statistical analyses are performed to answer the stated research questions. 



## Quality Assurance/Quality Control
*Protocol has been set by the Duke University Wetland Center for data collection and processing. These procesdures have been happening for many years as part of an ongoing study, and are therefore performed consistently besides any human error.

*All values are checked to see if they are within an expected range of data.

*Notes are made by the Lab Administrator of data gaps, unexpected values, or error in processing. These notes are taken into account within analysis.

*Boxplots and visualization techniques are used to discover any outliers within data, and these are flagged accordingly. 

*Data wrangling, exploration, and visualization steps within R are properly annotated for reproducible analysis.

*Naming conventions are used for reproducible files and datasets. 

