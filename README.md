# kayaking_geospatial_project
Placeholder for side project that employs geospatial analysis of satellite imagery &amp; USGS water mission area APIs to generate data first view of potential kayaking trips

## What is this!
This is a potential outline for side project. It would built on this earlier work from 2015 in ArcGIS but instead use open-source Python and JavaScript tooling. http://justingosses.com/map-of-houston-area-paddling-experiences-post-1/

## Premise
Most kayaking trip resources fall into two categories. Either they are books that describe trips or webpages with a bunch of community provided put-in locations on a map. The ease of certain geospatial analysis for land-cover analysis, topography changes from digital elevevation models as well as plentiful USGS APIs on things like river level, flow rate, river level forecast, downstream and upstream river segments, etc. these days opens up the possibilities of providing different information about kayaking trips in a different form.

## Potential 'different' information that typical kayaking resources
- <i>Proportion of different landcover types:</i> (residential, forested, marsh, coastal, industrial, urban) along a kayak trip segment. 
- <i>Potential view distance:</i>  For example, inside a steep valley it might be tens of feet where as on a bay it might be miles.
- <i>Steepness:</i>  from DEM could give overall trip number of feet dropped, sparkline of entire trip topography, and locations of break points.
- <i>Current flow levels vs. typical:</i>  how unusual current flow levels are for this river over X years or X years at this month of the year.
- <i>Current flow levels vs. known trip times:</i>  based on date & time of reported trips.
- <i>Current flow levels vs. known aborted trip times:</i>  based on date & time of reported aborted trips.
- <i>Current flow levels vs. okay to paddle levels :</i>  based on user reported informatin.
- <i>What portion of river segment has most reported trips?</i> Based on user reported informatin.
- <i>ML recognition of rapids in satellite imagery</i> would require developing a model?
- <i>All place where a bridge crosses a river</i> would need to calculate from street vector data vs. river outline vector data. Bridges are potential put-in or take-out points as well as common locations for barriers or shallow water that require walking.


## Features
### Vector


#### Points
- points for put-ins and take-outs
- points for rapids
- points for bridges
### lines
- river polylines
- river polyines split whereever a put-in or take-out occurs
- bay vs. river polylines
- ocean vs. bay/river polylines
#### Polygons
- river outline polygons (probably comes in segments)
- marsh polygons
- bay polygons
- lake polygons
- ocean polygons
### Raster & associated things
- land use
- point cloud types from lidar pointclouds
- digital elevation models (DEM)
## Operations
- calculate river length between two points that intersect river.
- take a point from lat long and find nearest point that intersects river polygon.
- take a point from lat long and find nearest point that intersects river polyline.
- Take polyline & DEM and calculate topography alone polyline.
- Take polyline & DEM and calculate topography across polyline every X units in order to find likely view distance along polyline every X units and return as array.
- Create polygon of likely view distance from preceeding step.
- Calculate landuse type proportions within view polygon and return as array for every X units along polyline.



## Pre-calculated data products
## On-the-fly calculated data products
