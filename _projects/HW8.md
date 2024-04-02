---
name: HW8 Visualization Project
tools: [Python, HTML, vega-lite]
description: This is a "showcase" project that uses vega-lite for interactive viz for building usages!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

## Building Usage Analysis

Here is an interactive visualization of building counts by congressional district:

<vegachart schema-url="{{ site.baseurl }}/assets/json/viz1.json" style="width: 100%"></vegachart>




For the visualization 1, I did the bar chart to visualize the building counts v. the congress dist. Because this is a plot to show the number of buildings of different congress dist, which is showing the sum/counts, so the bar chart is clear for audiences to see. The encoding type are different for x axis and y axis, for x axis, the variable is “Congress Dist”, which have number from 0 to 18, it is not regarded as quantitative because it is discrete and is is a symbol variable so I encoded them as ordinal, which could make the plot’s x axis more easy to read. I did not do a lot of transformations for plot 1, but I pre-processed the data which could be used more clearly. I used groupby() method to group the original big building dataset by the congress dist. Then I used count() method to count the number of buildings of each congress dist and then make them as two columns to the new dataframe called district_count. Then I used the new dataframe as the data to make the visualization 1. Also, for the interactive part, this viz 1 is quite basic for panning and zooming, also, this viz 1 enables users to hover on one bar and by the tooltip, once users hover on the bar, it will display the congress dist number and also the building counts.

Here is an interactive visualization of building counts of different usages by congressional district:


<vegachart schema-url="{{ site.baseurl }}/assets/json/viz2.json" style="width: 100%"></vegachart>





For visualization 2, it is quite an “upgrade” of viz 1. I changed it to be more specifically. It is also quite similar to what I did for HW7, but the difference is I group the data by congress dist, which is a variable that I did not include in HW7. And I added the dropdown for different usage descriptions, in order to provide a more specific interaction between the plot and users. Users could select the dropdown’s usage and once users change the selection, the plot also change accordingly, other than this, it is generally the same logic with visualization 1. The reason why I choose bar plot here is also the same to the viz 1, because this is an aggregation of different congress dist, so the bar plot is one of the most suitable method to show. The encoding types are also quite the same, the count() here is the same as the number of buildings in viz1. And the congress dist is ordinal. The interactive way here does not include panning and zooming, but same to the viz 1, it has the hover-selection interaction. 


## The Data & Methods

Below are links to the data and the Jupyter notebook used for these visualizations:

<div class="left">
  {% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv" text="The Data" %}
</div>

<div class="right">
  {% include elements/button.html link="https://github.com/0HANNING2/0HANNING2_jekyll_page/blob/b420d13e8f8b248ce57a7f5ec798aad40017682b/python_notebooks/Workbook.ipynb" text="The Analysis" %}
</div>
