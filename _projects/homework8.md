---
name: Homework 8
tools: [Python, HTML, vega-lite]
image: assets/pngs/homework8cover.png
description: Homework 8 submission
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Homework 8

## Visualization #1

<vegachart schema-url="{{ site.baseurl }}/assets/json/chart1_hw8.json" style="width: 100%"></vegachart>

### Write Up
INSERT THE WRITE UP HERE

## Visualization #2

<vegachart schema-url="{{ site.baseurl }}/assets/json/chart2_hw8.json" style="width: 100%"></vegachart>

### Write Up
INSERT THE WRITE UP HERE

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jgl4/mis/blob/main/Workbook.ipynb" text="The Analysis" %}
</div>