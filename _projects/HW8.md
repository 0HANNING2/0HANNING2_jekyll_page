---
title: "Your Visualization Title"
date: 2024-04-02
tags: [Data Visualization]
description: "This post contains interactive visualizations of building usage."
---


For the visualization 1, I did the bar chart to visualize the building counts v. the congress dist. Because this is a plot to show the number of buildings of different congress dist, which is showing the sum/counts, so the bar chart is clear for audiences to see. The encoding type are different for x axis and y axis, for x axis, the variable is “Congress Dist”, which have number from 0 to 18, it is not regarded as quantitative because it is discrete and is is a symbol variable so I encoded them as ordinal, which could make the plot’s x axis more easy to read. I did not do a lot of transformations for plot 1, but I pre-processed the data which could be used more clearly. I used groupby() method to group the original big building dataset by the congress dist. Then I used count() method to count the number of buildings of each congress dist and then make them as two columns to the new dataframe called district_count. Then I used the new dataframe as the data to make the visualization 1. Also, for the interactive part, this viz 1 is quite basic for panning and zooming, also, this viz 1 enables users to hover on one bar and by the tooltip, once users hover on the bar, it will display the congress dist number and also the building counts.

<div id="visualization"></div>
<script type="text/javascript">
  fetch('path') 
    .then(response => response.json())
    .then(vegaSpec => {
      vegaEmbed('#visualization', vegaSpec);
    })
    .catch(err => console.error(err));
</script>


# Example including vega-lite

Example comes from this [great blog post right here](https://blog.4dcu.be/programming/2021/05/03/Interactive-Visualizations.html) that was also used in [our test import script](https://github.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/blob/main/week01/test_imports_week01.ipynb).

We can use a vegachart HTML tag like so:

```
<vegachart schema-url="{{ site.baseurl }}/assets/json/cars.json" style="width: 100%"></vegachart>
```

<vegachart schema-url="{{ site.baseurl }}/assets/json/cars.json" style="width: 100%"></vegachart>

In theory, you can also use [Jekyll hooks](https://jekyllrb.com/docs/plugins/hooks/) to do it, but I haven't figured out a way that looks nice yet.


## Search The Data & Methods

Below is where we can put some links to both the data and the analysis code as buttons:

```
<div class="left">
{% include elements/button.html link="https://github.com/vega/vega/blob/main/docs/data/cars.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://blog.4dcu.be/programming/2021/05/03/Interactive-Visualizations.html" text="The Analysis" %}
</div>
```

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/vega/vega/blob/main/docs/data/cars.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jnaiman/online_cv_public/blob/main/python_notebooks/test_generate_plots.ipynb" text="The Analysis" %}
</div>

