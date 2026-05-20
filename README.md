# Predicting-Health-Outcomes-in-Bristol-using-Access-to-Greenspace-Indicators

# Background
This project aims to assess whether ordnance survey data containing average access to local greenspace, number of postcodes in a built up area and IMD rank can be used to build an accurate supervised learning model that can accurately predict if an LSOA in Bristol has a general healthy or unhealthy population. Previous studies have focused on using supervised machine learning classification models such as K nearest neighbours (Suyal and Goyal,2022) and decision trees to predict specific health conditions such as Covid-19 (Muhammad et al.,2020), however there are few studies that quantify overall general health across local communities.

This study sets out a clear workflow that cleans and joins data sets to answer set research questions and will create a set of health class labels based on Office for National Statistics data to train two models that will be able to classify LSOAs across Bristol into ‘healthy’ and ‘unhealthy’ areas, this information can then be used by local planning organisations and governments to quantify the importance of access to greenspace, population density and deprivation level on public health when planning new housing developments (Shaw, 2004, Fenning and Ting, 2025).

# Research Questions 
***Question 1:*** Are the data variables suitable for predicting health class?

***Question 2:*** Can a supervised leaning model accurately predict whether an LSOA is classed as healthy or unhealthy based on average distance to green space (m), IMD rank per LSOA and number of postcodes in a built up area?

***Question 3:*** Which type of Supervised learning model is most effective a Decision tree or Knn (k nearest neighbours )?


# Data 

**Nomis 2021 Census Data (2021)** - General Health (TS037). Available at: https://www.nomisweb.co.uk/datasets/c2021ts037 (Accessed:20/01/26)

General health data (csv) was obtained from the Office for National Statistics nomis data finder. This data was collected at a LSOA level during the 2021 census and represents persons per health catagory as well as all usual residents per LSOA boundary. This data is crucial for establishing a threshold for catagorising healthy and unhealthy LSOAs that can be used as labels in the creation of supervised learning models.

**Ordnance Survey Access to Public Greenspace data (2020)** - Available at: https://www.ons.gov.uk/economy/environmentalaccounts/datasets/accesstogardensandpublicgreenspaceingreatbritain (Accessed:20/01/26)

OS Greenspace data (csv) was obtained from the Office of National Statistics, it displays multiple variables assosiated with access to greenspace across the whole UK. This data is useful as it will aid the creation of train data for supervised learning classification models. This data can be joined spatially at a LSOA level to Bristol boundary shapefiles and can also be joined to csv health data from Bristol on common join columns.


**Bristol LSOA shapefile (2021)** - Open Data Bristol. Available at: https://opendata.bristol.gov.uk/datasets/lower-layer-super-output-areas-2021-precise/about (Accessed:20/01/26)

Bristol LSOA boundries (shp) where obtained from the Bristol open data portal, this data shows LSOAs as they where in 2021. This data can be joined to both health and greenspace csv data files to create a spatial visualisation of key variables by matching them to geometry that can then be plotted.  
