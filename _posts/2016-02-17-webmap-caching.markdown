---
layout: post
title: "Arctic Web Map Tile Cache"
date: 2016-02-17
author: james
categories:
---

A recent hardware issue on the Arctic Web Map Tile Server caused a short outage earlier this week. As February 15 was a public holiday, the outage lasted 23 hours and was corrected on February 16.

To maintain some availability of Arctic Web Map tiles during any future Tile Server issues, I have set up a tile caching server in front of the Arctic Web Map Tile Server. This cache server is hosted with Cybera in Calgary, on a separate infrastructure system than Arctic Web Map which is hosted at the nearby University of Calgary.

In this new setup, when requests are made for a tile they are passed through this cache server to the main tile server and the result is cached in a disk store on the cache server. If a subsequent request is made for the same tile and the tile has not past its expiry date, then the cache server will return its local copy instead of asking for a copy from the tile server.

If the tile server is unavailable, then the cache server will return a local tile to you if there is one in the cache. Otherwise, a 504 error is returned. Currently the cache server will wait up to 3 seconds to open a connection to the tile server. If the tile server does not respond *at all*, then it will be considered unavailable for that request. This does not affect cases where the tile server is online and a new tile needs to be rendered, but takes more than 3 seconds to generate: in that case, the cache server will still open a connection within the 3 second limit.

You do not need to do anything to use this new service as it was activated automatically when I switched the DNS to point *.tiles.arcticconnect.org to the cache server today (February 17).

If you have any issues with the tiles for Arctic Web Map, you can [contact us by email](mailto:support@arcticconnect.org) or [leave a GitHub issue](https://github.com/GeoSensorWebLab/awm-styles/issues). 
