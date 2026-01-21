---
title: "Clipping Rasters in ArcGIS Pro"
layout: "home"
description: ""
permalink: "/"  #! Remove this if not the homepage
---

# Clipping Rasters in ArcGIS Pro

This tutorial covers two methods for clipping raster datasets from ArcGIS Pro.

**Table of Contents**

* [Introduction](#Introduction)
* [Setting up working environment](#Setting up working environment)
	+ [Step 1 \- Download the DEM dataset](#Step 1 - Download the DEM dataset)
	+ [Step 2 \- Download City of Toronto boundary file](#Step 2 - Download City of Toronto boundary file)
	+ [Step 3 \- Setting up a working directory and establish folder connection](#Step 3 - Setting up a working directory and establish folder connection)
* Clipping Rasters \- Two ways
	+ [Clipping Rasters \- Using toolboxes](#Clipping Rasters - Using toolboxes)
	+ [Clipping Rasters \- Export data](#Clipping Rasters - Export data)

**Introduction**
----------------

Clipping rasters allows you to only work on or display a certain area of interest. It could be defined by a boundary from a vector shapefile, or it could be defined by the extent of the window.

**Setting up working environment**
----------------------------------

In this tutorial, we will be working with the Digital Elevation Model (DEM) from Government of Canada's Geospatial Data, as well as the City of Toronto Former Municipality Boundaries file from City of Toronto Open Data Catalogue. Digital Elevation Model is a raster dataset that represents the surface of elevations. You can find a more[detailed explanation of a DEM on the Esri documentation page.](https://learn.arcgis.com/en/related-concepts/digital-elevation-models.html)

 

### **Step 1 \- Download the DEM dataset**

First, download the Digital Elevation Model. There are multiple sources where you can retrieve Digital Elevation Models. This tutorial will lead you to download the raster dataset from [Government of Canada's Geospatial Data Extraction website](https://maps.canada.ca/czs/index-en.html).

Alternative sources to download DEMs are provided at the end of this tutorial.

In the "Find a location" tab, search for "Toronto". Choose the "**Toronto, York, Ontario \- City**" option and zoom to this selection on the map.

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_001_1.png' | relative_url }}' alt='The Government of Canada's geospatial data extraction page. In the "Find a location" text box, the prompt "Toronto" has been used.' title='' width='100%' height='100%' />

Then, make sure you set the clipping area to the "**Current Map Extent**". After you check this box, the Map Navigation should highlight the selected area in yellow.

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_002_0.png' | relative_url }}' alt='Expanding the "Select clipping area" tab, "Current Map Extent" is selected' title='' width='1149' height='1010' />

In the "**Select data to be extracted**" tab, select "**Elevation**".

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_003_0.png' | relative_url }}' alt='Expanding the "Select data to be extracted" tab, "Elevation" is selected.' title='' width='1154' height='1011' />

In the "Select options and submit job" tab, select "**Canadian Digital Elevation Model**". Leave the polygon extent as it has already set to the Toronto boundary. For product, select only the "**Digital Elevation Model (DEM)**". Choose the **WGS84**coordinate system for this tutorial. Leave the image resolution as default (20m), and input your email address to download the raster dataset.

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_004_0.png' | relative_url }}' alt='Expanding the "Select options and submit job" tab, "Canadian Digital Elevation Model" is selected in the "Elevation product type" menu. "Digital Elevation Model (DEM)" is checked of in the products list. The selected coordinate system is "WGS 84 / Pseudo-Mercator (ESPG: 3857) and the image resolution is 20m. There is a prompt beneath the image resolution box for you to input your email address.' title='' width='100%' height='100%' />

You will be able to see the job status on the website. Usually the request is processed immediately but sometimes it might take a few hours if the volume for requests are very high. Check your email for the download link. In the email you received, copy the link ending with ".zip" in a new tab in the browser. Click "Enter" and the file will start to download.

 

### **Step 2 \- Download City of Toronto boundary file**

**City of Toronto's open data catalogue** is a great source to access the a variety of data from the municipal government. You can search from the [City of Toronto's Open Data Catalogue portal](https://open.toronto.ca/catalogue/)

For the first task, search for the "**Former Municipality Boundaries**".

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_005.png' | relative_url }}' alt='The City of Toronto's Open Data portal. "Former Municipality Boundaries" has been searched and is the first result seen.' title='' width='100%' height='100%' />

Also, download the dataset with the **WGS84** coordinate system for this dataset to be consistent with the DEM we downloaded.

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_006.png' | relative_url }}' alt='Data preview showing the extent of the Former Municipality Boundaries.' title='' width='100%' height='100%' />  

### 

 

### **Step 3 \- Setting up a working directory and establish folder connection**

To ensure that all of your data are saved properly, create a folder to save all your data and maps in. Make sure you are **not including spaces** in all the folder names in the directory, because folders with spaces might result in unexpected errors when running analysis in ArcGIS Pro.

After creating folders, extract the data you just downloaded to your working folder. Repeat the same steps for other zipped datasets.

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_007_2.png' | relative_url }}' alt='7Zip window showing contents in a zipped folder.' title='' width='100%' height='100%' />

Open ArcGIS Pro, select Map and choose a file directory where your project will be stored.

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_008.png' | relative_url }}' alt='Creating a new project on the home page of ArcGIS Pro.' title='' width='100%' height='100%' />

In the **Catalog pane**, right click on the **Folder** button. Click on "**Add Folder Connection**". You can also click on the button on the top of the panel to establish folder connection (highlighted in the screenshot below).

If your Catalog pane is missing, you can always click on Catalog Pane button located in the View tab at the top of your screen to open it.

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_009_0.png' | relative_url }}' alt='By right-clicking the Folder tab in the Catalog pane, the Add Folder Connection button appears.' title='' width='100%' height='100%' />

Choose your working folder.

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_010.png' | relative_url }}' alt='Add Folder Connection window where Clipping_Rasters is being connected to the project.' title='' width='75%' height='75%' />

After connecting to folder, your Catalog Pane should display the folder you've created. Now you can start adding your downloaded and extracted data to your map by **dragging** them to the **map area** or the **Table Of Contents pane**.

For the raster image, drag in the **DEM.tif** file (this raster image format is TIFF). And for the City of Toronto boundaries, drag in the **cityprj\_former\_municpality.shp**. This is the shapefile for the boundaries. Dragging in the .xml file and the .txt would not show any layers in the map.

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_011_0.png' | relative_url }}' alt='Catalog pane showing recently downloaded layers in the Clipping Rasters folder. The Drawing Order can be manipulated in the Contents pane.' title='' width='100%' height='100%' />

When adding in the raster dataset, you might get a pop\-up window asking if you would like to calculate statistics. You can proceed by clicking either "Yes" or "No", it won't affect this exercise. Clicking "Yes" could help you to improve the display performance of the raster dataset.

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_012.png' | relative_url }}' alt='Calculate statistics window prompted upon uploading the DEM to the project.' title='' width='75%' height='75%' />

On the Table of Contents pane on the left, you can **adjust the drawing order** (display order) of the two dataset if you want to have the boundaries layer on top of the DEM. Simply drag the layers up and down in the list would change the order to display them. Make sure you have the "**List By Drawing Order**" tab checked (highlighted in red).

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_013.png' | relative_url }}' alt='Contents pane showing the drawing order of the DEM and boundaries layers.' title='' width='100%' height='100%' />

 

**Clipping Rasters \- Two ways**
--------------------------------

 

### **Clipping Rasters \- Using toolboxes**

The first method to clip a raster is by using the Data Management toolbox in ArcGIS Pro. Click on Tools in the Analysis tab found in the ribbon at the top of your screen. This should open up the Geoprocessing pane.

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_014_0.png' | relative_url }}' alt='In the ribbon, the Tools button can be found in the Analysis tab.' title='' width='100%' height='100%' />

In ArcGIS Pro, there are two different clipping tools for vector and raster datasets. To find the Clip tool that's specifically designed for raster dataset, follow this directory: **Toolboxes  → Data Management Tools  → Raster  → Raster Processing  → Clip Raster.** Alternatively, you can use the *Find Tools* search bar at the top of the geoprocessing pane and type out "**Clip Raster**".

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_015.png' | relative_url }}' alt='Geoprocessing pane showing the location of the Clip Raster tool found by navigating to the Raster and Raster Processing tabs in Data Management Tools' title='' width='35%' height='35%' />

Open the Clip Raster tool. The **Input Raster** should be the Digital Elevation Model we downloaded. Set up the City of Toronto Former Municipality Boundaries file as the **Output Extent**. You can also manually adjust the extent of the rectangle by changing the X Max/Min and Y Max/Min numbers.

The Clipping tool will clip your raster dataset to a rectangle that covers your extent. If you want your clipped raster data to be **exact same shape as the clipping layer** (the City boundaries, in this case), make sure you check the "**Use Input Features for Clipping Geometry (optional)**" box.

In the Output Raster Dataset, save your output dataset to your preferred directory.

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_016.png' | relative_url }}' alt='Clip Raster window where the "Use Input Features for Clipping Geometry" has been selected.' title='' width='100%' height='100%' />

Click OK after all settings are properly changed.

Note: every time you click on one of the settings, the **Tool Help panel** on the right will show you a detailed explanation of this option. You can read through if you are needs clarification with some of the options.

After the clipping process is completed, the clipped layer should be added to display automatically. If not, find your clipped dataset under the folder you chose to export the data in the ArcCatalog panel, and add it to the map.

The clipped raster dataset should look similar to the following image.

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_017.png' | relative_url }}' alt='DEM clipped to the size of the Toronto Municipality Boundaries layer.' title='' width='100%' height='100%' />  

 

### **Clipping Rasters \- Export Data**

You can also zoom to the extent you wish to be working on and clip your dataset based on your zoomed extent. Let's say you are specifically interested in Toronto's islands and port lands.

First, zoom to the islands and port lands.

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_018.png' | relative_url }}' alt='Map zoomed into the Toronto's islands and port lands.' title='' width='100%' height='100%' />

Then, right\-click on the raster layer you wish to clip from. **Choose Data → Export Data...**

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_019_0.png' | relative_url }}' alt='Contents pane showing the Export Raster tool, found by expanding the Data dropdown menu.' title='' width='100%' height='100%' />

In the Export Raster Data setup window underneath the header "Clipping Geometry", make sure you select **"Current Display Extent"** to only export the data within your zoomed dataframe. You can keep the Spatial Reference same as the original one.

You can also choose to export the raster file as the same format as the original dataset (TIFF). Saving the raster file as a TIFF could also avoid compressing the dataset.

Make sure you save the exported file to your working directory.

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_020_3.png' | relative_url }}' alt='Export Raster window with selected Output Format as TIFF and Clipping Geometry set to "Current Display Extent".' title='' width='75%' height='75%' />

Add your exported layer the map area. Your clipped layer should look similar to this.

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_021.png' | relative_url }}' alt='Clipped DEM on Former Municipality Boundaries layer.' title='' width='100%' height='100%' />

Some alternative sources to download Digital Elevations Models:

[**Province Digital Elevation Model \- Ontario Open Data**](https://www.javacoeapp.lrc.gov.on.ca/geonetwork/srv/en/main.home?uuid=012e3632-22a2-49d8-bbaf-ad8fbc0d0ceb) (In "Transfer Options", choose "**Provincial Digital Elevation Model \- South \- Revised Package September 2016**")'

[**Swift Current LiDAR Project 2009 \- DEM \- Federal Open Data**](https://open.canada.ca/data/en/dataset/72003a79-c799-49de-b135-de5af833f029) (In the list of "Resources", choose "**Pre\-packaged GeoTIF files (No linguistic component)**"

[**USGS Earth Explorer**](https://earthexplorer.usgs.gov/)("Search Criteria" \- identify your area of interests; "Data Sets" \- choose "Digital Elevation")

Technique: [Extracting data](/technique/extracting-data) \| Tools: [ArcGIS Pro](/taxonomy/term/70) \| Data Format: [DEM](/data-format-tutorials/dem), [Raster](/data-format/raster)**Date Created:** 2024\-01\-15**Updated:** 2024\-04\-12
