# ML_projects

The goal of this competition is to build efficient models capable of predicting short-term volatility in the stock market across a variety of sectors. This is particularly relevant for options trading, where the price of an option is directly linked to the volatility of the underlying asset.

My methodology centers around two key areas: (1) feature engineering, and (2) model development.

In the feature engineering phase, I utilized a 5-fold cross-validation technique with a 31-gap time-series approach, carefully constructed to eliminate potential data leakage from the training set into the validation set. I also calculated the mean of the absolute values of all resp target variables, thereby formulating sample weights. This enables the model to prioritize and accurately predict those samples with greater weights.

In terms of model development, I combined an autoencoder and a Multilayer Perceptron model. The autoencoder was used to create new features, which were then combined with the original ones for the MLP model. To prevent data leakage, both models were trained simultaneously within each CV split. Furthermore, the autoencoder was enhanced with target data and a Gaussian noise layer was introduced to combat overfitting.

My observation was that integrating a tree-based ensemble model could potentially lead to superior and more importantly, more stable results.
