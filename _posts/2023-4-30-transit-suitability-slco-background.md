---
layout: post
title: Assessing transit suitability in Salt Lake County
---

Over the last few months, I’ve grown my spatial and analytical skills through an advanced technical course in my graduate program and I’m excited to share the results of my first major spatial analysis project. The course in question, CMP 6455 Spatial Data Analytics, had three objectives: 

* Understand fundamental concepts and principles in spatial data science
* Process and manipulate spatial data using R and other open-source software (QGIS, GeoDa)
* Perform advanced spatial data science techniques

These techniques included point pattern analyses such as kernel density estimation or K functions; accessibility analyses such as network buffers or two-step floating catchment areas; areal data analyses such as autocorrelation and Moran’s I; and suitability analyses such as binary or weighted overlays. Additionally, we learned how to use the Census Bureau’s API to query demographic data and administrative boundaries within R. 

## Background: 

For my semester project in the course, I partnered with two classmates to perform a suitability analysis for bus service expansion in Salt Lake County. I’m fascinated by how transit networks are designed – and occasionally redesigned ([Houston](https://nacto.org/case-study/metro-bus-network-redesign-houston/), [Columbus](https://usa.streetsblog.org/2017/05/02/columbus-just-launched-a-completely-redesigned-bus-network/), [Boston](https://www.mbta.com/projects/bus-network-redesign), and others) – and saw the project as an opportunity to explore that interest. 

In order to meet the criteria for the project, we decided to focus on determining suitability for expansion, rather than assessing the effectiveness of the existing network. Large swaths of the county are rapidly urbanizing, and the county’s population is expected to grow by over 40% in the next few decades. A majority of this growth will happen outside of Salt Lake City (barring substantial changes to zoning policy and land use planning), which will necessitate expanded service. 

That being said, our findings are inherently an assessment of the network since we can compare existing transit routes to expected need (based on the factors we chose). This is especially true for neighborhoods on the west side of Salt Lake City, many of which were [red-lined](https://local.sltrib.com/redline-utah/) and have failed to receive the same level of transportation investment as the east side. 

## Process: 

I worked with two students in my program – Corey Bishop and Muwaffaq Usman Adam – both of whom played an important role in the project. Muwaffaq helped to situate our research question and suitability factors within existing literature on transit ridership, while Corey helped to define our methodology and turn our vision into something actionable. I focused on the analysis itself and handled the coding and data visualization. 

## Outcome:

Our methodology and findings are detailed in the following StoryMap: [Assessing Transit Suitability in Salt Lake City](https://storymaps.arcgis.com/stories/3b36f06f0d0542f9b7c4b4978eb3a087).

It works best on a desktop, since we embedded several interactive maps (all of which were generated within R using the tmap package). The full R code is available on [GitHub](https://github.com/dritter4/Transit-Suitability/blob/main/R-Code/SaltLakeCounty-CMP6455.R) for those who may be interested in seeing the specific process or replicating the analysis. Several sections of code are commented out; these sections were run only once early in the analysis since they were time intensive.


## Next steps:

This will be the first of several related posts as I make some tweaks locally (incorporating growth projections) and apply the methodology to other places (Washington, DC). Additionally, I’m attempting to build an interactive Shiny tool where users can select their own weights for the suitability analysis, and I may explore drawing potential bus routes using the suitability values and a least-cost path algorithm. 
