# AR6-landues-databast-downscaling-by-Demeter
This repository is to discuss how Demeter is used to downscale the AR6 database.<br>
We thank IIASA for providing the AR scenario data, which you can find here (https://data.ece.iiasa.ac.at/ar6/#/login).<br>
We thank Demeter for being able to support us (https://github.com/JGCRI/demeter). We are very grateful to Dr Narayan, Kanishka Balu for his contribution.<br>
AR6 can only support exporting future scenario data for each country at most. Mostly, a country has multiple basin mapping relationships, which requires us to assign them according to some principle. 
I'm currently going to do a weighted allocation based on the area of the basin or a proportional allocation based on the relationship of the basin values in gcam_ref_scenario_reg32_basin235_v5p1p3.csv. 
