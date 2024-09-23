# Slice Demand Project 

## Project Overview: 

A challenge a local Miami restaurant faces is the cost of waste associated with their menu items. There are a variety of factors that might influence the performance of a restaurant daily. With that said, the main question becomes: how can we reduce waste based on historical data of the restaurant to increase or maximize profits? My project intends to address the number of slices the restaurant should produce to minimize waste. This includes exploring the relationships between the number of slices sold and other factors that the owners believe could impact the demand at certain points throughout the year. Using machine learning models, particularly time series models, restaurant owners can predict customer demand based on historical data. 

## Data Dictionary

| Column Name        | Description                                        | Data Type     | Notes                          |
|--------------------|----------------------------------------------------|---------------|--------------------------------|
| **Date**           | Date associated to each column                     | `datetime64`  | Datetime Index                 |
| **Sold (Qty)**     | Total slices sold                                  | `int64`       |                                |
| **Produced (Qty)** | Total slices produced                              | `int64`       |                                |
| **Waste (%)**      | Percentage of slices wasted                        | `float64`     |                                |
| **Waste (Qty)**    | Total slices wasted                                | `int64`       |                                |
| **Temperature (Avg.)** | Average temperature of the day                 | `float64`     |                                |
| **Revenue/ Profit**| Total Profit of slices                             | `int64`       |                                |
| **Pepperoni**         | Binary column to indicate flavor                | `int64`      | OneHot encoded feature created from Flavor column|
| **Cheese**         | Binary column to indicate flavor                   | `int64`      | OneHot encoded feature created from Flavor column|
| **Napolitana**         | FBinary column to indicate flavor              | `int64`      | OneHot encoded feature created from Flavor column|
| **Primavera**         | Binary column to indicate flavor                | `int64`      | OneHot encoded feature created from Flavor column|
| **Vegetariana**         | Binary column to indicate flavor              | `int64`      | OneHot encoded feature created from Flavor column|
| **Season**         | Time of year for restaurants                             | `int64`      | Ordinally encoded due to order of season (ex: High season, etc.)|
| **Rain?**          | Binary column showing whether it rained or not that day | `int64`   |                                |

**Link:** https://docs.google.com/spreadsheets/d/1j2NBFPLa7XLYg_B2TPCAy_oTp6ze0eRUaGnZPPVHeOQ/edit?usp=sharing

## Key Insights 
<img width="531" alt="image" src="https://github.com/user-attachments/assets/07fe191b-6cf6-433b-8776-8342b4bf86ed">

Takeaways:
- There doesn't seem to be a clear trend on a day-to-day basis as shown by the inconsistent spikes throughout the trend visual. There is a big spike around March which is likely due to Miami being a hotspot for spring break which usually occurs around the month of March. 
    - It could be interesting to see if these patterns change on an hourly or weekly resampling of the data. 
- When it comes to the Seasonal visualization, we are able to see a strong seasonal component which is supported by the repeating patterns. When hovering over the plots you are able to determine a weekly cycle within the seasonal visualization. 
- The residuals show that there are some irregularities and noise that might need further investigation or might be resolved when incorporating other variables that might influence customer demand such as temperature and rainfall.
  
<img width="522" alt="image" src="https://github.com/user-attachments/assets/bf118744-9063-4ab7-b04b-b6ef5665b564">

 Takeaways: 
 - There is a strong positive correlation when lag is 1, which indicates that a past value might influence the next value heavily. 
 - There seems to be a repeated pattern for every seven lags which might indicate a weekly pattern. 

 <img width="522" alt="image" src="https://github.com/user-attachments/assets/4f780acb-b602-4dcf-9f7b-df9338036b15">
 
Takeaways: 
- A peak when lag is 1 seems to indicate that the AR(1) component might be relevant. Once again presenting the idea that the value of the previous day is influential to the next value. 
- A peak when lag is 7 seems to indicate that values from the previous week can be influential to the following or upcoming week. 
- A peak when lag is 8 seems to indicate that values from 8 days ago might be influential, however, this influence might not be as strong as when lag is 7. 



## Model Evaluations
<img width="556" alt="image" src="https://github.com/user-attachments/assets/21dbaf22-6307-40b6-ad68-8268a8434b30">

The first model showed an acceptable understanding of customer demand at the second and third fold but struggled with the first fold. Looping through different combinations might allow for the model to perform better in this regard. When it comes to our Auto Arima model, this model performed the worst and only showed an acceptable understanding of customer demand in the second fold which is something all of our models share. In terms of the Prophet model, it performed better than the aforementioned models but also struggled to capture customer demand on the first fold. Like our baseline model, attempting different combinations might also improve the model's performance within the first fold and also overall. Now, our last model, the LSTM neural network showed a consistent MAE across all folds which makes it our best model despite only outperforming other models in the first fold.

Below you can see a visual representation of our best model: 

<img width="320" alt="image" src="https://github.com/user-attachments/assets/c9e0008e-5f69-4762-a114-517965fe6fb0">

## Next Steps

- Productionizing the best-performing model into a dynamic dashboard for the owners of the pizza place.
- Evaluating model performance continuously.
- Improve the model as needed including more layers, changing the parameters, etc.
- Investigate other features that might affect demand (i.e. using rainfall amount instead of whether it rained or not.)




