
# When's the Money?  
## Time Series Analysis of Online Poker Traffic
## General Assembly Capstone Project - Richard Chadwick




For the Data Science Immersive  Capstone Project I challenged myself to produce a proof of concept for a commercially viable poker product not already in existence. My data set was a years sample of game summaries from a popular poker website. 

With exploratory data analysis I identified two classes of poker players, professionals who consume traffic and recreational players who drive it. Using these classes I identify profitable and unprofitable components of hourly traffic, namely the number of games including at least one recreational player per hour and the number of professionals online per hour. 

Applying a Seasonal AutoRegressive Moving Average model to these time series, I developed one and two step ahead forecasts for each component of traffic, evaluated them and drafted a roll out strategy for a poker traffic forecasting product.

Despite a relatively small data set, there is clear evidence that a poker traffic forecasting product can provide valuable information players can use to improve increase their profit. 

## Presentation and work
Powerpoint presentation and notebooks can be viewed by clicking the titles below (presenting notebooks with nbviewer is necessary to view plotly graphs).

### [Powerpoint presentation with notes](https://docs.google.com/presentation/d/1itoDwOIfXFC4ZXFLbjpyEphQ91OKC59xC89_1S6z6rQ/edit?usp=sharing)

A walk through of the process and discussion of the proposed products and roll out strategy.


### [Part 1, Anonymise and wrangle data](https://nbviewer.jupyter.org/github/richchad/DSI-Capstone/blob/master/Part%201%2C%20Anonymise%20data.ipynb)

To protect the privacy of the players the data is anonymised. In this notebook I anonymise the tournament summary data and create two additional tables for exploratory data analysis; games per hour and player summary statistics.

### [Part 2, Exploratory data analysis](https://nbviewer.jupyter.org/github/richchad/DSI-Capstone/blob/master/Part%202%2C%20EDA.ipynb)

Review of the time series (games per hour), comparison of players summary statistics and investigation of player networks including visualsations and comments. I provide justification for classifying players (as professional or recreational) and establish some common sense thresholds for these classifications.

### [Part 3, Classifying players and constructing data frames for time series](https://nbviewer.jupyter.org/github/richchad/DSI-Capstone/blob/master/Part%203%2C%20Classifying%20players%20and%20constructing%20data%20frames%20for%20time%20series.ipynb)

Using insights from the exploratory data analysis players are classified. This allows for the creation of three time series, games per hour (all games), games per hour (including at least one recreational player) and number of professionals online. With these classifications I perform an additional (brief) exploratory data analysis. 


### [Part 4, Time series modelling](https://nbviewer.jupyter.org/github/richchad/DSI-Capstone/blob/master/Part%204%2C%20Time%20series%20modelling.ipynb)

For each time series I check for stationarity (Dickey-Fuller Test), seasonality (with auto correlations and partial auto correlations) and establish a common sense base line (predicting the previous observation).

To optimise for order and moving averages I create a seperate notebook for each time series and run for loops on the model with different parameters. I discuss the best performing models in this notebook and review their effectiveness for two step ahead dynamic forecasts.

## Libraries used
1. Scikit-learn
2. StatsModels
3. Scipy
1. Pandas
2. NumPy
3. Matplotlib
4. Plotly
5. Cufflinks
6. Networkx

