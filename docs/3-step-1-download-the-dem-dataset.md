---
title: Step 1 - Download the DEM dataset
parent: Clipping Rasters in ArcGIS Pro
layout: default
nav_order: 3
---

### Step 1 - Download the DEM dataset

First, download the Digital Elevation Model. There are multiple sources where you can retrieve Digital Elevation Models. This tutorial will lead you to download the raster dataset from [Government of Canada's Geospatial Data Extraction website](https://maps.canada.ca/czs/index-en.html).

Alternative sources to download DEMs are provided at the end of this tutorial.

In the "Find a location" tab, search for "Toronto". Choose the "**Toronto, York, Ontario - City**" option and zoom to this selection on the map.

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_001_1.png' | relative_url }}' alt='The Government of Canada's geospatial data extraction page. In the "Find a location" text box, the prompt "Toronto" has been used.' title='' width='100%' height='100%' />

Then, make sure you set the clipping area to the "**Current Map Extent**". After you check this box, the Map Navigation should highlight the selected area in yellow.

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_002_0.png' | relative_url }}' alt='Expanding the "Select clipping area" tab, "Current Map Extent" is selected' title='' width='1149' height='1010' />

In the "**Select data to be extracted**" tab, select "**Elevation**".

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_003_0.png' | relative_url }}' alt='Expanding the "Select data to be extracted" tab, "Elevation" is selected.' title='' width='1154' height='1011' />

In the "Select options and submit job" tab, select "**Canadian Digital Elevation Model**". Leave the polygon extent as it has already set to the Toronto boundary. For product, select only the "**Digital Elevation Model (DEM)**". Choose the **WGS84** coordinate system for this tutorial. Leave the image resolution as default (20m), and input your email address to download the raster dataset.

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_004_0.png' | relative_url }}' alt='Expanding the "Select options and submit job" tab, "Canadian Digital Elevation Model" is selected in the "Elevation product type" menu. "Digital Elevation Model (DEM)" is checked of in the products list. The selected coordinate system is "WGS 84 / Pseudo-Mercator (ESPG: 3857) and the image resolution is 20m. There is a prompt beneath the image resolution box for you to input your email address.' title='' width='100%' height='100%' />

You will be able to see the job status on the website. Usually the request is processed immediately but sometimes it might take a few hours if the volume for requests are very high. Check your email for the download link. In the email you received, copy the link ending with ".zip" in a new tab in the browser. Click "Enter" and the file will start to download.