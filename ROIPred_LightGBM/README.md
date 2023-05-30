# ML_projects

This competition asked participants to develop a model predicting Return on Investment using historical pricing data. 

 LightGBM was my model of choice for the analysis, a widely preferred model in the realm of quantitative finance. Boasting superior learning capacity and robustness compared to traditional machine learning and DNN models. Feature-wise, 300 preprocessed features are provided with surprisingly very good quality. To avoid the risk of overfitting, I didn't perform additional feature engineering, and focused solely on the official 300 features.
Initially, I tuned the parameters within the TimeSeriesSplit at a 50% discount (with a 4:1 ratio for training and validation). Once the parameters were finalized, I proceeded to train with the complete dataset. And I customized the loss function within LGBM to be 'pearsonr'. 
