# qnavigate
## QGIS plugin for navigation

Draft specs:
* load marine charts [check free ones from OpenCPN: S57 is an unsupported data source, whereas it should be supported by GDAL http://www.gdal.org/drv_s57.html]
* choose polar for your boat
* define optional variables
  * % reduction for night navigation
  * % reduction for strong winds
  * avoidance of high waves
* define start and end points, plus optional intermediate points
* define start time
* download GRIB files (bounding box taken from points above; start date taken from above) [see http://www.zygrib.org/]
![Grib downolad popup](img/zygrib_download.png?raw=true "ZyGrib downolad popup")
* problem: EPSG code misinterpreted
* configure an appropriate visualization (wind speed and direction, wave height and direction)
  * problem: find which bands convey the necessary info
  * problem: GRIB is loaded as a raster; not trivial to add wind direction and speed arrows, possibly a raster to vector conversion is necessary
* calculate optimal route [see https://www.sailgrib.com/] and add as temporary layer
  * avoid land masses
* communicate with autopilot to set the helm
