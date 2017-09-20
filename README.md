# INFSCI 2415 Assignment 1
This project is the 1st assignment of INFSCI 2415 Information Visualization (2017 Fall).

## Project discription:

Task: Generate visualizations to compare the poverty data by states, by races, and by time.
* Download the poverty data from US Census:
    + (D1) Distribution of the Poor by Race and Hispanic Origin
    + (D2) Number of Poor and Poverty Rate, by State
* Work in groups (3-4 members per group) to create three visualization designs using D3
* Submit your report in PDF, and your code in *.zip, via courseweb. One submission per group.
* Due: 2017-09-25 11.59pm
* Demo time: to be scheduled

1. Read the description about Census Poverty Measure at Census.gov.
2. Generate three visualizations to compare the data by states, by races, and by time.
    + Use dataset D1. To compare data across races and over time, generate a time-series plot to show how the poverty by race change from 1990 to 2015. You need to show at least three time points in the plot: 1995, 2005, and 2015. Omit race categories with “NA” values.
    + Use dataset D2. To compare data across states and over time, generate three bar charts corresponding to poverty of the states in 1995, 2005, and 2015 (one chart per year), where each bar represents a state.
    + Use datasets D1 & D2. Use your creativity to design and generate a composite visualization to show how the data change between 1990 and 2015, by state and by race. The visualization can include multiple charts or mix different types of charts.
3. All visualizations need to be properly annotated and labeled to help clearly explain what the visualizations show.
4. Explain in your report:
* what you intend to show in the visualization
* the rationale for each design (why is it an effective representation for the things you intend to show?)
* in the beginning of the report, describe your team contribution, including (a) names and PITT IDs of all members, and (b) one paragraph to briefly describe the contribution of each member

## Working plan:

### Data preprocessing:

For by-race dataset (D1):
* The survey question about race changed around 2001 -- before that a person can only choose one race identity, but after that can choose a combination of several races. This change leads to a lot of NAs in the dataset. Therefore, we decide to merge "white alone" and "white", "white alone not hispanic" and "white not hispanic", "black alone or in combination" and "black" (discard "black alone"), "Asian alone or in combination" and "Asian & Pacific islander" (discard "Asian alone"). And keep "hispanic". After this manipulate, we can avoid most NAs in this dataset.
* 2013 has two rows of data due to different methods of determine poverty. We will take the average of the two rows as the data of 2013.

For by-state dataset (D2):
* add a column of "Year"
* add a column of "State_short"
* remove the two columns of "Standard error" which we will not use for visualiztion
* remove all extra cells of table introduction and footnote

### Time-series plot of D1

### Bar chart of D2

### Visualization:

For D1 by-race data, we will use [How the Giants of Finance Shrank, Then Grew, Under the Financial Crisis](http://www.nytimes.com/interactive/2009/09/12/business/financial-markets-graphic.html) as an example

For D2 by-state data, we will use [Dorling Cartogram of Obesity in the United States (1995 to 2008)](https://homes.cs.washington.edu/~jheer//files/zoo/ex/maps/cartogram.html) as an example

### Visulization samples:
Can read codes from here. They are really helpful.
https://github.com/d3/d3/wiki/Gallery



 
