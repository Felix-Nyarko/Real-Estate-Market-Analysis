# Introduction
This project explores housing rental trends using a real estate dataset to uncover valuable market insights for investors, property managers, and renters.


# Background
Driven by a quest to already understand the existing insights of real estate, this project was born from a dataset that contains rental property 
listings scraped from Tonaton.com, one of Ghana's leading online platforms. It provides valuable information on rental prices across various regions 
in Ghana, along with other property details.
## The questions I seek to answer;
1. Which locations (region/localities) have the highest rental yields (price per square meter)?
2. What is the price distribution by locality - and where are the most affordable vs. luxury hotspots?
3. Are furnished properties rented at a significant premium compared to unfurnished?
4. Which property type (flats, detached, etc.) dominates each region in terms of availability?
5. Identify the top 5 high-demand localities (lots of listings, high prices)
6. Localities that are undervalued (large floor area but relatively low price)
7. Properties with parking space


# Tools I Used
For my deep dive into the real estate market, I harnessed the power of several key tools;
- Power BI: The backbone of my analysis allowing me to create visualizations
- SQL : Used the tool for some basic EDA queries
- Github : Essential for version control and portfolio showcase

# The Analysis

# MARKET INSIGHTS

## 1. Which locations (region/localities) have the highest rental yields (price per square meter)?
The total average price per square meter is **14.38**. 
The locations in terms of regions with the highest rental yields are as follows;
| Regions       | Average price per SQM (GHS) |
|----------------|---------------------|
| Volta        | 457.14              |
| Northern        | 30.07                | 
| Eastern       | 20.79                | 
| Ashanti       | 18.61               |
| Greater Accra       | 14.33                |
| Western       | 9.06                |
| Central       | 9.02                |
| Brong Ahafo       | 4.70                |

 ![Highest Rental Yield](https://github.com/Felix-Nyarko/Real-Estate-Market-Analysis/blob/main/Question%201.png)

*A pie chart showing the average sqaure meters with regards to the region*


## 2. What is the price distribution by locality - and where are the most affordable vs. luxury hotspots?
The price distribution by locality shows that there are more luxury hotspots are in these five (5) localities and they are all located in Greater Accra;
- East Legon
- Spintex
- Airport Residential
- Accra Metropolitan
- Cantonments

![Distribution_By_Locality](https://github.com/Felix-Nyarko/Real-Estate-Market-Analysis/blob/main/Question%202.png)

*A Bar Chart showing the visual representation of the areas with the most distribution of afforadable and luxury accommodation units*


## 3. Are furnished properties rented at a significant premium compared to unfurnished?
Comparing the average price of furnished properties to unfurnished properties, you will discover that *furnished apartment attract 58.1%* of the market as compared to an *unfurnished apartment of 17.88%*

![Furnished_Properties_Vrs_Unfurnished_Properties](https://github.com/Felix-Nyarko/Real-Estate-Market-Analysis/blob/main/Question%203.png)

*A pie chart showing the impact of furnished and unfurnished on rentals*

## 4. Which property type (flats, detached, etc.) dominates each region in terms of availability?
From the table below, it is clear that the property type that dominates the market is the flats followed by detached units.
| Region       | Flat | Detached Units | 
|----------------|---------------------|------------------|
| Greater Accra          | 10,619             | 4,638              |
| Ashanti Region         | 500                | 159              | 
| Central        | 144                | 45              | 
| Northern        | 147                | 47              | 

![Dominant_Property_Type](https://github.com/Felix-Nyarko/Real-Estate-Market-Analysis/blob/main/Question%204.png)

*A Bar Chart showing the distribution of flats, detachedhomes, etc with regards to the regions*

# PRICING AND INVESTMENT STRATEGY
## 5. Identify the top 5 high-demand localities (lots of listings, high prices)
To identify localities that have high demand, I first created measures to count the total listings and for average price respectfully.
``
TotalListings = COUNTTROWS(HouseRentals)
``
``
AveragePrice = AVERAGE(HouseRentals(Price))
``
Using a scattered chart, Total Listings for X-axis, and Average Price for Y-axis.

![High_Demand_Localities](https://github.com/Felix-Nyarko/Real-Estate-Market-Analysis/blob/main/Question%205.png)

The top 5 high-demand localities include;
| Locality       | Number of Listings| Average Price | 
|----------------|---------------------|------------------|
| East Legon          | 2,565            | $14,000 | 
| Spintex      | 1,800                | $6,698 |
| Teshie        | 1,334                | $5,420
| Adenta        | 1,253                | $3,061
| Accra Metropolitan        | 1,035    | $9,181


## 6. Localities that are undervalued (large floor area but relatively low price)
To identify areas that are undervalued, I created a measure to determine the *Average Price Per Square Meter* and *Average Floor Area*
From the visual, it was discovered that **Volta Region** followed by **Nortern Region** have *larger floor area but offered relatively low price*

![Large_Floor_Area_Low_Price](https://github.com/Felix-Nyarko/Real-Estate-Market-Analysis/blob/main/Question%206.png)


## 7. Properties with parking space
On a broader scale, parking spaces didn't have direct impact on prices. It is only few areas that had direct relationsip with prices and they are predominantly located in 
Accra. Those areas are Cantonments, Burma Camp, etc.


![LProperties_with_Parking_Space](https://github.com/Felix-Nyarko/Real-Estate-Market-Analysis/blob/main/Question%207.png)


# What I learned
- Analytical Thinking in Real Estate: Learned how to interpret property data to identify market trends — such as rental yields, affordable housing zones, and luxury market clusters — and translate them into actionable business insights.

- Power BI Visualization & Storytelling: Enhanced my ability to design interactive dashboards that clearly communicate key findings, making complex housing data easy to understand for investors and decision-makers.
- Analytical Wizadry: leveled up my real-world puzzle-solving skills, turning questions into actionable, insigtful SQL queries.

# Conclusions
# Insights
1. **The locations (region) that have the highest rental yields** are Volta, Northern and Eastern because they offer the highest average per square meter.
2. **The price distribution by locality - in terms of the most luxury hotspots** are areas all within Greater Accra. In terms of the luxury, we are looking at Spintex,Cantonments, Airport Residential, East Legon and Accra Metropolitan (for the affordable ones)
3. **Furnished properties are rented at a significant premium compared to unfurnished**. This is because when you compare the average price of furnished properties to unfurnished properties, you will discover that furnished apartment attract 58.1% of the market as compared to an unfurnished apartment of 17.88%
4. **The property type (flats, detached, etc.) that dominates each region** in terms of availability are flats as they record high records in all the regions
5. **The top 5 high-demand localities that have lots of listings and attract high prices** are as follows; - East Legon, Spintex, Teshie, Adenta and Accra Metropolitan.
6. **Localities that are undervalued (large floor area but relatively low price)** are localities in the Volta Region
7. **Properties with parking spaces didn't have direct impact on prices**. It is only few areas that had direct relationsip with prices and they are predominantly located in Accra. Those areas are Cantonments, Burma Camp, etc.

# Closing Thoughts
