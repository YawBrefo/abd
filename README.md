#############
REPO CONTENTS
#############
- .png exemplars of desired planetscope image "look"
- .shp file 40K 

#######
#NOTES#
#######

##[Dec 1st 2022]
- created the plan with phases
LOGISTICS
- slack: soon, email for now
- scheduling:2 months in GMT+5, prefer mornings
- availability - discuss later/ in the new year
- Action Items:
  - add repo content
  - talk to David about internal deadline and phases feedback
  
##############
#HAVE ON HAND#
##############
Github: mchll-ln, YawBrefo
###############################################################
# PHASE 1:EVERYTHING WORKS ON 100 TILES W WELLS AUTOMATICALLY #
###############################################################

Step 0: Ensure the following data runs on dataset with size 100 wells (not full dataset)
Step 1: get all the planetscope geotiffs from Planet that contain a well

(SCRAPPED: get all the alberta (40K km^2))
command line or the apis - just keep it documented

For every PlanetScope tile[?]:
- June -> August (summer)
- Cloud coverage < 5%
- 3m/px (same resolution) 
- SR product
- * 1 image of each well*  -> might be a separate script

QUESTION: GEE needed?

Step 2: store it a cloud container (Azure)  AND/OR mila computers (<miniscratch>)

QUESTION: how much storage in miniscratch

*Note - Look into: [COG]  https://developers.planet.com/docs/planetschool/an-introduction-to-cloud-optimized-geotiffs-cogs-part-1-overview/

Step 3:  Organization of the data 

- cropping separation: Use GDAL to a) crop the images based on their label= location of well (point in the shp file)  2k*2km "tile" b) create binary masks for the ML model
- [?] separate by directory the training and val and test data
- preserve the <deployment> images (have no well from the cropping) in 2km*2km

COMMENT: get PlanetScope access

Internal Deadline: mid-end January -> confirm this with david

###############################################
PHASE 2: EVERYTHING WORKS AUTO ON 40 000 TILES W WELLS 
#################################################
- repeat all steps above
- GDAL may have issues  handling lots of data

