---
layout: post
title: Simple City Geocoder and Web Map
excerpt_separator: <!--more-->
categories:
  - Projects
---
### The Web Map

Shown below is an example output from a geocoding and web map tool that I scripted.
This project was designed to take user input, geocode the provided city, and update the web map.
<br>
[Project repository can be found here](https://github.com/RaeJanzen/Simple-City-Geocoder-and-Webmap){:target="_blank" rel="noopener"}

<div>
<iframe
style = 'width:100%; height:400px'
src = '/projects/assets/webMap/index.html'>
</iframe>
</div>

<!--more-->

### Javascript 

OpenLayers API was used to create the web map display. To avoid clutter and overcrowding, the data layer is clustered. 
The symbology is rendered such that the size is dependent on the number of unique data entries included in the cluster. 
Pop ups include information on the city name and the number of times that city has been requested for geocoding.

{% highlight javascript %}
{% include_relative /assets/webMap/scripts/main.js %}
{% endhighlight %}

### Geocoder 

This geocoding script is written in python and uses the geopy library to access Nominatim's free geocoding service.

{% highlight python %}
{% include_relative /assets/webMap/scripts/Geocoder.py %}
{% endhighlight %}