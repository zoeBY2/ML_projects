# ML_projects

The daily strategy I developed is to verify the effectiveness of a mkt neutral PCA & ETF based mean-reverting global strategy described in a paper.

My goal is to decompose individual ETF returns into systematic and idiosyncratic components, and statistically model the idiosyncratic part as alpha. This alpha strategy based on the concept of "co-integration," which is a statistical property that exists between two or more time series that move together in the long run, even if they may diverge in the short term. The systematic factor is calibrated using PCA.

The intraday strategy aims at verifying whether the market timing strategies work as described in the paper, across various ETFs, under the assumption of no transaction costs.

Both the two strategies center around three key areas: (1) Data Engineering (2) Model Development and (3) Backtesting
