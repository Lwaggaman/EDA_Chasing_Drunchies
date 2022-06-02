## Chasing Drunchies
The goal of this project is to aid a Food Truck owner in branching out to nightlife in NYC in a pandemic.

![](https://i.imgur.com/YeGU0Ap.png)


Alcohol consumption tricks the brain into starvation mode and stimulates hunger, a phenomenon known as the 'drunchies'[](https://www.healthline.com/health-news/got-the-drunchies-why-you-feel-hungry-when-youre-drunk)  . This is why show that the average event-goer spends 13% of their budget in late-night snacks[](https://f.hubspotusercontent00.net/hubfs/8020908/DS01_Nightlife%20Spending%20Study.pdf?utm_medium=email&_hsmi=93438620&_hsenc=p2ANqtz-8U6ZzwcZD3viqHxCpLrvy_EXyxj-99EyUoXe0B_BmNgINPYir9Zq9oiuIp78vTThtjm_m_aZkO2UjuJ5BOfTal2DMjIQ&utm_content=93438620&utm_source=hs_automation) .

This presents an opportunity for food food truck owners who want to expand. While the pandemic has been good to food truck owners, nightlife has been greatly impacted by it.

#### **Solution: EDA**
Food truck owners would be right to be hesitant, which is why I set out to help them make data-driven decisions though Exploratory Data Analysis.

My work attempts to answer the following questions:

-   _Has Nightlife recuperated as NYC reopens?_
-   _If it has shown signs of recuperating, has this trend been maintained or was this just 'Reopening' enthusiasm and activity started to wane as soon as COVID 19 cases started to rise again?_
-   _What are the best spots to take advantage of late-night dwellers' spending on snacks?_



#### **Design**
-   **Nightlife**: Areas with high concentration of licenses to serve alcohol.
-   **Activity**: NYC late night party-goers, unlike in other big cities, rely mostly on the subway for their transportation to and from events. [](https://f.hubspotusercontent00.net/hubfs/8020908/DS01_Nightlife%20Spending%20Study.pdf?utm_medium=email&_hsmi=93438620&_hsenc=p2ANqtz-8U6ZzwcZD3viqHxCpLrvy_EXyxj-99EyUoXe0B_BmNgINPYir9Zq9oiuIp78vTThtjm_m_aZkO2UjuJ5BOfTal2DMjIQ&utm_content=93438620&utm_source=hs_automation). This makes MTA turnstile data a reliable sample for representation of the movement patterns of people in NYC out for the night.
-  **'Recuperated'**: To determine if nightlife has, in fact, recuperated, I will use compare activity levels from 2021 to the same periods in 2019 and 2020. This will allow me to contrast the 2021 late-night traffic against the lows of 2020 and pre-pandemic levels of 2019 and see if any increase in activity was sustained as the ‘reopening’ excitement passed.
![](https://i.imgur.com/cmnBSn1l.png)
![](https://i.imgur.com/cmnBSn1m.png)
#### Data
-   MTA turnstile data.
-   Liquor Authority Current List of Active Licenses.
-   Subway stations’ coordinates.

#### Tools
-   SQLAlchemy to query into Python from database.
-   Pandas and NumPy for data wrangling.
-   Fuzzywuzzy to match station names from different data sources.
-   Matplotlib, Seaborn, and GeoPandas for visualizations.
