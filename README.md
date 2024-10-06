# Burned Area Monitor
(from script FireMonitor.ipynb but added many stuff)

## Features
- Finds Sentinel 2 images from a given box (AOI) (BurnedAreaBox.json)
- Filters images with clouds, half images(where AOI is in 2 images and not in one)
- Auto Selects Pre and Post Fire images
- Auto Saves NBR_PRE_FIRE.tiff, NBR_POST_FIRE.tiff
- Auto saves NDVI_PRE_FIRE.tiff, NDVI_POST_FIRE.tiff
- Auto Creates and Saves DNBR.tiff
- Generates Bunred Area Polygon Shapefile (remove small holes and uses gaussian smooth for the final polygon)
- Generates Burned Area Grading (Low, Moderate, High, Very High) in Raster and Vector form.


## How to Use
- Open BurnedAreaBox.json and paste your AOI box that you copy from Sentinel Data Space
- Open **config_fire_monitor.yaml** and input :<br />
```Fire_start_Date: '2024-07-10'```&ensp;&ensp;Fire ignition date, it will search 15 before and 15 days after the fire <br />
```Fire_Name: 'xios_fire'```&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;Output name of files<br />
```EPSG: EPSG:32635```&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;Output EPSG of Raster and Vector files<br />
```DNBR_Threshold: 0.1```&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;Threshold for burned pixels<br />
```cloudCover: 5```&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;Change if no images and found<br />
```outputFolder: output/```&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;Output folder for all files<br />
- Run **main.py**

## Output
- DNBR.tiff output example (xios fire, 2024-07-10)
![Alt text](https://github.com/nikos230/Burned-Area-Mapping/blob/main/screenshots/DNBR.jpg) <br />

- Burned Area Polygon example (xios fire, 2024-07-10)
![Alt text](https://github.com/nikos230/Burned-Area-Mapping/blob/main/screenshots/polygon.jpg) <br />

- Burned Area Grading (Vector) example (xios fire, 2024-07-10)
![Alt text](https://github.com/nikos230/Burned-Area-Mapping/blob/main/screenshots/classify.jpg) <br />

- Burned Area Grading (Raster) example (xios fire, 2024-07-10)
![Alt text](https://github.com/nikos230/Burned-Area-Mapping/blob/main/screenshots/calssify_png.jpg)





