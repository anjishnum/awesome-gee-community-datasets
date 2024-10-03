# Digital Earth Australia Coastlines

Digital Earth Australia Coastlines is a continental dataset that includes annual shorelines and rates of coastal change along the entire Australian coastline from 1988 to the present. The product combines satellite data from Geoscience Australia's Digital Earth Australia program with tidal modelling to map the most representative location of the shoreline at mean sea level for each year. The product enables trends of coastal retreat and growth to be examined annually at both a local and continental scale, and for patterns of coastal change to be mapped historically and updated regularly as data continues to be acquired. This allows current rates of coastal change to be compared with that observed in previous years or decades.

The ability to map shoreline positions for each year provides valuable insights into whether changes to our coastline are the result of particular events or actions, or a process of more gradual change over time. This information can enable scientists, managers and policy makers to assess impacts from the range of drivers impacting our coastlines and potentially assist planning and forecasting for future scenarios. You can find [additional details here](https://cmi.ga.gov.au/data-products/dea/581/dea-coastlines) and you can [download the datasets here](https://data.dea.ga.gov.au/?prefix=derivative/dea_coastlines/2-2-0/)

Disclaimer: Whole or parts of the dataset description were provided by the author(s) or their works.

Annual shoreline vectors that represent the median or ‘most representative’ position of the shoreline at approximately 0 m Above Mean Sea Level for each year since 1988. Dashed shorelines have low certainty and Annual shorelines include the following attribute fields:

| **Attribute**   | **Description**                                                                 |
|-----------------|---------------------------------------------------------------------------------|
| **year**        | The year of each annual shoreline.                                               |
| **certainty**   | A column providing important data quality flags for each annual shoreline.       |
| **tide_datum**  | The tide datum of each annual shoreline (e.g. “0 m AMSL”).                       |
| **id_primary**  | The name of the annual shoreline’s Primary sediment compartment from the Australian Coastal Sediment Compartments framework. |


#### Citation

```
Bishop-Taylor, R., Nanson, R., Sagar, S., Lymburner, L. 2021. Digital Earth Australia
Coastlines. Geoscience Australia, Canberra. https://doi.org/10.26186/116268
```

#### Publications

```
Bishop-Taylor, R., Nanson, R., Sagar, S., Lymburner, L. (2021). Mapping Australia's dynamic
coastline at mean sea level using three decades of Landsat imagery. Remote Sensing of
Environment, 267, 112734. Available: https://doi.org/10.1016/j.rse.2021.112734

Nanson, R., Bishop-Taylor, R., Sagar, S., Lymburner, L., (2022). Geomorphic insights into
Australia's coastal change using a national dataset derived from the multi-decadal Landsat
archive. Estuarine, Coastal and Shelf Science, 265, p.107712. Available: https://doi.org/10.1016/
j.ecss.2021.107712

Bishop-Taylor, R., Sagar, S., Lymburner, L., Alam, I., & Sixsmith, J. (2019). Sub-pixel
waterline extraction: Characterising accuracy and sensitivity to indices and spectra. Remote
Sensing, 11(24), 2984. Available: https://www.mdpi.com/2072-4292/11/24/2984
```

![dea_coastlines](https://user-images.githubusercontent.com/6677629/227800601-a7f6b5b7-4876-4cda-824f-c5819f77bcc1.gif)

#### Earth Engine Snippet

```js
var shoreline_annual = ee.FeatureCollection("projects/sat-io/open-datasets/DEA/COASTLINES/coastlines_v220_shorelines_annual");
var hotspot_zoom_1 = ee.FeatureCollection("projects/sat-io/open-datasets/DEA/COASTLINES/coastlines_v220_hotspots_zoom_1");
var hotspot_zoom_2 = ee.FeatureCollection("projects/sat-io/open-datasets/DEA/COASTLINES/coastlines_v220_hotspots_zoom_2");
var hotspot_zoom_3 = ee.FeatureCollection("projects/sat-io/open-datasets/DEA/COASTLINES/coastlines_v220_hotspots_zoom_3");
var rate_of_change = ee.FeatureCollection("projects/sat-io/open-datasets/DEA/COASTLINES/coastlines_v220_shorelines_annual");
```

Sample code: https://code.earthengine.google.com/?scriptPath=users/sat-io/awesome-gee-catalog-examples:oceans-shorelines/DEA-Shorelines

#### License
These datasets are made available under the CC BY 4.0 Attribution 4.0 International license. This license allows users to distribute, remix, adapt, and build upon the material in any medium or format, so long as attribution is given to the creator.

Created by: Digital Earth Australia

Curated in GEE by : Samapriya Roy

Keywords : Sea, ocean and coast, marine and coastal, coast, erosion, waterline extraction,
subpixel waterlines, coastal change, DEA CoastLines, coastline data, coastal erosion

#### Changelog
* In August 2024 , the DEA Coastlines product was updated to version 2.2.0. This update consists of the addition of annual shoreline data for 2023.
* In August 2023, the DEA Coastlines product was updated to version 2.1.0. This update consists of the addition of annual shoreline data for 2022. The 2022 shoreline is interim data that is subject to change, and will be updated to a final version in the following 2023 DEA Coastlines update (in July 2024).

Last updated : 2024-09-13
