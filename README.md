# Bike Sharing Analysis

## Project Name
This project involves the analysis of a bike-sharing dataset to understand the trends and factors affecting bike usage. The following sections provide a detailed analysis using various data visualization and statistical techniques.

## Problem Statement
This assignment is a programming assignment wherein you have to build a multiple linear regression model for the prediction of demand for shared bikes. You will need to submit a Jupyter notebook for the same. 
## Business Goal
You are required to model the demand for shared bikes with the available independent variables. It will be used by the management to understand how exactly the demands vary with different features. They can accordingly manipulate the business strategy to meet the demand levels and meet the customer's expectations. Further, the model will be a good way for management to understand the demand dynamics of a new market. 

## Data Dictionary
- instant: record index
- dteday : date
- season : season (1:spring, 2:summer, 3:fall, 4:winter)
- yr : year (0: 2018, 1:2019)
- mnth : month ( 1 to 12)
- holiday : weather day is a holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)
- weekday : day of the week
- workingday : if day is neither weekend nor holiday is 1, otherwise is 0.
+ weathersit : 
    - 1: Clear, Few clouds, Partly cloudy, Partly cloudy
    - 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
    - 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
    - 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
- temp : temperature in Celsius
- atemp: feeling temperature in Celsius
- hum: humidity
- windspeed: wind speed
- casual: count of casual users
- registered: count of registered users
- cnt: count of total rental bikes including both casual and registered

## Exploratory Data Analysis (EDA)

### Observations from the count plot:

- There is a significantly lower count of holidays.
- The count of working days is nearly double that of non-working days, indicating higher bike-sharing activity on working days.
- The majority of bike usage occurs during weather condition 1, which includes clear, few clouds, partly cloudy, and partly cloudy skies.

### Heatmap of Correlations

To visualize the correlations between numerical variables, a heatmap is generated. The following numerical columns are used:

- `yr`
- `holiday`
- `workingday`
- `temp`
- `hum`
- `windspeed`
- `cloudy`
- `lightrain`
- `spring`
- `summer`
- `winter`
- `Aug`
- `Dec`
- `Feb`
- `Jan`
- `May`
- `Nov`
- `Sep`
- `Sat`
- `Sun`

### Variance Inflation Factor (VIF)

#### Handling High VIF Values:

- **Perfect Multicollinearity:** The features `holiday`, `workingday`, `Sat`, and `Sun` have VIF values of `inf`, indicating perfect multicollinearity. This means that these features can be perfectly predicted by a combination of other features.
  
- **Feature Removal:** To handle perfect multicollinearity, we can remove one of the collinear features. For example, removing either `holiday` or `workingday`, and either `Sat` or `Sun`.

- **Recompute VIF:** After removing collinear features, the VIF should be recomputed to ensure that multicollinearity has been adequately addressed.

By managing multicollinearity through VIF analysis, we ensure that our regression model remains reliable.

## Conclusion

This analysis provides insights into the factors influencing bike-sharing usage. Further steps could include developing predictive models and optimizing bike-sharing operations based on these insights.

## Technologies Used
- Jupyter notebook
- Libraries - pandas, numpy, matplotlib.pyplot, seaborn
- Model library - sklearn, statsmodels 

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
- This project was inspired by upgrad/IIIT-B

**Author -Abhishek Pathak**
