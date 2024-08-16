# Slice Demand Project 

## Project Overview: 

An area of interest for me is hospitality, specifically: Restaurants. A challenge a restaurant could face is the cost of waste associated with their menu items. How can we reduce waste based on historical data of the restaurant to increase or maximize profits? My project intends to address the number of slices the restaurant should produce based on various factors that might impact the sales for each day. By using machine learning, especially time series models, restaurant owners can benefit from predicting their production values for everything on their menu and driving down the cost of unconsumed items. 


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
| **Flavor**         | Flavors of the slices                              | `object`      |                                |
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
