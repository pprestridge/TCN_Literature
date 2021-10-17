# TCN_Literature

Althougth RNN and LSTM networks considered to be the "Gold Standard" for time series analysis, TCN networks have risen in popularity. More importantly, TCN networks have shown their ability to outperform RNN and LSTM networks on their own benchmark tests. This repo will examine and recreate literature showing off TCN networks.     


# Anomaly Detection

This notebook follows the work outlined by ["https://arxiv.org/pdf/1905.13628.pdf"]. Abnormality detection is done in an unsuperivized manner in which a TCN is trained to predict the next value in a time series on good data, or data without an abnormality. The assumption is that the model is well-trained and will predict the correct value, and the error between the prediction and the gound truth will be used as the metric to predict abnormality.


1.) Train with Early Stopping to prevent overfitting of the training data

2.) Fit a distribution to the losses of the trained model on the train data

3.) Set a threshold and equation from which to classify an anomaly

4.) Implement Model and abnormality detection on a test set


Signal Creation

![image](https://user-images.githubusercontent.com/17886837/137638162-3e1e009d-c67e-4be0-8b6a-6e12b62b2484.png)

Trained TCN Forecast

![image](https://user-images.githubusercontent.com/17886837/137638178-7124006a-2cfd-45ce-a7e7-997ba244c9ef.png)

Error Analysis

![image](https://user-images.githubusercontent.com/17886837/137638191-ba0dfe9d-0972-4de1-ab85-6a2885afcde9.png)

Anomaly Prediction

![image](https://user-images.githubusercontent.com/17886837/137638216-a186dfce-d652-4cbc-bbda-2a30a80fad87.png)

![image](https://user-images.githubusercontent.com/17886837/137638210-5a21b02e-192b-44e7-b96b-92d2d4448be6.png)


# Copy Memory

In this task, each input sequence has length T + 20. The first 10 values are chosen randomly among the digits 1, . . . , 8, with the rest being all zeros, except for the last 11 entries that are filled with the digit ‘9’ (the first ‘9’ is a delimiter). The goal is to generate an output of the same length that is zero everywhere except the last 10 values after the delimiter, where the model is expected to repeat the 10 values it encountered at the start of the input.

Ex.

Input  = 1234567876 000000000 99999999999 
         
         Message        T     Delimeter+Space

 Output = 0000000000 000000000 01234567876

                              Message
Bai et al. ["https://arxiv.org/pdf/1803.01271v2.pdf"]   
![image](https://user-images.githubusercontent.com/17886837/137637968-7f59b1c0-5253-46ce-bbb8-f301d4845298.png)



TCN Copy Memory.ipynb

![image](https://user-images.githubusercontent.com/17886837/137637946-b76754c8-8533-4d58-8337-a3c3ef7dd7eb.png)

![image](https://user-images.githubusercontent.com/17886837/137638064-4cd17cce-3298-4289-83d8-993bd0fbca42.png)
![image](https://user-images.githubusercontent.com/17886837/137638070-8e5754fa-cf50-4817-98a1-e5a45946e812.png)     
