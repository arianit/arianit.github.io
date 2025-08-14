---
layout: post
title: Marking road surfaces on OpenStreetMap 
---

I noticed that on OpenStreetMap we were missing types of surfaces for many important roads in Kosovo.

Car navigators use surfaces when routing and calculating travel times.

So entering this information became a goal, a time bound mission I could do on my own within a short period of time and see the results, which is just what I like.

The roads in OpenStreetMap are largely classified as *primary* (highways), *secondary* (regional roads), *tertiary() (local roads) and residential.

I decided to work on the first three and smaller sections connecting these classified as *primary_link*, *secondary_link* and *tertiary_link*. The first three for the most part are asphalt in Kosovo, and it’s easy to guess when this may not be the case. Being larger, it’s also easier to confirm on aerial photography that they are indeed paved in asphalt.

First, getting a view of the situation. Here, [Overpass turbo](https://overpass-turbo.eu/) is great.

This code will highlight all the primary road surfaces that haven’t been specified.
```
[out:json][timeout:25];
way["highway"~"primary"]["surface"!~"."]({{bbox}});
out geom;
```
Replace *primary* with *secondary*, *tertiary*, *primary_link* and so forth as needed.

Next, map editing.

Going through roads one by one and looking at status is tedious. Here comes JOSM and the amazing filtering function I hadn’t used before.

Open *Windows* > *Filter* and enter:
```
highway=primary
```
Check *E* (enable) and *I* (inverse) checkboxes.

For the downloaded area of the map, this will highlight surfaces that need to be specified. Referring to all the aerial imagery available, change them to *surface=asphalt* and upload.

And voila, almost all primary, secondary and tertiary road surfaces in Kosovo have been completed. In some rear cases I couldn’t tell from aerial imagery available what the status was. I also didn’t work on residential roads which are much more in number but less critical for navigation and where local knowledge would be quite helpful.

Happy mapping!
