# Burned Area Monitor
(from script FireMonitor.ipynb but added many stuff)

## Features
- Finds Sentinel 2 images from a given box (AOI) (BurnedAreaBox.json)
- Filters images with clouds, half images(where AOI is in 2 images and not in one)
- Auto Select Pre and Post Fire images
- Auto Saves NBR_PRE_FIRE.tiff, NBR_POST_FIRE.tiff
- Auto saves NDVI_PRE_FIRE.tiff, NDVI_POST_FIRE.tiff
- Auto Creates and Saves DNBR.tiff
- Generates Bunred Area Smoothed Shapefile
- Generates Burned Area Grading (Low, Moderate, High, Very High) in Raster and Vector form.


## How to Use
- Open BurnedAreaBox.json and paste your AOI box that you copy from Sentinel Data Space
- Open **config_fire_monitor.yaml** and input :<br />
```Fire_start_Date: '2024-07-10'``` <br />
```Fire_Name: 'xios_fire'```<br />
```EPSG: EPSG:32635```<br />
```DNBR_Threshold: 0.1```<br />
```cloudCover: 5```<br />
```outputFolder: src/FireMonitoring_OpenDataCube/output/```<br />
- Run **main.py**

