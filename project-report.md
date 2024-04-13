# Exploring Environmental Trends: Air Quality and Commuting Patterns Across States

## Project - CS 625, Spring 2024

   Mohammed-Hamza Chao
   
Due: Apr 12 by 11:59 pm

## I. Datasets: 
For this project, I utilized four distinct datasets:

1. Air Pollution Dataset: This dataset, available at [Data Society](https://data.world/data-society/us-air-pollution-data), provides comprehensive information on air pollution across the United States.

2. Commute Mode Dataset: The dataset, sourced from the [Bureau of Transportation Statistics (BTS)](https://www.bts.gov/browse-statistical-products-and-data/state-transportation-statistics/commute-mode), offers insights into commuting patterns and modes of transportation used by residents.

3. Population Datasets: Population data spanning from 2000 to 2016 were obtained from the U.S. Census Bureau's [Population Estimates Program](https://www2.census.gov/programs-surveys/popest/datasets/), facilitating demographic analysis.

4. State Codes Dataset: This dataset, retrieved from [OpenDataSoft](https://public.opendatasoft.com/explore/dataset/georef-united-states-of-america-state/export/?flg=en-us&disjunctive.ste_code&disjunctive.ste_name&sort=year), provides information on state codes necessary for geographical mapping and analysis.

## II. Questions
 ### 1- Is there any correlation between the mode of commute and air pollution levels from 2000 to 2016?
![](https://i.ibb.co/cTT2XRm/12-04-2024-19-54-08-REC-ezgif-com-video-to-gif-converter.gif)

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

#### Explanation

&nbsp;&nbsp;&nbsp;&nbsp;I think this chart effectively demonstrates the connection between pollutants and commute modes. I focused on "green modes" of transportation, which include options like public transportation, cycling, walking, remote work, carpooling, taxi usage, and other eco-friendly alternatives. These modes are generally considered less harmful to the environment compared to driving alone.

Covering a span of 16 years from 2000 to 2016, the chart allows us to observe how the adoption of these modes has changed over time. On the other hand, the second chart examines the "average pollutants," encompassing gases such as NO2, SO2, CO, and O3, all significant contributors to air pollution. Also spanning the same 16-year period, this chart seeks to uncover any correlations between the two datasets.

The results were unexpected; they contradicted the anticipated outcome. Despite an increase in the usage of green transportation modes in some states, there wasn't a consistent decrease in pollutant levels. This suggests the presence of other factors influencing air quality instability.

#### Final Thoughts

&nbsp;&nbsp;&nbsp;&nbsp;Creating these charts presented challenges, particularly in visualizing the data effectively due to the large number of states involved (50 in total). To address this issue, I discovered a solution using Altair that allowed me to implement a dropdown menu. This feature enables users to select a specific state and view the visualizations accordingly, ensuring clarity and ease of interpretation.

Additionally, I encountered the need to merge the commute modes dataset with a population dataset for normalization purposes. This step was crucial to ensure accurate comparisons and meaningful insights across different states and years.
