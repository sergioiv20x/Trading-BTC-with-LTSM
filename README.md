# Trading-BTC-with-LTSM
¿ Can day-trading in cryptocurrency (Bitcoin) markets be better assessed through a deep learning approach that includes, among others, social media data?”

In This repository I explore the possibility of forecasting price movements in BTC markets, by implementing deep learning models, exploiting other types of features more than just the market indicators commonly used; with this purpose in mind, it is important to explore which set of features derives in a model with higher predictive power, consequently, better trading opportunities can be assessed.
The research gathers and organizes data from July 2017 until August 2019, among those features there are included Social media data (Tweets volume, Google trends scores), characteristic Technical Analysis indicators and Fundamental metrics proper of the blockchain. Two different LSTM configurations apt for multistep time series forecast are explored: sequence to vector (Vector output models) and sequence to sequence (Encoder-Decoder model) recurrent neural networks.
Models including a mix of social media data and fundamental metrics improve forecasts based on LSTM neural networks.
Special Thanks are given to Phd. Jason Brownlee and his tutorials and books of Machine learning in https://machinelearningmastery.com/ which help a lot not only to comprehend but also to develop and validate the models. 

What you will find:
1- DATA GATHERING:
  + Tweets:
  Jupyter Notebook used to gather the BITCOIN related tweets thorugh the GetoldTweets3 API
  Output_got_2017_X.csv: CSV files of the collected tweets
  Jupyter notebook used to combine and count the collected tweets
  output file: "Tweet_Counts_2017.xlsx"		
  + Google Trends: 
  Jupyter Notebook used to obtain the hourly Gtrends score for the desired period
  two excel files containing the weeks you want to get the google trend scores
  output file: "bitcoingtrends.xlsx"
  + Coinmetrics: 	Daily data available  in the coinmetris portal, bitcoin blockchain features and its dictionary.

2- DATA EXPLORE:
 + Jupyter Notebook of:
>>
visual exploration of gathered data by plotting pairwise relationships, correction of erros in gathered data
, correlation scores and the join of all data into a single dataset

Output file: previous output files joined alltogether wiht the daily coinmetrics data "Dataset_raw.xlsx"
 + NOTE: To the ""Dataset_raw.xlsx"" the R-Studio notebook is used to correct the Gtrend missing values by using spline interpolation. Adittionally we use the Maximal Infomration coefficient(MIC) of the minerva Rlibrary in the R-Studio notebook to identify which features are more useful.
Final Dataset: "Dataset.xlsx"

3- LTSM Models:
  >>After the Definition of 5 different subsets,
  >>Within the "Stacked LTSM 2/3 layers" Notebooks, you will find the definition build and predictive performance of the different subsets
  >>Within the Encoder-Decoder LTSM notebook, you will fin an ENCODER-DECODER architechture implemented with the Best ranked features.

RESULTS:
<space><space>*<space>YES! It is possible to assess better day-trading decisions with models integrating other types of data.
<space><space>*<space>This models can be used to asses your crypto-trading.
<space><space>*<space>Best mix of features: social media and fundamental metrics from the blockchain derive in more robust and more accurate models than the ones using the typical market indicators
 Please refer to my FINAL REPORT  for a better detailed explication of my project. 
