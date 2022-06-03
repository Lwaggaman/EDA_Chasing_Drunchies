
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

#### Data
-   MTA turnstile data.
-   Liquor Authority Current List of Active Licenses.
-   Subway stations’ coordinates.

#### Tools
-   **SQLAlchemy** to query into Python from database.
-   **Pandas** and **NumPy** for data wrangling.
-   **Fuzzywuzzy** to match station names from different data sources.
-   **Matplotlib**, **Seaborn**, and **GeoPandas** for visualizations.

### Results
#### Nightlife
Brooklyn and Manhattan have more nightlife, more tighly packed.
![](https://i.imgur.com/rEVjesz.png)
![](https://i.imgur.com/OBBGr6u.png)

The following are the 3 zipcodes with the highest concentration of establishments licensed to serve alcohol in Brooklyn and Manhattan.
![](https://i.imgur.com/1VdkyND.png)

#### Activity Levels
While late-night weekend traffic between 8pm and 4am in these zipcodes has doubled since reopening, it is nowhere near pre-pandemic levels.
![](https://i.imgur.com/NmdwS0J.png)

If we break it down by week, we can see that the difference between 2020 and 2021, understood to be people going out since reopening, gets smaller as time passes and Delta variant cases start increasing in NYC in August 2021.
![](https://i.imgur.com/r0in9Sd.png)


#### Best Location to Park
###### Brooklyn
This heatmap combines concentration of nightlife establishments per zip with the location and traffic of the subway stations within them. By considering location, we can see how close some stations are to each other.
![](https://i.imgur.com/qtxR22u.png)

- Zipcode 11201 contains three stations with a great amount of traffic very close to each other, making it a good place to park a food truck.
- Zipcode 11211 has the most nightlife establishments in the borough, and the station with the most amount of traffic (Bedford Av), along with two stations with high traffic very close together. 
![](https://i.imgur.com/n2X5Pn9.png)


###### Manhattan
Here you can see traffic in Manhattan stations contrasted with concentration of nightlife establishments by zip.
![](https://i.imgur.com/twYaNAm.png)
Once you zoom in on the 3 zipcodes with the most nightlife, you can see that some of the bubbles with the highest traffic disappear once we filter out those contained in the zipcodes. Stations like Times Sq-42 St are labeled as being in a different zipcode because they're on the other side of the street. Adjusting this will lead to better informed decisions.
![](https://i.imgur.com/wEg6cSu.png)
![](https://i.imgur.com/4MnrYeu.png)
- Zipcode 10036 has the two stations with the most traffic, but it must be considered that this is Times Sq traffic, where there are plenty of food vendors and the crowds are mostly tourists. You can see by the color depth in the heatmap that it has significantly less nightlife establishments than the other two zipcodes as well. 
- Zipcode 10019 has more nighlife establishments than 10036 and more traffic than 10003, so it could be a better option. Within it, 59 St station is a good option, since it has the most traffic, but somewhere near 7 Av is a good option as well, since two other stations, 50 St and 57 St, are three minutes away walking.
- Zipcode 10003 has less traffic but it has the most nighlife establishments in the borough and by parking between 8 St-NYU and Astor Pl stations we can reach the most people, including students who walk back home to NYU campus after a night out and don't register as subway traffic.

![](https://i.imgur.com/mJ1QfW8.png)

### Conclusion
While nightlife has not resumed to pre-pandemic levels, 1-2 million of the people that were staying home during the pandemic are visiting nightlife zip codes on weekend nights. Ultimately, it will be up to the food-truck owner to decide whether it is worth it to try to service them. If they decide to do so, I have indicated some of the best areas based on the information available, and they can make their final decision based on other factors, such as daytime route, place of residence, or ease of permits.