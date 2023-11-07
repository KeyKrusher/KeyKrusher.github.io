---
name: Homework 8
tools: [Python, HTML, vega-lite]
image: assets/pngs/chart1.png
description: This is a small project for homework 8.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# First visualization
<vegachart schema-url="{{ '/assets/json/chart1.json' | relative_url }}" style="width: 100%"></vegachart>

## Analysis
In this visualization, we explore the distribution of buildings across various agencies. Each bar represents the number of buildings managed by a specific agency, providing a clear visual hierarchy of agencies by their infrastructure scale. The 'Agency Name' is encoded as a nominal variable on the x-axis, and the 'Number of Buildings' as a quantitative variable on the y-axis. A color scheme of steelblue for selected agencies and light gray for others was chosen to highlight the user's selection, enhancing the interactivity and focus. Compared to Homework #7, this visualization has been modified with interactive selection features, allowing viewers to click on an agency to isolate and examine its data more closely. 

# Second visualization
<vegachart schema-url="{{ '/assets/json/chart2.json' | relative_url }}" style="width: 100%"></vegachart>

## Analysis
The second visualization provides a historical perspective by showcasing the years in which buildings were acquired. It is a histogram where the x-axis represents the 'Year Acquired' as a quantitative variable, binned into 50 distinct intervals for clarity, and the y-axis shows the 'Number of Buildings' as a quantitative count. The color encoding is consistent with the first visualization for a unified look and feel. Data transformation included filtering out records with 'Year Acquired' before 1867 to focus on relevant years as the University of Illinois Urbana-Champaign was founded that year. This removes certain extraneous values that have a year of '0'. This plot differs from Homework #7 by incorporating a dynamic binning approach and an interactive element that allows users to hover over bars to see detailed tooltip information.

It's also worth noting that I had to write some css code to fix an issue with the tooltips, under their initial specification if the user was in 'dark mode' as I often am. The 'Count of Records' part of the tooltip had a dark grey background, so you couldn't read it very easily. Through some research, I was able to find the right 'id' to use in order to change the styling so that it would be readable.

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/KeyKrusher/HW8/blob/master/HW8.ipynb" text="The Code" %}
</div>
