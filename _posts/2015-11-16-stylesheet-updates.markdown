---
layout: post
title: "Web Map Tile Updates"
date: 2015-11-16
author: james
categories:
---

The tiles for Arctic Web Map have been updated!

[The first issue](https://github.com/GeoSensorWebLab/awm-styles/issues/1) fixed is related to rendering glitches visible in the lower-right quadrant of each map projection. It affected both the OpenStreetMap data layer as well as the bathymetry and geographic line layers. The OSM glitches were caused by some of the layers not having the correct projection specified; they are stored as EPSG:3573 in the database but Mapnik was reading them as if they were EPSG:4326 layers. This has been fixed. The problems with the bathymetry and geographic line layers were fixed by reprojecting them to EPSG:3573 and not having Mapnik do the reprojection on the fly.

[The next issue](https://github.com/GeoSensorWebLab/awm-styles/issues/2) caused "slivers" of blue water to appear in various parts of the globe. This was caused by the land shapefiles not being segmentized before being transformed from EPSG:4326 to EPSG:3573, causing gaps where there are long boundaries. This was fixed by segmentizing the land shapefiles before they are reprojected into EPSG:3573.

[The last issue](https://github.com/GeoSensorWebLab/awm-styles/issues/3) was the ground layer not being rendered at high zoom levels (13+). This was fixed by specifying the correct projection for those layers in the project file.

The styles were also updated to better select the layers to load at different zoom levels. This should give a minor boost to the tile rendering performance.

I use a script to automatically download, extract, and process shapefiles for Arctic Web Map data layers. This has been updated to allow more fine-grained control over how each layer is processed. It will also support parallel processing soon.

[I added partial indexes](https://github.com/GeoSensorWebLab/awm-styles/blob/master/indexes.sql) to our OSM database mirror. This should help the tile render speed on some queries.

The tiles are currently being regenerated for zoom levels 0 through 10. This will take a few weeks to complete. Zoom levels above 10 are rendered on the fly and are considerably faster.

If you have any issues with the tiles for Arctic Web Map, you can [contact us by email](mailto:support@arcticconnect.org) or [leave a GitHub issue](https://github.com/GeoSensorWebLab/awm-styles/issues).
