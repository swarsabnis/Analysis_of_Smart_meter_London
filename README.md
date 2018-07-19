

	
#  Analysis of Smart Meter in United Kingdom

<p> This repo is used to understand energy consumption pattern in UK. The dataset consisted of 5,566 London households and their energy consumption between November 2011 and February 2014. The readings for each household were taken every half hour. Households in UK have been allocated to CACI ACORN(Classification of Residential Neighborhoods) groups, which is a geo-demographic segmentation of UK's population. UK energy Tariff plans are broadly categorized into two groups: Dynamic Time of Use and Standard. The Dynamic Time of Use plan is set up so that each household is made aware of its tariff prices(high, low and normal) a day in advanced and the Standard plan has a constant flat rate daily. </p>

<p>This dataset was used to understand energy consumption patterns across different ACORN groups. Initial analysis consisted of understanding the different ACORN groups and the difference between them. The next steps of analysis consisted of a deep dive into the dataset which contains the records of household energy consumption (monitored every half hour) to try to establish different consumption patterns based on tariff plans and the ACORN groups. Analysis of weather impacts on energy consumption across groups was also conducted. The resulting output comprised of visualizations of various parameters which exhibit energy consumption trends  within and across ACORN groups.</p>

### Dependencies:

#### Python Packages used:
<ol>
	<li>pandas</li>
	<li>numpy </li>
	<li>matplotlib</li>
	<li>seaborn </li>	
	<li>datetime </li>
	<li>plotly</li>
	<li>calendar</li>
</ol>

### Datasets used:
<ol type="i">
<li>informations_households.xls : Contains all the information on the households including type of acorn group and type of tariff plan used in each household respectively.</li>

<li>Halfhourly_dataset.zip : Zip file contains the block files with the half-hourly smart meter measurement. Since, we could not read all the block files present in folder because of its size, we chose a few blocks representing each ACORN group( Affluent/ Comfortable/ Adversity).
Blocks used : Block_0, Block_2, Block_4, Block_62, Block_78, Block_79, Block_80, Block_95, Block_96, Block_105</li>

<li>acorn_details.xls : Contains detail on acorn groups and profile of individuals in each group based on social, demographic, economic and other differentiating aspects.The first three columns are the attributes studied, the ACORN-* is the index of the attribute for each acorn group. At a national scale, the index is 100 if for one column the value is 150 it means that there are 1.5 times more people with this attribute in the ACORN group than at the national scale. You can find an explanation on the <a href="https://acorn.caci.co.uk/what-is-acorn">CACI website </a>.</li>

<li>weather_hourly_darksky.csv : Contains hourly data from darksky api. It consists of hourly weather information across UK including minimum-maximum temperature and wind data.</li>

<li>Tariff:Contains half hourly Tariff rates(High, Normal, Low) for the households subscribed to Dynamic Time of Use plan for the year 2013.</li>
</ol>

## Table Of Contents:

#### Reading Datasets

#### Cleaning Datasets
<a href="https://github.com/swarsabnis/Smart_meter_London/blob/master/Jupyter_Notebooks/Smart_meter_london_cleaning_data.ipynb">Link to Jupyter Notebook for Cleaning</a>

#### Visualization

#### Interpretations 
<a href="https://github.com/swarsabnis/Smart_meter_London/blob/master/Jupyter_Notebooks/Smart_meter_london_visualizations.ipynb">Link to Jupyter Notebook for Visualization</a>


#### Summary


![Screenshot](hourly.png)

<p>Energy consumption is not the same throughout the day, energy needs change every hour. The usage is very high during evening hours and less during day time. As expected, the mean energy usage dips down to the lowest during late night hours. Interesting to see that this pattern remains same irrespective of their tariff rates (high, normal, low). Also, it is seen that when high rates are charged, subscribers tend to use little less energy so as to reduce their total expenses. Whereas, at lower rates, the average energy consumption is more compared to when high/normal energy rates were applied.</p>

![Screenshot_2](consumption_per_month.png)

<p>From the chart, it seems that there is a pattern followed by all the ACORN groups throughout the year. All the three ACORN groups, in general, have high energy consumption in month of December, January, February and March which eventually drops down for the rest of the year.Weather information on second Y-axis located on the right side of the plot. Weather (green line) shows that the average temperature for the months of December, January, February and March was below 5°C.It explains higher energy consumption during this period as heating systems would have been used extensively. So, temperature change plays a major role in energy consumption irrespective of different ACORN groups.</p>


