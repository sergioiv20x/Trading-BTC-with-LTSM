# Trading-BTC-with-LTSM
¿ Can day-trading in cryptocurrency (Bitcoin) markets be better assessed through a deep learning approach that includes, among others, social media data?”

In This repository I explore the possibility of forecasting price movements in a specific cryptocurrency market, by implementing deep learning models, exploiting other types of features more than just the market indicators commonly used; with this purpose in mind, it is important to explore which set of features derives in a model with higher predictive power, consequently, better trading opportunities can be assessed.
The research gathers and organizes data from July 2017 until August 2019, among those features there are included Social media data (Tweets volume, Google trends scores), characteristic Technical Analysis indicators and Fundamental metrics proper of the blockchain. Two different LSTM configurations apt for multistep time series forecast are explored: sequence to vector (Vector output models) and sequence to sequence (Encoder-Decoder model) recurrent neural networks.
Models including a mix of social media data and fundamental metrics improve forecasts based on LSTM neural networks, they result in more robust and more accurate models than the ones using the typical market indicators. The use of this models can help investors to take better-informed decisions when performing day-trading in cryptocurrency markets. 
Special Thanks are given to Phd. Jason Brownlee and his tutorials and books of Machine learning in https://machinelearningmastery.com/ which help a lot not only to comprehend but also to develop and validate the models. 

What you will find:

<space><space>*<space>1- DATA GATHERING:
<space><space>*<space>	Tweets: 
<space><space>*<space>		-Jupyter Notebook used to gather the BITCOIN related tweets thorugh the GetoldTweets3 API
<space><space>*<space>		-Output_got_2017_X.csv: CSV files of the collected tweets
<space><space>*<space>		-Jupyter notebook used to combine and count the collected tweets
<space><space>*<space>		-output file: "Tweet_Counts_2017.xlsx"		
<space><space>*<space>	Google Trends: 
<space><space>*<space>		-Jupyter Notebook used to obtain the hourly Gtrends score for the desired period
<space><space>*<space>		-two excel files containing the weeks you want to get the google trend scores
<space><space>*<space>		-output file: "bitcoingtrends.xlsx"
<space><space>*<space>	Coinmetrics: 	Daily data available  in the coinmetris portal, bitcoin blockchain features and its dictionary.
<space><space>*<space>2- DATA EXPLORE:
<space><space>*<space>	Jupyter Notebook of:
<space><space>*<space>		visual exploration of gathered data by plotting pairwise relationships
<space><space>*<space>		correction of erros in gathered data
<space><space>*<space>		correlation scores and the join of all data into a single dataset
<space><space>*<space>	Output file: previous output files joined alltogether wiht the daily coinmetrics data "Dataset_raw.xlsx"
<space><space>*<space>	NOTE: To the ""Dataset_raw.xlsx"" the R-Studio notebook is used to correct the Gtrend missing values by using spline interpolation
<space><space>*<space>		Adittionally we use the Maximal Infomration coefficient(MIC) of the minerva Rlibrary in the R-Studio notebook to identify which features are more useful.
<space><space>*<space>	Final Dataset: "Dataset.xlsx"

<space><space>*<space>3- LTSM Models:
<space><space>*<space>	After the Definition of 5 different subsets: 
<space><space>*<space>	Name of Datasubset	Dimensions	Features included
<space><space>*<space>	Basic_DS		3		Only BTC market indicators (3) (closing price, Volume in BTC and volume in USD)
<space><space>*<space><space><space>*<space>	Social_DS		5		BTC market ind. (3) + Social Media (2) ( Tweets count and Google trends scores)
<space><space>*<space>	Fundamental _DS		6		BTC market ind. (3) + Fundamental metrics (3) (NVT signal, active address, mean avg transfer)
<space><space>*<space>	Technical_DS		6		BTC market ind. (3) + Technical ind. (3)  (RSI, MACD,TRIX)
<space><space>*<space>	Ranked_DS		7		BTC market ind. (3) +Best ranked features: NVT signal + G.trends + Avg Transaction USD+Tweets

 	Within the "Stacked LTSM 2/3 layers" Notebooks, you will find the definition build and predictive performance of the different subsets
 	Within the Encoder-Decoder LTSM notebook, you will fin an ENCODER-DECODER architechture implemented with the Best ranked features.

RESULTS:
<space><space>*<space>YES! It is possible to assess better day-trading decisions with models integrating other types of data.
<space><space>*<space>This models can be used to asses your crypto-trading.
<space><space>*<space>Best mix of features: social media and fundamental metrics from the blockchain derive in more robust and more accurate models than the ones using the typical market indicators
 Please refer to my FINAL REPORT  for a better detailed explicaiton of my project. 
