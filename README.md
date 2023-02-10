# The Impact of Interest Rates on Recession, Inflation and the Global Economy
## The Most Interesting Team: Armann Andaya, Kenan White, Michelle Owino, Riley Unverferth and Justin Dean
______________________________________________________________________________________________________________________
![image](https://user-images.githubusercontent.com/119831680/217723305-0bce79b8-4c06-4c5f-9a0e-2298e6ecbbb3.png)

## Background
Recently, the Federal Reserve, the US central bank has been increasing the interest rates to stabilize the economy. Since March of 2022 the rate change (bps) has been increased 8 times. The Fed was created to help the United States economy run smoothly by monitoring several economic indicators, such as inflation, unemployment, consumer prices, and gross domestic product (GDP). The increasing rates are affecting all of us. Rate hikes generally mean higher credit card rates, higher interest on car and loans, and even mortgages. 

Our goal for this project is to analyze how interest rate hikes and drops impact the economy. 

## Methodology
For this analysis we used FRED to extract data. Data was from 1940s to 2022.  FRED is short for Federal Reserve Economic Data. It’s an online database consisting of hundreds of thousands of economic data time series from scores of national, international, public, and private sources. 

# Analysis
## Interest Rate vs GDP
![mergeddf](https://user-images.githubusercontent.com/119654958/217726303-d9fefcf9-6e04-46d4-866a-bcfdce5efebe.png)

This graph is of the two data frames merged (interest rate and GDP) from 1940s to 2022. GDP is trending upward. Interest rates fluctuates throughout the years. It was the highest in the 1980s at around 19%. At first glance it seems as though there is no relationship between the two variables but as we look closer, we notice that between 1940s to 1990 GDP was growing at a slower rate when compared to 1990 to 2022. At the same time interest rates grew significantly from 1940s to 1990s and then started decreasing. The average GDP annual growth rate from 1962 to 1981 was 1%. While the average GDP annual growth rate from 1982 to 2021 was 8%. 

In contrast, the average interest rates from 1962 to 1981 was 6.59%. While the average interest rate from 1982 to 2021.  The data suggest that when the Feds started aggressively decreasing the interest rates the GDP grew at a higher rate.  

![scatterplot](https://user-images.githubusercontent.com/119654958/217726395-5d3bddaa-1bec-41c5-8798-d7959b0dd0c1.png)

To see how closely the two variables relate to one another we performed a linear regression. The correlation coefficient r is 0.5. This supports the conclusion that there is a weak to moderate linear relationship between GDP and interest rates. Higher interest rates can slow down the economy.

# Interest Rate vs Inflation
Economic forces, both intentional and unforeseen, are constantly impacting the US economy. In the US, the inflation rate is one metric used to determine the health of the economy. A higher inflation rate means that consumers are generally spending more on goods and services. A lower inflation rate means that consumers are generally spending less on goods and services. In times of high inflation, the Fed will raise the interest rate to curb inflation.

![image](https://user-images.githubusercontent.com/119831680/217729856-39dc72c1-241a-42e1-959f-bd72120f1788.png)

The inflation rate in the US from 1954 - 2022 (shown above) has certianly fluctuated with its peak in the 1980s.

![image](https://user-images.githubusercontent.com/119831680/217730294-12943a91-8b7c-4a66-9063-75216189205c.png)

The above graph shows that the interest rate follows inflation. This make sense considering the main tool the FED uses to slow inflation is raising the interest rate.

![image](https://user-images.githubusercontent.com/119831680/217731389-b5ed7629-f754-47b0-8021-0a0471e741a0.png)

The r-value is 0.710. The represents a strong correlation between inflation and interest rate. This strong correlation indicates that raising the interest rate by the fed is a working solution to combat rising inflation.

# Interest Rate vs Unemployment Rate

 ![image](https://user-images.githubusercontent.com/119831680/217732920-9bcf2259-8227-43f1-b25b-fdc42f45cbcc.png)
 
 ![image](https://user-images.githubusercontent.com/119831680/217733063-a8ceb393-f6a6-48ae-9d71-a5986dfefb8d.png)
 
 # The Global Impact of the US Federal Interest Rate

To see if the Federal Interest Rate had an impact on the economies of other countries, we chose three countries: one with an economy close in size to ours, one with an economy around the bottom of the list of the 50 biggest economies, and a developing country. The countries are China, Finland, and Sudan respectively, and were chosen because they all had complete data of their GDPs as early as the 1960s on FRED. 

![int_vs_china_gdp_line](https://user-images.githubusercontent.com/117890937/217742813-293f7592-8471-42e0-a79d-33aace71f07a.svg)
![int_vs_fin_gdp_line](https://user-images.githubusercontent.com/117890937/217742826-4af2e044-d5c3-47ea-8917-3b4f6b479ac9.svg)
![int_vs_sudan_gdp_line](https://user-images.githubusercontent.com/117890937/217742851-cf24cb8b-1be2-4de8-a16a-84263256bc1f.svg)

Using the data pulled from the FRED API, we were able to assemble a DataFrame and create graphs that put the Federal Interest Rate against the GDPs of each country. In order to more clearly see the GDP trajectories, the Fed Interest Rate was multiplied by 1,000,000, 20,000, and 10,000 for China, Finland, and Sudan, respectively. 

![int_vs_china_gdp_plot](https://user-images.githubusercontent.com/117890937/217743578-831d7dff-d85a-42fe-af73-b72e88f4200f.svg)
![int_vs_fin_gdp_plot](https://user-images.githubusercontent.com/117890937/217743602-8896b55a-86bb-4b21-8747-8d0d2d77d241.svg)
![int_vs_sudan_gdp_plot](https://user-images.githubusercontent.com/117890937/217743618-a8392ebf-17d7-4757-b29c-4b0f866b4881.svg)

After plotting a linear regression, we found only moderate or weak negative correlations between the two. This generally proves a null hypothesis: the Federal Interest Rate does not have a strong impact on the economies of other countries.
 
 # Interest Rate vs Other Economic Factors
 
![image](https://user-images.githubusercontent.com/119831680/217733369-8a159e41-2438-4ab3-939f-ab33bd1f6f16.png)
 
![image](https://user-images.githubusercontent.com/119831680/217733551-68d3d67c-3395-493b-af97-123e04fb3e66.png)



### Dependancies 

- import pandas as pd
- import numpy as np
- import requests
- import json
- import matplotlib.pyplot as plt
- from datetime import datetime
- from pprint import pprint
- from scipy.stats import linregress
- import scipy.stats as st
- import matplotlib.dates as mdates
- from config import fred_key

### Conclusion 

The strong correlation between interest rates and inflation suggests  that raising the interest rate is a working solution to combat rising inflation.

Interest rate and unemployment rates are related, but rising interest rates don't necessitate low unemployment rates.

There is a weak to moderate linear relationship between GDP and interest rates. Higher interest rates can slow down the economy. 

Rises and falls of the Federal Interest Rate do not affect the Global Economy.

There is no definitive economic indicator that can predict the next recession. 

Retail sales, real personal income, and the industrial production index outperform interest rate in correlation to GDP. 



### Data Source

"https://api.stlouisfed.org/fred/series/observations?"
