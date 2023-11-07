---
name: Homework 8
tools: [Python, HTML, vega-lite]
image: assets/pngs/homework8cover.png
description: Here is my submission for homework 8.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Homework 8
The code for this assignment was taken from the IS 457: Data Visualization materials, specifically [In class Jekyll Resources - Week 10](<https://github.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2023/tree/master/week10/inClass>), [In Class Notebook - Week 10](<https://uiuc-ischool-dataviz.github.io/is445_bcubcg_fall2023/nbv.html?notebook_name=%2Fis445_bcubcg_fall2023%2Fweek10%2FinClass_week10.ipynb>), [In class Jekyll Resources - Week 11](<https://github.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2023/tree/master/week11/inClass>), and [In Class Notebook - Week 11](<https://uiuc-ischool-dataviz.github.io/is445_bcubcg_fall2023/nbv.html?notebook_name=%2Fis445_bcubcg_fall2023%2Fweek11%2FinClass_week11.ipynb>). Outside of the course resources [Filter Transform Documentation](<https://vega.github.io/vega-lite/docs/filter.html>), [Encoding Documentation](<https://altair-viz.github.io/user_guide/encodings/index.html>), [Interactive Charts Documentation](<https://altair-viz.github.io/user_guide/interactions.html>), and [Layered and Multi-View Charts Documentation](<https://altair-viz.github.io/user_guide/compound_charts.html>) were used. Lastly, the charts were improved based on [Homework #7](<https://starboard.gg/jgl4/homework7-nLGT2NO>).

## Visualization #1

<vegachart schema-url="{{ site.baseurl }}/assets/json/chart1_hw8.json" style="width: 100%"></vegachart>

### Write Up
The first visualization showcases the relationship between square footage and Senate districts. As stated in Homework #7, “the audience can find insights [in this visualization] about the amount of square footage different senate districts have occupancy in.” 

Similar to Homework #7, I maintained the selection of a rectangular grid map because “Senate districts are categorical values” and “the audience can easily see information on specific Senate districts of interest”. The encoding types used are quantitative for square footage and log square footage because both are a continuous quantity which is set with a maximum number of bins of 20. Senate districts are ordinal values because they are discrete yet ordered values. Since binning is used, I implemented a color bar with the default values to highlight the frequency of this square footage range for the Senate District. The sequential color map made sense for this visualization because as there were more records the color would become darker and more blue.

In the Homework #7, I indicated that with “more time, I would like to clean the data so that each record represents a building “[allowing] the audience to get more value out of the color by seeing how many buildings of that square footage that Senate district has occupancy in.” For this assignment, I accomplished this by looping over all of the unique location names and only adding one of each to the pandas dataframe unless another Senate district had occupancy in it.

Another improvement that was mentioned in my Homework #7 submission was “[removing] outliers of square footage to get a better representation of how square footage less than 100,000 varies across Senate districts.” Instead of removing outliers that could result in misrepresenting the square footage makeup of Senate districts, I decided to create a Log Square Footage field to address this issue. First, I converted all of the zero values to nan and then created a new column for Log Square Footage that took the log of the cleaned Square Footage column.

In order to highlight this change and allow the audience to see the real square footage values for interactivity I chose a dropdown menu. For the x-axis field, the audience can now select between Square Footage and Log Square Footage. The default value is set to square footage for the audience to gain an understanding of the general square footage range and see which Senate districts have a larger number of records. Then, the log square footage allows for a better understanding of how the square footage differs since there are less records in every individual bin.

## Visualization #2

<vegachart schema-url="{{ site.baseurl }}/assets/json/chart2_hw8.json" style="width: 100%"></vegachart>

### Write Up
The second visualization “[highlights] the dataset features of Agency Name, Floors Below Grade, and Total Floors.” The audience can gain an understanding of the total number of floors occupied by an agency as well as what proportion of those floors are below grade.

Similar to Homework #7, I kept the selection of a stacked bar graph because “it allows you to see how the floors below grade contribute to the total sum of recorded floors.” I confirm that this is a good choice because it leverages one of the preattentive attributes humans have known as line length to easily compare what agencies have more total floors and floors below grade than others. The encoding type used for the x-axis of the Agency Name field was nominal because it is a discrete category that has no significant order. Meanwhile, for the y-axis made up of the fields of the sum of Total Floors and Floors Below Grade I used quantitative because they are continuous numerical values. I maintained the same colors used in Homework #7 because I think they do not cause an overwhelming clash since they are within the same color family. These colors are also different enough for someone to easily identify where the cut off between floors below grade and the rest of the floors are.

In Homework #7, I wrote that with more time I wanted “each record [to be] unique to the building… [allowing] the audience to get more value out of the stacked bar plot by seeing the unique number of floors that summed to the total floors value.” To address this issue, I created a new pandas dataframe that looped over each of the unique location names and only added duplicates if the building was occupied by multiple agencies. Without the repeated buildings that were in the first iteration of the visualization, the sum of total floors y-axis scale only reaches 300 as opposed to 4,000. For this reason, I did not find it necessary to add the filter to make sure that there was a sum of total floors greater than zero since it is easier to see the smaller values, especially with the ability to zoom in. 

One of the changes in bringing this graph into Altair was how the layering of the two bar graphs worked. In vega-lite, I created two layers that are within the same plot whereas in Altair I had to create two distinct charts and then join them together using the operator form of the layer chart.

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jgl4/mis/blob/main/Workbook.ipynb" text="The Analysis" %}
</div>