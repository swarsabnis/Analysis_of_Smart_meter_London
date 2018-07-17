

## SmartMeter and its impact on energy consumption in UK
<p>This repo is used to understand energy consumption pattern in UK. Dataset consisted of 5,566 London households and their energy consumption between year November 2011 to February 2014.Readings for each household were taken every half hour. Households in UK have been allocated to a CACI Acorn(Classification of Residential Neighborhoods) groups, which is a geo-demographic segmentation of UK's population. UK energy Tariff plans are broadly categorized into two groups: Dynamic Time of Use and Standard. Dynamic Time of Use plan has the feature of sharing tariff prices(high, low and normal) with the household a day ahead and Standard plan had a constant flat rate throughout. </p>

<p>This dataset was used to understand energy consumption patterns across different acorn groups. Initial analysis consisted of understanding different acorn groups and point of difference within them. Dived into the half hourly dataset which comprised data for different household energy consumption monitored every half hour to see different patterns, if they exist, based on their tariff plans and based on the acorn groups. Curious to see if weather impacts energy consumption and does that vary across groups. Were able to visualize various parameters and could see trends on energy consumption within and across Acorn groups.</p>

### Dependencies:

#### Python Packages used:
	pandas
	numpy 
	matplotlib
	seaborn 	
	datetime 
	plotly
	calendar

#### Dataset used:
1. informations_households.xls : Contains all the information on the households including type of acorn group and type of tariff plan used in each household respectively.

2. Halfhourly_dataset.zip : Zip file contains the block files with the half-hourly smart meter measurement. Since, we could not read all the block files present in folder because of its size, we chose a few blocks representing each ACORN group( Affluent/ Comfortable/ Adversity).
Blocks used : Block_0, Block_2, Block_4, Block_62, Block_78, Block_79, Block_80, Block_95, Block_96, Block_105

3.acorn_details.xls : Contains detail on acorn groups and profile of individuals in each group based on social, demographic, economic and other differentiating aspects.The first three columns are the attributes studied, the ACORN-* is the index of the attribute for each acorn group. At a national scale, the index is 100 if for one column the value is 150 it means that there are 1.5 times more people with this attribute in the ACORN group than at the national scale. You can find an explanation on the CACI website.<a href="https://acorn.caci.co.uk/what-is-acorn">CACI website </a>

4. weather_hourly_darksky.csv : Contains hourly data from darksky api. It consists of hourly weather information across UK including minimum-maximum temperature and wind data.

5.Tariff:Contains half hourly Tariff rates(High, Normal, Low) for the households subscribed to Dynamic Time of Use plan for the year 2013.

### Table Of Contents:

#### Reading Datasets

#### Cleaning Datasets

#### Visualization

#### Interpretations 

#### Summary



