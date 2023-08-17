# Springboard-Capstone3---Transfer_Learning

### Soccer or Rugby Image Classification

This project uses pre-trained weights to create an classification model which recognized images as either 'soccer' or 'rugby'. This project also deploy the model as a web application using Streamlit.

Data Source: [Kaggle-Football 🏈 Vs Rugby 🏉 Image Classification](https://www.kaggle.com/datasets/ligtfeather/football-vs-rugby-image-classification)

#### 01_Data_Overview [Notebook](https://github.com/lorihe/Springboard-Capstone3---Transfer_Learning/blob/main/01_Data_Wrangling_EDA.ipynb)
The raw data source contains images sorted as below: \
'train' folder --- 'rugby' folder (1224 images)\
               --- 'soccer' folder (1224 images)\
'test' folder  --- 'rugby' folder (305 images)\
               --- 'soccer' folder (305 images)              

All images are in one of these formats: 'JPEG', 'JPG', 'BMP', 'PNG', 'MPO.

By browsing images in the raw data, it was noticed that:\
- A few basketball/American football pictures were placed in the soccer folders. Those pictures are manually replaced for this project.
- Multiple American football pictures were placed in the rugby folders. Those pictures are not corrected at the moment.
- All soccer images files in 'soccer' folder were named as 'rugby'. Those file names were corrected in code.

#### 02_Game_Classification [Notebook](https://github.com/lorihe/Springboard-Capstone3---Transfer_Learning/blob/main/02_Game_Classification.ipynb)  
I used MobileNetV2 as base model to train on the updated datasets. The training resulted in accuracy 0.9493 on training set and 0.918 on validation set.

#### 03_Streamlit.ipynb [Notebook](https://github.com/lorihe/Springboard-Capstone3---Transfer_Learning/blob/main/03_Streamlit.ipynb.ipynb)  
[application](https://github.com/lorihe/Springboard-Capstone3---Transfer_Learning/blob/main/Web_app.gif)
To deploy:
Save [model](https://github.com/lorihe/Springboard-Capstone3---Transfer_Learning/blob/main/model.hdf5) in the same directory. Run 03_Streamlit.ipynb. Open 'your url' and input the 'External URL' (remove 'http://' and ':8501')

#### 04_Performance.ipynb [Notebook](https://github.com/lorihe/Springboard-Capstone3---Transfer_Learning/blob/main/04_Performance.ipynb.ipynb)
I applied the model to newly collected datasets:\
'rugby' folder (50 images)\
'soccer' folder (50 images)




