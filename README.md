## 'Soccer or Rugby' Image Classification

This project uses pre-trained weights to create a classification model which recognized images as either 'soccer' or 'rugby'. This project also deploys the model as a web application using Streamlit.

Data Source: [Kaggle-Football 🏈 Vs Rugby 🏉 Image Classification](https://www.kaggle.com/datasets/ligtfeather/football-vs-rugby-image-classification)

### 01_Data_Overview [Notebook](https://github.com/lorihe/Springboard-Capstone3---Transfer_Learning/blob/main/01_Data_Wrangling_EDA.ipynb)
The raw data source contains images sorted as below: \
'train' folder --- 'rugby' folder (1224 images)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; --- 'soccer' folder (1224 images)\
'test' folder&nbsp;  --- 'rugby' folder (305 images)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; --- 'soccer' folder (305 images)              

All images are in one of these formats: 'JPEG', 'JPG', 'BMP', 'PNG', 'MPO.

By browsing images in the raw data, it was noticed that:
- A few basketball/American football pictures were placed in the soccer folders. Those pictures are manually replaced for this project.
- Multiple American football pictures were placed in the rugby folders. Those pictures are not corrected at the moment.
- All soccer image files in 'soccer' folder were named 'rugby'. Those file names were corrected in the code.

### 02_Game_Classification [Notebook](https://github.com/lorihe/Springboard-Capstone3---Transfer_Learning/blob/main/02_Game_Classification.ipynb)  
I used MobileNetV2 as the base model to train on the updated datasets. The training resulted in an accuracy of 0.9493 on the training set and 0.918 on the validation set.

### 03_Streamlit.ipynb [Notebook](https://github.com/lorihe/Springboard-Capstone3---Transfer_Learning/blob/main/03_Streamlit.ipynb.ipynb)  
![application](https://github.com/lorihe/Springboard-Capstone3---Transfer_Learning/blob/main/Web_app.gif)

To deploy:
- Save [model](https://github.com/lorihe/Springboard-Capstone3---Transfer_Learning/blob/main/model.hdf5) in a selected directory on your Google Drive. 
- Open '03_Streamlit.ipynb' on Google Colab.
- Direct the connection to your selected directory in code. Run through all lines.
- Use the output of the last line. Open 'your url' and input the 'External URL' (remove 'http://' and ':8501').
- Pick a picture to predict.

### 04_Performance.ipynb [Notebook](https://github.com/lorihe/Springboard-Capstone3---Transfer_Learning/blob/main/04_Performance.ipynb.ipynb)
I applied the model to newly collected datasets:\
&nbsp;&nbsp;---'rugby' folder (50 images)\
&nbsp;&nbsp;---'soccer' folder (50 images)

**Prediction performance metrics & wrongly labeled images:**

  <img src="https://github.com/lorihe/Springboard-Capstone3---Transfer_Learning/blob/main/performance/cm.JPG?raw=true" alt="Image Description" width="360" height="250">
  
![errror](https://github.com/lorihe/Springboard-Capstone3---Transfer_Learning/blob/main/performance/error.JPG?raw=true)



As shown, the model performs much better in recognizing soccer than in rugby. The next step would be cleaning up the noise in training data to see if it improves the performance.



