---
layout: page
title: Documentation
permalink: /documentation/
---

## Welcome to the Arctic Connect Platform Documentation.

This page contains the information to understand the Arctic Connect project/platform and how to get started with building on that platform.

Arctic Connect is a platform with multiple services. These services combine to provide a set of useful tools for Arctic researchers and communities.

#### Arctic Bio Map

Arctic BioMap (ABM) enables members of the scientific community and northern residents to contribute observations on arctic animal species for the purpose of biodiversity monitoring, assessment, research, management and education. It consists of a mobile client, an API service (Arctic Bio Map Server), and a visualization service (Arctic Bio Map Portal).

#### Arctic Scholar

Arctic Scholar enables researchers, educators, interested private sector entities, government agencies, and the general public to access and share arctic data and information contained in assorted formats including publications, grey literature, research licenses, photo archives, field notes, and project metadata from arctic field stations. It takes data from the ASTIS catalog and geographically indexes the results using the Arctic Scholar service. The data is then visualized using the Arctic Scholar Portal service.

#### Arctic Sensor Web

Arctic Sensor Web (ASW) enables research stations around the pan-Arctic to connect their sensors, including those that provide near-real time data, to a cloud service for visualization, information sharing, and collaborative analysis. It has a database back-end based on the GeoCENS RPI, and a frontend (Arctic Sensor Web Workbench) based on the GeoCENS RPI workbench.

#### Arctic Web Map

Arctic Web Map (AWM) provides an Arctic-specific web mapping tool allowing researchers to customize map projections for scientifically accurate visualization and analysis, a function that is critical for arctic system research but missing in existing web mapping platforms.  It provides a visually appealing tool for education and outreach to a wider audience. It is built on the same open-source mapping stack as OpenStreetMap, combining OpenStreetMap data with CanVec and Natural Earth Data. The style data is open-source (Arctic Web Map Style). The tile API can be accessed directly via the same API as OpenStreetMap, or via the PolarMap.js JavaScript library for web browsers.

### Download and Source

All Arctic Connect services are hosted and managed by the GeoSensorWeb Lab, with source code available for download.

<ul>
  <li>
    <h4><a href="https://github.com/GeoSensorWebLab/arctic-biomap-server">Arctic Bio Map</a></h4>
    <p>Server for collecting wildlife observation data from clients.</p>
  </li>
  <li>
    <h4><a href="https://github.com/GeoSensorWebLab/abm-portal">Arctic Bio Map Portal</a></h4>
    <p>Portal for visualizing data in the Arctic Bio Map Server.</p>
  </li>
  <li>
    <h4><a href="https://github.com/GeoSensorWebLab/arctic-portal">Arctic Portal</a></h4>
    <p>Portal for accessing the ArcticConnect services and reporting Arctic Web Map tile issues.</p>
  </li>
  <li>
    <h4><a href="https://github.com/GeoSensorWebLab/Arctic-Scholar">Arctic Scholar</a></h4>
    <p>Application for indexing results from ASTIS and automatically do geographic lookup on the data. Data is then loaded into ElasticSearch.</p>
  </li>
  <li>
    <h4><a href="https://github.com/GeoSensorWebLab/Arctic-Scholar-Portal">Arctic Scholar Portal</a></h4>
    <p>Portal for viewing data from Arctic Scholar on a map using PolarMap.js/Arctic Web Map.</p>
  </li>
  <li>
    <h4><a href="https://github.com/GeoSensorWebLab/asw-workbench">Arctic Sensor Web Workbench</a></h4>
    <p>Front-end for viewing data in the Arctic Sensor Web database.</p>
  </li>
  <li>
    <h4><a href="https://github.com/GeoSensorWebLab/awm-styles">Arctic Web Map Style</a></h4>
    <p>Style code for Arctic Web Map tiles.</p>
  </li>
  <li>
    <h4><a href="https://github.com/GeoSensorWebLab/polarmap.js">PolarMap.js</a></h4>
    <p>Custom Leaflet plugin for re-projecting maps and map features.</p>
  </li>
</ul>

### Fact Sheet

