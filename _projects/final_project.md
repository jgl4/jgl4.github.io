---
name: Salmonella in the United States -- Cases, Rates, and Serotypes
tools: [Python, HTML, vega-lite]
image: assets/pngs/final_project_header.png
description: Submission for final project
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Salmonella in the United States: Cases, Rates, and Serotypes
By Jacqueline Léveillé

## Disease in the United States

The Centers of Disease and Prevention selected a total of 16 nationally notifiable diseases, not including sexually transmitted diseases, to collect information on from 1950 to 2019. Since 1980, Salmonellosis has had the most new cases per 100,000 population peaking at 27.37 cases per 100,000 population in 1985. In the most recent year of data collected (2019), there were 58,371 new cases of Salmonellosis in the United States revealing the evident impact of this bacterial disease in the present day. The line chart below highlights Salmonellosis history as the leading disease with new cases in the United States. Salmonellosis is the only disease to diverge from the blue-purple color palette in order to spotlight the subject of this project.

<vegachart schema-url="{{ site.baseurl }}/assets/json/disease_chart.json" style="width: 100%"></vegachart>
Source: [Centers For Disease Control and Prevention](https://www.cdc.gov/nchs/data/hus/2020-2021/IDNotif.pdf)

**<u>Note</u>**: I created the contextual visualization seen above using the source data. The code used to create the visualization is linked through "The Analysis" button at the bottom of this page. 

## Salmonella Rates

In an effort to prevent new cases of Salmonella in the United States, it is valuable to understand which states have the highest Salmonella-positivity rates to limit the spread of the disease. The United States Department of Agriculture’s Food Safety and Inspection Service conducted testing from March 28, 2021 to March 26, 2022 in different poultry establishments across the United States Suozzo, Ngu, Grabell, & Yeung, 2021). The state with the highest salmonella rate is Maine with 47.83% and the state with the least is Nevada with 0%. The results of the testing can be seen in the map below colored based on the salmonella rate with an interactive slider that allows you to see the states that have rates above the cutoff.

