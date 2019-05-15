# Ethno-religious diversity and recovery after conflict in post-ISIL Iraq: A Geospatial Approach - Replication Code and Data
Replication code and data for "Ethno-Religious Diversity and Recovery After Conflict in Post-ISIL Iraq: A Geospatial Approach" (Lloyd Lyall, 2019). The thesis is avaliable at https://purl.stanford.edu/qb151vz4409. Readers are referred to the thesis Works Cited section for citations and acknowledgements. 

# A note on settlement-level ethno-religious composition data

The settlement-level IOM survey data on ethno-religious composition is potentially sensitive. For this reason it is not publicly available; I obtained written permission from IOM to use it. The parts of this dataset I use in this thesis could probably be considered public knowledge, but out of an abundance of caution, the publicly available dataset posted here excludes settlement-level ethno-religious composition information collected by IOM.

Instead, the publically avaliable code uses ethno-religious data from Izady's (2015) Iraqi Group Divisions Map to code settlement level ethno-religious composition and diversity for all settlements. I intersected the map with my set of settlements and used it to code the majority group in each settlement. This map is publically avaliable, but the results of using it to code settlement-level ethno-religious composition are likely less accurate than the IOM survey data. As a result, some emperical results obtained with the publically avaliable code will be different and slightly less accurate than the emperical results of the thesis.

Users seeking to replicate the thesis exactly using the IOM ILA III settlement-level ethno-religious data should first obtain written permission from the IOM Iraq team to access the IOM ILA III dataset for Iraq with ethno-religious variables; I would then be happy to share the full dataset. 

# Replication Data
Running the publically avaliable R replication code requires the following 7 data files:

"control.dbf", spatial data on territorial control. 

"luminosity_all.dbf", spatial data on luminosity for all settlements.

"Mosul_neighborhoods_lum.dbf", spatial data on luminosity for Mosul neighborhoods.

""nearest_iom_point.dbf", spatial data on the location of IOM ILA III survey points relative to settlement locations.

"covariates.dbf", spatial data on all other covariates.

"date_panel.csv", a csv panel with dates.

"settlement_diversity_scores", spatial data on diversity scores. 

All of the above data files are avaliable on the GitHub and Stanford Libraries page for this project. Users can download them all, put them in the same folder, set it as their working directory (the first line in the R code) and begin. The replication file folder also contains shapefiles of these datasets, so users can open them in GIS software as well if they wish to. 

If users were to gain permission from IOM to access the full dataset, they can add "ILA3_ethnicity.dbf" to their working directory - I will provide this file - and flip the global control "use_settlement_er_data" to TRUE). 



# Replication Code
This code replicates all the tables and core emperical results from this thesis - every table and figure from the beginning of Chapter 3 through to the end of Appendix 1 (except for the maps, which were created in QGIS). Replication code for the luminosity validation exercizes in Chapter 2 is avaliable on request. 

Chunks 2 and 3 of R code must be set by the user: users input the filepath of where the replication data is stored locally in chunk 2, and the filepath of where they want results to be stored in chunk 3 (the instructions are clear in the code). Chunk 4 contains a number of constants that can be optionally adjusted by the user, depending on which figures the user wants to create and which tests they want to run. The instructions are clearly delineated in the comments. 

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
