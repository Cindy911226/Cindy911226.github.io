---
name: IS445 Analysis of Building Data Visualizations
tools: [Python, HTML, vega-lite]
image: assets/pngs/cars.png
description: This is a HW6 interactive viz!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


## Visualization 1: Average Square Footage by Year Constructed with Usage Filter (Interactive)



```
<vegachart schema-url="{{ site.baseurl }}/assets/json/chart1.json" style="width: 100%"></vegachart>
```

<vegachart schema-url="{{ site.baseurl }}/assets/json/chart1.json" style="width: 100%"></vegachart>


In this plot, I am visualizing the **average square footage of buildings** grouped by their **year of construction** and **usage type** (e.g., office, residential, commercial). The chart uses a **bar chart** format to show how the average square footage has changed over time for each usage type. On the x-axis, I have mapped the **year constructed** as an ordinal variable, and on the y-axis, I’ve plotted the **average square footage** as a quantitative variable. I also applied **color encoding** to differentiate between building usage types, choosing a **categorical color scheme** to make it easy to distinguish between the various categories. I chose this color scheme because it provides clear contrasts between the different usage types, allowing for easier comparisons across years. The color is mapped to the **usage description**, and this distinction helps viewers quickly identify patterns specific to each usage type.

For data transformations, I grouped the dataset by **year constructed** and **usage description**, calculating the mean square footage for each combination. This was achieved through **Pandas’ groupby() function**. Afterward, I used `reset_index()` to prepare the aggregated data for use in the visualization. The interactivity in this plot is added through a **dropdown filter** for the **usage description**. This feature allows users to focus on a specific building usage type, which helps to isolate trends and makes the visualization more dynamic. The interactivity improves clarity by enabling viewers to explore the data more closely, and it makes the plot more engaging than a static chart. This interactivity, specifically the dropdown filter, enhances the user experience and makes the data easier to understand by enabling users to explore specific subsets of the data.


## Visualization 2: Distribution of Building Usage Across Locations

```
<vegachart schema-url="{{ site.baseurl }}/assets/json/chart2.json" style="width: 100%"></vegachart>
```

<vegachart schema-url="{{ site.baseurl }}/assets/json/chart2.json" style="width: 100%"></vegachart>



For the second plot, I am visualizing the **distribution of building usage types across different locations**. This is displayed using a **bar chart**, where the x-axis represents the **location** (such as park names) and the y-axis represents the **number of buildings** in each location. The **color encoding** is applied to differentiate between building usage types, just like in the first visualization, but I used a **sequential color palette** in this case to reflect the magnitude of the number of buildings. A sequential palette helps highlight the varying number of buildings by usage type, where darker colors represent higher counts of buildings. This visual encoding makes it easier to spot trends in the distribution, such as which usage types are more prevalent in particular locations.

The data for this visualization was transformed by using **Pandas' groupby() function** to aggregate the count of buildings by **location** and **usage description**. This transformation allowed me to show the count of buildings for each combination of usage type and location. Unlike the first visualization, there is no interactivity included in this plot, as it primarily focuses on providing a static comparison between the distribution of buildings. However, the design choice of grouping by location and usage type in the bar chart format provides a clear and accessible way to examine how buildings are distributed across different areas. Adding interactivity in future versions could improve exploration, but the simplicity of the current approach allows for immediate insights without additional complexity.



## Links to Data and Analysis

- [The Data](https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv)
- [The Analysis](https://github.com/Cindy911226/Cindy911226.github.io/blob/main/Workbook.ipynb)


<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/Cindy911226/Cindy911226.github.io/blob/main/Workbook.ipynb" text="The Analysis" %}
</div>

