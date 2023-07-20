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
affiliations:
 - name: Vielca Ingenieros, S.A., Avda. Aragón 17, PC 46010, Valencia (Spain) 
   index: 1
 - name: Vielca Medioambiente, S.L., Avda. Aragón 17, PC 46010, Valencia (Spain)
   index: 2
date: 30 July 2023
bibliography: paper.bib
---

# Summary

Satellite imagery and remote sensing data provide the physical characteristics of the Earth surface from the measures of the radiation reflectance of special cameras [@Caoetal_2019]. Such a property allows the use of these information for environmental monitoring. 

However, one of the weaknesses of this appraisal is the spatial and temporal granularity of the information [@TANG2021130]. While some satellite raster products have almost daily information but poor spatial resolution – e.g. Sentinel 3 provides Chl and TSM information at 300 m spatial resolution [@TANG2021130], or VIIRS [@Wolfeetal_2013] and MODIS [@d14040277] provides Chl at 750 m and 1000 m resolution, respectively –; aerial image is provided by Sentinel 2 at 10-60 m resolution [@TANG2021130; @rs12081284; @d14040277], but with a temporal granularity of 5-10 days [@rs12081284]. 

Daily Aerial Image (DAI) algorithm interpolation method adapts the spatial Inverse Distance Weighting (IDW) method to temporal series for spatial interpolation of the RGB bands of two aerial images in order to obtain interpolated daily images between two dates.

DAI has been fully implemented in Python and its source code has been archived to Zenodo with the linked DOI: [@zenodo]

# Acknowledgements

Authors acknowledge Vicente M. Candela Canales for supporting the R&D investment and programs within the Vielca companies.

# References
