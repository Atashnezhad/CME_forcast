
# Interplanetary Coronal Mass Ejection (ICME) Forcasting - Geomagnetic Storms
A big potential threat and a dangerous event that might happen in your lifetime. Geomagnetic storms! On September 1st, 1859, the largest solar storm on record hit the earth.
<p align="left">
  <img width="700" src="Assets/3._cme_gif_11660.gif" >
</p>


You may have already heard about the so called carrington event that happen back in 1859. 
The carrington event was such a powerful solar storm that sat the telegraph papers on fire!
The Coronal Mass Ejection (CME) starts on the surface of the sun where the intense magnetic field makes an arc shapes of materials that have a high tendency to snap (wellknown coronal mass ejection).

<p align="left">
  <img width="400" src="Assets/cme.gif" >
</p>

The goal of this project is to forecast the solar storms speed 18 days ahead using classical and modern tools.




# Data Scraping

The data was scraped form **Near-Earth Interplanetary Coronal Mass Ejections Since January 1996** webpage [here](http://www.srl.caltech.edu/ACE/ASC/DATA/level3/icmetable2.htm#(k)).

<p align="left">
  <img width="1200" src="Assets/data_webpage.png" >
</p>



Intense solar storms ionize the earth's atmosphere which affects any magnetic communication such as cell phone, internet, etc. 
Such an event has the potential to cause a very large blackout entire planet


<p align="left">
  <img width="400" src="Assets/CME_phenomena_update.jpg" >
</p>

[image source](https://www.swpc.noaa.gov/phenomena/coronal-mass-ejections)



# EDA

<p align="center">
  <img width="400" src="Figures/P02_02_EDA_BDE.png" >
  <img width="400" src="Figures/P02_02_EDA_MC.png" >
    <img width="400" src="Figures/P02_02_EDA_BIF.png" >
  <img width="400" src="Figures/P02_02_EDA_Qual.png" >
</p>




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
