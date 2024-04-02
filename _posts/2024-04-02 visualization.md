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



![corg](https://media.istockphoto.com/photos/welsh-corgi-picture-id962032196?k=20&m=962032196&s=170667a&w=0&h=NhIyQdJgVw0cw_EeLtP3LcLExLuiAWPwzL6_WsRKUfQ=)

## 5. The last thing

This is my final thing, probably would be great if this was a TL;DR or summary.  But I don't have that for you.  I have given you so little already, why start saying anything useful now?

Besides, all anybody wants is the DERP:

![MAXIMUM DERP](http://3.bp.blogspot.com/-AXnXOPZgqMk/Un-xCBAa4gI/AAAAAAAAsWA/z_lZsvDoCRk/s1600/derpstages.jpg)
