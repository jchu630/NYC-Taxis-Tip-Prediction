# NYC-Taxis-Tip-Prediction
Using machine-learning to predict whether NYC taxi riders will leave a tip based on trip data. Analyzes key factors influencing tipping behavior using data-driven insights.

[NYC Taxis Tip Prediction](https://jchu630.github.io/NYC-Taxis-Tip-Prediction/)

## Project Rundown

### Overview

In the USA, many service workers rely heavily on tips for their income. Tips are voluntary payments given by customers in addition to the listed price. For yellow taxis in New York, tourist advice suggests tipping 15-20%.

This project utilizes a rich dataset from [New York Taxis](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page) to build a predictive model for tip amounts. The dataset includes two weeks of taxi trips in New York City, containing information on the time of day, day of the week, trip distance, fare price, number of passengers, and pickup/dropoff locations.

*Note that the two sets of data were too large to be added in the repo. Access them from the website [here](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page). 

### Main Task

We used data from the second week of February 2017 to construct a model that predicts tip amounts. The model’s performance was then evaluated using the mean squared prediction error (MSPE) on data from the fourth week of February 2017.

### Steps Taken:

**1. Data Exploration and Cleaning**

- Imported the dataset and performed initial data visualization.

- Addressed unusual data points and inconsistencies.

- Conducted feature engineering to enhance model performance.

**2. Model Fitting and Cross-Validation**

- Developed a tunable strategy to find the best model & implemented that strategy using CV

- Evaluated model performance on test data.

**3. Interpretation**

- Assessed face validity by checking logical consistency of predictors.

- Identified model flaws and areas for improvement.

## Key Takeaways

### Model Performance

- The model achieved an MSPE of 7.26, which translates to a Root Mean Squared Prediction Error (RMSPE) of approximately $2.69.

- Given that the average tip amount is $1.79, the model’s predictions show considerable variability, leaving room for improvement.

### Strengths

- **Relevant Predictors:** Features such as trip distance, fare amount, time of day, and RatecodeID levels showed strong relationships with tipping behavior.

- **Logical Interpretability:** The model’s coefficient signs aligned with expectations, e.g., higher fares and longer trips correlated with higher tips.

### Limitations & Future Improvements

- **Uncaptured Human Factors:** Tipping behavior is influenced by subjective elements like passenger mood, service quality, and driver-passenger interactions, which are absent from the dataset.

- **Missing External Influences:** Factors such as traffic conditions, weather, and major city events could impact tipping trends but were not included in the model.

- **Generalization Concerns:** The model's accuracy might decline when applied to different timeframes or locations due to potential seasonal effects or external influences.

## Conclusion

The model successfully identifies key factors influencing tipping behavior but remains limited by missing human and environmental variables. While it provides reasonable predictions, the level of error suggests that tipping behavior is highly complex and influenced by external factors beyond what is captured in the dataset. Future iterations could incorporate additional data sources to refine predictions further.
