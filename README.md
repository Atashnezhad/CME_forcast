<p align="left">
    <img width="1200" src="Assets/carington_ev.png" >
</p>

# Interplanetary Coronal Mass Ejection (ICME) Forecasting - Geomagnetic Storms
A big potential threat and a dangerous event that might happen in your lifetime. Geomagnetic storms! On September 1st, 1859, the largest solar storm on record hit the earth. You may have already heard about the so called carrington event that happen back in 1859. The carrington event was such a powerful solar storm that sat the telegraph papers on fire! The Coronal Mass Ejection (CME) starts on the surface of the sun where the intense magnetic field makes an arc shapes of materials that have a high tendency to snap (wellknown coronal mass ejection). 

<p align="left">
  <img width="400" src="Assets/3._cme_gif_11660.gif" >
</p>

## Problem Statment:

A similar solar storm if happen today, it most likely wipes out the whole data on all computers due to the fact they are mostly not electromagnetic pulse protected.
Intense solar storms ionize the earth's atmosphere which affects any magnetic communication such as cell phone, internet, etc. 
Such an event has the potential to cause a very large blackout entire planet
The goal of this project is to forecast the solar storms speed 18 days ahead using classical and modern tools. The ICME record of the last 30 years is seen in the following figure (Image by author).

<p align="left">
  <img width="1200" src="Figures/P02_01_EDA_plt33.png" >
</p>



## Directory Contents

The project directory tree structure is provided below.

```
├───Assets
├───Codes
│   │   P01_01_Data_Scraping.ipynb
│   │   P01_02_Data_Scraping.ipynb
│   │   P02_01_EDA.ipynb
│   │   P02_02_EDA.ipynb
│   │   P02_03_EDA.ipynb
│   │   P02_04_EDA.ipynb
│   │   P03_01_Univar_ARIMA_AR.ipynb
│   │   P03_02_Univar_LSTM.ipynb
│   │   P03_03_Univar_LSTM.ipynb
│   │   P03_04_Univar_ML.ipynb
│   │   P03_05_Multivar_LSTM.ipynb
│   │   P03_06_Multivar_tf_supervised.ipynb
│   │   P04_01_tf.ipynb
│   │   P04_02_tf.ipynb
│   └───archive
│           P01_02_Data.ipynb
│           P02_01_EDA.ipynb
├───Data
│       Data_CME.csv
│       Data_ICME_Edited_Decoded_out_P02_03.csv
│       Data_ICME_Edited_out_P02_02.csv
│       Data_ICME_Engineered_P02_04.csv
│       Data_ICME_scraped.csv
│       Data_ICME_speed_transformed_18D_P03_01
│       Data_univar_ICME_lag60tsp_supervise_P03_04
│       HCME_WP4_V01.json
│       ICME_WebScr_data.html
│       save_coded_values_P02_03_EDA.json
├───Figures
├───Models
│   │   LSTM_1_univariate.h5
│   │   LSTM_2_univariate.h5
│   │   LSTM_Multivariate_P03_05.h5
│   │   P03_02_LSTM_1_univariate.h5
│   ├───dnn_model_tf_p03_06
│   └───dnn_model_tf_p3_6
└───proj
```


## Data Scraping

The data was scraped form **Near-Earth Interplanetary Coronal Mass Ejections Since January 1996** webpage [here](http://www.srl.caltech.edu/ACE/ASC/DATA/level3/icmetable2.htm#(k)).

<p align="left">
  <img width="1200" src="Assets/data_webpage.png" >
</p>







## EDA

<p align="left">
  <img width="800" src="Figures/P02_02_EDA_MC.png" >
</p>

**P02_02_EDA:** 
From the above figure, It is clear that the events reported by Huttunen et al have reported some outliers in the overall data set. It is seen that the Huttunen et al group have reported some very high ICME speeds. This observation opens room for investigating the whole data reported by their team to discover the reason behind these outliers. is there any difference between the measurement tools used by their team?


<p align="left">
  <img width="500" src="Figures/p04_02_tf_hist2d_3.png" >
</p>

**P04_02_tf:** 
From the above plot, it is observed that the majority of ICME speed falls between 400 to 500 km/s and magnetic activity of -50nT to -60 nT. Note that, the Dst < -100 nT are considered severe solar storms (Zhang et al. 2007).
Although there is some high ICME speed recorded above 450 km/s, however, the data shows both low and high magnetic index disturbance which makes it inconclusive.

At the top- right side of plot, a severe solar strom is seen with ICME speed of around 800 km/s and Dst index of -99.


## Results

### ARIMA 5,1,0 Forecasting for 18 days ahead

<p align="center">
  <img width="1200" src="Figures/ARIMA510_GIF.gif" >
</p>

### AR 150 lags Forecasting for 18 days ahead
<p align="center">
  <img width="1200" src="Figures/AR_150.gif" >
</p>


### LSTM Forecasting for 18 days ahead
<p align="center">
  <img width="1200" src="Figures/P03_02_LSTM_2_univar.gif" >
</p>
