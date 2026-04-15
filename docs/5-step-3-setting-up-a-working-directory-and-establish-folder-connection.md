---
title: Step 3 - Setting up a working directory and establish folder connection
parent: Clipping Rasters in ArcGIS Pro
layout: default
nav_order: 5
---

### **Step 3 - Setting up a working directory and establish folder connection**

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

For the raster image, drag in the **DEM.tif** file (this raster image format is TIFF). And for the City of Toronto boundaries, drag in the **cityprj_former_municpality.shp**. This is the shapefile for the boundaries. Dragging in the .xml file and the .txt would not show any layers in the map.

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_011_0.png' | relative_url }}' alt='Catalog pane showing recently downloaded layers in the Clipping Rasters folder. The Drawing Order can be manipulated in the Contents pane.' title='' width='100%' height='100%' />

When adding in the raster dataset, you might get a pop-up window asking if you would like to calculate statistics. You can proceed by clicking either "Yes" or "No", it won't affect this exercise. Clicking "Yes" could help you to improve the display performance of the raster dataset.

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_012.png' | relative_url }}' alt='Calculate statistics window prompted upon uploading the DEM to the project.' title='' width='75%' height='75%' />

On the Table of Contents pane on the left, you can **adjust the drawing order** (display order) of the two dataset if you want to have the boundaries layer on top of the DEM. Simply drag the layers up and down in the list would change the order to display them. Make sure you have the "**List By Drawing Order**" tab checked (highlighted in red).

<img src='{{ '/assets/images/clipping_rasters_in_arcgispro_013.png' | relative_url }}' alt='Contents pane showing the drawing order of the DEM and boundaries layers.' title='' width='100%' height='100%' />