# DataProject
Data Analysis on Wetland Center SWAMP sites 2019

## Summary
Data is sourced from the Duke University Wetland Center, 2019. Data was collected as part of the long term analysis of water quality being contributed from Duke Univeristy's central campus to Sandy Creek and down to the Cape Fear River. Additional water quality data is being collected in the Duke Forest as part of a long term analysis on wetland and stream restoration sites.


## Database Information
This data was collected, processed, and compiled by the Duke University Wetland Center. It contains data from 3 ponds in Duke Gardens: South, Upper, and Duke Pond, Durham, NC, over the year 2019. Certain water quality parameters are reported from the use of a YSI instrument, while others are from grab samples processed in a lab under various protocols. 


## Investigators
Duke University Wetland Center

Curt Richardson, Director
Neal Flanagan, Assistant Director

Belen De La Berrera, Lab Administrator, Main Data Source Contact, belen.de.la.barrera@duke.edu
Bryan Stokes Cawley, Lab Assistant

Autumn Dunn, Lab Graduate Assistant
Kathleen Mason, Lab Graduate Assistant, Main Data Analysis Contact, kathleen.f.mason@duke.edu


## Keywords

Duke University, Duke Gardens, water quality, water testing, watershed restoration, reducing nutrients, nutrient pollution, water supply, monitoring, management, data summary


## Folder structure, file formats, and naming conventions 

Folder Structure:
Code-R markdown code for data wrangling, data exploration/analysis, and data visualization
Output-This contains any .pdf documents of maps, as well as .jpg or .png exported files of graphs.
Processed-Exported .csv files of wrangled datasets, so particular formatted datasets can be accessed again or shared.
Raw- Original .xlsx sheets of the data, which are also saved as .csv files for use in R.There is one .xlsx and .csv for each of the three ponds.



Naming Convention:
Files are named according to the following naming convention: `databasename_datatype_details_stage.format`, where: 

**databasename** refers to the database from where the data originated, all files in this folder include DG2019, or Duke Gardens 2019

**datatype** is a description of data 

**details** are additional descriptive details, particularly important for processed data or outputs

**stage**refers to the stage in data management pipelines (raw, wrangled, or processed)

**format** is a non-proprietary file format (.csv, .txt, .pdf, .png, .jpg, .xlsx)



## Metadata

Description of the data contained in each of the below data sets.

DG2019_UpperPond_raw.csv
DG2019_SouthPond_raw.csv
DG2019_DuckPond_raw.csv

Column name, data description, class, associated units

Parameters calculated using laboratory protocols:
Month, the name of the month the data was collected in, character
Rep, the number of the replicate sample those data belong to, character
FOP, ___, numeric, (µg/L)
TP, total phosphorus concentrations, numeric, (µg/L)
NOx, total nitrates, numeric, (µg/L)
NHx, total ammonium, numeric, (µg/L)
TN, total nitrogen, numeric, (µg/L)
TSS, total suspended solids, numeric, (mg/L)
Fecal Coliform, total concentration of the bacteria fecal coliform, numeric, (CFU/100mL)

Parameters Obtained from the YSI:
T, temperature, numeric, (degrees Celcius)
Oxygen Saturdation, total oxygen saturation, numeric, (%)
Oxygen Concentration, total oxygen concentration, numeric, (mg/L)
Specific Conductivity, how well water can conduct an electric current, numeric, (uS/cm)
Electrical Conductivity, ___, numeric, (uS/cm)
Dissolved Solid TDS, total dissolved solids within the water, numeric, (mg/L)
Salinity, a measure of the contents of salts, numeric, (%)
pH, a measure of how acidic or basic the water is, numeric



## Scripts and code

<list any software scripts/code contained in the repository and a description of their purpose.>

## Quality assurance/quality control

<describe any relevant QA/QC procedures taken with your data. Some ideas can be found here:>
<https://www.dataone.org/best-practices/develop-quality-assurance-and-quality-control-plan>
<https://www.dataone.org/best-practices/ensure-basic-quality-control>
<https://www.dataone.org/best-practices/communicate-data-quality>
<https://www.dataone.org/best-practices/identify-outliers>
<https://www.dataone.org/best-practices/identify-values-are-estimated>