## Stock Price Predictor

This project was built to help my understanding of how machine learning models can be applied to financial data.  
I learnt key concepts like data preprocessing, model training, and visualization.

**Next steps:** I'm experimenting with creating notebooks on Kaggle and here on Github to progress further on my journey in learning data science and machine learning.

How to use:

This was built in Jupyter Lab, so you should ideally use it in there, but it also works on Jupyter Notebook or Visual Studio.

You can mess around with certain values to get different results, here are a few noteable ones:
- device(type='.....') # you can change this to CPU if you don't have an Nvidia GPU.
- ticker = 'MSFT' # You can change the value inside the apostrophes to show data from another stock, such as AAPL for Apple Inc or INTC for Intel Corporation
  df = yf.download(ticker, '2020-01-01') #Change the start date if you want more years of data
- model = PredictionModel(input_dim=1, hidden_dim=32, num_layers=2, output_dim=1).to(device) # You change hidden_dim or num_layers depending on how much you want to train the model, the current values are good for ~6-8GB VRAM on Nvidia GPU's
- num_epochs = 200 # Again, increase for more training
- ax1.plot(df.iloc[-len(y_test):].index, y_test, color='blue', label='Actual Price') # If the colours bother you, you can change them here.
  ax1.plot(df.iloc[-len(y_test):].index, y_test_pred, color='green', label='Predicted Price')

