# IPL-PLAYER-PRICE-PREDICTION
The objective of this project is to develop a machine-learning model that can accurately predict the price of player(batsmen, bowlers, and all-rounders) by taking IPL and international stats as input. Various factors affect the price of a player in the auction. For this, we need to consider different cricketing and non-cricketing stats (like age) of the players.
The dataset is taken from Kaggle. It consists of data of players (Batting, Bowling stats) in IPL in the respective years from 2016 to 2022. I added International Stats of players that I collected through Cricbuzz, and created the final Data Set. Batting average (Avg), strike rate (SR), economy rate (Econ), and SR(bowling) are filled using existing features.
Some of the preprocessing stepsP 
Label encoding- converted country and team to numerical values
Converted SOLD_PRICE column
Feature selection based on the correlation matrix
Handling missing values using forward fill
For each player (batsman, bowler, all-rounder) different models were trained. The models include linear regression, lasso regression, ridge regression, decision tree regressor, and random forest regressor.
Suitable model is selected based on performance metrics such as MSE, MAE and R-Squared error.
And I compared different models by taking national, international stats and both for batting, bowling and all-rounders. 
The results obtained from the project were promising. 
In conclusion, for batsmen and all-rounders: random forest regressor
Bowlers: Linear regression are selected
Overall, this project provides valuable insight into the factors that influence player prices in the IPL auction and presents an effective approach for predicting player prices. The project's findings can be used by franchises to make informed decisions while purchasing players in the auction, ultimately leading to the formation of a strong and competitive team.
