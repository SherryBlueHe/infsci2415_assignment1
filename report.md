# INFSCI 2415 Information Visualization
## Report of Homework 1: Generate Visualizations to Compare the Poverty Data by States, by Races, and by Time

### Team Member and Contribution:

He, Jiexiao  
Song, Chen chs222@pitt.edu  
Xie, Jingran jix73@pitt.edu  

Jiexiao completed the first visualization: a time-series plot to show how the poverty by race change from 1990 to 2015. Chen did the data preprocessing, drafted the report and completed the second visualization: three bar charts corresponding to poverty of the states in 1995, 2005, and 2015. Jingran completed the third visualization: how the data change between 1990 and 2015, by state and by race. And we discussed the methods to preprocess the data and design the visualizations together. 


### Exploration and Preprocessing of the Dataset:

There are two datasets: D1 is Distribution of the Poor by Race and Hispanic Origin, D2 is Number of Poor and Poverty Rate by State. After some exploration of the two datasets, we found two things we need to deal with before we start:  

1. Measurement of poverty changed in 2013, therefore in both the two datasets, there are two rows can be mapped to 2013, each one holds a method of measurement. To deal with this problem, we took the average of the two rows as the final data element of 2013. We believe the average method can smooth the data from one measurement method to the other.  

2. Method in survey about race identification changed between 2001 and 2002. Before that people can only chose one race identification; after that people can chose one or a combination of race identifications. This change created a lot of NAs in D1. To omit the NAs, we decided to merge the data of a race before and after 2001 into a column together. The problem is, which column we should choose when we do the merge, [raceName] or [raceName only]. It is clear that the first one contains the people have multiple race identifications so there will be some overlaps, but the second one excludes the multiple race identifications people, so there will be some gaps. We prefer overlap than gap, so that we will not lose any information. Based on this, we decide to merge "white alone" and "white", "white alone not hispanic" and "white not hispanic", "black alone or in combination" and "black" (discard "black alone"), "Asian alone or in combination" and "Asian & Pacific islander" (discard "Asian alone"). We keep "hispanic". Since hispanic can be any race, this column contains overlap information naturally, which is consistent with previous merges. After this manipulate, we can avoid most NAs in D1.  

After dealing with these two crusial problems, we also did several other steps in data preprocessing. We deleted the titles, instructions and footnotes in the two tables, the rows before 1995 or after 2015 in both tables, as well as standard errors columns in D1, which we will not need in the visualization. In D2, we added a column of abbreviations of the states, which we can use in our visualization later. Also for D2, we splited it into 26 tables, one year each table, for later use of time slider. Finally, we change all the tables into csv files. All these preprocessing steps were finished in Excel.  


### Visualization Design:

##### Visualization I: A time-series plot to show how the poverty by race change from 1990 to 2015
##### Visualization II: Three bar charts corresponding to poverty of the states in 1995, 2005, and 2015
##### Visualization III: How the data change between 1990 and 2015, by state and by race


### Discussion:

### Reference: 
1. D3js v4 Stacked Bar Chart - with Tooltip Hover, Mike Foster, [https://bl.ocks.org/mjfoster83/7c9bdfd714ab2f2e39dd5c09057a55a0](https://bl.ocks.org/mjfoster83/7c9bdfd714ab2f2e39dd5c09057a55a0).
