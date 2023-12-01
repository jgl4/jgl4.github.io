---
name: Final Project - Salmonella
tools: [Python, HTML, vega-lite]
image: assets/pngs/interactive_legend.png
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

<vegachart schema-url="{{ site.baseurl }}/assets/json/disease_chart.json" style="width: 100%"></vegachart>

## Salmonella Rates

<vegachart schema-url="{{ site.baseurl }}/assets/json/cutoff_chart.json" style="width: 100%"></vegachart>

## Serotype Counts

<vegachart schema-url="{{ site.baseurl }}/assets/json/bar_chart.json" style="width: 100%"></vegachart>

## Dashboard

<vegachart schema-url="{{ site.baseurl }}/assets/json/dashboard.json" style="width: 100%"></vegachart>

## Infantis

![chart.png](/assets/pngs/chart.png)

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://www.propublica.org/datastore/dataset/usda-poultry-plant-salmonella-inspection-data" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jnaiman/online_cv_public/blob/main/python_notebooks/test_generate_plots.ipynb" text="The Analysis" %}
</div>