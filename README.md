# The-Impact-of-Cobalt-Mines-on-the-Wellbeing-of-DRC-Communties
## Purpose:
Climate change is an increasing threat to the world and countries are taking steps in hopes to reduce the number of carbon emissions. This includes switching to using electric vehicles and renewable energy sources such as solar and wind. These energy sources all require the use of cobalt in their battery cells. The majority of the cobalt in the world is in the Democratic Republic of Congo (DRC). There is a great concern that the mining of these minerals for global gain will negatively impact the economies, environmental health, and human health of the region. The DRC also has a heavy use of artisanal small mines that are illegal zones where people independently mine with no oversight. These sites are notorious for child labor, gender-based violence, and environmental damage. This project focuses on cobalt artisanal small mines (ASMs) as the country is exploring ways to formalize these zones so that they may still be an economic source for local communities while reducing the dangers they present. This analysis will explore if this policy should be pursued or if it does not have enough economic benefits for the communities to justify formalization. 
The analysis was done to assess how cobalt ASMs affect the province's economic well-being compared to the provinces without cobalt ASMs. This seeks to answer the question if it is beneficial for the people to have mines or if cobalt mining should be banned due to the risks associated with them. This will be done using severe poverty as a measure of economic wellbeing. In this case, severe poverty uses the indicators such as access to healthcare, water, electricity, and food security. This is then compared to the conflict in each province to determine if there is a relationship between conflict and ASMs. The number of internally displaced people in a province is an indicator of conflict.
## Scripts use in order:
**<p>1.collect.py<p>**
sources: cod_mines_curated_all_opendata_p_ipis.csv from https://ipisresearch.be/fr/publication/ipis-open-data-dashboard-on-the-artisanal-and-small-scale-mining-sector-in-eastern-drc/
Using the cod_mines_curated_all_opendata_p_ipis.csv to get out the provinces that have artisanal small mines located in them. Using the data only from 2020 for a comparison that can be used across the different scripts. The data will be trimmed to only 2020 producing dates.csv. After trimming the data based on year, the provinces will be trimmed to the ones only containing artisanal small mines. Saving this information into a csv called minesprov.csv for future use in other scripts.
<h2>2.poverty.py <h2>
sources: cod-region-results-mpi-2021.xls from https://data.humdata.org/dataset/democratic-republic-of-the-congo-mpi
minesprov.csv from the previous script
Using the cod-region-results-mpi-2021.xls to get the number of people in severe poverty by province. This is an excel that is still useable, but I had to manually remove the first rows of the file that just contained the title and empty spaces. The minesprov.csv is used to separate the provinces based on whether they contain ASMs. This is then further separated into provinces with cobalt small mines. This will produce the figures: pov_mining.png, pov_mining1.png, pov_nonmining1.png, pov_cobalt.png. The script will also list the average amount of people in severe poverty grouped by whether they have ASMs or not. It will also give the number of people in poverty in each province.</p>
<h2>3.population.py <h2>
sources: cod_admpop_adm1.csv from https://data.humdata.org/dataset/d1160fa9-1d58-4f96-9df5-edbff2e80895
rdc_mouvement_de_population_deplace_octobre_2021.xlsx from https://data.humdata.org/dataset/drc-displacement-deplace-site-assessment-ocha
The file cod_admpop_adm1.csv is used to gather the population for each province in 2020 for comparison when looking at those in severe poverty in each province. The rdc_mouvement_de_population_deplace_octobre_2021.xlsx is used to see the level of conflict in each province by gathering the amount of internally displaced people in each province. This script will produce: conflict.png, conflict2.png</p>
<h2>4.GIS Mapping<h2> 
Sources: cod_mines_curated_all_opendata_p_ipis from https://ipisresearch.be/fr/publication/ipis-open-data-dashboard-on-the-artisanal-and-small-scale-mining-sector-in-eastern-drc/
rdc_zone_de_sante_04012019 from https://data.humdata.org/dataset/rdc-statistiques-des-populations
This step is done only in GIS. The file rdc_zone_de_sante_04012019 is used to get the political boundaries of the DRC based on provinces. The shapefile cod_mines_curated_all_opendata_p_ipis is then merged into the previous file. The file is used to display the ASMs in the DRC. The map will show all ASMs in blue while the ones for cobalt will be in red. This will produce: Coballt_Mines.pgw, Coballt_Mines.png, Cobalt_Othermines.pgw, Cobalt_Othermines.png</p>

## Assessment 
Attached is a PowerPoint presentation that further breakdowns the results that have been found called DRC_Cobalt_Asms.pptx. When viewing the number of people in severe poverty across the DRC on average the number is lower in provinces with ASMs. This is even lower when just observing the average number of people in severe poverty in provinces with cobalt. This average number of severe being lower is significant because one of the two cobalt mining provinces, Haut-Katanga, has the third-highest population in the region at 6,102,542 people. The number of displaced people in the country is focused on the eastern portion of DRC where all the ASMs are located. While this may suggest that ASMs increase the amount of conflict in a region, it also suggests that this level of conflict does not impede a higher rate of economic success in cobalt mining provinces. Due to these factors, it is recommended that the DRC have an increased focus on formalizing cobalt ASMs. These mines are shown to have an economic benefit in the region and are crucial to their success. research could explore if formalizing small mines could lead to a reduction of conflict in communities, environmental damage, child labor, and gender-based violence. The relationship to these factors would be influenced by higher levels of regulation and an increased stable income for the people of the region. 
