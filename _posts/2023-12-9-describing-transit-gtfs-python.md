---
layout: post
title: Describing transit systems using GTFS data in Python
thumbnail: /images/gtfs-python/uta-frequency-thumbnail.png
---

After [learning R](https://dritter4.github.io/transit-suitability-slco-background/) during the spring semester (and tinkering with this site), I was eager to expand my programming knowledge, which led me to GEOG 6180 Geoprocessing with Python. The course had three main objectives: 
* Learn fundamental principles of programming in Python
* Use Python to manipulate and analyze geographic data
* Write scripts for geoprocessing in Python and ArcGIS

I learned the basics of Python and `arcpy` during the first few weeks of the semester before moving onto "classic" spatial analyses, such as calculating the optimal location for a site based on the minimum weighted travel distance or determining slope and aspect from a digital elevation model, or DEM. These [assignments](https://github.com/dritter4/GEOG-6180/tree/main/Assignments) focused on the theory and structure behind each type of analysis and used simple inputs to illustrate the basic process.

![_config.yml]({{ site.baseurl }}/images/gtfs-python/slope-aspect-uofu.png)

For my semester project, I decided to write a script to process [General Transit Feed Specification](https://gtfs.org/) data. GTFS is a standard text-based data format used by thousands of transit agencies worldwide to share operational data, including routes, schedules, live tracking, and more. A few months ago, I had seen two intriguing fellowships with the USDOT Bureau of Transportation Statistics that involved handling GTFS data, and I thought this would be the perfect opportunity to gain some firsthand experience.

I used Jupyter to write separate notebok scripts to [describe a single bus system](https://github.com/dritter4/GEOG-6180/blob/main/Describe-System-GTFS/GEOG6180_GTFS-Describe.ipynb) and [compare two bus systems](https://github.com/dritter4/GEOG-6180/blob/main/Compare-Systems-GTFS/GEOG6180_GTFS-Compare.ipynb), which used the `gtfs_functions` package to handle the initial data processing, `geopandas` and `pandas` for data analysis, and `keplergl` for map visualizations. I won't go into detail on the process since the notebooks include some commentary, but it was a great learning experience and now I have a script that can theoretically take any GTFS feed and spit out some basic statistics and maps.

I have a much stronger grasp of the basic fundamentals of programming after taking this course. Even though I had written plenty of R code during the spring, I was primarily focused on cleaning and analyzing specific datasets in a linear, step-by-step process. This course introduced functions, `for` loops, `if/elif/else` statements, and other statements or methods that will help me write more advanced scripts. Plus, knowing the basics of `arcpy` will be a gamechanger as I work more in ArcGIS Pro. I'm excited to keep expanding my expertise in Python, especially as I begin thinking about what my early career could look like.