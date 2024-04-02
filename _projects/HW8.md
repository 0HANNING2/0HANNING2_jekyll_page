---
title: "Your Visualization Title"
date: 2024-04-02
tags: [Data Visualization]
description: "This post contains interactive visualizations of building usage."
---


For the visualization 1, I did the bar chart to visualize the building counts v. the congress dist. Because this is a plot to show the number of buildings of different congress dist, which is showing the sum/counts, so the bar chart is clear for audiences to see. The encoding type are different for x axis and y axis, for x axis, the variable is “Congress Dist”, which have number from 0 to 18, it is not regarded as quantitative because it is discrete and is is a symbol variable so I encoded them as ordinal, which could make the plot’s x axis more easy to read. I did not do a lot of transformations for plot 1, but I pre-processed the data which could be used more clearly. I used groupby() method to group the original big building dataset by the congress dist. Then I used count() method to count the number of buildings of each congress dist and then make them as two columns to the new dataframe called district_count. Then I used the new dataframe as the data to make the visualization 1. Also, for the interactive part, this viz 1 is quite basic for panning and zooming, also, this viz 1 enables users to hover on one bar and by the tooltip, once users hover on the bar, it will display the congress dist number and also the building counts.

<script type="text/javascript">
  fetch('https://raw.githubusercontent.com/0HANNING2/0HANNING2_jekyll_page/388c7c446512ddaa10df60fda6dbb98ac953b7e5/assets/json/viz1.json')
    .then(response => response.json())
    .then(vegaSpec => {
      vegaEmbed('#visualization', vegaSpec);
    })
    .catch(err => console.error(err));
</script>