<vegachart schema-url="{{ site.baseurl }}/assets/json/cutoff_chart.json" style="width: 100%"></vegachart>
Sources: 
[ProPublica Data Store](https://www.propublica.org/datastore/dataset/usda-poultry-plant-salmonella-inspection-data),
[Jason Ong](https://github.com/jasonong/List-of-US-States/blob/master/states.csv), 
[Mike Bostock](https://cdn.jsdelivr.net/npm/us-atlas@3/states-10m.json)

## Serotype Counts

According to the Centers for Disease Control and Prevention (2022), “[s]erotypes are groups within a single species of microorganisms, such as bacteria or viruses, which share distinctive surface structures.” Salmonella bacteria have many different serotypes as seen in the bar chart below. The serotypes can be distinctive to a specific animal or a particular geographic region (CDC, 2022). The CDC (2022) credits “[s]erotyping [as] the core of public health monitoring of Salmonella infections for over 50 years, because of the ability to detect more outbreaks. Therefore, the bar chart below that allows you to filter using the state dropdown showcases the prominent serotypes found in each state as well as across all states. Please note that only 44 states are included in the dropdown because only positive salmonella samples can have a serotype and 6 states do not have a record of a positive salmonella sample.

<vegachart schema-url="{{ site.baseurl }}/assets/json/bar_chart.json" style="width: 100%"></vegachart>
Sources: 
[ProPublica Data Store](https://www.propublica.org/datastore/dataset/usda-poultry-plant-salmonella-inspection-data),
[Jason Ong](https://github.com/jasonong/List-of-US-States/blob/master/states.csv) 

## Dashboard

The dashboard below is a combination of the “Salmonella Rates by State” and “Serotype Counts Based on State” charts. The primary difference is that the dashboard eliminates the need for a state dropdown because the state(s) selected on the map will adjust the bar chart accordingly. The map begins being entirely steelblue because all of the states are initially selected. However, once the audience clicks on a state of interest, the orange coloring based on salmonella will be revealed. If the shift key is pressed while clicking, it will select multiple states, to allow the counts across states to be represented in the bar graph. Please note that the 6 states without a record of a positive salmonella sample will have no data for the bar graph because only positive salmonella samples can have a serotype.

<vegachart schema-url="{{ site.baseurl }}/assets/json/dashboard.json" style="width: 100%"></vegachart>
Sources: 
[ProPublica Data Store](https://www.propublica.org/datastore/dataset/usda-poultry-plant-salmonella-inspection-data),
[Jason Ong](https://github.com/jasonong/List-of-US-States/blob/master/states.csv), 
[Mike Bostock](https://cdn.jsdelivr.net/npm/us-atlas@3/states-10m.json)

## Infantis

A failure in Food Safety and Inspection Service regulations and safety plans caused the spread of the serotype Infantis resulting in a 32-state outbreak of salmonella in 2019 (The Pew Charitable Trusts, 2021). Therefore, according to the Pew Charitable Trusts (2021), “reducing the prevalence of any variety—even those that pose little or no risk to people—can count as success” in terms of Salmonella control. According to the Chicken Checker (2021) data, Infantis is the leading serotype in the United States with nearly 800 samples found during their testing period. The chart provided by the Pew Charitable Trusts, displays the percent of positive Salmonella samples of the serotype Infantis in different parts of a chicken. For the audience, it can reveal information on which parts of the chicken are most important to test in order to limit the spread of Infantis.

![chart.png](/assets/pngs/chart.png)
Source: [The Pew Charitable Trusts](https://www.pewtrusts.org/en/research-and-analysis/data-visualizations/2021/12-charts-explore-americas-salmonella-problem-and-steps-to-solve-it)

## Sources
#### Data
&ensp;&ensp;&ensp;&ensp;Bostock, M. (2023, April 18). *US Atlas*. GitHub. [https://github.com/topojson/us-atlas](https://github.com/topojson/us-atlas)
<br>&ensp;&ensp;&ensp;&ensp;*Chicken Checker*. ProPublica Data Store. (2021, November). [https://www.propublica.org/datastore/dataset/usda-poultry-plant-salmonella-inspection-data](https://www.propublica.org/datastore/dataset/usda-poultry-plant-salmonella-inspection-data)
<br>&ensp;&ensp;&ensp;&ensp;Ong, J. (2012, July 23). *List of US States*. GitHub. [https://github.com/jasonong/List-of-US-States/blob/master/states.csv](https://github.com/jasonong/List-of-US-States/blob/master/states.csv)
<br>&ensp;&ensp;&ensp;&ensp;*Table IDNotif. Selected nationally notifiable disease rates and number of new cases: United States, selected years 1950–2019*. Centers for Disease Control and Prevention. (n.d.). [https://www.cdc.gov/nchs/data/hus/2020-2021/idnotif.pdf](https://www.cdc.gov/nchs/data/hus/2020-2021/idnotif.pdf)
#### Other Sources
&ensp;&ensp;&ensp;&ensp;Centers for Disease Control and Prevention. (2022, September 9). *Serotypes and the importance of serotyping salmonella*. Centers for Disease Control and Prevention. [https://www.cdc.gov/salmonella/reportspubs/salmonella-atlas/serotyping-importance.html](https://www.cdc.gov/salmonella/reportspubs/salmonella-atlas/serotyping-importance.html)
<br>&ensp;&ensp;&ensp;&ensp;The Pew Charitable Trusts. (2021, December 10). *12 charts explore America’s salmonella problem-and steps to solve it*. The Pew Charitable Trusts. [https://www.pewtrusts.org/en/research-and-analysis/data-visualizations/2021/12-charts-explore-americas-salmonella-problem-and-steps-to-solve-it](https://www.pewtrusts.org/en/research-and-analysis/data-visualizations/2021/12-charts-explore-americas-salmonella-problem-and-steps-to-solve-it)
<br>&ensp;&ensp;&ensp;&ensp;Suozzo, A., Ngu, A., Grabell, M., &amp; Yeung, B. (2021, October 29). *About the data: Chicken checker*. ProPublica. [https://projects.propublica.org/chicken/methodology/](https://projects.propublica.org/chicken/methodology/)

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://www.propublica.org/datastore/dataset/usda-poultry-plant-salmonella-inspection-data" text="The Primary Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jgl4/jgl4.github.io/blob/main/python_notebooks/Workbook.ipynb" text="The Analysis" %}
</div>