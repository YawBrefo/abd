# Project Update

#############
REPO CONTENTS
#############
- .png exemplars of desired PlanetScope image "look"
- .shp file 40K
- .ipnyb script for processing satellite and mask images
- .pictures of proposed polygon shapefiles

############
Documentation
############
- step a. 7,264 polygon shapefiles of the entire Alberta was acquired from the official Alberta Township System (ATS) version 4.1 Coordinate files.

Specifically, all the V4-1_TWP layers were used

The ATS file contains lat/long coordinates (degrees & decimal degrees) of all governing quarter section corner in the province of Alberta. The file is referenced to NAD 83 with an accuracy of +/-3 metres.(https://open.canada.ca/data/en/dataset/45dbaf52-c4c8-4e5d-89fe-d14cec62fc41)


It is a land survey system used in Western Canada to divide land in 1 square mile sections. The system was later adopted in land sales and leases for hydrocarbon exploration rights. It is used for the location and identification of oil and gas wells in Alberta. (https://chinookpetroleum.com/alberta-township-system/)

 - step b. ATS polygons is intersected with 80,972 well point features in QGIS, the resulting 4,052 (wells_poly) multipolygons within which the wells were located was filtered out.

 - step c. from the 4,052 wells_poly shapefiles 10 polygon samples are selected for planet download.

 - step d. 10 polygon shapefiles are converted to 10 geojson files.

 - step e. Manually, each geojson is imported to Planet Explorer, with dimension of 9.8km x 9.8km, total area of 95km_squared.

 - step f. Filter parameters: 
IMAGERY TYPE
	Medium Resolution (3-7m)
		* PlanetScope Scene
		
ENVIRONMENTAL CONDITIONS
	Area coverage > 100%
	Cloud cover > 0%

ADVANCED FILTERS
	* Include only surface reflectance
	* Include only results with ground control
	* Show only standard image quality
	
DATE
	* June 1, 2022 to July 31, 2022
	(however July 3, mostly better optical view)
	
step g. PlanetScene SR-4B imagery is then ordered.
	* focus is on single scene with almost or total AOI coverage.


##############
#HAVE ON HAND#
##############
Github: mchll-ln, YawBrefo
