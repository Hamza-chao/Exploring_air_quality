# Project - CS 625, Spring 2024

   Mohammed-Hamza Chao
   
Due: Apr 12 by 11:59 pm

## Exploring Environmental Trends: Air Quality and Commuting Patterns Across States

### I. Datasets: 
For this project, I used four distinct datasets:

1. Air Pollution Dataset: This dataset, available at [Data Society](https://data.world/data-society/us-air-pollution-data), provides comprehensive information on air pollution across the United States.

2. Commute Mode Dataset: The dataset, sourced from the [Bureau of Transportation Statistics (BTS)](https://www.bts.gov/browse-statistical-products-and-data/state-transportation-statistics/commute-mode), offers insights into commuting patterns and modes of transportation used by residents.

3. Population Datasets: Population data spanning from 2000 to 2016 were obtained from the U.S. Census Bureau's [Population Estimates Program](https://www2.census.gov/programs-surveys/popest/datasets/), facilitating demographic analysis.

4. State Codes Dataset: This dataset, retrieved from [OpenDataSoft](https://public.opendatasoft.com/explore/dataset/georef-united-states-of-america-state/export/?flg=en-us&disjunctive.ste_code&disjunctive.ste_name&sort=year), provides information on state codes necessary for geographical mapping and analysis.

### II. Questions
 #### 1- Is there any correlation between the mode of commute and air pollution levels from 2000 to 2016?
![](https://i.ibb.co/KVxXKtP/air-ezgif-com-video-to-gif-converter-4.gif)

Link to the chart: [https://colab.research.google.com/drive/13XR3Mrmnk8zkY_20SsQ4OiFTnDwvUegF#scrollTo=e0f3c810-1fe1-45c6-9090-53624544e825&line=1&uniqifier=1](https://colab.research.google.com/drive/1mmQuAl0U9vuQReWKF-nNkd4-K1Ah1U8U?authuser=2#scrollTo=e0f3c810-1fe1-45c6-9090-53624544e825&line=1&uniqifier=1)

Left Idiom: Line Chart / Mark: Line
| Data: Attribute | Data: Attribute Type  | Encode: Channel | 
| --- |---| --- |
| population of green modes | quantitative | vertical spatial region (y-axis) |
| Year | temporal | horizontal position on a common scale (x-axis) |

Right Idiom: Line Chart / Mark: Line
| Data: Attribute | Data: Attribute Type  | Encode: Channel | 
| --- |---| --- |
| Pollutants Mean | quantitative | vertical spatial region (y-axis) |
| Date Local | temporal | horizontal position on a common scale (x-axis) |

Explanation

&nbsp;&nbsp;&nbsp;&nbsp;I think this chart effectively demonstrates the connection between pollutants and commute modes. I focused on "green modes" of transportation, which include options like public transportation, cycling, walking, remote work, carpooling, taxi usage, and other eco-friendly alternatives. These modes are generally considered less harmful to the environment compared to driving alone.

Covering a span of 16 years from 2000 to 2016, the chart allows us to observe how the adoption of these modes has changed over time. On the other hand, the second chart examines the "average pollutants," encompassing gases such as NO2, SO2, CO, and O3, all significant contributors to air pollution. Also spanning the same 16-year period, this chart seeks to uncover any correlations between the two datasets.

The results were unexpected; they contradicted the anticipated outcome. Despite an increase in the usage of green transportation modes in some states, there wasn't a consistent decrease in pollutant levels. This suggests the presence of other factors influencing air quality instability.

Final Thoughts

&nbsp;&nbsp;&nbsp;&nbsp;Creating these charts presented challenges, particularly in visualizing the data effectively due to the large number of states involved (50 in total). To address this issue, I discovered a solution using Altair that allowed me to implement a dropdown menu. This feature enables users to select a specific state and view the visualizations accordingly, ensuring clarity and ease of interpretation.

Additionally, I encountered the need to merge the commute modes dataset with a population dataset for normalization purposes. This step was crucial to ensure accurate comparisons and meaningful insights across different states and years.

##### a. Subquestion: Is there a relationship between commute mode choice and specific air pollutants?

![](https://i.ibb.co/SPrM4C6/charts3.png=20x20)
![](https://i.ibb.co/pQXH8jy/chart2.png=20x20)
![](https://i.ibb.co/BBCLQ83/charts1.png=20x20)
![](https://i.ibb.co/y0mBz6t/charts.png=20x20)

Link to the chart: https://colab.research.google.com/drive/1mmQuAl0U9vuQReWKF-nNkd4-K1Ah1U8U?authuser=2#scrollTo=acb2fe48-33f6-46e4-a902-22a96a00af21&line=4&uniqifier=1

First Idiom: hexbin plot  / Mark: Point
| Data: Attribute | Data: Attribute Type  | Encode: Channel | 
| --- |---| --- |
| NO2 AQI | quantitative | vertical spatial region (y-axis), color |
| Drove alone| quantitative | horizontal position on a common scale (x-axis), color |

Second Idiom: hexbin plot  / Mark: Point
| Data: Attribute | Data: Attribute Type  | Encode: Channel | 
| --- |---| --- |
| O3 AQI | quantitative | vertical spatial region (y-axis), color |
| Drove alone | quantitative | horizontal position on a common scale (x-axis), color |

Third Idiom: hexbin plot  / Mark: Point
| Data: Attribute | Data: Attribute Type  | Encode: Channel | 
| --- |---| --- |
| SO2 AQI | quantitative | vertical spatial region (y-axis), color |
| Drove alone | quantitative | horizontal position on a common scale (x-axis), color |

Fourth Idiom: hexbin plot  / Mark: Point
| Data: Attribute | Data: Attribute Type  | Encode: Channel | 
| --- |---| --- |
| CO AQI | quantitative | vertical spatial region (y-axis), color |
| Drove alone | quantitative | horizontal position on a common scale (x-axis), color |

Explanation

&nbsp;&nbsp;&nbsp;&nbsp;The hexbin plots aimed to assess whether solo driving correlates with pollutant levels. By analyzing driving populations across all states from 2000 to 2016, I created hexbin charts to pinpoint concentration areas. However, the results were inconclusive. While SO2 AQI and CO AQI plots indicated concentration in regions with lower AQI values and driving populations, NO3 AQI and O3 AQI charts showed increased AQI levels despite consistent driving populations. This suggests no direct link between pollutant AQIs and solo driving populations, possibly due to other factors like industrial gas emissions.

Final Thoughts

&nbsp;&nbsp;&nbsp;&nbsp;Creating these charts presented several challenges. Initially, I had to merge multiple datasets, with the first merge focusing on normalizing the driving-alone population data. Following that, I merged it with the pollutant dataset. After merging, I needed to clean the data to ensure accuracy. Finally, I visualized the cleaned data using hexbin charts.

####  2. How are commute modes of transportation and air pollution levels distributed across all states from 2000 to 2016?

Air Pollution

![](https://i.ibb.co/hMb2tvB/air-ezgif-com-video-to-gif-converter.gif)

Commute Modes

![](https://i.ibb.co/dmRZf8s/commute-ezgif-com-video-to-gif-converter.gif)

First Idiom: Choropleth Map plot  / Mark: Geoshape
| Data: Attribute | Data: Attribute Type  | Encode: Channel | 
| --- |---| --- |
| Type | MultiPolygon | color |

Second Idiom: Choropleth Map plot  / Mark: Geoshape
| Data: Attribute | Data: Attribute Type  | Encode: Channel | 
| --- |---| --- |
| Type | MultiPolygon | color |

Explanation

For these charts, my goal was to illustrate the distribution of various pollutants across all states, as well as the distribution of different commute mode percentages across all states averaging the values from 2000 to 2016.

Final Thoughts

For these charts, I aimed to enhance clarity by implementing a dropdown menu selection feature. To achieve this, I needed to transpose certain columns into rows, preparing them for integration with the dropdown option.

### References

https://altair-viz.github.io/

https://seaborn.pydata.org/

https://matplotlib.org/stable/users/explain/colors/colormaps.html

https://www.data-to-viz.com/graph/density2d.html

https://pandas.pydata.org/docs/index.html
