---
title: 'DAI Algorithm: a QGIS plugin for Daily Aerial Image interpolation.'
tags:
  - satellite imagery
  - QGIS plugin
  - spatial interpolation method
authors:
 - name: Pablo Blanco-Gómez
   orcid: 0000-0001-9465-2912
   affiliation: 1
 - name: José Luis Jiménez-García
   orcid: 0000-0001-6619-9057
   affiliation: 2   
 - name: Constancio Amurrio-García
   orcid: 0009-0005-4681-0281
   affiliation: 2   
affiliations:
 - name: Vielca Ingenieros, S.A., Avda. Aragón 17, PC 46010, Valencia (Spain) 
   index: 1
 - name: Vielca Medioambiente, S.L., Avda. Aragón 17, PC 46010, Valencia (Spain)
   index: 2
date: 30 July 2023
bibliography: paper.bib
---

# Summary

Daily Aerial Image (`DAI`) algorithm is implemented to fill the existing gap of satellite images for the Landsat (7 or 8) and Sentinel 2 projects, including both, the temporal coverage of the respective projects and the existance of clouds.

Aerial images are composed of three bands RGB - standing for Red, Green and Blue colours - with numerical values ranging from 0 to 255 [@BLANCOGOMEZ2023101356; @s120607063]. Such a characteristic allows a separated interpolation for R, G and B bands between two images - that correspond to different dates -, obtaining intermediate numerical values for different timestamps and when combining them in a three-banded (RGB) raster product, interpolated aerial images.

`DAI` establishes the daily timestamp for the interpolation, but the algorithm could be adapted for different purposes varying the corresponding timing.

# Statement of need

Satellite imagery and remote sensing data provide the physical characteristics of the Earth surface from the measures of the radiation reflectance of special cameras [@Caoetal_2019]. Such a property allows the use of these information for environmental monitoring. 

However, one of the weaknesses of this appraisal is the spatial and temporal granularity of the information [@TANG2021130]. While some satellite raster products have almost daily information but poor spatial resolution – e.g. Sentinel 3 provides Chlorophyl-a (Chl) and Total Suspended Matter (TSM) information at 300 m spatial resolution [@TANG2021130], or VIIRS [@Wolfeetal_2013] and MODIS [@d14040277] provides Chl at 750 m and 1000 m resolution, respectively –; aerial image is provided by Sentinel 2 at 10-60 m resolution [@TANG2021130; @rs12081284; @d14040277], but with a temporal granularity of 5-10 days [@rs12081284]. 

`DAI` algorithm adapts the spatial Inverse Distance Weighting (IDW) method to temporal series for spatial interpolation of the RGB bands of two aerial images in order to obtain interpolated daily images between two dates.

`DAI` has been fully implemented in Python and its source code has been archived to Zenodo with the linked DOI: [@zenodo].

# Performance

`DAI` interpolation method needs the following input information \autoref{fig:panel}:

* Aerial Image `Ini`: A three-banded (RGB) raster map with the oldest aerial image that needs to be interpolated. 
* Aerial Image `End`: A three-banded (RGB) raster map with the most recent aerial image that needs to be interpolated. 
* Dates: Defines the day/month/year (dd/mm/yyyy) of both, Aerial Image `Ini` and `End`. 
* Area of interest (shp): Defines the outer interpolation polygon with a shape file. 
* Working folder: Defines de destination route. 

![QGIS interface panel of `DAI` algorithm interpolation method. \label{fig:panel}](panel.pdf)

The program calculates the intermediate days between dates `Ini` and `End`; and interpolates the original images according to the temporal distance to them of every single date.

# Acknowledgements

Authors acknowledge Vicente M. Candela Canales for supporting the R&D investment and programs within the Vielca companies.

# References
