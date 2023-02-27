---
title: NASDAQ Stock API Tracker
subtitle: Utilizing NASDAQ API to collect data on specific stock markets and specific companies, then perform simple elementary analysis on the json data
image: "assets/img/portfolio/05-thumbnail.jpg"
alt: Stock Photo

caption:
  title: NASDAQ Stock API Tracker
  subtitle: Data Science
  thumbnail: "assets/img/portfolio/05-thumbnail.jpg"
---
<style> 
.noPadding { 
  margin: 0px !important;
  border: 0px solid brown; 
} 
</style>
NASDAQ data set will focus on the Frankfurt Stock Exchange (FES) and analyze the stock prices of a company named Carl Zeiss Meditec, which manufactures tools for eye examinations, as well as medical lasers for laser eye surgery: https://www.zeiss.com/meditec/int/home.html. The company is listed under the stock ticker AFX_X.

<figure style="text-align: center">
<img src="assets/img/portfolio/stock_data_afx.png" alt="Stock data json " width="700" class="noPadding">
<figcaption>
    <em> Stock data output return as a JSON</em>
  </figcaption>
</figure>

<figure style="text-align: center">
<img src="assets/img/portfolio/open_tick_price.png" alt="Stock data Tick Opening Price" width="300" class="noPadding">
<figcaption>
    <em> Stock Open Price</em>
  </figcaption>
</figure>


Simple Exploratory data analysis was conducted, answering simple questions like: 
<br/>
What is the highest and lowest opening prices of stocks within a certain time period?

<figure style="text-align: center">
<img src="assets/img/portfolio/maxminprice.png" alt="Maximum and minimum opening price" width="300" class="noPadding">
<figcaption>
    <em> What is the largest change in a single day?</em>
  </figcaption>
</figure>

<figure style="text-align: center">
<img src="assets/img/portfolio/changeprice.png" alt="Maximum change price per day" width="400" class="noPadding">
<figcaption>
    <em> This data preprocessing exercise can be the foundation for a more complex machine learning pipeline or system.  
</em>
  </figcaption>
</figure>

To be completed...

More details about the data preprocessing can be found in the public github: <a href="https://github.com/jccheung/nasdaq-stock-api-tracker-miniproject">Github Project Link</a>

<br />
<br />
<h4>Libraries:</h4>
Some of the tools required to make this project work: 
<br>
<a href="https://pypi.org/project/requests/">Python GET requests</a> - Python Requests GET API Methods <br>
<a href="https://jupyter.org/">Jupyter Notebooks</a> - web-based interactive development environment for notebooks, code, and data.<br>
