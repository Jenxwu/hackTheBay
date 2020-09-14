<img src="https://github.com/jvhuang1786/teamHackTheBay/hackTheBay/blob/master/images/landcoverimage.png"></img>

# Analysis of Total Nitrogen Water Pollution Using Land and Air Data

## Team Hackathon Devpost Chesapeake Bay Water Quality Hackathon

## Introduction

This project was a team project that looked at land features, air quality and nitrogen oxide and its affect on the Chesapeake bay.  

The water quality data was collected from the hackathon github repo:

https://drive.google.com/file/d/12uoFlcn8pgeuxD2-seFak36KTvrFPKCt/view

Landcover was collected through here:

https://www.mrlc.gov/viewer/

Air quality data was collected through here:

https://www.ncdc.noaa.gov/data-access/model-data/model-datasets/north-american-regional-reanalysis-narr

Nitrogen Oxide Data was collected through here:

https://echo.epa.gov/tools/data-downloads

**The goal of the model was to try to see what features and how it was affected**

### Libraries Used for the Hackathon


<table>

<tr>
  <td>Original Data Collection</td>
  <td>pandas, matplotlib, numpy regex</td>
</tr>

<tr>
  <td>Data Collection from other Sources</td>
  <td>pandas, geopy, numpy, seaborn, sklearn, geopandas, certify, urllib3, scipy.spatial</td>
</tr>

<tr>
  <td>Data Visualization</td>
  <td>plotly, seaborn, matplotlib</td>
</tr>

<tr>
  <td>Modeling</td>
  <td>catboost, randomforest from sklearn, xgboost, shap</td>
</tr>

<tr>
  <td>Future Model</td>
  <td>sklearn random forest, shap</td>
</tr>


</table>


## Original Data and merging it with landcover, air quality and nitrogen oxide. 

Steps of Collected the Data: 

     * Total Nitrogen was first collected out of the water_final.csv from the hackathon repo.
     * Landcover was collected 
     * Narr air quality data was collected    
     * These features were merged together with the total nitrogen chemical choosing total nitrogen from the parameter feature in water_final.csv
     * Nitrogen oxide data and correlation was added into the csv. 
     * Since land coverage data was from 2016 we decided to use datapoints from 2016 to the end of 2019. 
     * A chemicals csv was also created to take a look at the relationship among chemicals in the water. 

**CSV Files and data collection write up**
* [Detailed Description of the Steps](https://github.com/teamHackTheBay/hackTheBay/blob/master/writeup-sections/data_acquisition_writeup.pdf)
* [Final CSV using Landcover, airquality and nitrogen oxide](https://github.com/teamHackTheBay/hackTheBay/blob/master/data/final_water.csv)
* [Chemical Comparison CSV](https://github.com/teamHackTheBay/hackTheBay/blob/master/images/dfnitro.csv)

**Feature engineering and merging**
* [Adding of Distance Feature](https://github.com/teamHackTheBay/hackTheBay/blob/master/feature_engineering/add_distance_feat.ipynb)
* [Adding huc12_enc Feature](https://github.com/teamHackTheBay/hackTheBay/blob/master/feature_engineering/huc_mean_target.ipynb)
* [Importing Narr Data](https://github.com/teamHackTheBay/hackTheBay/blob/master/exploration/narr_import.ipynb)
* [Joining LandCover and Narr with hackthebay csv](https://github.com/teamHackTheBay/hackTheBay/blob/master/exploration/htb_lc_data_join.ipynb)
* [Gathering Nitro Oxide data](https://github.com/teamHackTheBay/hackTheBay/blob/master/exploration/epa_no2_monitoring_data.ipynb)
* [Combining new features with Total Nitrogen](https://github.com/teamHackTheBay/hackTheBay/blob/master/exploration/adding_nitro_oxide.ipynb)


## Data Visualization and Findings

Visualization of the Chemicals:

     Further from input the less details we can see.
     

* [Chemical Visualization Notebook](https://github.com/teamHackTheBay/hackTheBay/blob/master/images/dfnitro_figures_2.ipynb)

Visualization of Location:

     Further from input the less details we can see.
     
* [Feature Map](https://nbviewer.jupyter.org/github/jvhuang1786/mhxxCapStone/blob/master/feature_map.ipynb)

## Modeling 

Shap file here 

<img src="https://github.com/jvhuang1786/mhxxCapStone/blob/master/images/mhxx.gif" width="480"></img>

Feature Importances and Hyperparameters used. 

       Generator uses Conv2DTranspose
       Discriminator uses Conv2D
       Hyperparameters:
          Filter
          kernel_size
          Stride
          Padding
          kernel_initializer

* [Notebook for chosen Xgboost model](https://github.com/teamHackTheBay/hackTheBay/blob/master/models/all_feature_model/no_huc_xgb/all_features_no_huc_corr_xgb_model.ipynb)
* [Notebook for Catboost model](https://github.com/teamHackTheBay/hackTheBay/blob/master/models/catboost/HackTheBay%20Catboost%20water_final%20dataset-no%20huc%20all%20features%20.ipynb)


## Future Models to Consider 

<img src="https://github.com/jvhuang1786/mhxxCapStone/blob/master/images/mhxx.gif" width="480"></img>

Feature Importances and Hyperparameters used. 

       Generator uses Conv2DTranspose
       Discriminator uses Conv2D
       Hyperparameters:
          Filter
          kernel_size
          Stride
          Padding
          kernel_initializer

* [Deep Convolutional GAN](https://nbviewer.jupyter.org/github/jvhuang1786/mhxxCapStone/blob/master/dcgan_mhxx.ipynb)



## Authors

* Berenice Dethier
  Science, travel, and food enthusiast
  [GitHub: berenice-d](https://github.com/berenice-d)
* Bryan Dickinson
  [GitHub: bryan-md](https://github.com/bryan-md)
* Justin Huang
  Into anime, finance computer vision, and NLP.
  [GitHub: Jvhuang1786](https://jvhuang1786.github.io/)
* Tim Osburg
  Geophysicist and avid runner.
  [GitHub: Tosburg](github.com/Tosburg)
* Jen Wu
  Entrepreneur and nature nerd.
  [GitHub: Jenxwu](https://github.com/Jenxwu) (edited) 