Please see the [Arctic Connect Site](http://arcticconnect.org/arcticconnect).

### License

Most components are MIT licensed. Some are BSD 2-clause licensed to increase compatibility with other libraries.

<ul>
  <li>
    <h4><a href="https://github.com/GeoSensorWebLab/arctic-biomap-server">Arctic Bio Map</a></h4>
    <p>MIT License.</p>
  </li>
  <li>
    <h4><a href="https://github.com/GeoSensorWebLab/abm-portal">Arctic Bio Map Portal</a></h4>
    <p>MIT License.</p>
  </li>
  <li>
    <h4><a href="https://github.com/GeoSensorWebLab/arctic-portal">Arctic Portal</a></h4>
    <p>MIT License.</p>
  </li>
  <li>
    <h4><a href="https://github.com/GeoSensorWebLab/Arctic-Scholar">Arctic Scholar</a></h4>
    <p>MIT License.</p>
  </li>
  <li>
    <h4><a href="https://github.com/GeoSensorWebLab/Arctic-Scholar-Portal">Arctic Scholar Portal</a></h4>
    <p>MIT License.</p>
  </li>
  <li>
    <h4><a href="https://github.com/GeoSensorWebLab/asw-workbench">Arctic Sensor Web Workbench</a></h4>
    <p>MIT License.</p>
  </li>
  <li>
    <h4><a href="https://github.com/GeoSensorWebLab/awm-styles">Arctic Web Map Style</a></h4>
    <p>Public Domain License.</p>
  </li>
  <li>
    <h4><a href="https://github.com/GeoSensorWebLab/polarmap.js">PolarMap.js</a></h4>
    <p>BSD 2-Clause License.</p>
  </li>
</ul>

### Provenance

New releases of the managed Arctic Connect components are handled by James Badger ([@openfirmware](https://github.com/openfirmware)). Before each release any tests for the component or service are run to verify integration. After release the services are monitored by a service run by the GeoSensorWeb Lab. Each release will be accompanied by commits and changelog updates on their respective git repositories.

Our third-party software and libraries are kept locked at specific versions. The Arctic Connect components will receive updates when these libraries are updated for specific improvements and security patches. As this is usually server-side for Arctic Connect services, users should not notice any disruptions.

### Release Notes

Each Arctic Connect service is managed and deployed separately to servers in Cybera's Rapid Access Cloud or at the University of Calgary. Please see the release notes for each separate component.

<ul>
  <li>
    <h4><a href="https://github.com/GeoSensorWebLab/arctic-biomap-server/blob/master/CHANGELOG.markdown">Arctic Bio Map</a></h4>
  </li>
  <li>
    <h4><a href="https://github.com/GeoSensorWebLab/abm-portal">Arctic Bio Map Portal</a></h4>
  </li>
  <li>
    <h4><a href="https://github.com/GeoSensorWebLab/arctic-portal">Arctic Portal</a></h4>
  </li>
  <li>
    <h4><a href="https://github.com/GeoSensorWebLab/Arctic-Scholar">Arctic Scholar</a></h4>
  </li>
  <li>
    <h4><a href="https://github.com/GeoSensorWebLab/Arctic-Scholar-Portal">Arctic Scholar Portal</a></h4>
  </li>
  <li>
    <h4><a href="https://github.com/GeoSensorWebLab/asw-workbench">Arctic Sensor Web Workbench</a></h4>
  </li>
  <li>
    <h4><a href="https://github.com/GeoSensorWebLab/awm-styles/blob/master/RELEASE.markdown">Arctic Web Map Style</a></h4>
  </li>
  <li>
    <h4><a href="https://github.com/GeoSensorWebLab/polarmap.js">PolarMap.js</a></h4>
  </li>
</ul>

### Support

Support is available from the GeoSensorWeb Lab. Please leave an issue on the GitHub or Bitbucket page for the component/service, or send an email to <a href="mailto:support@arcticconnect.org">support@arcticconnect.org</a>.

### Try Arctic Connect

<ul>
  <li>
    <h4><a href="http://portal.arcticconnect.org">Arctic Portal</a></h4>
  </li>
  <li>
    <h4><a href="http://scholar.arcticconnect.org">Arctic Scholar</a></h4>
  </li>
  <li>
    <h4><a href="http://records.arcticconnect.org/#ac_3573/4/90.00/0.00">Arctic Scholar Portal</a></h4>
  </li>
  <li>
    <h4><a href="http://sensorweb.arcticconnect.org">Arctic Sensor Web Workbench</a></h4>
  </li>
  <li>
    <h4><a href="http://webmap.arcticconnect.org/#ac_3573/2/90.0/0.0">Arctic Web Map</a></h4>
  </li>
  <li>
    <h4><a href="http://webmap.arcticconnect.org/examples/PolarMap/geosearch/index.html#ac_3573/4/90.00/0.00">PolarMap.js</a></h4>
  </li>
</ul>
