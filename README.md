# Slice Demand Project 

## Project Overview: 

A challenge a local Miami restaurant faces is the cost of waste associated with their menu items. There are a variety of factors that might influence the performance of a restaurant daily. With that said, the main question becomes: how can we reduce waste based on historical data of the restaurant to increase or maximize profits? My project intends to address the number of slices the restaurant should produce to minimize waste. This includes exploring the relationships between the number of slices sold and other factors that the owners believe could impact the demand at certain points throughout the year. Using machine learning models, particularly time series models, restaurant owners can predict customer demand based on historical data. 



## Data Dictionary
#### Dataset
https://docs.google.com/spreadsheets/d/1j2NBFPLa7XLYg_B2TPCAy_oTp6ze0eRUaGnZPPVHeOQ/edit?usp=sharing
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

## Key Insights 
<img width="522" alt="image" src="https://github.com/user-attachments/assets/88b8cb86-02bf-44a5-9ff3-8235aba3becc">


