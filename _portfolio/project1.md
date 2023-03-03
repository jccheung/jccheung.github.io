---
title: Renewable Energy Prediction
subtitle: Prediction of Solar and Wind Renewable Energy using Deep Learning
image: "assets/img/portfolio/renewable.jpg"
alt: Solar Image

caption:
  title: Renewable Energy Prediction
  subtitle: Deep Learning
  thumbnail: "assets/img/portfolio/renewable.jpg"
---

<style> 
.noPadding { 
  margin: 0px !important;
  border: 0px solid brown; 
} 
</style> 
Long Short Term Memory (LSTM) model was developed to monitor short term power output predictions from 4 hour ahead to 6 hours ahead. This research paper demonstrated a unique approach of utilizing nearby publicly available meteorological
data to predict renewable energy power output that could potentially be used for wind and solar farm scheduling to prevent curtailment of clean energy.
<br />
<br />
This paper was written for completion of my Masters major research project under Toronto Metropolitan University and as a result the paper cannot be shared publicly without explicit permission from the University. It was written in Python with Pandas, Numpy, Tensorflow and other supporting libraries.
<br />
<br />
<b style="font-size:larger">Questions to be Answered:</b>

1. Can all of Ontario's power demands be met with renewable energy? <br>
2. What are the key features for determining renewable energy? <br>
3. What would be the best algorithm choice to predict renewable energy? <br>
<figure style="text-align: center">
<img src="assets/img/portfolio/month_bar_electricity.png" alt="Comparing electricity per month" width="700" class="noPadding"> 
 <figcaption style="text-align: center"><em>Data Directory style</em>
 </figcaption>
</figure>
<br>
The dataset used was collected from the <a href ="https://www.ieso.ca/">[Independent Electricity System Operator] </a> and the <a href ="https://power.larc.nasa.gov/data-access-viewer/"> [NASA Solar Satelitte dataset.]</a>
<br />
<br />
The dataset made up of approximately 50 meteorological features total over a 4 year time period. Notable features such as wind speed, solar radiation, air temperature, dew point temperature and humidity all played a role in determining total solar and wind power generation capacity.
<br />
<br />

<figure style="text-align: center">
<img src="assets/img/portfolio/model_lifecycle.JPG" alt="model_life contents" width="500" class="noPadding"> 
  <figcaption style="text-align: center">
    <em>Model lifecycle utilized in this project </em>
  </figcaption>
</figure>

The data was then run through exploratory data analysis: simple correlation operations to determine the feature with the greatest correlation to wind power. The data was also cleaned and outlier values were either removed or replaced with average values.
<br />
<figure style="text-align: center">
<img src="assets/img/portfolio/wind_corr.png" alt="Pearson_corr" width="700" class="noPadding">
  <figcaption>
    <em>Pearson Correlation for Wind Power</em>
  </figcaption>
</figure>
<br />
<br />
The Long Short Term Memory LSTM deep learning algorithm is trained on 3 years worth of data, with the 4th year being the validation/ testing year. This results in a 75% training, 25% testing split. The benefit of using LSTM networks over a traditional mathemetical model such as the ARIMA (Autoregression Integrated Moving Average), is that there doesnt need to be a processing step to remove trends and seasonality.
<br />
<br />
The Long Short Term Memory algorithm requires a number of timesteps, also known as an input window size. To determine how many past values of the series will be used for the current prediction. For example, if i wanted to predict 2 pm, should consider weather at 1 pm, 12 pm, and 11 am as my past values, meaning my window size is 3 hours.
<br />

<br />
Here we can see the output result for the solar farm, seperated by season. The algorithm is predicts the next 4 hours ahead with relative certainity. The wind farm is also predicted and both results are shown below.
<br>

<figure style="text-align: center;">
<img src="assets/img/portfolio/solar_season_2.png" alt="Solar Season Forecast Example" width="700" class="noPadding"> <figcaption>
    <em>Solar Season Forecast Example</em>
  </figcaption>
</figure>

<figure style="text-align: center;">
<img src="assets/img/portfolio/dillon_t16.png" alt="Wind Season Forecast Example" width="700" class="noPadding"> <figcaption>
    <em>Wind Season Forecast Example</em>
  </figcaption>
</figure>

<br />
Additional work would be to include more weather variables and try utilizing a CNN model to the algorithm before utilizing the LSTM.
<br />
<br />
<h4>Libraries:</h4>
Some of the tools required to make this project work: 
<br>
<a href="https://www.python.org/">Python</a> - Python is a programming language that lets you work quickly and integrate systems more effectively.<br>
<a href="https://scikit-learn.org/stable/">Scikit-Learn</a> - An open source Machine learning library in python used for data preprocessing, classification, regression, etc... <br>
<a href="https://pandas.pydata.org/">Pandas</a> - Pandas is a fast, powerful, flexible and easy to use open source data analysis and manipulation tool,
built on top of the Python programming language.<br>
<a href="https://jupyter.org/">Jupyter Notebooks</a> - web-based interactive development environment for notebooks, code, and data.<br>


