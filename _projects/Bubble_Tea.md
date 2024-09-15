---
layout: post
title: Bubble Tea Locations
excerpt_separator: <!--more-->
categories:
  - Projects
---

## A Map of Bubble Tea Cafes Within the Metro Vancouver Regional District

Inspired by the seemingly endless number of bubble tea cafes in the Metro Vancouver area, I was curious if the spatial distribution of such retail spaces was as abundant as my impression.  I made this map to display all the points of interest (POI) within the Metro Vancouver area marked with the bubble tea tag in OneStreetMaps (OSM) data. SkyTrain lines are included to give some context to the POI data in relation to major public transit hubs. 
![There should be a lovely cluster map right here](/assets/images/BubbleTea.png)

<!--more-->

##### Data Acquisition and Layer Derivation
POI, SkyTrain lines, and the Metro Vancouver area boundaries were sourced from OSM using Overpass Turbo and Overpass Query Language. For the POI data, a query was built to pull every location with a cuisine key that matched “bubble_tea” as a value. The official boundaries for the Metro Vancouver Area extend past the coastline. Since this project used this data to define and highlight the study area, it was beneficial to create a layer with polygons fitting the coastline. For this purpose, a layer with polygon features detailing the boundaries of the Province of BC was obtained from geoBoundaries. This data detailed the coastline sufficiently for the purposes of this project. Using the BC layer and the Metro Vancouver area layer, the clip tool was used to create a layer describing the chosen study area with a nice and tidy coastline. 

##### Observations & Discussion
Originally the perception of bubble tea cafes within the Metro Vancouver area is that they are absolutely everywhere. When visualizing the data as a cluster map, it becomes clear that the noted places are nearly exclusive to highly built up and high traffic places that are easily accessible by public transit.
<br>
One glaring limitation lies within the data collection. The POI data relied on the accuracy of crowd sourced data. Consistency with regards to the richness of the data, specifically as it pertains to the tagging system, is difficult to achieve. The data acquisition relied on all bubble tea retail locations being tagged as such. The real world is clearly not so neat and tidy. With a little bit of investigation, primarily using Google Maps, it was easy to find a handful of locations that fit the POI criterion but had not been included in the list of POI retrieved from OSM. That being said, the spread of locations found using Google Maps did not vastly differ visually from the map created using OSM data.

##### Full Attributions
This map was made with data obtained from multiple sources. The basemap, SkyTrain routes, and bubble tea locations layers were obtained from OpenStreetMap. The bubble tea and SkyTrain data was extracted using Overpass Turbo. This data is licensed by OpenStreetMap and its contributors under the [Open Data Commons Open Database License (ODbL)](https://www.openstreetmap.org/copyright){:target="_blank" rel="noopener"}. The study area layer was derived from data obtained from geoBoundaries licensed under the [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/){:target="_blank" rel="noopener"} licence, found on the geoBoundaries website [www.geoboundaries.org](https://www.geoboundaries.org){:target="_blank" rel="noopener"}, and OpenStreetMap. The municipal labels are part of a dataset provided by the Metro Vancouver Open Data Portal under the [Open Government Licence – Metro Vancouver](https://open-data-portal-metrovancouver.hub.arcgis.com/pages/b58fa98464f14b54b6767ce0793427b5_){:target="_blank" rel="noopener"}. 
