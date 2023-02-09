# The Impact of Intrest Rates on Recession, Inflation and the Global Economy
## The Most Interesting Team: Armann Andaya, Kenan White, Michelle Owino, Riley Unverferth and Justin Dean
______________________________________________________________________________________________________________________
![image](https://user-images.githubusercontent.com/119831680/217723305-0bce79b8-4c06-4c5f-9a0e-2298e6ecbbb3.png)

## Backround
Recently, the Federal Reserve, the US central bank has been increasing the interest rates to stabilize the economy. Since March of 2022 the rate change (bps) has been increased 8 times. The Fed was created to help the United States economy run smoothly by monitoring several economic indicators, such as inflation, unemployment, consumer prices, and gross domestic product (GDP). The increasing rates are affecting all of us. Rate hikes generally mean higher credit card rates, higher interest on car and loans, and even mortgages. 

Our goal for this project is to analyze how interest rate hikes and drops impact the economy. 

## Methodology
For this analysis we used FRED to extract data. Data was from 1940s to 2022.  FRED is short for Federal Reserve Economic Data. It’s an online database consisting of hundreds of thousands of economic data time series from scores of national, international, public, and private sources. 

# Analysis
## Intrest Rate vs GDP
![mergeddf](https://user-images.githubusercontent.com/119654958/217726303-d9fefcf9-6e04-46d4-866a-bcfdce5efebe.png)

This graph is of the two data frames merged (interest rate and GDP) from 1940s to 2022. GDP is trending upward. Interest rates fluctuates throughout the years. It was the highest in the 1980s at around 19%. At first glance it seems as though there is no relationship between the two variables but as we look closer, we notice that between 1940s to 1990 GDP was growing at a slower rate when compared to 1990 to 2022. At the same time interest rates grew significantly from 1940s to 1990s and then started decreasing. The average GDP annual growth rate from 1962 to 1981 was 1%. While the average GDP annual growth rate from 1982 to 2021 was 8%. 

In contrast, the average interest rates from 1962 to 1981 was 6.59%. While the average interest rate from 1982 to 2021.  The data suggest that when the Feds started aggressively decreasing the interest rates the GDP grew at a higher rate.  

![scatterplot](https://user-images.githubusercontent.com/119654958/217726395-5d3bddaa-1bec-41c5-8798-d7959b0dd0c1.png)

To see how closely the two variables relate to one another we performed a linear regression. The correlation coefficient r is 0.5. This supports the conclusion that there is a weak to moderate linear relationship between GDP and interest rates. Higher interest rates can slow down the economy.

# Interest Rate vs Inflation
Economic forces, both intentional and unforeseen, are constantly impacting the US economy. In the US, the inflation rate is one metric used to determine the health of the economy. A higher inflation rate means that consumers are generally spending more on goods and services. A lower inflation rate means that consumers are generally spending less on goods and services. In times of high inflation, the Fed will raise the interest rate to curb inflation.

![image](https://user-images.githubusercontent.com/119831680/217729856-39dc72c1-241a-42e1-959f-bd72120f1788.png)

The inflation rate in the US from 1954 - 2022 (shown above) has certianly flucuated with its peak in the 1980s.

![image](https://user-images.githubusercontent.com/119831680/217730294-12943a91-8b7c-4a66-9063-75216189205c.png)

The above graph shows that the interest rate follows inflation. This make sense since the main tool the FED uses to slow inflation is raisingthe intrest rate

![image](https://user-images.githubusercontent.com/119831680/217731389-b5ed7629-f754-47b0-8021-0a0471e741a0.png)

The r-value is 0.710. The represents a strong correlation between inflation and interest rate. This strong correlation indicates that raising the interest rate by the fed is a working solution to combat rising inflation

# Interest Rate vs Unemployment Rate

 ![image](https://user-images.githubusercontent.com/119831680/217732920-9bcf2259-8227-43f1-b25b-fdc42f45cbcc.png)
 
 ![image](https://user-images.githubusercontent.com/119831680/217733063-a8ceb393-f6a6-48ae-9d71-a5986dfefb8d.png)
 
 # Interest Rate vs Other Economic Factors
 
![image](https://user-images.githubusercontent.com/119831680/217733369-8a159e41-2438-4ab3-939f-ab33bd1f6f16.png)
 
![image](https://user-images.githubusercontent.com/119831680/217733551-68d3d67c-3395-493b-af97-123e04fb3e66.png)

# The Global Impact of the US Federal Intrest Rate

This is all you, Riley!

### Dependancies 

import pandas as pd
import numpy as np
import requests
import json
import matplotlib.pyplot as plt
from datetime import datetime
from pprint import pprint
from scipy.stats import linregress
import scipy.stats as st
import matplotlib.dates as mdates
from config import fred_key

### Data Source

"https://api.stlouisfed.org/fred/series/observations?"
