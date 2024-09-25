# Method  ＆ Question

## **1.The land use data provided by AR6 and Demeter's standard land categories are not consistent.**

Using the example of Forest, Argentina.

In AR6：We can see 5 type: Foreset, Forest|Managed, Forest|Natural Forest, Forest|Afforestation and Reforestation, Forest|Forestry|Harvested Area, Forest|Share

![image.png](image.png)

In  Demeter projected data in default:  We can see 3 type: Foreset, ProtectedUnmanagedForest,UnmanagedForest

![image.png](image%201.png)

The solution we have used is

- For align with Demeter ref tale, we summed the values for Forest|Managed,Forest|Afforestation and Reforestation, Forest|Forestry|Harvested Area, Forest|Share as ProtectedUnmanagedForest.
- We use the value of Forest|Natural Forest as UnmanagedForest

Discussion

We note that not all of the GCAM region will be planted in the C1 scenario.We note that not all of the GCAM region will be planted in the C1 scenario. However, inside the Demeter Projected data there are Forest changes in each region. How does this need to be considered?

![image.png](image%202.png)

## **2.Weights for assigning basins to each country**

Since AR6 only provides values for each country, but we want to assign a basin in GCAM for Demeter.

The solution we have used is

We summed the 1975-2015 values for each BASIN section.

 For the assignment of weights we use

![image.png](image%203.png)

## **3.Result of example**

From the AR6 data and the Demeter data, we select the forest in the Argentine area as an example. We aim to reassign the AR6 country level to the basin level, which has been matched to the project table (gcam_ref_scenario_reg32_basin235_v5p1p3.csv) of the Demeter.

File description

- [Demeter_Argentina_forest.xlsx](https://github.com/CGL5230/AR6-landues-databast-downscaling-by-Demeter/blob/main/Demeter_Argentina_forest.xlsx) stands for the forest in the Argentine that we got from Demeter
- [AR6_Argentina_forest.xlsx](https://github.com/CGL5230/AR6-landues-databast-downscaling-by-Demeter/blob/main/AR6_Argentina_forest.xlsx) stands for the forest in the Argentine that we got from AR6 database
- [AR6_Argentina_Forest_allocation.csv](https://github.com/CGL5230/AR6-landues-databast-downscaling-by-Demeter/blob/main/AR6_Argentina_Forest_allocation.csv) stands for the forest in the Argentine that we reassigned.
- [demeter_forest_example.ipynb](https://github.com/CGL5230/AR6-landues-databast-downscaling-by-Demeter/blob/main/demeter_forest_example.ipynb) stands for the Method we mentioned before.