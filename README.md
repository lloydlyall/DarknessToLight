# Ethno-religious diversity and recovery after conflict in post-ISIL Iraq
Replication code and data for "Ethno-Religious Diversity and Recovery After Conflict in Post-ISIL Iraq: A Geospatial Approach" (Lloyd Lyall, 2019). The thesis is avaliable at https://purl.stanford.edu/qb151vz4409. Readers are referred to the thesis Works Cited section for citations and acknowledgements. 

# Overview
The emperical analysis of this thesis was conducted in the R programming language. The materials posted to this repository are sufficient to replicate every table and figure in the thesis from Chapter 3 through to the end of Appendix I in R with two exceptions:

-The maps and Figure 24 would require some additional assembly in a GIS software and Excel respectively.

-The settlement-level IOM survey data on ethno-religious composition is potentially sensitive. For this reason it is not publicly available; I obtained written permission from IOM to use it. The parts of this dataset I use in this thesis could probably be considered public knowledge, but out of an abundance of caution, the publicly available dataset posted here excludes settlement-level ethno-religious composition information. The posted code replicates all the core empirical analysis of this thesis, but some results will be slightly different because the code excludes ethno-religious group dummies from the calculations. Users seeking to replicate specifications which include ethno-religious dummies should first obtain written permission from the IOM Iraq team to access the IOM ILA III dataset for Iraq with ethno-religious variables; I would then be happy to share the full dataset. 

# Replication Data
Running the R replication code requires the following 7 data files:

"control.dbf", spatial data on territorial control. 
"luminosity_all.dbf", spatial data on luminosity for all settlements
"Mosul_neighborhoods_lum.dbf", spatial data on luminosity for Mosul neighborhoods,
"ILA3_ethnicity.dbf", spatial data on the ILA III ethnicity measure
""nearest_iom_point.dbf", spatial data on the location of IOM ILA III survey points relative to settlement locations
"covariates.dbf", spatial data on all other covariates
"date_panel.csv", a csv panel with dates 

All of these data files are avaliable on the GitHub and Stanford Libraries page for this project. Download them all, put them in the same folder, set it as your working directory (the first line in the R code) and you are good to go. The replication file folder also contains shapefiles of these datasets, so users can open them in GIS software if they wish. 

# Replication Code
This code replicates all the tables and core emperical results from this thesis - every table and figure from the beginning of Chapter 3 through to the end of Appendix 1 (except for the maps, which were created in QGIS, and figure 24, which requires creating the pie chart in Excel). Replication code for the luminosity validation exercizes in Chapter 2 is avaliable on request. 

Chunks 2 and 3 of R code must be set by the user: input the filepath of where the replication data is stored on your computer in the chunk 2, and the filepath of where you want results to be stored in chunk 3 (the instructions are clear in the code). Chunk 4 contains a number of constants that can be optionally adjusted by the user, depending on which figures the user wants to create and which tests they want to run. The instructions are clearly delineated in the comments. 

The replication code requires the following free R packages to run. You will need to download them to run the replication code if you have not already. 
(Metrics)
(reshape2)
(rsq)
(ggplot2)
(readr)
(gridExtra)
(gtable)
(grid)
(cowplot)
(foreign)
(lubridate)
(ggpubr)
(ggfortify)
(rgdal)
(raster)
(purrr)
(scales)
(spdep)
(texreg)
(stargazer)
(gsynth)
