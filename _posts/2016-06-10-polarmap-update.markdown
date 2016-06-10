---
layout: post
title: "PolarMap.js 1.2.0 Released"
date: 2016-06-10
author: james
categories:
---

I am happy to announce the release of version 1.2.0 of PolarMap.js today!

[Version 1.2.0](https://github.com/GeoSensorWebLab/polarmap.js/releases/tag/v1.2.0) adds a feature and fixes a bug. [The bug](https://github.com/GeoSensorWebLab/polarmap.js/issues/3) was that the projection extent for the polar projections was not correctly defined, causing markers to be mis-aligned from the underlying tiles by a small amount (under a metre). The fix correctly defined the extent as half the circumference of the WGS84 ellipsoid, a better choice than the estimated value that was present in previous versions of PolarMap.js.

The new feature is support for loading Arctic Web Map tiles over HTTPS. I have set up the Arctic Web Map tile cache server with an SSL certificate from [Let's Encrypt](https://letsencrypt.org), giving you the option of loading tiles securely. The first advantage is that it allows an already secure web page to load the tiles securely instead of over plain HTTP, which causes browsers to issue a security warning. SSL also means the tiles you are accessing are private between you and Arctic Web Map, no eavesdropping of which tiles you are using.

HTTPS will be enabled automatically for tiles if the enclosing webpage is HTTPS. Otherwise, tiles will be loaded over HTTP without encryption. If you are loading tiles manually then you should be aware SSL is enabled for tiles.arcticconnect.org and supports the alternate domains of a.tiles.arcticconnect.org, b.tiles.arcticconnect.org, and c.tiles.arcticconnect.org.

For more info on the SSL certificate, [check our new certificate on SSL Labs](https://www.ssllabs.com/ssltest/analyze.html?d=a.tiles.arcticconnect.org&latest).

If you have any issues with the tiles for Arctic Web Map, you can [contact us by email](mailto:support@arcticconnect.org) or [leave a GitHub issue](https://github.com/GeoSensorWebLab/awm-styles/issues). For support with PolarMap.js please use the [PolarMap.js issue tracker](https://github.com/GeoSensorWebLab/polarmap.js/issues).
