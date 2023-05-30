# ML_projects

The objective of this competition is to construct models capable of accurately predicting short-term volatility (over a span of 10 minutes) for an array of stocks spanning diverse sectors. This exercise is crucial in option trading, where the price of an option is directly tied to the volatility of the underlying asset.

This intriguing Kaggle competitionhas given me my first experience with understanding the generation of time-series data. It inspired me to enhance my implementation of time-id and stock-id Nearest Neighbor features, which substantially improved my scores.

My approach rests on two pillars: (1) feature engineering and (2) model development.

Regarding feature engineering, studying the process of data generation offers crucial insights. Despite the normalization of the provided data, discussions emphasize the possibility of using "tick size" to restore the actual prices pre-normalization, and recover the time-id order. The training data used spans from 1st January 2020 to 31st March 2021, this information enriched both feature engineering and time series cross-validation.

During this timeframe, there were 443 stock market open days. Given that there are 3830 unique time_ids in the training dataset, this suggests approximately 8.6 time_ids were recorded each trading day. After excluding both the initial and final half-hour of trading, at most 9 time_ids could be recorded - every 30 minutes from 10:30 to 15:00. This offers a fundamental understanding of the data generation process.

For each time_id, we can design stock_id nearest neighbors by aggregating features like realized volatility, stock size, and trading volume from various stocks that demonstrate similar "properties". This concept enabled me to derive features such as "the average tau of 20 similar stocks demonstrating comparable volatility across the 5 closest time-ids".

Thanks to the order of time_id, I can pinpoint features that fluctuate considerably over time, like trading volume and order count. We can transform these features into ranks or categorical data. (Given my use of MLP, I opted for ranks.)

Moving onto model development, I employed a tree-based ensemble model, LightGBM, and MLP. My CNN model, while not perfectly stable during training and computation-heavy, might warrant further exploration with more time, but the scores improved after blended with tree model. 
(RNN is another model that I am considering, as it does not require feature creation.)



