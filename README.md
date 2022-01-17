# the_depths
![Deep Learning](https://fedtechmagazine.com/sites/fedtechmagazine.com/files/styles/cdw_hero/public/articles/%5Bcdw_tech_site%3Afield_site_shortname%5D/201907/FedTech-DeepLearning.jpg?itok=nQa1FQBg)

## Synopsis
Here I will be using deep learning recurrent neural networks to model bitcoin closing prices. I will generate two models; one will use FNG indicators to predict the closing price, while the other will use a window of closing prices to predict the nth closing price.

Neural Networks themselves are algorithms designed to replicate the human brain. When I say replicate the human brain, I mean the idea of recognizing patterns and sensory data. One should then understand why Neural Networks are used in stock predictions. The premise of using RNN's, which are specifically Recurrent Neural Networks, is then to recognize these patterns and predict what is going to happen next. This sounds even better for making predictions, right? One can then put some icing on the cake by using an LSTM RNN, a Long Short-Term Memory Recurrent Neural Network. A mouthful, to say the least. The idea behind the LSTM is the fact that as RNN's are exposed to more data, they are exposed sequentially; the oldest data is further and further back. This eventually leads to the loss of information. One could say RNN's have horrible memory. LSTM, to an extent, puts "weights" on the "memories" and virtually keeps data that is most influential on the results. 

I will be playing with LSTM RNN models; more specifically, one model will be used two different ways. The goal is to test out the power of these models and, in the process, to see if using the Bitcoin Fear and Greed Index or if using windows of Bitcoin closing prices is better for predicting the nth closing price of Bitcoin. I hypothesize that the windows will be the best bet.

## Findings
When looking at these models, one wants the most negligible loss and the best predictions without overfitting. I broke my results into three questions
  
  1. Which model has a lower loss?
      
  
  2. Which model tracks the actual values better over time?
        
  
  3. Which window size works best for the model?

First, I would ask anyone reading this repo to look at the FNG model and then go from there. In the end, the FNG model was terrible compared to simply analyzing closing prices. The closing price model was not perfect, but it did relatively well in reality. The closing price model had the least loss and tracked the actual values better over time. Below, one can see a graph of the data using a 10-day window on closing prices.

![closing_model](/result_data/simply_closing_graph.png) 

![closing_model_data](/result_data/closing_data.png)

It was pretty close for the most part. When it comes to the best window, I would like to play around with this a little more, but I used a window of 10 for these tests.

One can compare the above data to the graphs and data found below using the fear and greed indicator.

![fng_model](/result_data/fng_predicted_graph.png)

![fng_model](/result_data/fng_data.png)

One can clearly see that the fear and greed predictions were a waste of time. While I am not a master of machine learning quite yet, one can see that this data is not working out. It adds to all the skepticism around sentiment analysis and NLP, but I am a firm believer in both. I will keep working with the model and see how I can improve it.  

For the time being, please check out my notebooks and enjoy!


  


