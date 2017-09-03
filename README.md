# Planet_OpenCalifornia
Series of Posts/Scripts on using data from Open California dataset by Planet

## Part 1 Open California dataset

http://www.acgeospatial.co.uk/blog/open-california-data-comparison/

## Part 2 Pan Sharpening Sentinel 2a data with Planet
Blog post detailing process and description 
http://www.acgeospatial.co.uk/blog/pan-sharpening-sentinel-2-with-planet-data/

![alt tag](http://www.acgeospatial.co.uk/wp-content/uploads/2017/08/01_title.jpg)

Gdal to sharpen
Raster files cover the SAME area!
blue_band_planet.tif = clipped blue band from Planet
sentinel2a.tif = Clipped RGB Sentinel2a data of any combination you like

gdal_pansharpen -w 0.52 -w 0.25 -w 0.23 -co PHOTOMETRIC=RGB blue_band_planet.tif sentinel2a.tif blue_sharpened.tif

repeat from Red and Green

Use outputs in [median_sharpen.py](https://github.com/acgeospatial/Planet_OpenCalifornia/blob/master/median_sharpen.py)


## Part 3 Using pan sharpened Sentinal 2a to run SVM pixel clusters 
Blog post detailing SVM on pixel clusters
http://www.acgeospatial.co.uk/blog/svm-on-recognizing-pixel-clusters/

![alt tag](http://www.acgeospatial.co.uk/wp-content/uploads/2017/08/01_title-1.jpg)

Project code is here [ML_planet.py](https://github.com/acgeospatial/Planet_OpenCalifornia/blob/master/ML_planet.py)
