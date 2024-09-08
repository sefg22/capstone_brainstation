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


### Organization

#### Repository 

* `data` 
    - contains link to copy of the dataset (stored in a publicly accessible cloud storage)
    - saved copy of aggregated / processed data as long as those are not too large (> 10 MB)

* `model`
    - `joblib` dump of final model(s)

* `notebooks`
    - contains all final notebooks involved in the project

* `docs`
    - contains final report, presentations which summarize the project

* `references`
    - contains papers / tutorials used in the project

* `src`
    - Contains the project source code (refactored from the notebooks)

* `capstone.yml`
    - Conda environment specification

* `README.md`
    - Project landing page (this page)

* `LICENSE`
    - Project license

#### Dataset

... Google Drive links to datasets and pickled models

### Credits & References

... Include any personal learning
